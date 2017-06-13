# HeadlessPiConfig

This  will get you up and running with a Raspberry Pi, connected to your wifi network and accessible over ssh, without ever needing to connect anything to it, besides power.

# Requirements:
* Raspberry Pi with integrated wifi chip - Pi 3 or Pi Zero W
* Compatible micro SD card - minimum 4GB
* Power source for the Raspberry Pi
* A wifi access point you want to connect the Pi to


# Prepare SD card with Raspbian or Raspbian lite
* Download the latest Raspbian LITE image from the official [Raspberry Pi website](https://www.raspberrypi.org/downloads/raspbian/)
* Use [Etcher](https://etcher.io/) to flash the Raspbian .img-file to the SD card. 
* When done leave the SD card in your PC
* A boot drive should appear. Open a terminal and cd to the boot drive using the following command

```cd /Volumes/boot```
# Configure ssh and wifi
* Enable ssh
By default, a clean Raspbian image will have ssh disabled
In the *boot* drive, create a file called ssh

```touch ssh```
This will enable ssh when you Pi boots for the first time.
# Connect wifi
* To make the Pi connect to your Wifi access point at first *boot*, store the wifi connection details on the Pi’s boot drive.
```nano wpa_supplicant.conf```
* Paste the following content in the wpa_supplicant.conf file, adjust it with your wifi details and save it with *ctrl + x* .
```
network={
    ssid="YOUR_SSID"
    psk="YOUR_WIFI_PASSWORD"
}
```

# First Boot
* The SD card is now ready to boot. Disconnect the SD card from your computer and put it in the Pi.
* Tunr the Pi on and after about 50 seconds the Pi should be fully booted and connected to your wifi network.
* Test that the Pi and is connected 
From you PC test if it is online on your local wifi 

```ping raspberrypi.local```

If it work you should have a response like 

```PING raspberrypi.local (192.168.1.68): 56 data bytes```




