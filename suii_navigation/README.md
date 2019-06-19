# Navigation

One Paragraph of project description goes here

## Getting Started

This is the repository for the Navigation solution for Suii. In the repository you will find motorcalibration software, the navigation manager and the euclidean calculator. 

### Prerequisites

This package requires the following packages to be installed:

* `laser_filters`
* `teb_local_planner`
* `costmap_converter`
* `global_planner`
* `local_planner`
* `amcl`

To install the packages use the following command:

```
sudo apt-get install ros-kinetic-<package_name>
```
Do take care to replace the underscores in the pakcage names with the normal '-' sign.


## Usage

#### Motor calibration
Motor calibration will happen automatically when lowlevel is initiated by pressing the green followed by the blue button. 

#### Running navigation
To run navigation the following command needs to be typed in a terminal:

```
roslaunch suii_bringup navigation.launch map_obstacle:=<map_name> map_amcl:=<map_name>
```

On the place of <map_name> the name of te created map needs to be filled in. The map_obstacles is for navigating the environment. The map_amcl is for localizing the robot. The to variables dont nesseserally need to use the same map.


#### Running the nodes
The command for running the manager node and the euclidean calculator is as follows:

```
rosrun suii_navigation manager.py
```
and
```
rosrun suii_navigation euclidean_calculator.py
```

#### Configuration files
In the Suii_Bringup package there is a map named 'config.' in this file all the configurationfiles are located for navigation.



## Authors

* **Lowie Koolen and Marian Lepadatu** - *in name of RoboHub Eindhoven* - [RoboHub Eindhoven website](https://robohub-eindhoven.nl/)
