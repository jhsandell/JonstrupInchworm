# Jonstrup Inchworm 3D Printer

## The Machine
This page explains the motivation for building a novel 3D printer with a unique kinematics. Design choices 
will be described in no particular order.

## Background
I discovered the 3D printing and associated Maker hype around 2010. For more than a year I just sat in front of 
my computer, and gobbled up loads of youtube videos, and trawel endless seas of webpages. In 2012 I finally 
found the funds (outside the household budget) for procuring a 3D printer: a RepRapPro Mendel (mono / legacy).
Almost the coincidentally I started flying RC model aircraft. And the primary purpose for buying a printer was
to print spare parts for the model aircraft __when__ they eventually crashed.

Later, I had the wish to print larger volumes, like aircraft wings, but the machines on the market did not scale
properly with costs, and to make matters worse, all seemed to take up way to much tabletop real estate. I simply
could not fit those into my cramped cave.

## Primary design points
- When build volume increases, you want the build platform to be static. Accellerating a huge platform back 
and forth is neither good for the object you are printing nor the machine itself. Oscillations will occur and
the machine will shake apart.
- A static build platform could also be the base for the machine. A disused kitchen tabletop would fit the
purpose; its structurally strong, its heat resistant, and to some point isolating.
- It has to sit on my desk, so it cannot be supported on the front side, or be enclosed like a Makerbot, a 
Ultimaker or a CNC machine.
- With increasing dimensions, the down-bending of the structural parts has to be considered. So first option 
was to use a hollow 2020 aluminium tube. A square tube is more stiff than a cylidrical of same cross section, 
and a hollow tube weighs less than a V-slot beam.
- All structural parts should be source-able from the local home depot. I bought tubing, and M5 leadscrews from 
Bauhaus.dk and Silvan.dk. I sourced M3 screws/washers/nuts, and electronics from various webshops.
- Controller, stepper motors and hotend from various 3D printer webshops. 


## Secondary design points
Taking inspiration from the locomotion of a Geometer Inchworm (https://www.youtube.com/watch?v=ncx4o-W9R2c) 
and the Kossel Delta printer I developed some novel solutions of my own. Basically, the machine is a hybrid 
of __2D delta (x- and y-axis) and 1D cartesian (z-axis)__.
And almost at the same time I discovered Manolo's Tuga (http://www.openbuilds.com/builds/reprap-tuga.390/).
- Instead of a Scott-Russel linkage i decided to implement a parallelogram. This would eliminate any torque 
induced by the hotend cooling fan. 
- Two carriages share one rail. The stepper motors and drive belts fit easily on the same rail. It just a 
design challenge to make non-mirrored parts.
- The Z-axis is a regular cartesian rail with stepper motors and a M5 leadscrew. I printed the bushing in 
nylon and tapped it manually, hoping that it would be a low friction solution. Later I might change this to 
a TR8x2 trapez leadscrew. I just have to by a TR8x2 TAP from Ebay.
- The parallellogram construction might also be a problem: the effector and hotend assembly induces torque on 
the X-rail. So the z-axis might be lower at one Y-position than another. 
- The max print speed is as usual determined by the heater. And print quality is determined by the vibrations
dependent on the accelleration and stiffness of the machine.
- The cooling fan (in the E3D hotend) should blow the heat away from all plastic parts. Coincidentially, it 
can also function as a structural part, holding the hotend to the effector arm. 




## Kinematics 
<describe the Inchworm kinematics>



## Firmware development
The kinematics calls for a open source firmware, where the math can easily be put in, without having to write
all from scratch. I tried to work with Repetier and Marlin. The firmwares have pros and cons, but in the end I 
settled on Marlin.  I have tried to make the changes as readable as possible. A fairly skilled programmer will
be able to port the code.
Either way ... my limited hobby-time presents a challenge in keeping up the primary Marlin Firmware development.
I have restarted my efforts twice to introduce the INCHWORM functions without breaking compatibility with the DEV branch.



