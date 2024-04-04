---
title: 卫生统计学思维导图
date: 2024-10-10 12:50:00
tags: 统计学
categories: 卫生统计学
mathjax: true
---

```mermaid
graph TD;
subgraph 分布类型
0[Binomial Distribution]-->|事件的结果>2|00[多项分布]

0-->|当n趋近无穷,p较小|1[Possion分布]

2[Normal Distribution];

2-->21[but i don't how]
2-->22[中心极限定理]
end

click 0 "https://ysz.asia/2024/03/14/Binomial%20Distribution/"
click 00 "https://ysz.asia/2024/03/14/Binomial%20Distribution/"
click 1 "https://ysz.asia/2024/03/16/Poisson%20Distribution/"
click 2 "https://ysz.asia/2024/03/24/Normal%20Distribution/"
click 22 "https://ysz.asia/2024/03/24/Normal%20Distribution/"

```

```mermaid
graph TD;
subgraph 统计推断
1[参数估计]-->1a[点估计]
1-->1b[区间估计]
2[假设检验]-->2a[t检验]
end
click 1a "https://ysz.asia/2024/10/10/interval%20estimation/"
click 1b "https://ysz.asia/2024/10/10/interval%20estimation/"
click 2 "https://ysz.asia/2024/04/04/hypothesis%20testing/"


```

