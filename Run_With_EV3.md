# Run With EV3

## Setup

1. Clone the rosev3

```bash
$ cd ~/
$ git clone https://github.com/YI-LING-BA-JI-JHUAN-TI-SHENG/rosev3.git
```

2. Set the ROS master URI

```bash
$ vim ~/rosev3/gripp3r/.env
```

+ Input string as following example.
+ Please replace xxx with your static ip and port.

```
MASTER_URI=http://xxx.xxx.xxx.xxx:xxx
```

## Execution Progress

1. Run roscore (terminal 1)

```bash
$ roscore
```

2. Connect to ev3 robot (terminal 2)

```bash
$ ssh root@192.168.1.101
```

3. Open ev3 manager (terminal 2)

```bash
$ ev3_manager
```

4. Run docker (terminal 3)

```bash
$ cd ~/rosev3/gripp3r/
$ sudo docker-compose up
```

5. Wait connection

+ Wait terminal 2 to finished running launch file

6. Open simulation and control environment

  a. Use gazebo to open a world (terminal 4)

```bash
$ roslaunch robot_simulation_pkg simulation.launch
```

  b. Navigation (terminal 5)

```bash
$ roslaunch robot_navigation_pkg multi_navigation.launch
```

  c. Open central control node (terminal 6)

```bash
$ roslaunch central_control_pkg multi_control.launch
```

  d. Publish a test instruction (terminal 7)

```bash
$ rostopic pub /speaker std_msgs/String 3:a
```

7. Close docker (terminal 3)

```bash
$ cd ~/rosev3/gripp3r/
$ sudo docker-compose down
```
