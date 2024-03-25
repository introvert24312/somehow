---
title: 常用概率分布-正态分布
date: 2024-03-24 18:46:27
tags: 统计学
categories: 卫生统计学
mathjax: true
---

## 引入

### 问题0

正态分布分布是什么？它是怎么来的？

---

正态分布是中心极限定理的发展

中心极限定理是什么？

例1:

假设你有100万人身高的数据，你定义样本X，样本大小为50，命令1000人每人制作一个样本X，当你收取1000人的样本均数$X_n$时，定义变量为$X_n$,绘制$X_n$的频数分布直方图，你会得到一个钟形曲线，也叫高斯曲线

进化

假设你从赌场获得了一批偏心骰子，这个骰子掷出1的概率为50%，掷出2、3、4、5、6的概率都为10%，投掷10次为1组，记录下每次的结果，你命令1000人每人产生一组结果同时计算骰子10次投掷结果的算数均数，把这个算数均数为$C_n$,定义变量$C_n$,绘制变量$C_n$的频率分布直方图

<img src="https://raw.githubusercontent.com/introvert24312/image/master/example%202%20of%20normal%20distribution.png" alt="example 2 of normal distribution" style="zoom: 25%;" />

<img src="https://raw.githubusercontent.com/introvert24312/image/master/example%201%20of%20normal%20distribution.png" alt="example 1 of normal distribution" style="zoom:25%;" />



### 目前我的能力限制我无法理解公式的来源，先记住它：

完成上述步骤后，高斯得到了正态分布的密度函数的标准形式：

$ f(x) = \frac{1}{\sqrt{2\pi\sigma^2}} e^{-\frac{(x-\mu)^2}{2\sigma^2}} $

在这里，$\mu$ 是误差的平均值，$\sigma^2$ 是方差，它们分别代表了测量误差的中心位置和分布的宽度。

