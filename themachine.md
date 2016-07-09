# Jonstrup Inchworm 3D Printer

## The Machine
This page explains the motivation for building a novel 3D printer with a unique kinematics. Design choices 
will be described in no particular order.

## Background
I discovered the 3D printing and associated Maker hype around 2010. For more than a year I just sat in front of 
my computer, and gobbled up loads of youtube videos, and trawled endless seas of webpages. In 2012 I finally 
found the funds (outside the household budget) for procuring a 3D printer: a RepRapPro Mendel (mono / legacy).
At the same time I started flying RC model aircraft. And the primary purpose for buying a printer was
to print spare parts for the model aircraft when they _eventually_ crashed.

Later, I had the wish to print larger volumes, like aircraft wings, but the machines on the market did not scale
properly with costs, and to make matters worse, all seemed to take up way to much tabletop real estate. I simply
could not fit those into my cramped cave.

> have you noticed how most designs scale almost equally on all three axis' ?

So I wanted to build a machine that could print a long and narrow object. Build platform should have some ridiculous
dimension on at least one axis: 2000mm (... and counting). (*)

(*) Well, being limited by the length of my desk, the x axis is almost 1800mm. But during development the 
the right-hand endstop is placed at 600mm.

## Primary design points
- When build volume increases, you want the build platform to be static. Accellerating a huge platform back 
and forth is neither good for the object you are printing nor the machine itself. Oscillations will occur and
shake the machine apart.
- A static build platform could also be the base for the machine. A disused kitchen tabletop would fit the
purpose; its structurally strong, its heat resistant, and to some point isolating.
- It has to sit on my desk, which I use for other things, so it cannot be supported on the front 
side, or be enclosed like a Makerbot, a Ultimaker or a CNC machine.
- With increasing dimensions, the down-bending of the structural parts has to be considered. So first option 
was to use a hollow 2020 aluminium tube. A square tube is more stiff than a cylidrical of same cross section, 
and a hollow tube weighs less than a V-slot beam.
- All structural parts should be source-able from the local home depot. I bought tubing, and M5 leadscrews from 
Bauhaus.dk and Silvan.dk. I sourced M3 screws/washers/nuts, and electronics from various webshops.
- Controller, stepper motors and hotend from various 3D printer webshops. 


## Secondary design points
Taking inspiration from the [locomotion of a Geometer Inchworm (Youtube)](https://www.youtube.com/watch?v=ncx4o-W9R2c) 
and the Kossel Delta printer I developed some novel solutions. Basically, the machine is a hybrid 
of __2D delta (x- and y-axis) and 1D cartesian (z-axis)__.
And almost at the same time I discovered [Paulo Gonçalves Tuga (OpenBuilds)](http://www.openbuilds.com/builds/reprap-tuga.390/).
- Instead of a Scott-Russel linkage i decided to implement a parallelogram. Any fans sitting at the effector 
hotend would induce some gyro torque when the head rotates. It might not be much, but I intuitively liked this better. 
- Two carriages share one rail. The stepper motors and drive belts fit easily side-by-side on the same rail. It just a 
design challenge to make unique parts all over the place. The carriages fit the square tube tightly and slides without 
any bushings, and without lubrication.
- The Z-axis is a regular cartesian rail with stepper motors and a M5 leadscrew. I printed the bushing in 
nylon and tapped it manually, hoping that it would be a low friction solution. Later I might change this to 
a TR8x2 trapez leadscrew. I just have to by a TR8x2 TAP from Ebay.
  - by the way: the Z-axis might be _any height_. Just buy two longer leadscrews and 2020 aluminium tubes.
- The parallellogram construction might also be a problem: the effector and hotend assembly induces torque on 
the X-rail. So the z-position might vary depending on Y-position. 
- The max print speed is as usual determined by the heaters ability to melt the plastic, as well as the 
steps-per-second rate of the controller . And print quality is determined by the vibrations
dependent on the accelleration and stiffness of the machine.
- The cooling fan (in the E3D hotend) should blow the heat away from all plastic parts. At the same time it 
can also function as a structural part, holding the hotend to the effector arm. 

# Proof of Concept
The idea just popped into my mind... And it might be a heritage of having played a lot with LEGO Technic as a kid.
So I sat down and printed a POC, using some smooth rods from an scrapped inkjet printer.
<img src="/pics/poc001.png" width="49%"></img>
<img src="/pics/poc002.png" width="49%"></img>


Please observe: The effector was printed lying down, while the two sliders were standing up (to allow printing the holes for the rails.) The XY plane and the Z-axis on my printer has bad calibration, so the holes of the effector and the sliders are not equally spaced. The effector rotates a bit, which can be seen in the first picture, compared to the second. (it may also be due to the _hot plastic_ sagging during printing, when it is not completely solidified). 

The conclusion is: print all effector parts in the same orientation, and preferably in one pass, if your printer can have all three parts on the build plate simultaneously. 

## Bending
The effector arms should be stiff and not bend. The hotend will have some weight and gravity will do its job on the machine. 
<img src="/pics/bending001.png" width="33%"></img>
<img src="/pics/bending002.png" width="33%"></img>
<img src="/pics/bending003.png" width="33%"></img>

## Iterations
The design evolved over time... A lot of PLA was spent on prototypes.
![proto001](/pics/proto001.png)

This is an early assembly picture. The x-axis is scalable: buy a longer 2020 alu tube and longer GT2 belts. Same goes for the z-axis and the leadscrews. The effector arms implies a 2*L cost on the x-axis. I intend to explain this later... 
![Assembly001](/pics/assembly_001.png)


## Kinematics 
> describe the Inchworm kinematics

> insert a picture

> describe the motion of the sliders.

> describe the motion of the effector.

> describe the different arm lengths and the trade-offs

> describe the inverse kinematics math.

> describe the forward kinematics math. (used for homing?)


## Firmware development
The kinematics calls for a open source firmware, where the math can easily be put in, without having to write
all from scratch. I tried to work with Repetier and Marlin. The firmwares have pros and cons, but in the end I 
settled on Marlin.  I have tried to make the changes as readable as possible. A fairly skilled programmer will
be able to port the code.
Either way ... my limited hobby-time presents a challenge in keeping up the primary Marlin Firmware development.
I have restarted my efforts twice to introduce the INCHWORM functions without breaking compatibility with the DEV branch.



