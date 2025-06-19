# Gamepad

## Description and Exigence
Hallo! This is my second attempt at hardware design! This time, instead of focusing on a PCB, I wanted to investigate how multiple different parts can come together to create a product. The goal of this project is to create a functional gameboy-esq device that I can play games on! Initially this project was meant to fit inside of an altoids tin, but that was above my skill grade, so I downgraded to a slighly clunkier console. 

I have always enjoyed playing video games but never really considered how the hardware was created. So, this project hit 2 birds with 1 stone: I get a super cool gaming console to add to my collection and I get to learn about hardware >:) 
This project helped me get a glimse and greater appreciation of how hard hardware desgining and moreso planning. However, I picked up some cool skills which was really fun. 

A goal I had for this project specficially was to learn how to CAD using code, which I was able to do using a python script! I can't wait to see how it looks printed out irl. I have always been into coding and its been great seeing a way to directly merge my interest for talking with computers with creating something physical. 

Okay enough yap. If you want more stream of consciousness, look at my journal ;)

## PICTURES

Okay so I made my case in 2 parts so getting 1 coherent 3d screenshot of it is hard so you (the viewer) gets something even better: 2 screenshots (mwuahahahaha)

### bottom:
<img width="394" alt="Screenshot 2025-06-19 at 7 35 33 AM" src="https://github.com/user-attachments/assets/0bbc38ec-8a8b-4231-9f29-af13f70d2dbc" />

### top: 
<img width="673" alt="Screenshot 2025-06-19 at 7 36 02 AM" src="https://github.com/user-attachments/assets/405e045f-d553-4d01-809d-009998ce22e0" />

Because all my components are generally bought (and thus propriotary), ive had a hard time finding 3d models of them and thus they are not in the above. So you have to trust me that they'll fit, but they will :)

So because I can't give you a 3d picture of that, here's a screenshot about how everything's layered and wired 

### layring and wiring
![IMG_4873](https://github.com/user-attachments/assets/9a27b048-a037-46a0-86bd-a43727e81154)

I have a lot of other progress pictures in my journal if you're curious!

## Firmware
So tldr I don't know how to code games (yet!) so I will be utalizing RetroPi. This is included in my firmware and production folders here. 

## BOM

Here's everything you need if you want to build this too! (also includes sweat and tears... forgot to include that in the table)

Also, you might be wonderign why everything is either from Microcenter or Adafruit and not cheaper alternatives like AliExpress. The short answer is my parents won't allow me to purchase stuff from aliexpress. However, if my cost goes above the alloted $150 with future edits or anything, I will be more than happy to pay out of pocket. 

| Item                           | Quantity | Cost   | Source       | Link                                                                                         |
|--------------------------------|----------|--------|--------------|----------------------------------------------------------------------------------------------|
| Raspberry Pi 5                 | 1        | 49.99  | Microcenter  | [Link](https://www.microcenter.com/product/683269/raspberry-pi-5)                           |
| 2.8" PiTFT Display             | 1        | 34.95  | Adafruit     | [Link](https://www.adafruit.com/product/2298)                                               |
| PiGRRL Gamepad PCB            | 1        | 4.99   | Microcenter  | [Link](https://www.microcenter.com/product/503949/adafruit-industries-pigrrl-20-custom-gamepad-pcb) |
| PowerBoost 1000c              | 1        | 19.99  | Microcenter  | [Link](https://www.microcenter.com/product/474415/adafruit-industries-powerboost-1000-charger-rechargeable-5v-lipo-usb-boost-@-1a) |
| 2500 mAh Battery              | 1        | 14.99  | Microcenter  | [Link](https://www.microcenter.com/product/454401/adafruit-industries-lithium-ion-polymer-battery-37v-2500mah) |
| PAM8302 2.5W Audio Amp        | 1        | 3.95   | Microcenter  | [Link](https://www.adafruit.com/product/2130)                                               |
| Mini Metal Speaker            | 1        | 1.95   | Adafruit     | [Link](https://www.adafruit.com/product/1890)                                               |
| 40 pin GPIO Ribbon Cable      | 1        | 2.95   | Adafruit     | [Link](https://www.adafruit.com/product/1988)                                               |
| Slide Switch                  | 1        | 0.95   | Adafruit     | [Link](https://www.adafruit.com/product/805)                                                |
| 6mm Tactile Buttons           | 10       | 9.99   | Microcenter  | [Link](https://www.microcenter.com/product/632688/inland-6x6mm-micro-momentary-tactile-push-button-switches-assortment-kit-10-values-180-pcs) |
| 12mm Tactile Buttons          | 2        | 0.00   | Microcenter  | [Link](https://www.microcenter.com/product/632688/inland-6x6mm-micro-momentary-tactile-push-button-switches-assortment-kit-10-values-180-pcs) |
| 2x20 pin IDC Box Header       | 1        | 0.75   | Adafruit     | [Link](https://www.adafruit.com/product/1993)                                               |
| Heat Sink Kit                 | 1        | 0.00   | Myself       | n/a                                                                                          |
| #4-40 3/8" Machine Screws     | 14       | 0.00   | Myself       | n/a                                                                                          |
| #2-56 3/8" Machine Screws     | 6        | 0.00   | Myself       | n/a                                                                                          |
| **Total**                     | **43**   | **145.45** |              |                                                                                              |

## Closing Remarks On Planning

This has been such a fun thing to fall into this rabbithole where I could desing this. Without Highway (shoutout Hack Club!) I would never have learned this much about hardware in such a short time; I am very grateful for this opportunity. While I do have to part now, I can't wait to build it and enter in my final remarks after I get this to work!
