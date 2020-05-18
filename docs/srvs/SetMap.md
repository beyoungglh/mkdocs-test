## 文件

robot_msg/srv/SetMap.srv

## 请求

类型|名称|描述
--|--|--
string | cmd| 地图操作命令

## 响应

类型|名称|描述
--|--|--
bool | result | 执行结果,成功或者失败
string | message | 额外信息描述，e.g. for error messages

## cmd 枚举

```
# cmd enum

    "building_map",     构建地图
    "save_map",         保存地图


```

