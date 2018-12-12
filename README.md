# Max3010Sensor Build Instruction
# Table of content
1. [Introduction](#introdution)
2. [Parts Required](#parts-required)
3. [Time Commitment](#time-commitment)
4. [OS image and sensor testing](#os-image-and-sensor-testing)
5. [Testing and Pins Soldering](#testing-and-pins-soldering)
6. [Max30105 Electronic File Design](#max30105-electronic-file-design)
7. [Assembly](#assembly)
8. [Code Testing](#code-testing)
9. [Case design and Assembly](#case-design-and-assembly)

# Introduction
<img src='https://user-images.githubusercontent.com/43187603/48815301-07242580-ed0c-11e8-836c-ad78ff526679.jpg' height=300 width=450>
<!-- remember to center image -->
This project is based on the MAX30105, which is a very powerful sensor (it can sense the distance, heart rate, particle in the air and even the blinking of an eye)
For this particular project I decided to implement only the heart rate functionality.
It is important that you read the <a href="https://cdn.sparkfun.com/assets/learn_tutorials/5/7/7/MAX30105_3.pdf">datasheet</a> of the sensor before any different connection than the one shown below are done.
For the project I am using the raspberry Pi as microcontroller, as I am already familiar on how it works.
The Max30105 has three on-board LEDs: green, red and IR which works on 5v but the sensor can work on 3.3V as well, as if 5V are applied to the raspberry pi, the GPIO will break.
Below, all the required material, assembly steps and code testing are explained. All the data below has been tested and tried and is the result of many failied attempt. 
It should not take you more than 3h to do everything supposing that you have all the required material.
# Parts required
The Parts required are (click on the product to be redicted where I bought the items, but feel free to buy them from anywhere more convenient to you):
<ul>
  <li><a href="https://www.canakit.com/raspberry-pi-3-model-b-plus-ultimate-kit.html">Raspberry Pi</a></li>
  <li><a href="https://www.amazon.ca/Sandisk-Ultra-Micro-UHS-I-Adapter/dp/B073K14CVB/ref=sr_1_4?s=electronics&ie=UTF8&qid=1537837988&sr=1-4&keywords=micro%2Bsd%2Bcard%2B16gb&th=1">Sd card (minimum 8GB)</a></li>
<li><a href="https://www.sparkfun.com/products/14045"> Max30105</a></li>
<li> <a href="https://www.amazon.ca/Haobase-120pcs-Multicolored-Female-Breadboard/dp/B01DLKLL6C/ref=sr_1_1?ie=UTF8&qid=1537837802&sr=8-1&keywords=jumper+wires+male+to+female
"> Male to female wires</a></li>
  <li>PCB (my PCB was printed by the <a href="http://munro.humber.ca/~mdrk0011/">prototype lab at Humber College</a> so feel free to use the method more convenient to you)</li>
  <li><a href="https://www.digikey.ca/products/en?keywords=SAM9289-ND">5 Header</a> <a href="https://www.digikey.ca/product-detail/en/sullins-connector-solutions/PPTC051LFBN-RC/S6103-ND/807239">and 6 pin header</a></li>
</ul>
 I spent around 119$ on the parts (<a href="https://github.com/gsmann997/Max3010Sensor/blob/master/documents/budget.xlsx">click here to download my budget</a>). Moreover, consider that it will take around 3/4 weeks to receive the parts, so please take extra time to order and receive the parts.
  
  # Time Commitment
  
  Once you receive that parts (included the PCB), it should take you around 5 hour to do the testing, mechanical assembly and power up.
  Please reference to my <a href= "https://github.com/gsmann997/Max3010Sensor/blob/master/documents/schedule.pdf">time commitment</a> and how I divided the work through 4 months. 
  However, it should not take this much time as I am supplying all required material and a detail guide to follow.
  
  # OS image and sensor testing
Once you received the Raspberry Pi and micro sd, you can proceed to install an OS in the PI.
To install the OS in the PI, reference to <a href="https://github.com/six0four/StudentSenseHat/blob/master/README.md#student-raspberry-pi-image-creation-and-test-code" >this link </a>, which cointains a detailed guide on how to install an OS in the Pi and has been given to us by our professor.
The second step, after the installion of the OS, is to make the PI accessible either via VNC (<a href="">click here to download vnc for Windows</a>). Activating VNC on the PI does not require much time, I used a guide on 
<a href="https://www.lynda.com/Raspberry-Pi-tutorials/Raspberry-Pi-Essential-Training/667376-2.html">lynda.com</a>, but if you do not have access to lynda.com use any resource.
# Testing and Pins Soldering

Before testing the sensor you need to solder the pins to the sensors. Moreover, before starting any soldering watch <a href="https://www.youtube.com/watch?v=BLfXXRfRIzY&list=PLQ32vZrF5U2lFOJTtZDytBWBYVLNp4RYz"> soldering videos </a> and <a href="https://safety.eng.cam.ac.uk/safe-working/copy_of_soldering-safety"> read risk assessments and chemical safety information</a>
Once you are reading for the soldering, solder the sensor with the pins.
The last step is breadbording and testing the connection/sensor and if every part is working fine.
Follow the wiring diagram below of the wiring:
<div>
<img src="https://user-images.githubusercontent.com/43187603/47398817-dac4bb80-d703-11e8-8afc-d6c36e0f06ec.png" height=400 width=400>
</div>
Your breadbord should look like the image below:
<div>
<img src="https://user-images.githubusercontent.com/43187603/47397450-5111ef80-d6fd-11e8-8374-09f96998d36e.jpg" height=400 width=400>
</div>

Once the wiring is done, turn on the pi, enable I2C from options.
Furthermore, open the command terminal and run the following command: <b> i2cdetect -y -1</b><br>
On the screen you should be able to see the address of your sensor, this is a quick test to check if all the wiring has been done properly.
Example of screen:
 <div><img src="https://user-images.githubusercontent.com/43187603/48308589-9d9b5e80-e536-11e8-8047-f5b777083972.PNG" heigth=300 width=300></div> 
 
# Max30105 Electronic File Design
The final project expects the sensor and the PI to be connected to each other through a PCB. 
I designed my PCB using <a href="http://fritzing.org/download/">fritzing </a>, here you can find <a href="https://github.com/gsmann997/Max3010Sensor/blob/master/documents/myPcb.fzz">my fritzing design</a> and <a href="https://github.com/gsmann997/Max3010Sensor/blob/master/documents/pcb_gerber.zip" >here you can find the gerber file of the PCB</a><br>This is the PCB diagram:

<div>
<img src="https://user-images.githubusercontent.com/43187603/47763723-365cef00-dc98-11e8-8152-0d059c520169.png" heigth=250 width=250>
</div>

Once you get the PCB, you can solder the pins header to the PCB.
This is the final result:

<div>
 <img src="https://user-images.githubusercontent.com/43187603/48309051-10103c80-e53f-11e8-970f-8a85809c0ed6.png" heigth=300 width=300> 
</div> 

# Assembly
Once you receive the PCB, assemble everything:

<img src="https://user-images.githubusercontent.com/43187603/48309070-69786b80-e53f-11e8-90d2-b840e2975a57.jpg"  heigth=300 width=300>

Then, test it again as you did with the breadboarding <a href="#testing-and-pins-soldering">click here to see the steps again</a>.
# Code Testing
Until now, we have focused only on the hardware part, but we have also to work on the software part.
For the coding part, I used the MAX30102 libraries as I did need only the heart beat and not the other functionality of the sensor.
I have the code uploaded on my github and I am also posting the source code from where I initially retrived it.(
<a href="https://github.com/vrano714/max30102-tutorial-raspberrypi">click here to retrive the code</a> or <a href="https://github.com/gsmann997/Max3010Sensor/tree/master/files">click here for the source code on my github</a>)
Once you upload the code on your raspberry pi, run the max30102.py file with python3 compile option to execute the file and get the RED and IR LED.
# Case design and Assembly
Once the software side is complete the only step remaining is to make and assemble the case.
For the design of the case I used  [CorelDRAW Graphics Suite](https://www.coreldraw.com/en/?link=wm) and you can retrive the design [from here](https://github.com/gsmann997/Max3010Sensor/blob/master/documents/Pi2Case_default.cdr).<br>
Picture of the CorelDraw:<br> <img src="https://user-images.githubusercontent.com/43187603/48814425-a8a97800-ed08-11e8-9e55-cb4080d570bd.PNG" heigth="250" width="250">
Once you get the case the only step left is assembling the case.
The final result is:
<img src="https://user-images.githubusercontent.com/43187603/48815301-07242580-ed0c-11e8-836c-ad78ff526679.jpg" heigth="300" width="300">



