### 数字钟

[TOC]

### 0x01 结构

```
- DigitalClock1-0
	- main
		// 主电路
    - sevenbit
    	// 七段数码表显示
    - foutbitcounter
		// 每个时刻输出+1
    - Basic
    	// 简单的封装
    - NaoZhong
    	// 闹钟
    - Jianfaqi
    	// 每个时刻-1 从9到0
    - Jianfaqisix
    	// 每个时刻-1 从6到0
    - Jianfaqitwo
    	// 每个时刻-1 从2到0
    - Date
    	// 日期
    - fourbitcounterdate
    	// 类似于4位计数器，初始为0001
    - fourbitcounterdate1
    	// 同4未计数器
```



### 0x02 功能介绍

+ main

  + input

    + CLK: 提供时钟信号
    + init: 初始化数字钟
    + H/M/S:调节数字钟初始时间
    + pause: 暂停数字钟运行
    + Twentyfour/twelve: 选择24小时或12小时模式
    + ho1/ho0/mi1/mi0/se1/se0: 设置闹钟时间
    + Reset: 关闭闹钟
    + y3/y2/y1/y/mm1/mm0/day1/day0: 设置日期
    + resetdate: 初始化日期到0000.00.01
    + Reverse: 倒计时选项，当高电平时为倒计时功能
    + resetReverse: 初始化倒计时时间
    + H1/H0/M1/M0/S1/S0: 设置倒计时时间

  + output

    无

+ sevenbit

  + input 
    + D3/D2/D1/D0: 4位数字信号
  + output
    + 连到七段数码表

+ fourbitcounter

  + input
    + T: when 1, output ++
    + Pause: to pause
    + Reset: to reset
  + output
    + a 4bit binary number

+ Basic

  + Simply packaging

+ NaoZhong

  + to compare the input time and the setted time and then output a 1bit binary signal

+ Jianfaqi/Jianfaqisix/Jianfaqi

  + output--

+ Date

  + like basic

+ fourbitcounterdate/fourbitcounterdate1

  + not to introduce

