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

<img width="500" alt="Screenshot 2025-06-20 at 3 31 56 PM" src="https://github.com/user-attachments/assets/b9e5242f-9268-46cf-aa45-03e38b53d607" />

<old version>
<img width="100" alt="Screenshot 2025-06-19 at 7 35 33 AM" src="https://github.com/user-attachments/assets/0bbc38ec-8a8b-4231-9f29-af13f70d2dbc" />

### top: 

<img width="500" alt="Screenshot 2025-06-20 at 3 31 39 PM" src="https://github.com/user-attachments/assets/de781935-8ae9-48c7-b6b3-5d8419f127f2" />

<old version>
<img width="100" alt="Screenshot 2025-06-19 at 7 36 02 AM" src="https://github.com/user-attachments/assets/405e045f-d553-4d01-809d-009998ce22e0" />

### Schematic

<img width="500" alt="Screenshot 2025-06-30 at 4 40 49 AM" src="https://github.com/user-attachments/assets/c07b6f1e-4d40-4ae4-80b6-50886e559fe4" />

<img width="100" alt="Screenshot 2025-06-23 at 3 18 57 PM" src="https://github.com/user-attachments/assets/17d8576e-a649-4678-a186-42d98876e26e" />

### PCB 

<img width="500" alt="Screenshot 2025-06-30 at 4 41 06 AM" src="https://github.com/user-attachments/assets/49769586-41db-4bbd-9350-b0e54036b774" />

<img width="100" alt="Screenshot 2025-06-23 at 3 19 37 PM" src="https://github.com/user-attachments/assets/48193e39-db1a-4de0-b8aa-46e1739a57ba" />

### project as a whole

![IMG_4874](https://github.com/user-attachments/assets/9a6960ba-4fce-481d-b7b9-d3b9cb52c08a)


I know that does not do the wiring justice, so here is a full diagram with pictures!
### layring and wiring

![IMG_4881](https://github.com/user-attachments/assets/7dcbc438-c314-4644-be83-9e41f7f7ddf1)


I have a lot of other progress pictures in my journal if you're curious!

## Firmware
So tldr I don't know how to code games (yet!) so I will be utalizing RetroPi. It is not included in this repo because 1) github was being finicky about pushing it from my desktop folder and 2) its avalible online readilly 

## BOM

Here's everything you need if you want to build this too! (also includes sweat and tears... forgot to include that in the table)

Also, you might be wonderign why everything is either from Microcenter or Adafruit and not cheaper alternatives like AliExpress. The short answer is my parents won't allow me to purchase stuff from aliexpress. However, if my cost goes above the alloted $150 with future edits or anything, I will be more than happy to pay out of pocket. If this project gets downgraded to 4 points, I'd also be willing to pay out of pocket because this is honestly pretty cool and I want to see it in person. I never got a handheld video game console as a kid and I'm excited that I'll be able to make one now :)

| Item                           | Quantity | Cost   | Source       | Link                                                                                         |
|--------------------------------|----------|--------|--------------|----------------------------------------------------------------------------------------------|
| Raspberry Pi Zero 2                 | 1        | 14.99  | Microcenter  | [Link](https://www.microcenter.com/product/643085/raspberry-pi-zero-2-w)                           |
| GPIO header             | 1        | 5.99  | Microcenter       | [Link](https://www.microcenter.com/product/480889/schmartboard-inc-schmartboard-inc-2-x-20-male-headers-qty-5)                                                                                          |

| 2.2" Display             | 1        | 24.95  | Adafruit     | [Link](https://www.adafruit.com/product/2315)                                               |
| Custom PCB           | 1        | $9 + shipping  | JCL PCB  |  |
| PowerBoost 1000c              | 1        | 19.99  | Microcenter  | [Link](https://www.microcenter.com/product/474415/adafruit-industries-powerboost-1000-charger-rechargeable-5v-lipo-usb-boost-@-1a) |
| 2500 mAh Battery              | 1        | 14.99  | Microcenter  | [Link](https://www.microcenter.com/product/454401/adafruit-industries-lithium-ion-polymer-battery-37v-2500mah) |
| stacking header     | 1        | 2.95   | Adafruit     | [Link](https://www.adafruit.com/product/1979?srsltid=AfmBOoqbo1ndLmYMVLTt_bqD4Yhi48SgEFRf9jc0nGi86ePSABa_MOBi)                                               |
| Slide Switch                  | 1        | 0.95   | Adafruit     | [Link](https://www.adafruit.com/product/805)                                                |
| 6mm Tactile Buttons           | 10       | 9.99   | Microcenter  | [Link](https://www.microcenter.com/product/632688/inland-6x6mm-micro-momentary-tactile-push-button-switches-assortment-kit-10-values-180-pcs) |
| #4-40 3/8" Machine Screws     | 14       | 0.00   | Myself       | n/a                                                                                          |
| #2-56 3/8" Machine Screws     | 6        | 0.00   | Myself       | n/a                                                                                          |
| **Total**                     | **44**   | **~115** |              |                                                                                              |

## Closing Remarks On Planning

This has been such a fun thing to fall into this rabbithole where I could desing this. Without Highway (shoutout Hack Club!) I would never have learned this much about hardware in such a short time; I am very grateful for this opportunity. While I do have to part now, I can't wait to build it and enter in my final remarks after I get this to work!
