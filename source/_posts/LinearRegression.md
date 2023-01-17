---
title: 线性回归模型
date: 2023/1/16
updated: 2023/1/16
tags:
- Linear Regression
- Mathematical Modeling
categories: 
- Mathematical Modeling
math: true 
index_img: /picture/LinearRegression/844px-Linear_least_squares.svg.png
banner_img: /picture/LinearRegression/844px-Linear_least_squares.svg.png
excerpt: 线性回归（Linear regression）是利用称为线性回归方程的最小二乘函数对一个或多个自变量和因变量之间关系进行建模的一种回归分析。
---

# 1  什么是线性回归

定义：线性回归是利用**回归方程**对一个或多个自变量和因变量之间关系进行建模的一种分析方式。

简而言之，已有线性回归的回归方程，利用**已知的多个实际输入以及对应的实际输出**，调整回归方程的参数，找到对已知数据来说最好的回归方程，就是做线性回归。

![](/picture/LinearRegression/844px-Linear_least_squares.svg.png)

**注意：每个红点代表一对实际输入和实际输出，蓝线是找到的最好的线性回归方程。**

# 2  一维线性回归

模型：
$$
y=\alpha+\beta x+\epsilon
$$
其中：
$$
\epsilon\sim N(0,\sigma^2)
$$
有一组观测值：
$$
(x_i,y_i),i=1,2,...,n
$$
满足：
$$
y_i=\alpha+\beta x_i+\epsilon_i
$$
其中：
$$
\epsilon_i相互独立，且\epsilon_i\sim N(0,\sigma^2),i=1,2,...,n
$$
目标函数：
$$
\sum_{i=1}^n(y_i-\hat{\alpha}-\hat{\beta}x_i)^2=\min_{\alpha,\beta}\sum_{i=1}^{n}(y_i-\alpha-\beta x_i)^2
$$
**注：变量上加个帽子表示的是预测值，线性回归的目标是找到满足目标函数的最好的预测值。**
