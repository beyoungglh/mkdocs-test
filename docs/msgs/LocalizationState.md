## 文件

robot_msg/msg/LocalizationState.msg

## 定义

类型| 名称 | 描述
--|--|--
int32 | localization_state | 机器人定位状态
[Vector3](http://docs.ros.org/api/geometry_msgs/html/msg/Vector3.html) | global_pose | 机器人全局位置坐标:<br>x, x坐标 (m) <br> y, y坐标  (m) <br> z, 姿态角 (rad)

## 定位状态枚举

```

# localization state enum

    int32 LOCALIZATION_STATE_MAP_BUILDING = 1   #建图中
    int32 LOCALIZATION_STATE_LOCATING     = 2   #定位中
    int32 LOCALIZATION_STATE_SUCCESS      = 3   #定位成功
    int32 LOCALIZATION_STATE_FAILURE      = 4   #定位失败

```