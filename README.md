# Super Ultimate Tmuxinator Mission Launch Script

## Setup
1. Install [Tmuxinator](https://github.com/tmuxinator/tmuxinator)
2. clone this repo onto your Remote PC (in any directory you like)


## Usage
Run the launch command from the directory of this repo
In your launch command, you must specify 1. dir of your Remote PC's ros_ws 2. hostname of your turtlebot, e.g.
```bash
tmuxinator start 2310_mission_launch ~/2310_workspace turtlebotIP=192.168.1.1
```

Additionally, you may also specify the following parameters 

```use_sim_time``` (default value: false)
```bash
tmuxinator start 2310_mission_launch ~/2310_workspace turtlebotIP=192.168.1.1 use_sim_time=True
```

```expected_ssh_time``` (default value: 0)
time (in seconds) that ssh is expected to take
Remote_PC scripts are programmed to start after waiting ```expected_ssh_time``` seconds
```bash
tmuxinator start 2310_mission_launch ~/2310_workspace turtlebotIP=192.168.1.1 expected_ssh_time=10
```


## Making Edits
From the directory of this repo, 
```bash
tmuxinator edit --local 2310_mission_launch
```


## Intended Usage Example
3 tmux windows are opened: RPi, Remote_PC, Monitors
RPi
 - rosbu
 - ir_node
 - launcher_service
Remote_PC (see below)
 - Mission_Control
 - Nav2_Stack
 - Slam_Toolbox
 - RViz
Monitors
 - RPi top
 - Remote PC top
 - extra pane for opening ros2 topic monitors

![image](https://github.com/user-attachments/assets/f2d3b5cf-ad08-453e-87c0-cd918de827fb)


