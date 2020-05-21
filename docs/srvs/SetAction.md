## 文件

robot_msg/srv/SetAction.srv

## 请求

类型| 名称| 描述
--|--|--
string | action_request_id | 动作请求id
[Vector3](http://docs.ros.org/api/geometry_msgs/html/msg/Vector3.html) | goal | 动作目标，如果没有具体目标值则填空：<br> x： x坐标(m) <br> y： y坐标(m) <br>z： 姿态角(rad)  

## 响应

类型| 名称 | 描述
--|--|--
string | action_response_id| 回复id，与当前action_request_id值相同，表明ros收到命令

## action_request_id 枚举

```
#   action_request_id enum: 		

    "sleep"			    - 休眠		
    "safety_forward"    - 前进，遇到障碍物停止
    "movebase_goal"	    - 导航到目标点		
    "rotate"		    - 旋转一定角度（body系）	
    "rotate_to"		    - 旋转到指定朝向（world系）
    "go_charging"	    - 返回充电				
    "separate_docker"	- 脱离充电桩		
    "remote_telep"	    - 远程遥控

```


