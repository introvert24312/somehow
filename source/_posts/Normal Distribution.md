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

正态分布的3σ（3西格玛）法则，也称为经验法则，是基于正态分布性质的一个规则，它描述了数据点分布在其平均值周围的情况。这个法则是从正态分布的数学性质中直接推导出来的。

### 正态分布的定义

首先，回顾一下正态分布的数学定义：一个随机变量 $X$ 如果服从一个均值为 $\mu$，标准差为 $\sigma$ 的正态分布，其概率密度函数（PDF）为：

$ f(x) = \frac{1}{\sigma\sqrt{2\pi}} e^{-\frac{(x-\mu)^2}{2\sigma^2}} $

### 3σ法则的来源

正态分布的一个关键特性是其对称性和特定的概率分布形状。3σ法则利用了正态分布的这些性质，具体规则如下：

- 约68.27%的数据点落在 $\mu - \sigma$ 和 $\mu + \sigma$ 之间（即平均值一个标准差内）。
- 约95.45%的数据点落在 $\mu - 2\sigma$ 和 $\mu + 2\sigma$ 之间（即平均值两个标准差内）。
- 约99.73%的数据点落在 $\mu - 3\sigma$ 和 $\mu + 3\sigma$ 之间（即平均值三个标准差内）。

### 数学推导

3σ法则的数学基础来自于正态分布的积分性质。具体地说，对正态分布的概率密度函数在特定区间内积分，可以得到数据点落在这个区间内的概率。例如，计算随机变量 $X$ 的值落在 $\mu - \sigma$ 和 $\mu + \sigma$ 之间的概率，可以通过下面的积分得到：

$ P(\mu - \sigma \leq X \leq \mu + \sigma) = \int_{\mu - \sigma}^{\mu + \sigma} \frac{1}{\sigma\sqrt{2\pi}} e^{-\frac{(x-\mu)^2}{2\sigma^2}} dx $

通过对正态分布进行积分，我们可以得到上述的概率值。实际上，这些具体的概率值（68.27%，95.45%，99.73%）来自于正态分布的累积分布函数（CDF），它提供了随机变量取值小于或等于某个值的概率。

`但数据的量化需要一个标准，于是标引入准分布，定义变量Z`

$Z = \frac{X - \mu}{\sigma}$

`绘制变量Z的频率直方图，得到标注的正态分布的曲线`

Z表如下

![z](https://raw.githubusercontent.com/introvert24312/image/master/z.png)
