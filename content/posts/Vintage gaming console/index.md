+++
date = '2025-09-07T23:19:45+02:00'
draft = false
title = 'Vintage_gaming_console'
+++

I certainly have a weak spot for vintage electronics. That’s why I absolutely wanted to revive this old CRT TV that we found when moving into our new place.

I transformed this TV into a vintage gaming console with a Raspberry Pi that runs RetroPie, an operating system that turns the Pi into a retro gaming machine.

Connecting the Pi to a TV that dates back to the beginning of the seventies was however not straightforward. Back then, TV’s were mostly used to watch live broadcasts so they lacked any kind of auxiliary inputs. This television set too only features a UHF/VHF antenna connector at the back.

The solution came in the form of a UHF transmitter that I found on AliExpress. It connects to the Pi’s composite video output and broadcasts the signal to a specific channel. All it then takes is to tune the TV to that channel. Note however that the use of such a transmitter may not be fully compliant with local regulations regarding radio transmitters.

This method works, but is definitely not perfect as the image is easily disturbed by any interference coming from e.g. the USB and power cables. The audio signal was also very faint and noisy, but this is probably due to ageing of the amplifier electronics in the TV. As a retro game is not complete without its 8-bit tunes, I added a separate amplifier and speaker to the Pi.

The Pi, UHF transmitter, audio amplifier and speaker are mounted in a 3D-printed box, designed to fit in the recessed section in the back of the TV. The box also powers the TV via it’s DC input. The controllers are cheap USB Nintendo SNES controllers that are compatible with the Raspberry Pi.

A more detailed article on the use of an UHF transmitter with a Raspberry Pi can be found here. The YouTube channel “Technology Connections” also made an excellent video on the magic of analog CRT TV’s