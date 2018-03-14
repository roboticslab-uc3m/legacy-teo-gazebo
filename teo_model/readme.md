# teo_model
This model is generated using the model in [teo-ros-simulation/teo_description/](https://github.com/roboticslab-uc3m/teo-ros-simulation/tree/master/teo_description). To run this model in Gazebo the .sdf format is needed, therefore the following conversions were performed:

XACRO
=====

- Convert xacro file into an urdf:     

```bash
rosrun xacro xacro.py teo_humanoid.urdf.xacro > teo_humanoid.urdf
```

URDF
====

- Check URDF: 
```bash
check_urdf teo_humanoid.urdf
```

- Visualize URDF:
```bash
urdf_to_graphiz teo_humanoid.urdf && evince teo.pdf
```

- URDF -> SDF:  
```bash

gzsdf print teo_humanoid.urdf > teo_humanoid.sdf
```


