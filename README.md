段选择子：https://blog.csdn.net/qq_35425243/article/details/82699195
https://blog.csdn.net/Lirx_Tech/article/details/42340619

## BookList
《Kafka技术内幕：图文详解Kafka源码设计与实现》郑奇煌 --- 有点晦涩，不适合入门，可作为参考书。

《深入理解Kafka：核心设计与实践原理》_朱忠华 --- Good，勘误：https://blog.csdn.net/u013256816/article/details/87834419

http://pdf.ebook23.com/ebook/5_mybatis相关/MyBatis从入门到精通__刘增辉(著).pdf
## TODO

Java核心技术 卷1 基础知识 原书第10版

Java核心技术 卷2 高级特性 原书第10版

Java NIO

## 用户态OVS
https://github.com/openvswitch/ovs/blob/master/Documentation/intro/install/userspace.rst
http://docs.openvswitch.org/en/latest/howto/userspace-tunneling/

《Orange'S：一个操作系统的实现》

```bash
目录	14
上篇	21
第1章 马上动手写一个最小的“操作系统”	22
	1.1 准备工作	22
	1.2 十分钟完成的操作系统	23
	1.3 引导扇区	24
	1.4 代码解释	24
	1.5 水面下的冰山	26
	1.6 回顾	27
第2章 搭建你的工作环境		28
	2.1 虚拟计算机Bochs	28
	2.1.1 Bochs初体验	28
	2.1.2 Bochs的安装	29
	2.1.3 Bochs的使用	30
	2.1.4 用Bochs调试操作系统	32
	2.2 QEMU	35
	2.3 平台之争：Windows还是*nix		36
	2.4 GNU/Linux下的开发环境	40
	2.5 Windows下的开发环境	42
	2.6 总结	43
第3章 保护模式（Protect Mode）	45
	3.1 认识保护模式	45
	3.1.1 保护模式的运行环境	49
	3.1.2 GDT（Global Descriptor Table）	51
	3.1.3 实模式到保护模式，不一般的jmp	53
	3.1.4 描述符属性	55
	3.2 保护模式进阶	58
	3.2.1 海阔凭鱼跃	58
	3.2.2 LDT（Local Descriptor Table）	64
	3.2.3 特权级概述	68
	3.2.4 特权级转移	71
	3.2.5 关于“保护”二字的一点思考	85
	3.3 页式存储	85
	3.3.1 分页机制概述	86
	3.3.2 编写代码启动分页机制	87
	3.3.3 PDE和PTE	88
	3.3.4 cr3	91
	3.3.5 回头看代码	92
	3.3.6 克勤克俭用内存	93
	3.3.7 进一步体会分页机制	101
	3.4 中断和异常	107
	3.4.1 中断和异常机制	107
	3.4.2 外部中断	110
	3.4.3 编程操作8259A	111
	3.4.4 建立IDT	114
	3.4.5 实现一个中断	115
	3.4.6 时钟中断试验	116
	3.4.7 几点额外说明	118
	3.5 保护模式下的I/O	120
	3.5.1 IOPL	120
	3.5.2 I/O许可位图（I/O Permission Bitmap）	120
	3.6 保护模式小结	121
第4章 让操作系统走进保护模式	122
	4.1 突破512字节的限制	122
	4.1.1 FAT12	123
	4.1.2 DOS可以识别的引导盘	128
	4.1.3 一个最简单的Loader	128
	4.1.4 加载Loader入内存		129
	4.1.5 向Loader交出控制权	136
	4.1.6 整理boot.asm	136
	4.2 保护模式下的“操作系统”	137
第5章 内核雏形		139
	5.1 在Linux下用汇编写Hello World	139
	5.2 再进一步，汇编和C同步使用		140
	5.3 ELF（Executable and Linkable Format）	143
	5.4 从Loader到内核	147
	5.4.1 用Loader加载ELF		147
	5.4.2 跳入保护模式	151
	5.4.3 重新放置内核	157
	5.4.4 向内核交出控制权		162
	5.5 扩充内核		163
	5.5.1 切换堆栈和GDT	164
	5.5.2 整理我们的文件夹		168
	5.5.3 Makefile		169
	5.5.4 添加中断处理	175
	5.5.5 两点说明		188
	5.6 小结		189
第6章 进程	191
	6.1 迟到的进程		191
	6.2 概述	191
	6.2.1 进程介绍		192
	6.2.2 未雨绸缪——形成进程的必要考虑		192
	6.2.3 参考的代码	193
	6.3 最简单的进程	194
	6.3.1 简单进程的关键技术预测	195
	6.3.2 第一步——ring0→ring1	198
	6.3.3 第二步——丰富中断处理程序	209
	6.4 多进程	220
	6.4.1 添加一个进程体	220
	6.4.2 相关的变量和宏	220
	6.4.3 进程表初始化代码扩充	222
	6.4.4 LDT	223
	6.4.5 修改中断处理程序		223
	6.4.6 添加一个任务的步骤总结	226
	6.4.7 号外：Minix的中断处理	227
	6.4.8 代码回顾与整理		232
	6.5 系统调用		240
	6.5.1 实现一个简单的系统调用	242
	6.5.2 get_ticks的应用	247
	6.6 进程调度	252
	6.6.1 避免对称——进程的节奏感		252
	6.6.2 优先级调度总结		260
第7章 输入/输出系统	262
	7.1 键盘	262
	7.1.1 从中断开始——键盘初体验		262
	7.1.2 AT、PS/2键盘	263
	7.1.3 键盘敲击的过程	264
	7.1.4 用数组表示扫描码		268
	7.1.5 键盘输入缓冲区		271
	7.1.6 用新加的任务处理键盘操作		273
	7.1.7 解析扫描码	274
	7.2 显示器	283
	7.2.1 初识TTY	284
	7.2.2 基本概念	284
	7.2.3 寄存器	287
	7.3 TTY任务	290
	7.3.1 TTY任务框架的搭建	292
	7.3.2 多控制台		297
	7.3.3 完善键盘处理	301
	7.3.4 TTY任务总结	308
	7.4 区分任务和用户进程		309
	7.5 printf	311
	7.5.1 为进程指定TTY	312
	7.5.2 printf()的实现	312
	7.5.3 系统调用write()	314
	7.5.4 使用printf()	316
下篇	319
第8章 进程间通信	320
	8.1 微内核还是宏内核	320
	8.1.1 Linux的系统调用	322
	8.1.2 Minix的系统调用	323
	8.1.3 我们的选择	325
	8.2 IPC		326
	8.3 实现IPC	326
	8.3.1 assert()和panic()		329
	8.3.2 msg_send()和msg_receive()	333
	8.3.3 增加消息机制之后的进程调度	341
	8.4 使用IPC来替换系统调用get_ticks	342
	8.5 总结	344
第9章 文件系统		345
	9.1 硬盘简介	345
	9.2 硬盘操作的I/O 端口		346
	9.3 硬盘驱动程序	347
	9.4 文件系统	357
	9.5 硬盘分区表	358
	9.6 设备号	364
	9.7 用代码遍历所有分区		367
	9.8 完善硬盘驱动程序		372
	9.9 在硬盘上制作一个文件系统		375
	9.9.1 文件系统涉及的数据结构		376
	9.9.2 编码建立文件系统			378
	9.10 创建文件		386
	9.10.1 Linux下的文件操作	386
	9.10.2 文件描述符（file descriptor）	387
	9.10.3 open()		389
	9.11 创建文件所涉及的其他函数		397
	9.11.1 strip_path()	397
	9.11.2 search_file()	398
	9.11.3 get_inode()和sync_inode()	399
	9.11.4 init_fs()		401
	9.11.5 read_super_block()和get_super_block()		402
	9.12 关闭文件		403
	9.13 查看已创建的文件		404
	9.14 打开文件		406
	9.15 读写文件		407
	9.16 测试文件读写	410
	9.17 文件系统调试	413
	9.18 删除文件		415
	9.19 插曲：奇怪的异常	421
	9.20 为文件系统添加系统调用的步骤	423
	9.21 将TTY纳入文件系统	424
	9.22 改造printf		431
	9.23 总结	433
第10章 内存管理	434
	10.1 fork	434
	10.1.1 认识fork		434
	10.1.2 fork前要做的工作（为fork所做的准备）	437
	10.1.3 fork()库函数	441
	10.1.4 MM	441
	10.1.5 运行	447
	10.2 exit和wait		447
	10.3 exec	452
	10.3.1 认识exec		453
	10.3.2 为自己的操作系统编写应用程序		454
	10.3.3 “安装”应用程序	456
	10.3.4 实现exec		462
	10.4 简单的shell	467
	10.5 总结	469
第11章 尾声	471
	11.1 让mkfs()只执行一次	471
	11.2 从硬盘引导		475
	11.2.1 编写硬盘引导扇区和硬盘版loader		475
	11.2.2 “安装”hdboot.bin和hdldr.bin	481
	11.2.3 grub	481
	11.2.4 小结		483
	11.3 将OS安装到真实的计算机		485
	11.3.1 准备工作		485
	11.3.2 安装Linux	486
	11.3.3 编译源代码	486
	11.3.4 开始安装		487
	11.4 总结	487
参考文献	490
```
