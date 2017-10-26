---
title: KinectV1与KinectV2详细比较
date: 2017-10-25 22:07:32
updated: 2017-10-26 15:14:00
categories:
- Kinect
tags: 
- Kinect
- VR
---


# 外观

* Kinect for Windows V1

    {% asset_img KinectV1_外观.jpg %}


* Kinect for Windows V2

    {% asset_img KinectV2_外观.jpg %}


# 原理

* Kinect for Windows V1

    Kinect v1的Depth传感器，采用了「Light Coding」的方式，读取投射的红外线pattern，通过pattern的变形来取得Depth的信息。为此，Depth传感器分为投射红外线pattern的IR Projector和读取的这个的IR Camera。还有Depth传感器中间还搭载了Color Camera。
    Light Coding是以色列的PrimeSense公司的Depth传感器技术，于2013年被美国苹果公司收购。

* Kinect for Windows V2

    Kinect V2预览版的Depth传感器，采用的是「Time of Flight(TOF)」的方式，通过从投射的红外线反射后返回的时间来取得Depth信息。Depth传感器看不到外观，不过Color Camera旁边是红外线Camera和投射脉冲变调红外线的Porjector。


# 配置

{% asset_img Kinect配置比较.png %}

KinectV2与V1相比
* 颜色传感器的分辨率增加，视角变广。

    {% asset_img KinectV1_颜色传感器输出图片.jpg %}

    {% asset_img KinectV2_颜色传感器输出图片.jpg %}

* 深度传感器分辨率增加，视角变广,检测范围增大，识别精度增加。

    {% asset_img KinectV1_深度传感器输出图片.jpg %}

    {% asset_img KinectV2_深度传感器输出图片.jpg %}

* 可跟踪姿态的人物数量增多，识别的关节点数增多，可以识别大拇指。

    {% asset_img KinectV1_识别关节点.jpg %}

    {% asset_img KinectV2_识别关节点.jpg %}

* 取消了控制摄像头倾斜角的电机，只能通过手动来摇头。

* 支持多个应用程序同时从传感器中读取数据。

    {% asset_img Kinect_多程序支持比较.png %}


# 最小运行环境

{% asset_img Kinect最小运行环境比较.png %}

# SDK

* Kinect V1只能用于 Kinect SDK 1.8 及以下的版本。

* Kinect SDK 2.0 及以上只支持Kinect V2。

* Kinect SDK 1.8 与 Kinect SDK 2.0 有较大差距。

# 价格

* Kinect V1 淘宝参考价格（已停产）---- 758元/套

{% asset_img KinectV1价格.png %}

* Kinect V2 官方参考价格         ---- 1468元/套

{% asset_img KinectV2感应器价格.png %}
{% asset_img KinectV2电源适配器价格.png %}


# 其它

* Kinect for Windows V1 现已停产。
* 好吧，KinectV2今天也停产了…… (2017.10.26)

-----
