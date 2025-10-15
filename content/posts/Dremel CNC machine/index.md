+++
date = '2022-08-18T23:05:51+02:00'
draft = true
title = 'Dremel CNC machine'
+++

A CNC milling machine has a lot in common with 3D-printers: they both turn a digital design into a physical object. The difference however, is that they can use different materials such as wood or metal, alongside plastic. Having one in your workshop is thus really useful! In this post I’ll show how I built my own CNC machine using 3D printed parts and a cheap rotary tool.

## Background

Since I first heard about 3D-printers, I’ve always dreamt of having one myself. So back in 2018, when good printers became really affordable I got myself an Ender 3. I was extremely happy with this machine and it opened up so much new possibilities to design and print stuff. Combining this with my passion for electronics allowed me to start working on real projects and further developed my passion for making.

Recently however, I kinda had the feeling that I explored the world of 3D-printing enough and it was time to get my hands on something new. My first thought was to get a laser cutter, but after doing some research I found them rather expensive and was worried about the safety of these machines. Eventually I decided to build my own CNC milling machine.

When it comes to self-built CNC machines, there are tons of people who developed and built their own machines from scratch and provide detailed building instructions. At first I started looking at the MPCNC project. Though the machine looks sturdy and the documentation is quite good, I thought this machine would be too cumbersome and expensive for my needs.

Finally, I decided to build a Dremel CNC designed by Nikodem Bartnik. I thought the design looked promising and actually pretty awesome. This project is also extremely well documented in a series of YouTube videos and a well-written instructable. Another important aspect was the ability to find the different components pretty cheaply.

## Components

All the needed components can be found in a spreadsheet that Nikodem Bartnik made for this project.
I bought most of the electronics in a kit that bundles an Arduino UNO, CNC shield, stepper drivers… for a reasonable price on Amazon. The stepper motors can also be found pretty cheaply on Amazon. For the power supply I used an old 12V 2.5A adapter I had laying around.

Most of the mechanical components such as linear bearings, T-nuts, lead screws etc were also purchased from Amazon. I found the steel rods and aluminium extrusions on a german webstore “Dold Mechatronik” for a reasonable price and shipping fee. The screws and plywood for the bed can easily be found in a hardware store.

The first weeks of this project consisted solely of 3D printing all the components. Most of the parts require support and are quite long and complex to print, but my old Ender 3 handled the job just fine. The only problem I had was the filament spool falling of the machine near the end of a 20-hour print which was quite frustrating. I printed all the parts with PLA at a .25mm layer height and 25% infill. I guess that the total amount of material required is about 1kg.

The biggest change I made to the project is the use of an other spindle. For my machine, I used a cheap multitool I bought from Conrad a few years ago instead of the Dremel tool. To mount it to the machine, I designed my own holder using the original model that can be found on Thingiverse. Though this multitool is a little less powerful than the Dremel it does a good job at milling wood and is actually quite good for the money!

I estimate the total cost of this project (including spindle and filament) somewhat above €250, which is actually a pretty good deal for a machine this size

## The build

The build itself went surprisingly smooth (given my inexperience with mechanical projects) using the instructable and YouTube videos. I noticed however that the tolerances on my printer aren’t as accurate anymore. Because of this some of the parts cracked a bit when inserting the bearings. Luckily this didn’t result in a fatal fracture of the part. Also, to insert the steel rods into the openings quite some force and a hammer had to be used, with the risk of damaging the part.

I decided to use the original dimensions for my machine, so I cut the rods and lead screws to the specified lenghts. However, when assembling the Z-axis carriage, I noticed that the lead screw was a little bit too long. I solved this problem by 3D-printing a part that offsets the motor a little, but shortening the lead screw is also possible of course.

For the connection of the lead screw to the motor axis, the 3D printed couplers do a good job, but remember to provide some small set screws to hold everything together. It’s also possible to use metal couplers, but choose rigid ones as the flexible ones will introduce quite some backlash.

Assembling the electronics is quite straightforward for anyone that’s worked with Arduino before. The only problem I had was that the steppers for the X axis would move at different speeds causing the whole carriage to block. This was due to a bad connection between the microstepping jumpers.

After the assembly, testing and some final touches such as cable management, I ended up with the machine as in the picture above. I’m overall very happy with the way this machine turned out. I think it looks quite good and feels pretty sturdy.

Obviously, the goal of this machine isn’t to look good, but actually mill something. After mounting a piece of wasteboard and figuring out how the CAM module works in Fusion360, it was time for the first real test! I milled a simple circular test piece out of MDF almost successfully. The only problem was that I was a little too aggressive with the cut speed and spindle speed during the contour cut causing the machine to block. Using lower speeds successfully freed the piece. The dimensional accuracy of this first piece wasn’t great, but after changing to rigid couplers as discussed above, the accuracy improved a lot.

The machine already did a good job on MDF, but I’m looking forward to experiment with more materials such as different kinds of wood, acrylic and maybe even some aluminium. I’ll probably also do some upgrades such as a more powerful spindle and a dust collection system. At the end of this project, I’m really happy with the result and I’ve learned a lot during the process, both about making this machine and CNC milling in general!