# Extended Kalman Filter Project
Self-Driving Car Engineer Nanodegree Program

This project implements an extended kalman filter to estimate the state of a moving object of interest by combining noisy lidar and radar measurements.  The project code then tests the EKF's performance against ground_truth values using the root-mean-squared error.

Code for c++ implementation can be found in the [here](/src).

## Installation and Usage

This project involves the Term 2 Simulator which can be downloaded here

This repository includes two files that can be used to set up and install uWebSocketIO for either Linux or Mac systems. For windows you can use either Docker, VMware, or even Windows 10 Bash on Ubuntu to install uWebSocketIO. Please see this concept in the classroom for the required version and installation scripts.

Once the install for uWebSocketIO is complete, the main program can be built and run by doing the following from the project top directory.

mkdir build
cd build
cmake ..
make
./ExtendedKF

INPUT: values provided by the simulator to the c++ program

["sensor_measurement"] => the measurement that the simulator observed (either lidar or radar)

OUTPUT: values provided by the c++ program to the simulator

["estimate_x"] <= kalman filter estimated position x
["estimate_y"] <= kalman filter estimated position y
["rmse_x"]
["rmse_y"]
["rmse_vx"]
["rmse_vy"]

---

## Other Important Dependencies

* cmake >= 3.5
  * All OSes: [click here for installation instructions](https://cmake.org/install/)
* make >= 4.1 (Linux, Mac), 3.81 (Windows)
  * Linux: make is installed by default on most Linux distros
  * Mac: [install Xcode command line tools to get make](https://developer.apple.com/xcode/features/)
  * Windows: [Click here for installation instructions](http://gnuwin32.sourceforge.net/packages/make.htm)
* gcc/g++ >= 5.4
  * Linux: gcc / g++ is installed by default on most Linux distros
  * Mac: same deal as make - [install Xcode command line tools](https://developer.apple.com/xcode/features/)
  * Windows: recommend using [MinGW](http://www.mingw.org/)
  
## Example Output

![Output 1](/output_imgs/img1.png)
![Output 2](/output_imgs/img2.png)

Red circles are lidar measurements.

Blue circles are radar measurements (position markers inferred from radius and angle; the also-supplied radial velocity measurements are not shown).

Green markers are the car's position as estimated by the Kalman filter. It's clear that the Kalman filter does a good job of tracking the car's position with significantly reduced noise.

