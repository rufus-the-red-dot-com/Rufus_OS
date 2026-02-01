# 🏛️ The Rufus Hardware Archive
**Master Source for the Rufus Standard Handheld Ecosystem.**

This repository contains the complete Firmware Library and logic for the Rufus line of custom handhelds. These projects track the evolution from 3-button "Origin" devices to dual-stick and rotary-encoded systems.

## 📱 The Device Roster

1. **/Rufus_1.0**: The baseline stable build. Firmware Library.
2. **/Rufus_RTC**: Time-persistent build featuring Real-Time Clock integration.
3. **/Origin_Tetris**: 4-button tactical layout for falling-block logic.
4. **/Origin_Pool_Breakout**: 3-button physics-based "Origin" device.
5. **/Rufus_Rotary**: Precision input build using an incremental rotary encoder.
6. **/Rufus_Tiny**: Ultra-compact firmware optimized for minimal footprint.
7. **/Rufus_TwinStick**: Dual analog input configuration for 360-degree combat.
8. **/Rufus_MP3**: Multimedia build with DFPlayer/serial audio integration.

## ⚡ The Rufus Wiring Standard
Cross-compatibility is maintained through a unified hardware abstraction layer.

| Component | Pin | Logic |
| :--- | :--- | :--- |
| **OLED SDA** | A4 | I2C Data |
| **OLED SCL** | A5 | I2C Clock |
| **Joystick X / Rotary A** | A0 | Analog / Encoder A |
| **Joystick Y / Rotary B** | A1 | Analog / Encoder B |
| **Action / Fire** | D11 | Primary (Active Low) |
| **Menu / Back** | D10 | Secondary (Active Low) |
| **Buzzer High** | D3 | PWM (UI / Treble) |
| **Buzzer Low** | D6 | PWM (SFX / Bass) |
(make sure to double check wiring in code) 



## 🚀 Build Instructions
1. Install **U8g2** via the Arduino Library Manager.
2. Ensure your OLED is at I2C address `0x3C`.
3. For the **TwinStick**, secondary axes map to **A6/A7**.
4. For the **MP3 Player**, Serial RX/TX is handled on **D2/D4**.
5. Some devices may require other libraries ( such as the rotary requiring Encoder by paul stroffegen ) 
