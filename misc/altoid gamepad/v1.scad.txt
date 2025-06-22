// pigrrl_case.scad
// Parametric OpenSCAD model for a PiGRRL-style handheld case with screw bosses and component standoffs

////// PARAMETERS //////
// Raspberry Pi 5
pi_len     = 101.5;  // board length
pi_wid     = 65;     // board width
pi_h       = 23;     // board total height

// 2.8" PiTFT display
disp_w     = 72;     // active window width
disp_h     = 52;     // active window height
disp_th    = 5;      // PCB thickness

// Buttons (6mm and 12mm tactile)
btn1_dia   = 6;      // small buttons
btn2_dia   = 12;     // large buttons (start/select)
btn_hole   = btn1_dia + 0.5;  // add tolerance

// Slide switch
sw_w       = 9;
sw_h       = 3;
sw_th      = 4;

// Battery pouch
tol        = 0.5;   // general clearance

// Case dimensions
wall_t     = 2;     // wall thickness
floor_t    = 2;     // bottom floor thickness
overall_x  = pi_len + wall_t*2;
overall_y  = pi_wid + wall_t*2;
overall_z  = pi_h + disp_th + wall_t;

// Screw boss parameters (for #4-40 screws)
boss_od    = 7;     // outer diameter of boss
boss_id    = 3;     // inner clearance diameter
boss_h     = wall_t + 2;  // height into top half
// Positions for case screws (4 corners)
case_boss_pos = [
    [wall_t + 10,              wall_t + 10],
    [overall_x - wall_t - 10,  wall_t + 10],
    [wall_t + 10,              overall_y - wall_t - 10],
    [overall_x - wall_t - 10,  overall_y - wall_t - 10]
];

// Pi mounting standoffs (#2-56 screws)
pi_boss_od = 6;     // outer diameter
pi_boss_id = 2.2;   // clearance diameter
pi_boss_h  = pi_h;  // full board height
// Approximate Pi hole positions measured from board origin
pi_mount_pos = [
    [5,   5],
    [pi_len - 5,   5],
    [pi_len - 5, pi_wid - 5],
    [5,         pi_wid - 5]
];

////// MODULES //////
module bottom_half() {
    // Base shell with Pi pocket
    difference() {
        cube([overall_x, overall_y, floor_t]);
        translate([wall_t, wall_t, 0])
            cube([pi_len + tol, pi_wid + tol, pi_h]);
    }
    // Pi standoffs
    for (p = pi_mount_pos) {
        translate([wall_t + p[0], wall_t + p[1], 0])
            difference() {
                cylinder(h = pi_boss_h, r = pi_boss_od/2, $fn=32);
                translate([0,0,-1])
                    cylinder(h = pi_boss_h + 2, r = pi_boss_id/2, $fn=32);
            }
    }
    // Case screw bosses
    for (c = case_boss_pos) {
        translate([c[0], c[1], 0])
            difference() {
                cylinder(h = boss_h, r = boss_od/2, $fn=32);
                translate([0,0,-1])
                    cylinder(h = boss_h + 2, r = boss_id/2, $fn=32);
            }
    }
}

module top_half() {
    // Lid with cutouts
    difference() {
        translate([0,0, overall_z - wall_t])
            cube([overall_x, overall_y, wall_t]);
        // Display cutout
        translate([
            wall_t + (pi_len - disp_w)/2,
            wall_t + pi_wid - disp_h - tol,
            overall_z - wall_t - disp_th
        ])
            cube([disp_w + tol, disp_h + tol, wall_t + 1]);
        // Button holes (example grid)
        btn_x0 = wall_t + 15;
        btn_y0 = wall_t + 15;
        for (x = [0,1,2]) for (y = [0,1]) {
            translate([
                btn_x0 + x*20,
                btn_y0 + y*20,
                overall_z - wall_t - 1
            ])
                cylinder(h = wall_t + 2, r = btn_hole/2, $fn=32);
        }
        // Slide switch
        translate([
            overall_x - wall_t - sw_w - tol,
            wall_t + 10,
            overall_z - wall_t - sw_th
        ])
            cube([sw_w + tol, sw_h + tol, sw_th + 1]);
        // Case screw clearance holes
        for (c = case_boss_pos) {
            translate([c[0], c[1], overall_z - wall_t])
                cylinder(h = wall_t + 2, r = boss_id/2, $fn=32);
        }
    }
}

////// ASSEMBLY //////
bottom_half();
top_half();
