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

Additionally, you may also specify ```use_sim_time``` (default value false), as such
```bash
tmuxinator start 2310_mission_launch ~/2310_workspace turtlebotIP=192.168.1.1 use_sim_time=True
```


## Making Edits
From the directory of this repo, 
```bash
tmuxinator edit --local 2310_mission_launch
```
