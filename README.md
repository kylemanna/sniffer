# Sniffer

[![License: CC BY-SA 4.0](https://img.shields.io/badge/License-CC%20BY--SA%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-sa/4.0/)

Air quality sensor integration board that couples together the following modules:

- ESP32 TTGO T-Display module
- PMSA0003 module
- BME680 CJMCU module

I use this to track the AQI in my home.  This sensor measures within 1% of 3x different [PurpleAir sensors
scattered around my
neighborhood](https://www.purpleair.com/map?opt=1/i/mAQI/a10/cC0#12.69/37.74937/-122.43828).  The PMSA003 particulate air sensor module in this build should be an
improved version the PMS5003 found in the [PurpleAir
sensors](https://www2.purpleair.com/collections/air-quality-sensors).

Combined with [Home Assistant](https://www.home-assistant.io/), [InfluxDB](https://www.influxdata.com/),
and [Grafana](https://grafana.com/) I can track the long term air quality inside and outside my home.

## Details

* [Blog post with more details](https://blog.kylemanna.com/hardware/sniffer-air-quality-monitor-aqi-using-esp32-pmsa003-bme680/)

## Order PCBs

Want to build one?

[Visit the shared project on PCBWay for direct ordering](https://www.pcbway.com/project/shareproject/Sniffer_Air_Quality_Monitor.html).

## Early PCB Assembly

![Sniffer LCD Display](https://lh3.googleusercontent.com/pw/ACtC-3cUrlEqcjlo5lC5yUb1jhKA47HwOdIz_2EqyhSbRKBafn0sFT-LFw-hktcGfGLzMklzupLXcvpzygAOrUNhSO8iCpv7LB54ff_Vy3t7k4sswQHhVmiiHSoFrEV_OZZcB0HpGEvIkUFvzxMVi0j_Ls6svQ=w1912-h1085-no?authuser=0)

[Google Photos Image
Gallery](https://photos.google.com/share/AF1QipN3LYySqBTejioxieJ7yeqid8oVPh8rAkidfJqBqCnVjT7ktObNcwMXL6851PJW0A?key=LUZIQldwbzFlQjRHanFIWURqUy1ORU8ydTBkUnR3)

## TODO

### Hardware

- [x] Design Kicad schematic + PCB
- [x] Release Gerbers
- [x] Order PCBs from [PCBWay (use my referral code "3549" to save $5)](https://www.pcbway.com/setinvite.aspx?inviteid=3549)
- [x] Photograph real PCB + PCBA

- [ ] Add pin labels to silk screen
- [ ] Route out hole for TTGO T-Display battery connector so it fits flatter
- [ ] Find someone to make a 3D printable enclosure

### Software

- [x] Upload ESPHome YAML file
