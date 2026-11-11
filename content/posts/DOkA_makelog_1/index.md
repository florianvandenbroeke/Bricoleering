+++
date = '2026-11-11T00:42:09+01:00'
draft = false
title = 'DOkA - Hardware choices'
# tags = []
project = 'DOkA'
type = 'makelog'
nummer = 1
+++

The hardware for DOkA in a nutshell:
* Microcontroller: ESP32-S3-N8R8
* Camera: OV5640/OV2640
* Storage: microSD card
* Screen: 2.9" e-ink screen
* Battery charging: BQ21040 + separate power path

I wanted to design a custom PCB that I could assemble myself. I only have a soldering iron, so it was important that all the components are hand solderable without any special equipment (e.g. no QFN packages).

The microcontroller was by far the easiest component to select. The ESP32-S3-N8R8 has just enough GPIOs for the camera, the screen and the other components, offers PSRAM, has native USB support for the photo transfer and enough computing power.

Choosing the storage was less obvious than it may seem. I didn't want the user to unplug the card and see the photos before developing time was over. I first thought of using an SD NAND chip soldered directly to the board. However, these seemed quite expensive and difficult to find in a package that is hand-solderable. I had some microSD cards lying around, so I decided to use those for storage. The undeveloped photos will be encrypted, with the encryption key stored in the flash. Yes, it’s still possible to read the encryption key from the flash, and see the photos early, but if you do this, you clearly don’t understand the point of this device.

The OV2640 and OV5640 camera modules are easy to buy and very well documented. Their image quality isn’t the best, but enough for a camera that doesn’t want to be perfect. I’m still not sure whether to use the 2MP or 5MP option, but for now, I’m going with 5MP.

At first, I wanted to use a 1.54” e-ink screen. This would be more than enough to display the frame counter and camera status, but not for the live preview, so instead I went with a 2.9inch version.

Some battery charge ICs have built-in power path management (this separates the load from the battery while charging, so the charger isn’t disturbed by the load current), but these were rather hard to find in a hand-solderable package. I chose the BQ21040 because it has built-in temperature protection and implemented the power path separately with a diode and a P-channel MOSFET.