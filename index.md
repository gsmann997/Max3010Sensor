# Table of content
1. [Week 2](#Week-2)
2. [Week 3](#Week-3)
3. [Week 4](#Week-4)
4. [Week 5](#Week-5)
5. [Week 7](#Week-7)
6. [Week 8](#Week-8)
7. [Week 9](#Week-9)
8. [Week 10](#Week-10)
9. [Week 11](#Week-11)

#### Max3010Sensor
This file contains data for a project involving the Max3010x sensor
## Week 11
This week was due the power up milestone.
Unfortunately, as explained in last week posting I was already running late on my [schedule]( https://github.com/gsmann997/Max3010Sensor/blob/master/documents/schedule.pdf) and I have not been able to meet the deadline.
I tried to look up libraries for the integration of my sensor and the Pi but I was not able find anything.
The next step I took was looking up code online to get an idea of the type of code I need to write for my sensor.
However, not being familiar with this type of task made the whole process slower and time consuming.
So after I wrote my code, I tested it and unfortunatly It was not working. 
Then I tried to change approach, therefore I read the arduino libraries to get an idea of what I need but it has not been helpful.
In class I consulted the teacher and he advised me to take a smaller step and try to turn on the read LED on the sensor and look up all the register on the [datasheet](https://cdn.sparkfun.com/assets/learn_tutorials/5/7/7/MAX30105_3.pdf) of the sensor.
Moreover, I wrote some testing code but the reading on the screen was 0 and was not changing which meant It was not working.
After, I asked the teacher what I could do to fix the problem.
He advised me to test the code on another sensor: PCF8591.
Now, my next goals are going to be: learn how to push/ pull data from/to the PCF8591, write the code for the max30105 to get the readings within next week.
Regarding the [budget](https://github.com/gsmann997/Max3010Sensor/documents/budget.xlsx) no extra expenses where made.

# Update: 
After consulting Vlad from the prototype lab I decided to keep working on my sensor before trying to use the PCF8591, and after a couple more hours of research I find out that the previous version of my sensor (MAX30102) and the one I am using (MAX30105) are compatible.
The only difference between the two version is the fact that the older one does not have the green LED. However, the heart beat reading are calculated from the RED and IR LED.
After a couple more hours I was able to find a compatible library for my sensor on github([click here to retrive the code](https://github.com/vrano714/max30102-tutorial-raspberrypi) or [click here for the source code on my github](https://github.com/gsmann997/Max3010Sensor/tree/master/files)). Therefore, I installed and run the code.
Conclusion: I have been able to pull data from my sensor, but I still have to make the code I got mine.<br>
Next Goal: <br>   - Send the case to the prototype lab
           <br>   - Get ready for next week enclosure
<br>Below are the pictures of the code I run:<br><br>
![redlog](https://user-images.githubusercontent.com/43187603/48627087-a69a8e80-e981-11e8-976d-4c740fb5f91f.PNG)
<br><br>This are the readings I get from the RED LED<br><br>
![irlog](https://user-images.githubusercontent.com/43187603/48627131-c5992080-e981-11e8-99fc-5ba13a14e6b1.PNG)
<br><br>This are the readings I get from the IR LED<br><br>
![graph](https://user-images.githubusercontent.com/43187603/48627147-d3e73c80-e981-11e8-8208-7e5ba613ae08.PNG)
<br><br>Included in the files I got online, there was also a file to graph the two readings from the sensor.<br><br>

## Week 10
This week was due the PCB soldering. As advised by our teacher, I soldered headers to my PCB instead of soldering my sensor and the PI directly to the PCB, as if the PCB would not have worked I could have replaced the PCB instead of unsoldering everything.
Regarding the headers, in my last week posting I mentioned that I would be reaching out Kelly from the prototype lab for the headers. However, even though he provided me the headers for free, he did not have the 6x2 and 5x1 pin headers so he gave me bigger ones. 
Fortunately, I was able cut both the headers to fit my requirements.
My [budget](https://github.com/gsmann997/Max3010Sensor/documents/budget.xlsx)  did not see major changes thanks to the help of the prototype lab.
So my final result is:
![pcb](https://user-images.githubusercontent.com/43187603/48309051-10103c80-e53f-11e8-970f-8a85809c0ed6.png)
![pi pcb](https://user-images.githubusercontent.com/43187603/48309070-69786b80-e53f-11e8-90d2-b840e2975a57.jpg)

The next step after the soldering is testing. 
I tested the PCB using the i2c detect command and everything worked.
![proofofpcb](https://user-images.githubusercontent.com/43187603/48308589-9d9b5e80-e536-11e8-8047-f5b777083972.PNG)
<br><br>Next week is the power up milestone for which we have to push or pull data from/to the sensor.
For this milestone I am actually one week behind [schedule]( https://github.com/gsmann997/Max3010Sensor/blob/master/documents/schedule.pdf) so as a partial solution of this I am going to try to get it done in one week and be ready for next week milestone. 
Moreover, I was able to ask the teacher a question regarding the implementation of the software intended to read/write from the sensor, as there are no library available for the integration of the MAX30105 with the raspberry pi; so the professor advised me to implement the code for the sensor.
In conclusion the next step is being able to pull the raw data from the sensor.<br><br>
 ## Week 9
PCB designed and submitted Geber of the designed PCB to the prototype lab for printing.
During the design of the PCB I spent a lot of time while trying to find a compatible connector/sensor that will have the same pins as the one I am using. However I was not sure about the distance between pins so with more research I was actually able to find my sensors fritzing part online. <br><br>
![pcb](https://user-images.githubusercontent.com/43187603/47763723-365cef00-dc98-11e8-8152-0d059c520169.png)
# Progress Report:
So far everything is going as planned, even though I spent more time than what was necessary on the designing of the PCB, and I am behind schedule on the software part of the project (get readings from the sensor).<br>
This week I am going to try to catch on the schedule and go to the prototype lab to ask for help on the software part.<br>
My budget may see some changment with some extra cost due the fact that I am going to use two stackable headers: one of 6 pin and one of 5 pin to be able to get more modularity and versatility on my project, so even if my PCB will not work I will be able to design and use another one faster.
For this extra cost I have to see Vlad and Kelly from the prototype lab as they might have extra headers in the lab.
## Week 8
Breadboard milestone was due in this week (see picture below). <br>
Moreover, we had to check if everything is on track or not.
After meeting with my team member and checking the work done so far, I can say me and my team member are going as planned and we are meeting the goal set. Unfortunately I received my sensor late which left me behind with the soldering. However, I had already watched tutorial and practiced in class. 
So thanks to Vlad and Kelly I was able to catch up quickly.
So far no extra cost was required.
![breadboard_milestone](https://user-images.githubusercontent.com/43187603/47397450-5111ef80-d6fd-11e8-8374-09f96998d36e.jpg)
Before doing the breadboarding I prepared a fritzing diagram (my sensor was not available in fritzing so I used another sensor with the same Pin):<br>
![drawing](https://user-images.githubusercontent.com/43187603/47398817-dac4bb80-d703-11e8-8afc-d6c36e0f06ec.png)<br>
![drawing_scheme](https://user-images.githubusercontent.com/43187603/47398829-e57f5080-d703-11e8-8635-d47ca832b91e.png)<br>
## Week 7
This week we did the soldering.
![img_20181022_105531](https://user-images.githubusercontent.com/43187603/47303578-49195900-d5f2-11e8-87ba-8dbeb3edad9a.jpg)<br>
Pseudo-code was also written to get an idea of what code we will have to write for the power up
![pseudo-code](https://user-images.githubusercontent.com/43187603/47397204-32f7bf80-d6fc-11e8-9fbd-ab3781bbbd41.PNG)
## Week 5
## Proof of purchase
**Raspberry Pi**
![pi_invoice](https://user-images.githubusercontent.com/43187603/46380020-c5adbd00-c66e-11e8-900e-35b367c0bb0c.jpg)
**Wires**<br>
![wires_receipt](https://user-images.githubusercontent.com/43187603/46379957-867f6c00-c66e-11e8-8fb0-836faa98e8e6.jpg)
**MAX3010x Pulse & Oximetry sensor (0x57)**
![heart_beat](https://user-images.githubusercontent.com/43187603/46379917-65b71680-c66e-11e8-970e-56de38003e65.png)
## Week 4
## Schedule
![budjet_image](https://user-images.githubusercontent.com/43187603/47396269-05107c00-d6f8-11e8-91c7-b8277e08926f.PNG)
## Week 3
During the third week we planed our future steps and organized how to progress with the project.
![schedule_image](https://user-images.githubusercontent.com/43187603/47396526-21f97f00-d6f9-11e8-841b-e48650a2054c.PNG)
[schedule.pdf](https://github.com/gsmann997/Max3010Sensor/files/2508397/schedule.pdf)
### Week 2
This week I meet up with my group member and prepared the proposal.
![proposal](https://user-images.githubusercontent.com/43187603/47396723-f9be5000-d6f9-11e8-8147-1b7267c9a3f1.jpg)



