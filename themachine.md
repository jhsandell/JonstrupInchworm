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
Taking inspiration with Manolo's Tuga <put link here> I developed some novel solutions of my own. Basically, the machine 
is a hybrid of __2D delta (x- and y-axis) and 1D cartesian (z-axis)__.
- Instead of a Scott-Russel linkage i decided to implement a parallelogram. This would eliminate any torque induced by the hotend cooling fan. 
- Two carriages share one rail. The stepper motors and drive belts fit easily on the same rail. It just a design challenge to make non-mirrored parts.
- The Z-axis is a regular cartesian rail with stepper motors and a M5 leadscrew. I printed the bushing in nylon and tapped it manually, hoping that it would be a low friction solution. Later I might change this to a TR8x2 trapez leadscrew. I just have to by a TR8x2 TAP from Ebay.


