# Printing
This document describes various aspects of printing all the parts for the Jonstrup Inchworm. Look in the tables how 
many of each STL you need to print.

## PLA and NYLON
Most parts are printed in PLA. Three parts are printed in Taulman 618 nylon. Nylon is chosen either as a lubricant-free 
bushing on the z-axis or as the heat tolerant fan shroud on the E3D hotend. 

## Alignment and Brims and No Support 
The STL's shall be printed in the alignment shown in the pictures. This assures that critical dimensions are controlled by the same axis on all parts. In other words: do not rotate objects if holes or dimensions are supposed to be identical. _It will affect the INCHWORM's final precision_. 

Several large objects have _manual brims_. The brims assures adhesion to the buildplate, without having to put an automatic 
brim all the way around the objects edges. A few large objects shall be printed with automatic brim.

![without a brim](/pics/print_adh001.png) 

![with a brim - manual or automatic](/pics/print_adh002.png)

The objects can be printed without support material. Angles of overhangs are only 30 degrees of vertical. Most
holes require _bridges_ in one way or another. 

## STL parts list

The STL files have been reduced with in Meshlab with "Quadric Edge Collapse Decimation". Please let me know, if there are any faults in the files.  

<table>
  <tr>
    <th>Name</th>
    <th>File</th>
    <th>Copies</th>
    <th>Pics</th>
  </tr>
  <tr>
    <td>Effector</td>
    <td><a href="/stl/eff001.stl">eff001.stl</a></td>
    <td>1</td>
    <td rowspan="3"><img src="/pics/stl_eff_sli_001.png" width="200"></img></td>
  </tr>
  <tr>
    <td>Slider Left</td>
    <td><a href="/stl/eff002.stl">eff002.stl</a></td>
    <td>1</td>
  </tr>
  <tr>
    <td>Slider Right</td>
    <td><a href="/stl/eff003.stl">eff003.stl</a></td>
    <td>1</td>
  </tr>
  <tr>
    <td>Groove mount block</td>
    <td><a href="/stl/eff004.stl">eff004.stl</a></td>
    <td>1</td>
    <td rowspan="3"><img src="/pics/stl_eff_groovemount_fanshroud_001.png" width="200"></img></td>
  </tr>
  <tr>
    <td>Groove mount clamp</td>
    <td><a href="/stl/eff005.stl">eff005.stl</a></td>
    <td>1</td>
  </tr>
  <tr>
    <td><B>NYLON</B> Fan shroud (for E3Dv6 hotend)</td>
    <td><a href="/stl/eff006.stl">eff006.stl</a></td>
    <td>1</td>
  </tr>
  <tr>
    <td>Effector wide arm</td>
    <td><a href="/stl/eff007.stl">eff007.stl</a></td>
    <td>2</td>
    <td rowspan="2"><img src="/pics/stl_eff_arms.png" width="200"></img></td>
  </tr>
  <tr>
    <td>Effector narrow arm</td>
    <td><a href="/stl/eff008.stl">eff008.stl</a></td>
    <td>1</td>
  </tr>
  <tr>
    <td>Left X-axis motor mount</td>
    <td><a href="/stl/xmount001.stl">xmount001.stl</a></td>
    <td>1</td>
    <td rowspan="2"><img src="/pics/stl_xaxis_motor_001.png" width="200"></img></td>
  </tr>
  <tr>
    <td>Right X-axis motor mount</td>
    <td><a href="/stl/xmount002.stl">xmount002.stl</a></td>
    <td>1</td>
  </tr>
  <tr>
    <td>Belt shim</td>
    <td><a href="/stl/beltshim001.stl">beltshim001.stl</a></td>
    <td>4</td>
    <td><img src="/pics/stl_belt_shim_001.png" width="200"></img></td>
  </tr>
  <tr>
    <td>Cable clamp</td>
    <td><a href="/stl/clamp001.stl">clamp001.stl</a></td>
    <td>4</td>
    <td><img src="/pics/stl_cableclamp_001.png" width="200"></img></td>
  </tr>
  <tr>
    <td><B>NYLON</B> z-axis bushings</td>
    <td><a href="/stl/zbushings001.stl">zbushings001.stl</a></td>
    <td>1 set</td>
    <td><img src="/pics/stl_nylon_zaxis_bushing_001.png" width="200"></img></td>
  </tr>
  <tr>
    <td>Z-axis 2020 foot</td>
    <td><a href="/stl/foot001.stl">foot001.stl</a></td>
    <td>2</td>f
    <td rowspan="2"><img src="/pics/stl_foot_supp_001.png" width="200"></img></td>
  </tr>
  <tr>
    <td>Z-axis support foot</td>
    <td><a href="/stl/foot002.stl">foot002.stl</a></td>
    <td>4</td>
  </tr>
  <tr>
    <td>Z-axis left motor mount</td>
    <td><a href="/stl/foot003.stl">foot002.stl</a></td>
    <td>1</td>
    <td rowspan="2"><img src="/pics/stl_zaxis_motor_001.png" width="200"></img></td>
  </tr>
  <tr>
    <td>Z-axis right motor mount</td>
    <td><a href="/stl/foot004.stl">foot004.stl</a></td>
    <td>1</td>
  </tr>



</table>


