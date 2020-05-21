## 文件

robot_msg/srv/SetMap.srv

>**该文档以下功能还需再确定：**
>
> * 需不需要支持多个地图，多楼层等情况
> * 需不需要机器人间共享地图，同一区域多个机器人的情况


## 请求

类型|名称|描述
--|--|--
string | cmd| 地图操作命令
string | map_name | 构建地图名称

## 响应

类型|名称|描述
--|--|--
bool | result | 执行结果,成功或者失败
int32| message_code | 额外信息代码
string | message | 额外信息描述，e.g. for error messages

## cmd 枚举

```
# cmd enum

    "building_map",     构建地图
    "save_map",         保存地图


```

