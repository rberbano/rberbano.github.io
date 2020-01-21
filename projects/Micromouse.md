---
layout: project
type: project
image: images/TSM.png
title: Micromouse
permalink: projects/micromouse
# All dates must be YYYY-MM-DD format!
date: 2019-04-05
labels:
  - Robotics
  - Arduino
  - C++
  - PCB
summary: My team of 3 (Team Small Mouse) worked together to create a robotic mouse to solve a maze on its own integrating both hardware and software applications.
---

<div class="ui small rounded images">
   <img class="ui image" src="../images/Micromouse1.png">
  <img class="ui image" src="../images/Micromouse2.png">
  <img class="ui image" src="../images/Maze.png">
</div>

Micromouse is an event where small robot “mice” solve a 16 x 16 maze.  Events are held worldwide.  The maze is made up of a 16 by 16 gird of cells, each 180 mm square with walls 50 mm high.  The mice are completely autonomous robots that must find their way from a predetermined starting position to the central area of the maze unaided. Through the use of engineer design process and various hardware and software implementations such as circuit boards, pcbs, sensors, and more. The mouse will be able to track its own location within the maze and find its way back to the starting location without any bare to minimal collisions within the shortest time possible.

Within this project, I mainly worked with the software side of development specifically with debugging and doing various tests and experiments based on the output of our mouse. After figuring out how to work the adc code, I was able to make numerous plots to test the different kinds of adc values we were able to get in order to find the most optimal values for our mouse. Through many long days of working in the lab, staying long after school, and even spending most of spring break working on this project, we were able to complete the project as our Micromouse ran a left wall hugger algorithm to get to the center of the maze and right wall hugger to get back to its starting location.

This is some of the hardware design we had:
<div class="ui small rounded images">
  <img class="ui image" src="../images/HardwareDesign1.png">
  <img class="ui image" src="../images/ChassisDesign1.png">
</div>
Here is some code that illustrates how we read values from the line sensors:

```js
byte ADCRead(byte ch)
{
    word value;
    ADC1SC1 = ch;
    while (ADC1SC1_COCO != 1)
    {   // wait until ADC conversion is completed   
    }
    return ADC1RL;  // lower 8-bit value out of 10-bit data from the ADC
}
```

You can learn more at the [UH Micromouse Website](http://www-ee.eng.hawaii.edu/~mmouse/about.html).



