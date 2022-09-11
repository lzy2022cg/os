
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

