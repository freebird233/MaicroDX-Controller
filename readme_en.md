```markdown
# MaicroDX-Controller
An integrated circular control wheel based on CH552, compatible with most 11-inch tablets and the [MaicroDX frame](https://github.com/freebird233/MaicroDX)

<br>
<br>

 **Features:**  Integrated main control; full‑color lighting effects; all content open source.
<br><br>
**Known issues:**  Only 6‑key rollover; non‑feedback lighting; more to be discovered.
<br> <br> <br>

    This project is for learning and sharing. The keys simulate keyboard input, so you need to handle software‑side issues on your own.
    
[MaicroDX Tech Community](http://qm.qq.com/cgi-bin/qm/qr?_wv=1027&k=uaJAwiIXVH5AWTCzZIfZjyvK5NMUc5RV&authKey=3EfBhaKBnfT3eZ%2F9ZlTbbR4r84ucNtt%2F%2FNDzzINnJAItXKx8PftKUk%2FCVn4rtrLw&noverify=0&group_code=1055571063)
 <br> <br> <br>

 # Special Thanks



- __@Fandorabox__ for naming this project <br>

- **「He Yin Wu」 Riichi Mahjong / Rhythm Games / Arcade** for providing physical cabinets as scanning references <br>

- **JLCPCB & EasyEDA** for reducing costs for individual creators <br>

<br> <br> <br> 


# About the License

I created this project in my personal time without any financial interest or sponsorship. I will continue to improve it. I have done my best to ensure the accuracy and functionality of all content, but errors are always possible. I cannot be held responsible if you lose time or money due to using this open‑source project. Thank you for your understanding. The MaicroDX series follows the [by‑nc‑sa license](https://creativecommons.org/licenses/by-nc-sa/4.0/). This means you can only DIY for yourself and your friends – you may not use this project to make money, e.g., paid assembly, selling complete units, etc. Please note that group buys and pooled orders for original components are reasonable, and selling leftover components in a non‑profit way is also acceptable.
<br> <br> <br> 

# Operation Modes
The MaicroDX Controller (hereinafter MDXC) has two modes. Please decide which solution fits your use case before starting production.
<br> 
<br> 

| **A_Mode** (STBY shorted) | B_Mode (STBY open) |
| :--- | :--- |
| Integrated mode, ideal for portability. Connect the wheel directly to the device via a USB‑C cable. Attach the wheel to the tablet with “nano” tape. (**All components soldered**) | External control mode, used with the [MaicroDX frame](https://github.com/freebird233/MaicroDX). **Only solder the WS2802 LEDs and the FPC connector**, connect to an external control board, then to the tablet via a data cable. (Because most data cables do not have enough space to fit inside the frame.) |
<br> 
<br> 
<img width="270"  alt="_cgi-bin_mmwebwx-bin_webwxgetmsgimg__ MsgID=5978720347427026372 skey=@crypt_5b51cbfd_c97b3b7ed41217eeedefb33553f2231f mmweb_appid=wx_webfilehelper" src="https://github.com/user-attachments/assets/31d41ac2-2bd1-482f-ad18-089340bdea1b" />
<img width="310"  alt="Snipaste_2026-06-20_23-03-16" src="https://github.com/user-attachments/assets/fcc64922-dd17-4255-9f67-8fe9722c466b" />

<img width="365"  alt="MVIMG_20260702_210600" src="https://github.com/user-attachments/assets/7261631c-6163-49fe-ba23-75936402fdc6" />


<br> <br> <br> 
# 1. Purchase Components
1. Resistor 5.1kΩ ±1% 0805 package – 2 units
2. Resistor 10kΩ ±1% 0805 package – 2 units
3. Capacitor 0.1µF ±1% 0805 package – 2 units
4. WS2812B addressable RGB LEDs, side‑view type ×8 – approx. ¥6
5. Cherry low‑profile red switches ×8 – approx. ¥20
6. USB‑C receptacle, surface‑mount, TYPE‑C 16‑pin 2MD(073) – ¥1
7. CH552G MCU ×1 – ¥2
8. FPC connector, 12‑pin ×2 – AFC01‑S12FCA‑00 (optional, for B_Mode external board) – ¥2
9. FPC cable, 12‑pin, 50cm, reversed ×1 – ¥1~2
10. HC‑1.25‑2PWT balance connector (optional, for MDX frame, hot‑swappable 9‑pin key cable) – ¥1
11. FPC cable, 12‑pin, reversed (optional for B_Mode external board) – ¥1
12. M1.4×4.5 nickel plated countersunk self‑tapping screws ×8 (optional, for decoration) – ¥5.8
<br> <br>
Note: Soldering iron, solder paste, flux, desoldering wick, etc. are not listed here.
<br> <br>

# 2. Order PCB
- Choose the thinnest board thickness possible.<br><br>
For example, JLCPCB recently removed the non‑standard process fee; 2‑layer, 0.8mm thick, white, leaded HASL finish.<br>
Sample order cost approx. ¥16 per board.


<br> <br>
# 3. 3D Print the Case
Download Model.STEP from the Releases section. <br>
<img width="1200" alt="Snipaste_2026-07-02_23-48-56" src="https://github.com/user-attachments/assets/4cb6bfd1-12f3-4750-9b2f-d03b26c6ff84" />
It consists of two parts: “Case” and “Base”. Use the split function in your slicer to print them separately. (Interference fit.) <br> 
The case has large overhang areas; it is best to use different materials as support interfaces during printing (e.g., PLA as support for PETG). <br>
Same for the keycaps. <br>
(I will upload 3MF files later.) <br>

<br> <br>
# 4. Solder Components
Soldering usually follows the order from difficult to easy. The USB‑C receptacle, FPC connectors, and WS2812B LEDs are usually handled first. (Use solder paste and plenty of flux.) <br>
If using reflow soldering, note that the FPC connectors are on the bottom side of the board.
<br>
<br>
If using the external control board, only solder the LEDs and the FPC connector on the round PCB; leave the other components as shown below.<br>
<img width="480" alt="abd05224c374d1d27d987409a571683e" src="https://github.com/user-attachments/assets/f13a7d16-cb30-456b-a744-40a4c49857ca" />
<br>(The pads are left empty.) (The 12‑pin FPC connector is on the bottom layer.)

<br> <br>
# 5. Flash the Firmware
Download the programmer software [WCHISPStudio](https://www.wch.cn/downloads/WCHISPTool_Setup_exe.html) from the official website. <br> 
Download the .hex firmware from the Releases section.<br>
    (Keys 1‑8 output c, x, z, a, q, w, e, d respectively; key 9 outputs 3. At the same time, long‑press keys 3,4,5,6 for 400ms to toggle between track‑selection lighting and game lighting; long‑press keys 7,8,1,2 for 400ms to enter rainbow‑gradient lighting mode; to exit, long‑press 3,4,5,6 again.)<br>
Before powering on, remember to use a multimeter to check that 5V and GND pads are not shorted.<br>
<img width="720" alt="Snipaste_2026-07-02_20-34-18" src="https://github.com/user-attachments/assets/3abe23a6-3a7c-488c-9f09-9790bfdc47e0" /> <br>
Connect the board to the computer; the device name will appear.<br>
Click “Program”.<br>
Flashing complete.<br>

https://github.com/user-attachments/assets/6a8587d2-b886-4417-bf86-0edc023bd731

<br>

- Check that the indicator LEDs light up in sequence (as in the video above). Due to the serial‑data transmission characteristic of WS2812, if one LED’s signal pad is disconnected, all subsequent LEDs will remain off.<br><br>

- Short the two pads of each key to check that a key‑press signal is output, and that the white LED turns yellow.<br>

<br>
<br>

# 6. Assembly
<br>After confirming everything is correct, insert the FPC board into the 3D‑printed case, install the low‑profile red switches, and fill the gaps around the switch pins with solder. <br>
Close the back cover.
```
