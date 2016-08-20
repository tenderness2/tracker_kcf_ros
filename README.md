# tracker_ws
基于ros下应用深度相机的kcf追踪算法实现

# 开发环境：

Ubuntu 14.04 + ros indigo

# 传感器：

深度相机（Xtion pro live）

# 实验平台：

Aiibot


# 运行：

## 1.首先启动ros环境：
```
$roscore
```
## 2.运行ros打开深度相机的节点，发出可播放深度图像和rgb图像的topic：
```
$roslaunch openni_launch openni.launch
```
## 3.查看ros的topic列表中是否有深度图像和rgb图像的topic：
```
$rostopic list
```
## 4.编译：
```
$catkin_make
$source devel/setup.bash
```
## 5.运行：

运行前需要打开移动平台，运行移动平台启动程序 aiibot_bringup

程序链接：http://git.aiiage.com:9000/liu.f/aiibot_bringup

启动地盘程序：
```
$roslaunch aiibot_bringup base_control.launch
```
启动追踪程序
```
$rosrun track_pkg kcf_node
```
## 6.使用程序

程序启动后，在图像窗口内鼠标左键框选所要跟踪的目标
