---
layout:     post
title:      "计算机图形学实验一：Stickman"
subtitle:   "Paranoid Android"
date:       2017-03-31 
author:     "WangXingyu"
header-img: "img/ball.png"
catalog: true
tags:
    - Computer Graphics 
    

---

这次实验的任务是做一个可以动的人，也就是所谓的stickman。
配置实验环境对于做过好几门课程实验的我们来说已经不是什么难事了，我也相应地把Visual Studio和Codeblocks的环境也调试好了。图形库选择的是传统的openGL，主要考虑的是网上的教程更多一些。
这次实验的目的是让我们熟悉一种图形库的使用，理解图形学中变换(transformation)的原理。
我的思路是先把组成人体的各个部件画出来，然后通过旋转和平移变换让人动起来。

最后的效果如下图所示：

![img](/img/in-post/paranoid.gif)





