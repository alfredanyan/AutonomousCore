This project implements the core program for Localization, Control, Mapping of a self driving car using Total probability, particle filters, Markov localization, Bayes Theory

The goal of Localization in this context is to equip our self driving car with the skill of localizing itself, or identifying where it is with a 10cm error tolerance as compared to traditional GPS sattelite technology which has anywhere up to 10m error range. This will obviously cause our self driving car to crash and is not acceptable.

Google's self driving technology implements this by recording images of the road surface, and performs various other computations to equip it's self driving cars with this skill, enabling them to remain in lane even if there are no lane markings.

Initally, our robot (or self driving car), assigns a uniform probability to being in every location in it's world. This model's the robot's initial state where it has no idea where it is. It simply assumes that it could be anywhere and doesn't apply a higher probability for being in one place over the other. This can be referred to as the state of maximum confusion.

Next step is for the robot to identify distinctive features in it's environment (using cameras, sensors, radar, lasar etc.).
This provides it with new information to modify it's information (posterior belief - belief that occurs after new sensory information - or after a measurement has been taken.) about where it is, enabling it to modify the assignment of its probability ratings to different locations in the world - increasing it in certain, while decreasing it in other locations. This is referred to as posterior probability - probability ratings occuring after new information is received (MEASUREMENT).





