# EXPERIMENT-01-INTERFACTING-DIGITAL-OUTPUT-WITH-EDGE-DEVICE---RASPBERRYPI-PICO-
## NAME : S.MOULIDHARAN
## DEPARTMENT : AIML
## ROLL NO : 212224240095
## DATE OF EXPERIMENT : 24/02/2024

### AIM
To interface a digital output device (LED) with the Raspberry Pi Pico and control it using MicroPython.

APPARATUS REQUIRED
Raspberry Pi Pico
LED (Light Emitting Diode)
330Ω Resistor
Breadboard
Jumper Wires
USB Cable
Computer with Thonny IDE
## THEORY
Raspberry Pi Pico is a microcontroller board based on the RP2040 chip. It supports MicroPython, making it suitable for IoT and embedded applications.

Digital Output refers to controlling external devices like LEDs, buzzers, or relays using GPIO (General Purpose Input Output) pins. A GPIO pin can be set to HIGH (3.3V) or LOW (0V) to turn the device ON or OFF.

## Working Principle:

The LED is connected to one of the GPIO pins of the Pico.
The MicroPython script sets the GPIO pin HIGH to turn the LED ON and LOW to turn it OFF.
CIRCUIT DIAGRAM
Connect the anode (longer leg) of the LED to GP15 via a 330Ω resistor.
Connect the cathode (shorter leg) of the LED to GND (ground).


## PROGRAM (MicroPython)
```
from machine import Pin
from utime import sleep
led1=Pin(0,Pin.OUT)


while True:
    led1.toggle()
    sleep(0.5)
```
```
from machine import Pin
from utime import sleep
led1=Pin(0,Pin.OUT)
led2=Pin(1,Pin.OUT)
led3=Pin(2,Pin.OUT)

while True:
    led1.toggle()
    sleep(0.5)
    sleep(0.5)
    led2.toggle()
    sleep(0.5)
    led3.toggle()
    sleep(0.5)
```
```
from machine import Pin
from utime import sleep
led1=Pin(0,Pin.OUT)
led2=Pin(1,Pin.OUT)
led3=Pin(2,Pin.OUT)
buzz=Pin(3,Pin.OUT)
while True:
    led1.toggle()
    sleep(0.5)
    buzz.toggle()
    sleep(0.5)
    led2.toggle()
    sleep(0.5)
    buzz.toggle()
    sleep(0.5)
    led3.toggle()
    sleep(0.5)
    buzz.toggle()
    sleep(0.5)
```



## OUPUT
![COMPUT](https://github.com/user-attachments/assets/62427638-a939-47a2-afe1-dc42ba92bd7b)

![Screenshot 2025-02-24 113949](https://github.com/user-attachments/assets/f4c9eccc-2df5-4d1a-bc51-89428af4af07)


![EDGE](https://github.com/user-attachments/assets/08055457-cacf-40f0-a649-9f19dd35be0d)





 
## RESULTS
The LED connected to the Raspberry Pi Pico successfully turns ON and OFF at 1-second intervals, confirming the proper interfacing of a digital output.
