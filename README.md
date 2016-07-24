﻿# SimpleOscillograph_For_STM32

##功能：
  使用STM32作为核心器件，实现三通道示波器，在上位机处理和显示。支持多种触发方式，支持实时采集，最大三通道采样。可以对信号进行加窗处理，并具有FFT频谱分析等功能。<br>
  为了程序的可移植性和简单性，使用单独的外部中断边沿触发、使用ADC+DMA自动循环采集数据以及单独的定时器中断触发采集，而没有使用STM32 ADC的外部触发等特性。

##说明
  1.本程序使用STM32的USB开发了虚拟串口，更节约了硬件成本，本身就可以与上位机通信了。当然也可以配置宏并重新编译使用串口与上位机交互（具体见源代码MYDEF.H）。<br>
  2.需要配合基于LabVIEW开发的上位机程序使用。<br>LabVIEW源码地址：https://github.com/shuai132/SimpleOscillograph_For_LabVIEW
