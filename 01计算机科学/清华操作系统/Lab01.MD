# Lab1 bootloader 启动 ucore os

x86 启动顺序
* IA-32 Intel 体系结构软件开发者手册
  * 所有寄存器初始值
  * EIP + CS 决定启动地址
* 第一条指令
  * BIOS 的 EPROM 所在地
* 处于实模式的段
* 从 BIOS 到 Bootloader
  * BIOS 加载存储设备上的第一个扇区，的 512 字节到内存的 0x7c00
  * 然后跳转到 @ 0x7c00 的第一条指令
* 从 bootloader 到 OS
  * 切换到保护模式 protection mode，段机制 segment-level protection
  * 硬盘读取 kernl in ELF 个是的 ucore kernel，跟在 MBR 后面的扇区，并梵高内存中固定位置
  * 跳转到 ucore os 的入口点执行，此时控制权到了 ucore OS
* 段机制
  * 

C 函数调用

gcc 内联汇编 inline assembly

x86-32 下的中断处理