This project implements the core program for Localization, Control, Mapping of a self driving car using Total probability, particle filters, Markov localization, Bayes Theory

The goal of Localization in this context is to equip our self driving car with the skill of localizing itself, or identifying where it is with a 10cm error tolerance as compared to traditional GPS sattelite technology which has anywhere up to 10m error range. This will obviously cause our self driving car to crash and is not acceptable.

Google's self driving technology implements this by recording images of the road surface, and performs various other computations to equip it's self driving cars with this skill, enabling them to remain in lane even if there are no lane markings.

Initally, our robot (or self driving car), assigns a uniform probability to being in every location in it's world. This model's the robot's initial state where it has no idea where it is. It simply assumes that it could be anywhere and doesn't apply a higher probability for being in one place over the other. This can be referred to as the state of maximum confusion.

Next step is for the robot to identify distinctive features in it's environment (using cameras, sensors, radar, lasar etc.).
This provides it with new information to modify it's information (posterior belief - belief that occurs after new sensory information - or after a measurement has been taken.) about where it is, enabling it to modify the assignment of its probability ratings to different locations in the world - increasing it in certain, while decreasing it in other locations. This is referred to as posterior probability - probability ratings occuring after new information is received (MEASUREMENT).

Our robot now has a new function (curve on the xy-axis), representing it's new current belief of it's location.

Next step might be that our robot moves a short distance to one direction, and in the process, updates its belief function of where it is, a process that can be referred to as convolution.

At this point, the robot senses (measures) it's location again, and updates it's belief by multiplying it's current belief with the previous belief. Some locations might get a higher probability, others might reduce based on new information or images/ distinctive features it "sees" in it's environment that either confirm or debunk its previous belief of where it was.
This is the basic cycle of localization - Sense/ take measurements - where  information is increased, then move - a process which reduces information (information entropy), and then again sense - all the time updating it's belief by multiplying with the previous beliefs, then move again, repeating the convolution process (or adding it's...)





