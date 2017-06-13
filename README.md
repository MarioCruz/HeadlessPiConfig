# HeadlessPiConfig

This  will get you up and running with a Raspberry Pi, connected to your wifi network and accessible over ssh, without ever needing to connect anything to it, besides power.

# Requirements:
* Raspberry Pi with integrated wifi chip - Pi 3 or Pi Zero W
* Compatible micro SD card - at least 4GB
* Power source for the Raspberry Pi
* A wifi access point you want to connect the Pi to


# Prepare SD card with Raspbian or Raspbian lite
* Download the latest Raspbian LITE image from the official [Raspberry Pi website](https://www.raspberrypi.org/downloads/raspbian/)
* Use [Etcher](https://etcher.io/) to flash the Raspbian .img-file to the SD card. 
* When done leave the SD card in your PC
* A boot drive should appear. Open a terminal/comand promt and cd to the boot drive using the following command
''cd /Volumes/boot''
# Configure ssh and wifi
