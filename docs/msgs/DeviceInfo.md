## 文件

robot_msg/msg/DeviceInfo.msg

## 定义

类型| 名称 | 描述
--|--|--
bool | connected | 底盘连接状态： <br> true : 连接成功 <br> false： 连接失败
uint32 | bump_state | 碰撞传感器
uint32[] | adc_channal | ADC传感器通道值， **跌落传感器等**
uint32[] | range_sensor | 超声，tof等

### adc数据对应关系枚举示例

```
    # adc channal e.g.
     adc_channal[0]     -   cliff_left
     adc_channal[1]     -   cliff_mid
     adc_channal[2]     -   cliff_right
     ......
```

#### range数据对应关系示例
```
    # range sensor e.g.
    range_sensor[0]     - sonar_left
    range_sensor[1]     - sonar_right
    range_sensor[2]     - infrared_mid 
    ......
```