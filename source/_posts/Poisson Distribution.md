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

> 在解决问题0前，你需要意识到数学领域里的两个重要概念）[^1]
>
> 1. 数学家们将e定义为$lim_{n \to \infty}({1+\frac 1 n})^n$,就像是牛顿第一大定律，我称它为e的定义，为你无需证明它的由来，你可以认为，e是一个代表对于复利问题结果的无限正确的合理推测
> 2. 数学家们将$e^x$定义为$lim_{n \to \infty}({1+\frac x n})^n$，像是牛顿第二定律，我称它为$e^x$的定义，你同样不需要证明它的由来，你同样可以认为,$e^x$这个数学符号，代表了对于复利问题里，利率进化至x而不是1时，复利问题的结果的无限正确的合理推测

[泊松分布的推导](https://zhuanlan.zhihu.com/p/26263743)

二项分布[^2]进化至Poisson分布的关键步骤如下：

`二项分布进化至Poisson分布的过程"X"`

>$\begin{equation}\label{eq:1} =\frac{n!}{(n-k)!\times k!}\times(\frac{\lambda}{n})^{k}(1-\frac{\lambda}{n})^{n-k}\end{equation}$
>
>$\begin{equation}\label{eq:2} =\frac{n(n-1)(n-2)\ldots(n-k+1)}{n^k}\lambda^k\frac{1}{k!}(1-\frac{\lambda}{n})^{n-k}\end{equation}$
>
>$\begin{equation}\label{eq:3}
 =1(1-\frac1n)(1-\frac2n)\ldots(1-\frac{k-1}n)\lambda^k\frac1{k!}\frac{(1-\frac\lambda n)^n}{(1-\frac\lambda n)^k}
\end{equation}$

`过程"X"的推理解释部分`

>$\begin{equation}\label{4}
1(1-\frac1n)(1-\frac2n).\ldots(1-\frac{k-1}n)\to1
\end{equation}$
>
>$\begin{equation}\label{5}
(1-\frac\lambda n)^k\to1^k\to1
\end{equation}$
>
>$\begin{equation}\label{6}
(1-\frac\lambda n)^n=(1+\frac{-\lambda}n)^n\to e^{-\lambda}
\end{equation}$

`于是`

>$\begin{equation}\label{7}
=1(1-\frac1n)(1-\frac2n)\ldots(1-\frac{k-1}n)\lambda^k\frac1{k!}\frac{(1-\frac\lambda n)^n}{(1-\frac\lambda n)^k}\approx1\times\lambda^k\frac1{k!}\frac{e^{-\lambda}}{1}=\frac{\lambda^ke^{-\lambda}}{k!}
\end{equation}$

从公式推导中我们可知：

1. 从公式\ref{4}中得知，Poisson分布是二项分布以事件数趋近于无穷为背景的一个二级定理，若背景失效，Poisson分布的最终公式将无法使用
2. 从公式\ref{5}可知，若某段时间的事件发生数$\lambda$相对于$n$不再渺小，Poisson分布的最终公式依旧无法使用,
3. 从公式\ref{6}可知，若n不趋近于无穷，就无法套用$e^x$的定义对公式进行进行，若你想推测事件数k较大，这个公式同样不适用




`因此，Poisson分布的适用条件`

1. Poisson分布是二项分布模型在n趋近于无穷时的衍生

2. Pission分布是二项分布模型在事件发生概率相对于无穷的事件发生数趋近于0时的进化

`总结`

  <mark>Poisson分布时二项分布小概率无穷次的进化</mark>

### 问题0回溯
将呼叫中心接电话的情况视作Poisson分布，模型参数$\lambda=10$

模型解雇：$=\frac{10^ke^{-10}}{k!}$，其中k为事件推测发生数

[^1]:我是怎么发现的：{% post_link 常用概率模型-Poisson分布-碰到的问题 %}
[^2]:推理的基础：{% post_link 常用概率分布-二项分布 %}