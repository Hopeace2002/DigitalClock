## Digital Clock

[TOC]



### 0x01 Structure

```
- DigitalClock1-0
	- main
		// The main circuit
    - sevenbit
    	// To connect 7-Segment Display
    - foutbitcounter
		// Every clk, output++
    - Basic
    	// Simply packaging
    - NaoZhong
    	// Alarm Clock
    - Jianfaqi
    	// Every clk, output-- from 9 to 0
    - Jianfaqisix
    	// Every clk, output-- from 6 to 0
    - Jianfaqitwo
    	// Every clk, output-- from 2 to 0
    - Date
    	// Display the date
    - fourbitcounterdate
    	// Like the fourbit counter, only reset to 0001
    - fourbitcounterdate1
    	// Same as the fourbit counter
```

### 0x02 Introduction of every module

+ main

  + input

    + CLK: to provide the clock signal
    + init: to reset the forward clock
    + H/M/S: to adjust the initial time for Hour/Minute/Second of forward clock
    + pause: to pause the forward clock
    + Twentyfour/twelve: to select the mode of the forward clock
    + ho1/ho0/mi1/mi0/se1/se0: to set the alarm clock
    + Reset: to shut the alarm clock
    + y3/y2/y1/y/mm1/mm0/day1/day0: to set the initial date
    + resetdate: to reset the date to 0000.00.01
    + Reverse: when 0 to forward clock, when 1 to reverse clock
    + resetReverse: to reset the reverse clock
    + H1/H0/M1/M0/S1/S0: to set the reverse clock

  + output

       (Null)

+ sevenbit

  + input 
    + D3/D2/D1/D0: a 4bit binary number
  + output
    + a 7bit figure signal to connect the 7-Segment Display

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

