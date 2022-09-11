
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
### 批处理系统定义
- 用户使用系统提供的作业控制语言（JCL）来描述自己对作业运行的控制意图，并将这些控制信息连同作业一起提交给计算机。
- 由OS去控制、调度各作业的运行并输出结果。
- 由于作业进入系统后用户不在干预，从而提高了效率。
> 设计目标: 提高系统资源的使用效率；提高作业的吞吐量
------------------------------------------------------------------------------------------------------------
- 单道批处理系统的处理过程

为实现对作业的连续处理，需要先把一批作业以脱机方式输入到磁带上，并在系统中配上监督程序(Monitor)，在它的控制下，使这批作业能一个接一个地连续处理。
