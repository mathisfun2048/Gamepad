title: Gamepad

author: Arya Chakrabarti (Arya)

description: This project is to create a retro gamepad!

created at: 06-18-2025

total time spent prepping: 27 hours (in ~~one~~ two go(s)! Undiagnosed ADHD!) (will increase expoentnially once I have it in front of me and I find ways to improve it)

# June 8th
## 10AM -> 6 PM : planning (8 hours)
This is my first custom hardwre project, so I've been a tad nervous (thats why this took so long!). I spent this time researching what making a game console entails and sourcing possible parts. I have learned that this is more than just plug and play (haha) and in order to make a clean design I found I need to make some custom PCBs to wire everything up without clunky wires sticking out. I found multiple different processing chips, but settled on a raspberry pi because of how prevelent it is--I am new to this and am glad I will find support if I use this chip. In addition, I sketched out a rough drawing on what I want my gamepad to look like: I want a nintendo 3ds like setup with the screen on the top lid of the altoids tin and all the guts of the system on the bottom portion. For buttons, I want a D pad, A and B, and 2 system buttons. 


<img width="462" alt="Screenshot 2025-06-19 at 7 49 12 AM" src="https://github.com/user-attachments/assets/0c2a82fd-4653-41f9-8470-0f37c34e427e" />



### Projected BOM

#### Core Computing and Storage
- Raspberry Pi Zero 2W
- SanDisk Ultra 64GB microSD
- GPIO Header (40-pin)

#### Display
- 2.8" TFT LCD Display
- Ribbon Cable (10-wire)

#### Power
- Li-Po 3.7 V 1200 mAh
- PowerBoost 1000C power supply
- Power Switch
- USB-C Breakout

#### Controls
- Tactile Switches (8x)
- D-Pad Cap
- Button Caps (4x)
- MCP23017 I/O Expander

#### Audio
- MAX98357A I2S Amp
- Mini Speaker

#### PCBs
- Main PCB
- Display Lid PCB
- Resistors (Assorted)
- Capacitors (Assorted)
- JST Connectors
- Pin Headers
- Level Shifters (4x)

#### Assembly
- Altoids tin
- Piano Hinge
- Neodymium Magnets (2x)
- Heat-Set Inserts (16x)
- Machine Screws
- Ribbon Cable
- Cable Management
- Double Sided Tape
- Kapton Tape
- Silicone Wire Kit
- Heat Shrink Kit

#### 3D Printed Parts
- Top Lid Screen Bezel 
- Bottom Case Component Tray 
- Bottom Case Button Plate 
- Cable Management Guide

  
### Physical Design

#### Top Case
- 2.8" LCD screen mounted in 3D-printed bezel/frame
- Screen protection via recessed mounting
- Hinge mechanism for smooth 180° opening
- Magnetic closure for secure shut
- Cable routing through hinge area

#### Bottom Case

##### Layer 1 (Bottom): Core components
- Raspberry Pi Zero 2W
- 1200mAh Li-Po battery
- PowerBoost 1000C charging circuit
- MAX98357A audio amplifier

##### Layer 2 (Middle): Main PCB with controls
- 8-button tactile switch layout
- MCP23017 I/O expander
- Power switch and charging port
- Speaker  

##### Layer 3 (Top): 3D-printed button interface
- Button caps and D-pad
- Clean, comfortable gaming surface
- Logo/labeling area

# June 9th 
## 12AM -> 1AM (1 hour)

So I realized I am way over my head and with my current skill level this project is impossible! So I am going to try a easier version of this project because I still want to make a cool retro game device. Instead of an cramped altoid tin a altoid tin and a pi zero, I think I will move on to a full on raspberry pi. I will update this with an update BOM and design once I'm done researching. Hopefully this takes less time :D

## 1AM -> 2AM (1 hour)

Great news! I found a tutorial from a couple years ago about how to do exactly this: a beginer friendly raspberry pi retro gaming console tutorial. A problem is that this tutorial is a tad old, so I have to modernize it. This includes modernizing the computer PCB (from a raspberry pi 1 to a raspberry pi 5) and followingly change the power and thermal architechture. For this, I am going to include a signficiantly larger battery, a more powerful power supply, and incororpate heat sinks. This is really cool becasue now I can learn more about a different part of design than what I learned when I made my macropad: in that project, I focused enterily on the pcb basics itself while now in this project, I can consider the product more holistically. I'm excited!

### Updated BOM

#### electronics
- Raspberry Pi 5
- 2.8" PiTFT Display
- PiGRRL Gamepad PCB
- PowerBoost 1000c
- 6600 mAh battery
- PAM8302 2.5W Audio Amp
- Mini metal speaker
- 40 pin GPIO ribbon cable
- slide switch
- 10x 6mm tactile buttons
- 2x 12mm tactile buttons
- 2x20 pin IDC box header
- heat sink kit

#### hardware
- 14x #4-40 3/8 machine screws
- 6x #2-56 3/8 machine screws

## 2AM -> 4AM (2 hours)

Time to make the circuit diagram! This is going to be exciting. 

Here it is!:
![IMG_4873](https://github.com/user-attachments/assets/9a27b048-a037-46a0-86bd-a43727e81154)


Okay quick update though: I couldn't find online which were teh test pads for audio, which I need to know so I can solder the amp onto the raspberry pi. Because of this, I will have to manually check the testpads agaisnt gpio pins 12, 35, and 40 to see which ones are audio related. Thankfully this issue is not too big. One thing I did learn through making this wiring diagram is that even though this project is significantly more simplistic than my previous altoid tin design, it is still super challenging. I am glad I am learning though! 

## 4AM -> 7AM (3 Hours)
Time to make the CAD file for the case! Wish me luck...

mini update at 5AM 
I tried using scripts to automate it because I want a simple block-y case, but that did not go well! But this is fun so I think I'll continue
<img width="685" alt="Screenshot 2025-06-19 at 4 58 39 AM" src="https://github.com/user-attachments/assets/7482e1e0-d35d-49ae-9f89-d90b777d4ad5" />

Will update when I fix this!


Update: 5:30 AM: I GOT THE BOTTOM CASE TO WORK!!!!!
<img width="314" alt="Screenshot 2025-06-19 at 6 24 46 AM" src="https://github.com/user-attachments/assets/53782448-6fc8-4b35-b656-10cf89b3fe6d" />

Update: 6:30AM I think I am done with the case design! Doing it through code was a really fun exerciese and I'm glad I've been able to learn how to use python to CAD!

Bottom case:
<img width="426" alt="Screenshot 2025-06-19 at 6 43 27 AM" src="https://github.com/user-attachments/assets/dbebb43d-29a3-411e-b4fd-236a00e2d7c6" />

Top Case:
<img width="688" alt="Screenshot 2025-06-19 at 6 44 06 AM" src="https://github.com/user-attachments/assets/0de6b2b9-2076-4e89-b5e7-390e602f9970" />


## 7AM -> 9AM (2 hours)
In this hour I polished everything up for final review! Hopefully you llike what I made so far!! I want to affirm, though, that this was my first time really sourcing parts myself and buildign something so I expect myself to course correct after I have everythign in front of me--I am a very tactile perosn and I love fiddling arround :D

WHY DOES IT TAKE THIS LONG TO UPLOAD A STUPID DESKTOP FOLDER TO GITHUB AHGHGHGDHAKLGHASDLF AKSLD FJA;FA 
i digress...


# June 20

## 6AM -> 3PM (9 hours)

I was going over my initial PCB design and found I have need some more holes TO THE SIDE OF TEH DISPLAY

This means my horizontal design will no longer work and I need a vertical deign. 

I found a sample online gameboy knockoff that I realy liked, so I spent the last 9 hours emulating that! Its been fun learning more about CAD since this is my second project. As a homage to the first itteration, those files are still in the CAD and production folders, but for practical purpouses I will use the newer versions. I feel takign time to emulate a prof. design taught me a lot of things that I would not have learned by simply making a "box" --for one I leanred how to make screw holes which are not just straight through!!! Very cool indeed. One thing that mildly irked me is how stupidly clunky it looks now... maybe ill try to adapt this to a pi zero in the future.... stay tuned >:)

<img width="222" alt="Screenshot 2025-06-20 at 3 31 39 PM" src="https://github.com/user-attachments/assets/de781935-8ae9-48c7-b6b3-5d8419f127f2" />

<img width="223" alt="Screenshot 2025-06-20 at 3 31 56 PM" src="https://github.com/user-attachments/assets/b9e5242f-9268-46cf-aa45-03e38b53d607" />

super cool sketch:

![IMG_4874](https://github.com/user-attachments/assets/fc41fa02-a6a3-42e2-99ac-e5d54a4dd17d)


# June 21

## 2PM -> 3PM (1 hour)
switched pi5 to pi zero 2w to reduce cost!

Here is the updated wiring diagram!
![IMG_4876](https://github.com/user-attachments/assets/4c831d41-a360-4efc-9f62-8df22b359e21)


# I think I am done for now--I have the parts list, case design, and firmware ready. All thats left is to receive the parts, course correct as needed, and build this!










