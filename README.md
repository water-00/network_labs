﻿# network_labs

南开大学计算机学院 计算机网络实验课程代码

写在最前面：这个课程的实验没给任何的框架和文档，这是比较糟糕的，也很容易让人害怕，尤其是实验一，一上来就会让人感觉：“什么叫设计一个协议？？我连有哪些协议都不知道，难道要我去设计一个和HTTP一样的协议吗？？”其实不是的，A发消息-B能收到消息，反之亦然，这已经是一个协议了。另外socket编程听上去很复杂很难完全没接触过，但是实际上有很多框架性的、不需要知其所以然的东西，真正要自己实现的基本都是你学过的。所以别怕，多去查查资料，看看视频，问问chatGPT，最重要的是，**早开始**！

对于实验一的一个参考视频：

https://www.bilibili.com/video/BV1A4411s7pC/?spm_id_from=333.999.0.0&vd_source=fbedabb98d19c6fdc3cc8ab84fc4afeb

实验一：

1） 使用流式Socket，设计一个两人聊天协议，要求聊天信息带有时间标签。请完整地说明交互消息的类型、语法、语义、时序等具体的消息处理方式。

2） 对聊天程序进行设计。给出模块划分说明、模块的功能和模块的流程图。

3） 在Windows系统下，利用C/C++对设计的程序进行实现。程序界面可以采用命令行方式，但需要给出使用方法。编写程序时，只能使用基本的Socket函数，不允许使用对socket封装后的类或架构。

4）对实现的程序进行测试。

5）撰写实验报告，并将实验报告和源码提交至本网站。

评分原则：

1）协议设计：25%

2）程序设计：25%

3）程序实现：25%

4）实验报告：25%

实验二：

（1）搭建Web服务器（自由选择系统），并制作简单的Web页面，包含简单文本信息（至少包含专业、学号、姓名）和自己的LOGO。（2）通过浏览器获取自己编写的Web页面，使用Wireshark捕获浏览器与Web服务器的交互过程，并进行简单的分析说明。（4）提交实验报告。

评分标准（总分100分）

(1)  功能实现：

l Web服务器搭建、编写Web页面（提交HTML文档）（20分）

l Wireshark捕获交互过程（提交捕获文件）（20分）

(2)  演示并讲解（30分）

(3)  实验报告（30分）

实验三：

实验3-1：利用数据报套接字在用户空间实现面向连接的可靠数据传输，功能包括：建立连接、差错检测、确认重传等。流量控制采用停等机制，完成给定测试文件的传输。

实验3-2：在实验3-1的基础上，将停等机制改成基于滑动窗口的流量控制机制，采用固定窗口大小，支持累积确认，完成给定测试文件的传输。

实验3-3：在实验3-2的基础上，选择实现一种拥塞控制算法，也可以是改进的算法，完成给定测试文件的传输。

实验3-4：基于给定的实验测试环境，通过改变延迟时间和丢包率，完成下面3组性能对比实验：（1）停等机制与滑动窗口机制性能对比；（2）滑动窗口机制中不同窗口大小对性能的影响；（3）有拥塞控制和无拥塞控制的性能比较。

实验要求：
(1)	实现单向传输。

(2)	对于每一个任务要求给出详细的协议设计。

(3)	给出实现的拥塞控制算法的原理说明。

(4)	完成给定测试文件的传输，显示传输时间和平均吞吐率。

(5)	性能测试指标：吞吐率、时延，给出图形结果并进行分析。

(6)	完成详细的实验报告（每个任务完成一份）。

(7)	编写的程序应结构清晰，具有较好的可读性。

(8)	提交程序源码和实验报告。

评分标准：
(1)	每个任务最高100分。

(2)	每个任务分值分配

-   协议设计、功能实现（40分）
-   演示并讲解（20分）
-   程序及规范性（20分）
-   实验报告（20分）

得分分别是：

| 1    | 92   |
| ---- | ---- |
| 2    | 100  |
| 3-1  | 80   |
| 3-2  | 90   |
| 3-3  | 87   |
| 3-4  | 83   |

感觉3-2用选择重传（SR）得分应该会比回退N（GBN）高一些？

另外实验一是拿vs2019写的，实验三是拿Windows下vscode写的，如果要编译需要添加一些参数，自己根据报错去搜吧。当然你也不应该编译我的程序，而只应该参考一些逻辑。

另外我也没用发的路由程序，而是在代码里用生成0-1之间随机数的方式模拟发生丢包和延时的概率。
