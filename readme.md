#teo-gazebo
This repository contains the needed files to run an stand-alone simulation of the UC3M humanoid robot teo.

##Installation steps
1. **Clone** this repository in your pc.
 
2. **Copy the teo_model and teo_description** folders in your *local Gazebo *model database (~/.gazebo/models/), for that just go to the root of the directory and enter the following command in a terminal:

```
		cp -r teo_model teo_description ~/.gazebo/models/
```

##Starting the simulation
To start the simulation just enter the following command in the root of your clone directory environment.

```
		gazebo teo.world
```

###NOTES:
- This repository is intended to be a gazebo stand-alone repository. For this reasons all the additional no-gazebo parts are not implemented. This is the case for example of the **control**. For this reason to avoid the model to continously fall, a **fictional joint between the robot waist and the world** have been generated in the simulation, to fix the robot to the environment. This joint is called **"base_joint"**, and deleting this joint is as easy as commenting it out in the **.sdf file**.

###TODO:
- [ ] Fix the visual elements of the robot.