---
title: 假设检验
date: 2024-4-4 13:50:00
tags: 统计学
categories: 卫生统计学
mathjax: true
---

# 假设检验是干什么的？

例如：



零假设的统计量落在对应分布表里的一个边缘区间内，且这个边缘区间的概率为0.00001，那么意味着这个样本的统计量是一个个例，进行多次抽样后 ，出现这样的结果的概率很小很小

于是，这就称为了你拒绝0假设的证据

例如：这是一个用于判断两个独立样本的均值是否有明显差异的公式（用在样本量大于30、50的时候）

$$
z = \frac{\overline{X}_1 - \overline{X}_2}{\sqrt{\frac{\sigma_1^2}{n_1} + \frac{\sigma_2^2}{n_2}}}
$$

当然，数学家们通过数学推导确定了它服从某个分布（自由度为$\infty$的t分布—即正态分布）

> 因为正态分布的和与差均为正态分布

若z趋近于0，那么两样本的均值可认为没有差异，若z较大或较小，那么认为均值有显著差异（p小于0.05）

Z值服从的分布：

![独立样本z值的分布图](https://raw.githubusercontent.com/introvert24312/image/master/独立样本z值的分布图.png)

两样本A、B来源的变量：

![两服从正态分布的变量分布图](https://raw.githubusercontent.com/introvert24312/image/master/两服从正态分布的变量分布图.png)

# 假阳性错误与假阴性错误

Error I：报警器响了，小偷却没进你家

Error II：报警器没响，小偷却进入你家了