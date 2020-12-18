# teo-gazebo
This repository contains the needed files to run an stand-alone simulation of the UC3M humanoid robot teo.

## Dependencies 
- **Clone** teo-gazebo in your pc
```				
		cd; mkdir -p repos; cd repos  # make $HOME/repos if it doesn't exist; then, enter it
		git clone https://github.com/roboticslab-uc3m/teo-gazebo
```
## Installation steps
1. **Clone** this repository in your pc.

```				
		cd; mkdir -p repos; cd repos  # make $HOME/repos if it doesn't exist; then, enter it
		git clone https://github.com/roboticslab-uc3m/teo-gazebo
```
 
2. **Copy the teo_model and teo_meshes** folders in your *local Gazebo model database* (~/.gazebo/models/), from root enter:

```	
		cd; cd .gazebo; mkdir -p models
        cd; cd repos/teo-gazebo
		cp -r teo_meshes ~/.gazebo/models/
		cp -r teo_model ~/.gazebo/models/
```

## Starting the simulation
Enter the following command in the root of your clone directory environment.

```
		gazebo teo.world
```

### NOTES:
- This repository is intended to be a gazebo stand-alone repository. All the additional no-gazebo plugins are not implemented. This is the case for example of the **control**. In order to avoid the model to continously fall, a **fictional joint between the robot waist and the world** have been generated. This joint is called **"base_joint"**, and deleting this joint is as easy as commenting it out in the **.sdf file**.
- This repository uses a modified robot description from the following repository <https://github.com/roboticslab-uc3m/teo_robot> .
