# Run UVC_Camera with RPi3

1. Use RPi3
+ Method 1: Use RPi3 with screen
+ Method 2: Connect to RPi3
```bash
$ ssh ubuntu@192.168.1.108
```

2. Master setup
```bash
$ sudo vim /etc/hosts
```
set master ip
master xxx.xxx.xxx.xxx

3. Run UVC camera
```bash
$ rosrun uvc_camera uvc_camera_node
```
