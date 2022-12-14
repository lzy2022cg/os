
# 1.1 操作系统的目标和作用

> os定义 : os是直接控制和管理`计算机硬件`、`软件资源`，合理的对各类作业进行调度，以方便以用户使用的`程序集合`。

## 1.1.1 操作系统的目标和作用
- 方便性
- 有效性
- 可扩充性
- 开放性
## 1.1.2 操作系统的作用
- os作为用户与计算机硬件系统之间的接口
- os作为计算机系统资源的管理者
- os实现了对计算机资源的抽象
## 1.1.3 推动操作系统发展的主要动力
- 不断提高计算机资源利用率
- 方便用户
- 器件的不断更新换代
- 计算机体系结构的不断发展
# 1.2 操作系统的发展过程

## 1.2.1 未配置操作系统的计算机系统（了解即可）

## 1.2.2 单道批处理系统
------------------------------------------------------------------------------------------------------------
### 批处理系统定义（此框为额外添加）
- 用户使用系统提供的作业控制语言（JCL）来描述自己对作业运行的控制意图，并将这些控制信息连同作业一起提交给计算机。
- 由OS去控制、调度各作业的运行并输出结果。
- 由于作业进入系统后用户不在干预，从而提高了效率。
> 设计目标: 提高系统资源的使用效率；提高作业的吞吐量
------------------------------------------------------------------------------------------------------------
- 单道批处理系统的处理过程 :
  - 为实现对作业的连续处理，需要先把一批作业以脱机方式输入到磁带上，并在系统中配上监督程序(Monitor)，在它的控制下，使这批作业能一个接一个地连续处理。
- 单道批处理系统的缺点：
  - 系统中的资源得不到充分的利用。这是因为在内存中仅有一道程序，每逢该程序在运行中发出/0请求后，CPU便处于等待状态，必须在其1/0完成后才继续运行。又因1/O设备的低速性，更使CPU的利用率显著降低。

## 1.2.3 多道批处理系统

- 多道程序设计
  - 在多道批处理系统中，用户所提交的作业都先存放在外存上并排成一个队列，称为“后备队列”;然后，由作业调度程序按一定的算法从后备队列中选择若干个作业调入内存，使它们共享CPU和系统中的各种资源。
  - 所以为了进一步提高资源的利用率和系统吞吐量，在20世纪60年代中期引入了多道程序设计技术，由此形成了多道批处理系统。

- 多道批处理系统的优缺点
  - 资源利用率高
  - 系统吞吐量大
  - 平均周转时间长
  - 无交互能力

 - 多道批处理系统的特征
   - 多道性
   - 无序性
   - 调度性
 
- 多道批处理系统需要解决的问题
  - 处理机争用问题（处理cpu的争用问题）
  - 内存分配和保护问题
  - I/O设备分配问题
  - 文件的组织和管理问题
  - 作业管理问题
  - 用户与系统的接口问题
  
## 1.2.3分时系统
- 一台计算机连接多个终端，用户通过各自的终端把作业送入计算机;计算机又通过终端向各个用户报告其作业的运行情况。（理解）
- 计算机能分时轮流地为各终端用户服务，并能及时地对用户服务请求予以响应。（理解）
- 分时系统基本特征
  - 多路性
  - 独立性
  - 及时性
  - 交互性

## 1.2.5 实时系统
> 定义 : 提高系统的响应时间，对随机发生的外部事件作出及时响应并在规定的时间内对其进行处理。
- 实时任务，按任务执行时是否呈现周期性来划分
  - 周期性实时任务。
  - 非周期性实时任务。

- 都必须联系着一个截止时间(Deadline)。
  - 开始截止时间--任务在某时间以前必须开始执行
  - 完成截止时间--任务在某时间以前必须完成

- 根据对截止时间的要求来划分
  - 硬实时任务(hard real-time task) ： 系统必须满足任务对截止时间的要求，否则可能出现难以预测的结果
  - 软实时任务(Soft real-timetask) ： 它也联系着一个截止时间，但并不严格，若偶尔错过了任务的截止时间，对系统产生的影响也不会太大

- 实时系统基本特征
  - 快速的响应时间
  - 有限的交互能力
  - 高可靠性

# 1.3 操作系统的基本特性

## 1.3.1 并发
- 并发:指两个或多个事件在同一时间间隔内发生

- 并行:指两个或多个事件在同一时刻发生

## 1.3.2 共享
- 指系统中的支援可供内存中多个并发执行的进程共同调用
- 互斥共享方式 : 如打印机，磁带机
- 同时访问方式 : 所谓的`同时`，在单处理机下是宏观意义上的，而在微观上，这些进程对该资源的访问是交替进行的。 如 : 磁盘

## 1.3.3 虚拟
> 通过某种技术将一个物理实体变为若干个逻辑上的对应物的功能称为`虚拟`
- 时分复用技术
- 空分复用技术

## 1.3.4 异步
>  系统中并发执行的多道进程`走走停停`，以不可预知的速度向前推进
