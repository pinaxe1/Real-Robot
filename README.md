# Real-Robot
How to build a real robot?
This repo intended as lecture for a kindergaden students.

Plan
 What is a robot?
 is it it? https://www.youtube.com/watch?v=aw60Ma4c2bw
 Nope it looks much like a robot but it is not. It is AMP or Exosceleton. It requires a human to operate. It is de facto a puppet.
 A a robot in contrary is a machine that operates without a human supervision.
 this https://www.youtube.com/watch?v=Trxjd_2XwLs Prayer wheel
 or https://www.youtube.com/watch?v=x2qB0sR5IWA Water mill
 machines that could operate without humans. So I would call them a first ancient robots. Actually even anrdoids (a human like robots) are not a novelty. L'écrivain by Pierre Jaquet Droz is an example. It is 250 years old already.
 https://www.youtube.com/watch?v=U62Joxvw1Nw   L'écrivain. Some people even say that word "android" is derivation of inventors name Pierre Jaquet Droz. But he did called his creations automates.
 Contemporary analogues of L'écrivain are
 https://www.youtube.com/watch?v=HCndi1WC6iQ Zoltar
and  
 https://www.youtube.com/watch?v=sjAZGUcjrP8 Assembly line
 They all are not flexible and would do theyr "dances" no matter what. Either they have customer or not Is there Car on the assembly line or not. They just perform sequence of commands recorded some way on mechanical disks like L'écrivain or in a computer memory as an assembly line.
 
 What is real robot? BumbleBee. We are not there yet.
 Could robot be without legs? Wally. Not there yer either. But should it have hands? Not necessary. 
 Roomba.
 
 What all of them have in common? They act without human intervention and the more independent and adequate theyir behaviour in different environment and situations the more real they are. Let's range them.
 Transformers and Wally 100% They are smart and adaptable to any situations.
 Atlas and Spot 75% They can handle real world but still pretty stupid.
 Roomba 50% It can sense a wall or furniture but the way it handles goggy poop or stairs shows how narrow theyr limits. 
 Assembly line and Zoltar 10% because they are not more than a clockwork machines.
  
 Sorry guys can't bring you an Atlas or even Spot to play with so we will start from the Roomba level. 
 
 What main parts robot consists of?
 Power source.
 Control circuit.
 Actuator.
 Even prayer wheel has power source and actuator. And water mill has even a rudimentary control cirquit.
 Since power sources and actuators are well studied for ages we'll concentrate on control cirquits.
 
 Roomba has pretty elaborate control cirquit. It collects data from sensors to avoid obstacles (bumper sensors) to navigate home (IR beacon sensor) to check batterey level and power consumption (power sensors) new models even build a floor plan in their memory. So I would consider it a real robot. It moves it acts independently in changing environment But Roomba sill behaves pretty lame because it is legally blind. It sees nothing except an IR beacon.
 So let's add some vision to the system. It is easy to do. Get a computer and a USB camera. Done. We having a picture of the environment. But what to do with it? How to transform image into meaningfull movement of actuators?
 
Here is an example of 5DOF hydraulic arm made of shit and sticks. I mean Ice cream sticks and siringes. Siringes are actuators on the one side and control circuit on the other.
https://youtu.be/G0NZAUjhiag?t=27

If we will replace hydraulics with servos it would be easy to control the arm from a computer.
Record a list of commands and then send those commands to the meArm. We will get something like this.
https://www.youtube.com/watch?v=md4RQzFbGR0
But this robot is still blind. If there were no hanoy disks it will perform the same dance anyway.
Now we have to use information from the camera.
OpenCV library would let us to do something like this.
https://www.youtube.com/watch?v=s4jkMhVCvxM

Next step in image processing is tensorflow FCN which lets us know not only a center position of an object but classify each point
of the image.
https://www.youtube.com/watch?v=K7VlA_Jq8ks


