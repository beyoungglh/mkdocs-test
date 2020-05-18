## 文件

robot_msg/msg/DockingState.msg

## 定义

类型| 名称 | 描述
--|--|--
int32 | docking_state | 机器人回充状态

## 状态枚举

```

    # constants state enum

    int32 SEARCHING_STATION = 1     # 1-寻找充电桩 
    int32 DOCKING_STATION   = 2     # 2-对接中 
    int32 DOCKING_SUCCESS   = 3     # 3-对接成功 
    int32 SEARCHING_FAILURE = 4     # 4-失败-未找到充电桩
    int32 DOCKING_FAILURE   = 5     # 5-失败-对接失败

```