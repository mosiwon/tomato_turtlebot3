# tomato_mobile

required - > 'YDLidar-SDK
Link:https://github.com/YDLIDAR/sdk

.bashrc -- >
```
export TURTLEBOT3_MODEL=waffle
export LDS_MODEL=YDLidar
```

in tomato_mobile
```bash
colcon build --symlink-install
source install/setup.bash
```



turtlebot - bringup
```bash
ros2 launch turtlebot3_bringup robot.launch.py 
```

turtlebot teleop
```bash
ros2 run turtlebot3_teleop teleop_keyboard
```

turtlebot slam (cartographer)
```bash
ros2 launch turtlebot3_cartographer cartographer.launch.py
```

turtlebot navigation
```bash
ros2 launch turtlebot3_navigation2 navigation2.launch.py \map:=$HOME/tomato_mobile/map_addinedu.yaml 
```