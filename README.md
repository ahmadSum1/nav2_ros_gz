# To run simulation 

## Clone this repo
```
git clone --recurse-submodules -j8 git@github.com:kulkarni-raunak/nav2_ros_gz.git
```

## Inside nav2_ros_gz/

```
rosdep install -r --from-paths . --ignore-src --rosdistro $ROS_DISTRO -y
```

## Build

```
colcon build --symlink-install --packages-skip nav2_system_tests
```

## Launch
```
ros2 launch nav2_bringup tb3_gz_simulation_launch.py use_gz:=False headless:=False
```

## TODOs

Follow [migration of gazebos_ros_pkgs to ros_gz guide](https://gazebosim.org/docs/garden/migrating_gazebo_classic_ros2_packages) to tweak the packges related to nav2/navigation2. `Note: May not support Gazebo garden.`
