# gps_waypoint_navigation
gps_waypoint_navigation

## catkin_make error

以下のエラーが発生

```Error
fatal error: robot_localization/navsat_conversions.h: そのようなファイルやディレクトリはありません
 #include <robot_localization/navsat_conversions.h>

fatal error: move_base_msgs/MoveBaseAction.h: そのようなファイルやディレクトリはありません
 #include <move_base_msgs/MoveBaseAction.h>
```

以下のパッケージ群を全てインストールする
```bash
sudo apt-get install -y ros-melodic-robot-localization
sudo apt-get install ros-melodic-geographic-msgs
sudo apt-get install libgeographic-dev
```

```bash
$ sudo apt-get install ros-melodic-ddynamic-reconfigure
$ sudo apt-get install ros-melodic-tf2-sensor-msgs
$ sudo apt-get install ros-melodic-move-base
$ sudo apt-get install -y ros-melodic-gmapping ros-melodic-amcl ros-melodic-map-server
$ sudo apt-get install ros-melodic-dwa-local-planner
```

```bash
sudo apt install geographiclib-tools
git clone https://github.com/cra-ros-pkg/robot_localization.git
```

これでエラーが取れて、catkin_make出来た

