# Max3010Sensor Build Instruction
# Table of content
1. [Introduction](#introdution)
2. [Parts Required](#parts-required)
3. [Parts Required](#parts-required)
4. [Max30105 Electronic File Design](#Max30105-Electronic-File-Design)
5. [Assembly](#assembly)
6.[OS image and breadbording testing](#os-image-and-breadbording-testing)
7.[Code Testing](#code-testing)
8.[Case design and Assembly](#case-design-and-assembly)

# Introduction
<img src='https://user-images.githubusercontent.com/43187603/48815301-07242580-ed0c-11e8-836c-ad78ff526679.jpg' height=300 width=450><
<!-- remember to center image -->
This project is based on the MAX30105, which is a very powerful sensor (it can sense the distance, heart rate, particle in the air and even the blinking of an eye)
For this particular project I decided to implement only the heart rate functionality.
It is important that you read the <a href="https://cdn.sparkfun.com/assets/learn_tutorials/5/7/7/MAX30105_3.pdf">datasheet</a> of the sensor before any different connection than the one shown below are done.
For the project I am using the raspberry Pi as microcontroller, as I am already familiar on how it works.
The Max30105 has three on-board LEDs: green, red and IR which works on 5v but the sensor can work on 3.3V as well, as if 5V are applied to the raspberry pi, the GPIO will break.
Below, all the required material, assembly steps and code testing are explained. All the data below has been tested and tried and is the result of many failied attempt. 
It should not take you more than 3h to do everything supposing that you have all the required material.
# Parts required
The Parts required are:
<ul>
  <a href""><li>Raspberry Pi</li></a>
  <a href""><li>Sd card (minimum 8GB)</li></a>
 <a href""> <li>Max30105</li></a>
 <a href""> <li>Male to female wires</li></a>
 <a href""> <li>PCB</li> </a>
 <a href""> <li>5 & 6 pin Headers</li></a>
  

  
</ul>

