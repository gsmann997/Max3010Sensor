# Max3010Sensor Build Instruction
# Table of content
1. [Introduction](#introdution)
2. [Parts Required](#parts-required)
3. [Max30105 Electronic File Design](#Max30105-Electronic-File-Design)
4. [Assembly](#assembly)
5. [OS image and breadbording testing](#os-image-and-breadbording-testing)
6. [Code Testing](#code-testing)
7. [Case design and Assembly](#case-design-and-assembly)

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
  
 I spent around 119$ on the parts (<a href="https://github.com/gsmann997/Max3010Sensor/blob/master/documents/budget.xlsx">click here to download my budget</a>). Moreover, consider that it will take around 3/4 weeks to receive the parts, so please take extra time to order and receive the parts.
  

  
</ul>

