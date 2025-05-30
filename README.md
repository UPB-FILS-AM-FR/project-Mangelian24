# Capacitive Touch Piano with ESP32

| | |
|-|-|
|`Author` | Angelian Maria Georgiana 
**Grupa:** 1220FB
**E-mail:** maria.angelian@stud.fils.upb.ro 

## Description
The **Capacitive Touch Piano** is a simple digital piano implemented using an **ESP32 microcontroller**, an **MPR121 capacitive touch sensor**, and an **LM386 audio amplifier**. It allows users to play musical notes by touching capacitive pads connected to the MPR121. The ESP32 generates corresponding PWM signals to produce sound, which is then amplified and played on a passive piezo buzzer.

The aim of the project is to explore microprocessor architecture concepts such as:

- Interfacing with external peripherals via **I2C**
- Handling external **interrupts**
- Using **PWM timers** for sound generation
- Managing **real-time responsiveness**

## Motivation

## Architecture

### Block diagram

![Block Diagram](schematics/block_diagram.png)

### Schematic

![Schematic](schematics/kicad_schematic.png)

### Components

### 3.3. Components

### 3.3. Components

| Device                                       | Usage                                                    | Quantity | Unit Price (RON) | Total Price (RON) | Link / Source (Example)                                                                                                                     |
| :------------------------------------------- | :------------------------------------------------------- | :------- | :--------------- | :---------------- | :---------------------------------------------------------------------------------------------------------------------------------------- |
| ESP32 Dev Board (cu WiFi & Bluetooth)        | Microcontroller, control, signal generation              | 1        | 34.99            | 34.99             | [OptimusDigital](https://www.optimusdigital.ro/ro/placi-cu-bluetooth/4371-placa-de-dezvoltare-esp32-cu-wifi-i-bluetooth-42.html)       |
| MPR121 Capacitive Touch Sensor Module        | I2C touch sensor, reads up to 12 electrodes            | 1        | 8.39             | 8.39              | [Bitmi](https://www.bitmi.ro/electronica/modul-senzor-capacitiv-de-atingere-mpr121-10801.html)                                             |
| LM386 Audio Amplifier Module                 | Audio amplifier for passive buzzer                       | 1        | 6.48             | 6.48              | [OptimusDigital](https://www.optimusdigital.ro/ro/electronica-de-putere-amplificatoare-audio/45-amplificator-audio-lm386.html)              |
| Passive Buzzer Module (KY-006 or similar)    | **Passive sound output device (for notes)**              | **1**    | **2.39**         | **2.39**          | [Bitmi KY-006](https://www.bitmi.ro/electronica/modul-buzzer-pasiv-ky-006-10678.html)                                                      |
| Active Buzzer (3V)                           | Buzzer for simple alerts (optional, if used)             | 2        | 0.99             | 1.98              | [OptimusDigital](https://www.optimusdigital.ro/ro/audio-buzzere/635-buzzer-activ-de-3-v.html)                                           |
| Breadboard 750 points                        | Main prototyping area (if this is your primary one)      | 1        | 11.99            | 11.99             | [OptimusDigital](https://www.optimusdigital.ro/ro/prototipare-breadboard-uri/13245-breadboard-750-puncte.html)                           |
| Breadboard 400 points                        | Prototyping area (if used in 2-breadboard setup)         | 1        | 4.56             | 4.56              | [OptimusDigital](https://www.optimusdigital.ro/ro/prototipare-breadboard-uri/44-breadboard-400-points.html)                               |
| Breadboard 170 points (SYB-130)              | Auxiliary breadboard for ESP32 mounting (if used)        | 1        | ~5-8             | ~5-8              | *(Preț estimat, dacă a fost achiziționat)*                                                                                                   |
| Jumper Wires (Male-Male, 40pcs, 10cm)        | Connecting components                                    | 1 set    | ~7               | ~7                | [OptimusDigital M-M](https://www.optimusdigital.ro/ro/fire-fire-mufate/884-set-fire-tata-tata-40p-10-cm.html)                             |
| Jumper Wires (Female-Male)                   | Connecting components (ESP32 to breadboard points)       | 1 set    | ~7-10            | ~7-10             |  [OptimusDigital M-M]                                                                                      |
| DIY Touch Pads                               | Copper tape or other conductive material on cardboard    | ~1m      | ~5-10            | ~5-10             | ( cardboard)                                                                       |
| **SUBTOTAL ESTIMAT (config. 2 breadboards: 400pt + 170pt)** |                                                          |          |                  | **~80 - 96**      | *(ESP32, MPR121, LM386, Buzzer Pasiv, 2x Buzzer Activ, BB400, BB170, Fire M-M, Fire F-M, Condensator, DIY Pads)*                |
| **SUBTOTAL ESTIMAT (config. 1 breadboard mare: 750pt)**     |                                                          |          |                  | **~83 - 99**      | *(ESP32, MPR121, LM386, Buzzer Pasiv, 2x Buzzer Activ, BB750, Fire M-M, Fire F-M, Condensator, DIY Pads)*                  |

## Hardware Used

| Component                     | Description                                      |
|------------------------------|--------------------------------------------------|
| ESP32 Dev Board (Plusivo)    | Microcontroller for control and signal generation |
| MPR121 Capacitive Touch      | I2C touch sensor for reading up to 12 electrodes |
| LM386 Amplifier Module       | Audio amplifier for passive buzzer               |
| TMB12A03 Piezo Buzzer        | Passive sound output device                      |
| 0.1µF Capacitor              | DC blocking capacitor                            |
| Breadboards (400pt + 170pt)  | Prototyping area for mounting ESP32 and wiring   |
| Jumper Wires (M-M, F-M)      | Connections between components                   |
| USB Cable                    | Programming and power supply for ESP32           |

## Software Used

| Software            | Description                           |
|---------------------|---------------------------------------|
| Visual Studio Code  | Main IDE                              |
| PlatformIO          | Build system and library manager      |
| Arduino Framework   | Programming framework for ESP32       |
| Adafruit_MPR121     | Library for interfacing with MPR121   |
| Adafruit_BusIO      | I2C abstraction layer (dependency)    |

### Libraries

| Library | Description | Usage |
|---------|-------------|-------|
| [lib-name1](link-to-lib) | official description of the lib | Used for accesing the peripherals of the microcontroller  |
| [lib-name2](link-to-lib) | official description of the lib | Used for accesing the peripherals of the microcontroller  |

## Log

### Week 10
Set project theme and add project information
Created project page and briefly described functionality

### Week 12
Purchased project-specific parts, created electrical schematic + hardware implementation
Added Hardware Design and connected all physical components
Created the case for a nice exterior look.

### Week 13
Finished software implementation of the project, added software implementation and finished documentation page

## Reference links

[Tutorial 1](https://www.youtube.com/watch?v=wdgULBpRoXk&t=1s&ab_channel=BenEater)

[Tutorial 2] (https://randomnerdtutorials.com/vs-code-platformio-ide-esp32-esp8266-arduino/#4)

[Tutorial 3] (https://forums.raspberrypi.com/viewtopic.php?t=196514)

[Tutorial 4] (https://docs.sunfounder.com/projects/kepler-kit/en/latest/pyproject/py_fruit_piano.html)

[Tutorial 5] (https://www.youtube.com/watch?v=sqQzIN7G6Oc&ab_channel=Sinsay)

[Tutorial 6] (https://projecthub.arduino.cc/abhilashpatel121/diy-arduino-based-continuous-touch-piano-b0b8e3)

[Tutorial 7] (https://www.hackster.io/gatoninja236/capacitive-touch-sensing-grid-f98144)

[Tutorial 8] (https://blog.arduino.cc/2022/04/05/the-arduipiano-is-an-arduino-powered-floor-piano-that-lets-you-play-music-with-your-feet/?queryID=undefined)

[Tutorial 9] (https://www.instructables.com/MIDI-Bookmark/)

[Tutorial 10] (https://www.youtube.com/watch?v=Z2v-kq9tvgg&ab_channel=7DAYS)


