---
layout:     post
title:      "Experiment1:Stickman"
subtitle:   "Paranoid Android"
date:       2017-03-31 
author:     "WangXingyu"
header-img: "img/ball.png"
catalog: true
tags:
    - Computer Graphics 
    

---

这次实验的目的是让我们熟悉一种图形库的使用，并掌握变换(transformation)的实际意义。
实验思路是把组成stickman的每个元素画出来，通过平移和旋转组成一个整体。手臂和腿的运动是循环往复的，靠的就是设计的阈值，当转动角度达到阈值时运动反向且速度不变。
人的平移采用了比较简单的视角平移，设置了几个特殊键，当触发这些特殊键时就会做出相应的动作。
最后的效果如下图所示：
![img](/img/in-post/paranoid.gif)



