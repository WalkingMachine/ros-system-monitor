# ros-system-monitor

## Synopsis

System monitoring tools for ROS.

**Author(s):** Willow Garage, Inc., Jerome Maye, Ralf Kaestner
**License:** BSD License (BSD)
**Operating system(s):** Debian-based Linux

## Description

This project provides system monitoring tools for ROS in the form of the
following ROS nodes:

* CPU monitor
* HDD monitor
* Memory monitor
* Network monitor
* NTP monitor

Each node publishes ROS diagnostics which can conveniently be visualized
in the runtime monitor.

Note than this fork is made specifically for our robot Sara, for the kinetic ros distribution.

## Installation
### Building from source

This project may be built using the CMake build system with an open-source
macro extension called ReMake.

#### Installing build dependencies

The build dependencies of this project are available from the standard
package repositories of recent Ubuntu and ROS releases. To install them,
simply use the command

```
sudo apt-get install ros-kinetic-rospy ros-kinetic-message-generation ros-kinetic-std-msgs ros-kinetic-diagnostic-msgs sysstat
```
##### Cloning this repository on the src folder

* Switch into the src directory of your ros workspace
```
cd ~/ros_ws/src/
```

* Cloning repository
```
git clone http://github.com/WalkingMachine/ros-system-monitor.git
```

##### Building with CMake


* Switch into the package directory
  ```
  cd ~/ros_ws/src/ros-system-monitor
  ```

* Configure the build
  ```
  cmake -DROS_DISTRIBUTION=kinetic ~/ros_ws/src/ros-system-monitor
  ```

* Building the package
  ```
  sudo make
  ```

* If you intend to install the project, call
  ```
  sudo make install
  ```
