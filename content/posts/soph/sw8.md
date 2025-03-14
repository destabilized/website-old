---
date: 2025-03-13
title: "soph week 3/3 - 3/14 (sumobot)"
draft: false
categories: ["blog", "sumobot"]
---

long blog post because we didn't really do much last week, so i'm cramming everyhting into this blog post. 

we started the sumobot project, where we have to create a <500g robot which will play sumo with other robots.

i'm sadly doing the project solo, but will be getting some help from my friends to compensate. 

#### idea
last week, i spent most of my time researching professional sumobot competitions and studying the strategies used by other robots.

since many robots will likely use similar hardware, i decided to focus on a unique design. this gives me an idea of how other robots might operate and allows me to develop strategies to counter them.

#### motors
i had two options for plastic motors: 120:1 and 200:1. after some research, i chose the 200:1 motors because they sacrifice speed for more torque. since the robots are lightweight, i think torque will be more important than speed. 
![website](/img/soph/8/motor.jpeg)

after soldering one of the motors, i noticed that the other motor was faster, so i soldered another one to balance them out.

#### sensors
initially, i planned to use an irs21b ir sensor, but i decided against it because i didn’t want to deal with calibration. instead, my friends and i opted for roller lever switches. i also heard that some people paint their sumobots white to confuse ir sensors, so this seemed like a better choice.

![website](/img/soph/8/switch.jpeg)

i wrote code to control the sumobot based on three states:

    if the left sensor is triggered, it moves right.

    if the right sensor is triggered, it moves left.

    if both sensors are triggered, it performs a star pattern to avoid being pushed off.

![website](/img/soph/8/star_pattern.gif) 
###### hopefully something like this. will have to create a body to test my code.

#### circuit board
![website](/img/soph/8/circuit.jpg)
###### yes this is a mess. it'll be cleaned later.
the circuit includes a metromini as the microcontroller, an md17a to control the motors, two motors, two roller lever switches, and two buttons to initialize different start sequences depending on which side of the arena the robot starts on.

i’ll start designing the pcb soon, unless i decide to add more components later (more on that below).

#### code
![website](/img/soph/8/directions.png)
i created different functions depending on what direction the robot will have to move (left, right, forward, backwards(eventually), and stop). 

in addition, i created specific sequences and patterns depending on sensor state and which button is clicked. startL and startR will wait for the enemy sumobot, and attack them when they go forward towards the edge of the arena. 
![website](/img/soph/8/special.png) 
![website](/img/soph/8/skill_issue.gif) 
###### something like this hopefully, but i'm assuming that they will be able to detect the white line, and my robot will push them as a result.

#### future plans?
i’m considering adding collapsible wings to my sumobot. this would allow it to meet the size requirements while expanding during the match to potentially confuse opponents using front-mounted ir sensors.

![website](/img/soph/8/wings.gif) 
###### something like this, but collapsable.

furthermore, my code is also broken, where my roller lever sensors when only one is clicked doesn't work. this will be something i have to fix. in addition, i don't know if my code even works, as i haven't made a body or wheels for my sumobot.

we started the sumobot project, where we have to create a <500g robot which will play sumo with other robots.

i'm sadly doing the project solo, but will be getting some help from my friends to compensate. 