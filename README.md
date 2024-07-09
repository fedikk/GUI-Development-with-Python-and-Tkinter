# GUI-Development-with-Python-and-Tkinter

## Initial setup (for newer Pythonistas)
Hey, in this lecture we'll talk about how to do Python development, just in case you're coming from a different programming language.

### Python version
I recommend you use the latest Python version. For Tkinter development you really need to use Python 3.5+ as Tkinter added new features that make our programs much nicer.

### Work with Python
By far the easiest way to quickly code in Python is to use Repl.it. It's a fast, responsive, web-based editor that allows you to code in Python and also code in Tkinter (and shows you the output!).

I recommend this tool to all my students when they're starting out: [**repl**](https://repl.it)

If you want to take it to the next level and have the ability to code larger projects, and you want to work in your own IDE, I usually recommend PyCharm. PyCharm has a free version called the Community Edition that is plenty powerful for almost anything you'll ever need.

You can get PyCharm here: [**Pycharm**](https://www.jetbrains.com/pycharm/download/)

And you'll need to get Python downloaded as well: [**Python**](https://www.python.org/)

If you'd like to use a different editor, feel free to do so. I often use Visual Studio Code when I'm working on smaller files and projects.

Thanks again for joining me in this course, let's get started!

___ 

# Section2 : Python Refresher

## Get the Python Refresher code here
To make it easier for you to refer back to the code whenever it's necessary, we've put all the code that we'll cover in this section on GitHub.

You can read it and also download it here: [**Github**](https://github.com/tecladocode/python-refresher)

## Variables 

To define an __**int**__ : 
```python
x = 14 
```
To define a __**float**__ : 
```python
x = 14.7
```
To define a __**String**__ : 
```python
Ch = " TKinter Course "
print ( ch * 2 )
>>> TKinter Course TKinter Course 
```




## What is Navigation2 Stack, Why do we need it ?    

<blockquote> Navigation = Navigation2 = Nav2 </blockquote>
      
Benefits of ROS2: 
  * Create the base layer super fast
  * Provide a standard for robotics application
  * use on any robot
  * open source community
Whats navigation 2 Stack :
  - a collection of ROS packages created to acheive a specific goal :
  - the Robot must move safely from point A to Point B
  - 2 Step-Process
    1. create a map with SLAM
    2. MAke the robot navigate from point A to point B
# Section 2 : Setup and Installation for ROS2 and Nav2
## Setup and installation 
we are going to use __`ROS2 Humble`__ with __`Ubuntu 22.04`__

## PLEASE READ - DO NOT USE ROS2 FOXY
I'm just adding a quick note here to urge you not to use ROS2 Foxy, and instead go with a recent and supported version, such as ROS2 Humble.

The reason for this note is that many are still trying to work with Nav2 and Foxy, and unfortunately there are a lot of bugs and hard-to-solve issues. Also, the Simple Commander API won't work in Foxy.

And there is simply no solution to that, as Foxy is not supported anymore.

So, I strongly recommend that you install Ubuntu 22.04 and ROS2 Humble.

If you are still on Ubuntu 20.04, it might seem like a lot of setup and wasted time.

I can guarantee you that you will waste way more time trying to fix issues with Nav2 on ROS2 Foxy.

So, take the time to install ROS2 Humble, and this small time investment will actually save you a lot of time in the mid/long term :)

## [Recap] Install and Setup ROS2 on Ubuntu 22.04

Seen in ROS2_For_beginners

## Install the Navigation 2 Stack

```bash
sudo apt update
```
```bash
sudo apt upgrade
```
```bash
sudo apt autoremove
```
```bash
sudo apt install ros-humble-navigation2 ros-humble-nav2-bringup ros-humble-turtlebot3*
```

## Install the Tools We’ll Need For the Course

```bash
sudo apt install python3-colcon-common-extensions
```
```bash
sudo apt install git
```
```bash
sudo apt install terminator
```
```bash
sudo snap install --classic code
```
___

# Section 3 : Generate a Map with SLAM (Simultaneous Localization and Mapping)

[SLAM+Steps+(ROS2+Nav2+Course+-+Section+3).pdf](https://github.com/fedikk/ROS2-Nav2-Navigation-2-Stack---with-SLAM-and-Navigation/files/15121921/SLAM%2BSteps%2B.ROS2%2BNav2%2BCourse%2B-%2BSection%2B3.pdf)

```bash
gedit ~/.bashrc 
``` 

add this line : 

```
export TURTLEBOT3_MODEL=waffle
```

to Run the __`TurtleBOT3 world`__ run this command : 
```bash
ros2 launch turtlebot3_gazebo turtlebot3_world.launch.py
```
 you must see something like this : 

![image](https://github.com/fedikk/ROS2-Nav2-Navigation-2-Stack---with-SLAM-and-Navigation/assets/98516504/31f8c435-65d5-460f-9bce-17ae3907df8c)

to controll the robot mouvement from the keyboard : 

```bash
ros2 run turtlebot3_teleop teleop_keyboard
```
## Generate and Save a Map with SLAM in ROS2
Run the commands simultanly : 
### 1 
```bash
ros2 launch turtlebot3_gazebo turtlebot3_world.launch.py
```
### 2 
```bash
ros2 launch turtlebot3_cartographer cartographer.launch.py use_sim_time:=True
```
### 3 
```bash
ros2 run turtlebot3_teleop teleop_keyboard
```
After moving the robot in the world you must got somthing like this : 

![map](https://github.com/fedikk/ROS2-Nav2-Navigation-2-Stack---with-SLAM-and-Navigation/assets/98516504/7c250671-9463-449d-881c-f8aa9acd791d)

### 4
```bash
cd && mkdir maps
```
### 5
```bash
ros2 run nav2_map_server map_saver_cli -f ~/maps/my_map
```
```plaintext
[INFO] [1714081189.367483320] [map_saver]: 
	map_saver lifecycle node launched. 
	Waiting on external lifecycle transitions to activate
	See https://design.ros2.org/articles/node_lifecycle.html for more information.
[INFO] [1714081189.367973914] [map_saver]: Creating
[INFO] [1714081189.373619976] [map_saver]: Configuring
[INFO] [1714081189.379934597] [map_saver]: Saving map from 'map' topic to '/home/ros/maps/my_first_map' file
[WARN] [1714081189.380015574] [map_saver]: Free threshold unspecified. Setting it to default value: 0.250000
[WARN] [1714081189.380046128] [map_saver]: Occupied threshold unspecified. Setting it to default value: 0.650000
[WARN] [map_io]: Image format unspecified. Setting it to: pgm
[INFO] [map_io]: Received a 124 X 116 map @ 0.05 m/pix
[INFO] [map_io]: Writing map occupancy data to /home/ros/maps/my_first_map.pgm
[INFO] [map_io]: Writing map metadata to /home/ros/maps/my_first_map.yaml
[INFO] [map_io]: Map saved
[INFO] [1714081191.092074723] [map_saver]: Map saved successfully
[INFO] [1714081191.099774816] [map_saver]: Destroying
```

<blockquote> The Process of saving map may not run in the first times repeat it until it works </blockquote>

## Saved Map 

![maps_folder](https://github.com/fedikk/ROS2-Nav2-Navigation-2-Stack---with-SLAM-and-Navigation/assets/98516504/c07699e8-dc95-4c84-b0e7-c514bdec876c)
![my_first_map](https://github.com/fedikk/ROS2-Nav2-Navigation-2-Stack---with-SLAM-and-Navigation/assets/98516504/1dd483f5-8cd5-45a8-9bd7-6f74df297feb)

## What’s Inside the Generated Map? 

### my_first_map.yaml
```yaml
image: my_first_map.pgm
mode: trinary
resolution: 0.05
origin: [-1.25, -2.41, 0]
negate: 0
occupied_thresh: 0.65
free_thresh: 0.25
```
when you open __`my_first_map.pgm`__ :
```
P5
124 116
255
```
then : 124 * 0.05 = 6.2 m on X axis 
       116 * 0.05 = 2.8 m on Y axis

##  SLAM Activity - Create a New Map in Turtlebot3 House

Generate the map of TurtleBOT3 House !!

Hint :  to open the house world 
```bash
ros2 launch turtlebot3_gazebo turtlebot3_house.launch.py
```
### challenge_TurtleBOT3_house_map.yaml
```yaml
image: my_house.pgm
mode: trinary
resolution: 0.05
origin: [-5.76, -5.14, 0]
negate: 0
occupied_thresh: 0.65
free_thresh: 0.25
```
___ 
