# Max3010Sensor Build Instruction
# Table of content
1. [Introduction](#introdution)
2. [Parts Required](#parts-required)
3. [Time Commitment](#time-commitment)
4. [OS image and sensor testing](#os-image-and-sensor-testing)
5. [Max30105 Electronic File Design](#Max30105-Electronic-File-Design)
6. [Assembly](#assembly)
7. [Code Testing](#code-testing)
8. [Case design and Assembly](#case-design-and-assembly)

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
The Parts required are (click on the product to be redicted where I bought the items, but feel free to buy them from anywhere more convenient to you):
<ul>
  <li><a href="https://www.canakit.com/raspberry-pi-3-model-b-plus-ultimate-kit.html">Raspberry Pi</a></li>
  <li><a href="https://www.amazon.ca/Sandisk-Ultra-Micro-UHS-I-Adapter/dp/B073K14CVB/ref=sr_1_4?s=electronics&ie=UTF8&qid=1537837988&sr=1-4&keywords=micro%2Bsd%2Bcard%2B16gb&th=1">Sd card (minimum 8GB)</a></li>
<li><a href="https://www.sparkfun.com/products/14045"> Max30105</a></li>
<li> <a href="https://www.amazon.ca/Haobase-120pcs-Multicolored-Female-Breadboard/dp/B01DLKLL6C/ref=sr_1_1?ie=UTF8&qid=1537837802&sr=8-1&keywords=jumper+wires+male+to+female
"> Male to female wires</a></li>
  <li>PCB (my PCB was printed by the <a href="http://munro.humber.ca/~mdrk0011/">prototype lab at Humber College</a> so feel free to use the method more convenient to you)</li>
  <li><a href="https://www.digikey.ca/products/en?keywords=SAM9289-ND">5 Header</a> <a href="https://www.digikey.ca/product-detail/en/sullins-connector-solutions/PPTC051LFBN-RC/S6103-ND/807239">& 6 pin header</a></li>
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
The last step is breadbording and testing the connection/sensor and if every part is working fine.
Follow the wiring diagram below of the wiring:
<img src="https://user-images.githubusercontent.com/43187603/47398817-dac4bb80-d703-11e8-8afc-d6c36e0f06ec.png" height="400" width="400">
Your breadbord should look like the image below:
<img src="https://user-images.githubusercontent.com/43187603/47397450-5111ef80-d6fd-11e8-8374-09f96998d36e.jpg" height="350" width="300"
