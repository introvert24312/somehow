---
title: 常用概率模型-Poisson分布
date: 2024-03-16 00:55:50
tags: 统计学
categories: 卫生统计学
mathjax: true
---

## 引入

让我们通过一个具体的问题来深入理解泊松分布：

### 问题0

假设你管理着一个小型的呼叫中心。经过长时间的记录，你发现该中心平均每小时接到10个电话。使用泊松分布，我们想计算在下一个小时内接到不同数量电话的概率。

> 在解决问题0前，你需要意识到数学领域里的两个重要概念[^1]
>
> 1. 数学家们将e定义为$lim_{n \to \infty}({1+\frac 1 n})^n$,就像是牛顿第一大定律，我称它为e的定义，为你无需证明它的由来，你可以认为，e是一个代表对于复利问题结果的无限正确的合理推测
> 2. 数学家们将$e^x$定义为$lim_{n \to \infty}({1+\frac x n})^n$，像是牛顿第二定律，我称它为$e^x$的定义，你同样不需要证明它的由来，你同样可以认为,$e^x$这个数学符号，代表了对于复利问题里，利率进化至x而不是1时，复利问题的结果的无限正确的合理推测

[泊松分布的推导](https://zhuanlan.zhihu.com/p/26263743)

二项分布进化至Possion分布的关键步骤如下：

$\begin{equation}\label{eq:stand} =\frac{n!}{(n-k)!\times k!}\times(\frac{\lambda}{n})^{k}(1-\frac{\lambda}{n})^{n-k}\end{equation}$

$\begin{equation}\label{eq:step 2} =\frac{n(n-1)(n-2)\ldots(n-k+1)}{n^k}\lambda^k\frac{1}{k!}(1-\frac{\lambda}{n})^{n-k}\end{equation}$

$\begin{equation}\label{eq:save}
 =\frac{n!}{(n-k)!\times k!}\times\left(\frac{\lambda}{n}\right)^{k}\left(1-\frac{\lambda}{n}\right)^{n-k}
\end{equation}$

Possion分布是二项分布模型在n趋近于无穷时的衍生

[^1]:我是怎么发现的：{% post_link 常用概率模型-Poisson分布-碰到的问题 %}