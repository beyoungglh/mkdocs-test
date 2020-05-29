## 文件

robot_msg/msg/ActionState.msg

## 定义

类型| 名称 | 描述
--|--|--
string | action_state_id | 机器人所处功能状态id
int32 | action_feedback | 动作执行实时状态反馈

## 状态枚举

```

#   action_state_id enum: 	

    "idle"			    - 空闲		
    "sleep"			    - 休眠	
    "safety_forward"    - 前进，遇到障碍物停止	
    "movebase_goal"	    - 导航到目标点		
    "rotate"		    - 旋转一定角度（body系）	
    "rotate_to"		    - 旋转到指定朝向（world系）
    "go_charging"	    - 返回充电				
    "separate_docker"	- 脱离充电桩		
    "remote_telep"	    - 远程遥控

# action_feedback enum

    int32 NONE              = 0     # none
    int32 SET_NEW_GOAL      = 1     # 收到指令
    int32 RUNNING           = 2     # 动作执行中
    int32 GOAL_REACHED      = 3     # 成功 - 目标达到
    int32 GOAL_CANCLE       = 4     # 成功 - 目标被取消
    int32 OBSTACLE          = 5     # 失败 - 存在障碍物
    int32 NO_PATH           = 6     # 失败 - 没有可行路径
    int32 ERROR_NODEFINE    = 7     # 失败 - 其他异常 STUCK

```
