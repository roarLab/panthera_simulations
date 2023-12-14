![](assets/img1.png)
# Panthera Gazebo Simulation

ROS packages for simulating Panthera robot using Gazebo Simulator. We provides several environment worlds to test the robot. ROS controller for Panthera can be found in this [repository](https://github.com/roarLab/panthera_controller).

## Dependencies

Make sure you have ROS noetic installed, although other ros-distros might also work. This simualtion package also relies on the following external packages, so make sure you have installed everything from source before building this package.

- [panthera_msgs](https://github.com/roarLab/panthera_msgs)
- [panthera_controller](https://github.com/roarLab/panthera_controller)

## Build from source

```
cd <ros1_ws>/src
git clone https://github.com/roarLab/panthera_simulations
cd ..
rosdep install -y --from-paths src --ignore-src --rosdistro <YOUR_ROS_DISTRO>
catkin_make
```

## Simulate panthera in empty world

```
cd <ros1_ws>
source devel/setup.bash
roslaunch panthera_gazebo panthera_empty_world.launch
```

## Simulate panthera in hallway-like environment

```
cd <ros1_ws>
source devel/setup.bash
roslaunch panthera_gazebo panthera_hallway_world.launch
```

## Simulate panthera in town/city world (Not tested yet)

```
cd <ros1_ws>
source devel/setup.bash
roslaunch panthera_gazebo panthera_town_world.launch
```

## Citation

If you are interested in these self-reconfigurable systems, you may take a look at our T-RO paper.

 - Kyaw, Phone Thiha, et al. [**Energy-efficient path planning of reconfigurable robots in complex environments**](https://ieeexplore.ieee.org/abstract/document/9716740). IEEE Transactions on Robotics (T-RO), 2022.
 
 ```bibtex
@article{kyaw2022energy,
  title={Energy-efficient path planning of reconfigurable robots in complex environments},
  author={Kyaw, Phone Thiha and Le, Anh Vu and Veerajagadheswar, Prabakaran and Elara, Mohan Rajesh and Thu, Theint Theint and Nhan, Nguyen Huu Khanh and Van Duc, Phan and Vu, Minh Bui},
  journal={IEEE Transactions on Robotics},
  volume={38},
  number={4},
  pages={2481--2494},
  year={2022},
  publisher={IEEE}
}
```
