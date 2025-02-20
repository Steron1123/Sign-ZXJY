# 职教家园打卡-可商化版

> 写在前面：鸣谢[rialll](https://github.com/rialll)，本项目核心代码见[fuckZXJY](https://github.com/rialll/fuckZXJY)

## 介绍
1、增加多种推送模式，例如Pushplus、DingDingWebHook机器人、Server_Turbo推送、自建Smtp邮件推送（邮件推送支持一对多、一对一）。

2、增加打卡倒计时，可设置账号打卡截止时间。

3、增加添加用户功能（可交互和非交互两种）、无需每次更改json文件。

4、优化推送、可设置满足某一条件推送，默认为运行时间为早七点时推送。详情见config.py第8行。

## 使用说明

平台推荐：7x24小时的Linux系统、Windows系统、青龙面板

安装所需依赖`pip install requirements.txt`

添加用户运行`python AddUser.py`/`python AddUser-noinput.py`

打卡主程序`python Main.py`

## 推送模块说明

>详情可见项目：[长目飞耳](https://github.com/zycn0910/Message-Push)



## user.json结构说明

```
{
    # 是否开启打卡
    "enabled": true,
    # 添加日期
    "adddate": "2023-10-15 12:23:32",
    # 打卡结束日期
    "enddate": "2023-10-16 12:23:32",
    # 账号别名
    "name": "测试名字",
    # 职校家园账号
    "phone": "测试账号",
    # 职校家园密码
    "password": "测试密码",
    # 打卡设备型号
    "deviceId": "测试手机型号",
    # 设备token， 添加账号时自动生成
    "dToken": "5xw7cfuznlo13yjv4prt862qiaskhd0meb9g",
    # 随机经纬最后一位数，默认开启
    "modify_coordinates": true,
    # 打卡地址
    "address": "河南郑州",
    # 经度，自动获取
    "longitude": "113.640100",
    # 纬度，自动获取
    "latitude": "34.724680",
    # 推送模式，为空则默认本地控制台
    "pushmode": "",
    # 推送数据
    "pushdata": {
        # DingDing机器人推送，模式1生效
      "Ding": {
        "Secret": null,
        "Token": null
      },
        # Pushplus推送，模式2生效
      "PushPlus": {
        "Token": null
      },
        # Server酱推送，模式3生效
      "Server_Turbo": {
        "Token": null
      },
        # 邮件推送，模式4且config内邮件信息为空生效
      "Email": {
        "Send": null,
        "Password": null,
        "Server_Address": null,
        "Smtp_Port": null,
        "Receiver": null
      }
    }
  }
```

## 重要

>本项目基于[GPL3.0开源协议](/GNU%20General%20Public%20License%20v3.0.html)
> 
> 项目内仅有一处版权信息，详情在`main.py`203行

