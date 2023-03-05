TSL2561 Library
=======================================


A MicroPython library for interfacing with the TSL2561 light sensor.

It's a fork of the depreciate lib : https://github.com/adafruit/micropython-adafruit-tsl2561

Works fine with Raspbery pi pico and micropython.
Tested with : 
  sysname='rp2'
  nodename='rp2'
  release='1.19.1'
  version='v1.19.1-910-g4937174b4 on 2023-03-01 (GNU 12.1.0 MinSizeRel)'
  machine='Raspberry Pi Pico with RP2040'

## Usage
```python
from machine import Pin, I2C
from tsl2561 import TSL2561

i2c=I2C(0,sda=Pin(4),scl=Pin(5), freq=100000) # 100 kHz!!!
sensor = TSL2561(i2c) #default addr is 0x39 = 57
lum = sensor.read()

print(f"Luminosity : {lum} lux")
```

