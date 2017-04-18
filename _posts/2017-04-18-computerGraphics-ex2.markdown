---
layout:     post
title:      "Experiment2: RayTracing"
subtitle:   "Shading of sphere"
date:       2017-04-18 
author:     "WangXingyu"
header-img: "img/ball.png"
catalog: true
tags:
    - Computer Graphics 
    

---

这次实验的任务是实现光线追踪（RayTracing）算法，要求至少使用两种不同的光照模型。这里我使用的是phong和blinn-phong模型。
phong模型课上讲得已经比较清楚，利用光的反射原理求出反射光的向量，以入射光和法线为已知量；
![img](/img/in-post/cg-ex2-phong-model.png)
而blinn-phong模型则是利用了入射光和观察者方向计算的中间向量H：
![img](/img/in-post/cg-ex2-blinn-phong-model.png)
其他的部分二者基本相同，都是对顶点的法向量进行计算后对平面上任意点的法向量计算，进而求出每个像素的颜色。
最终的效果如下图所示：
![img](/img/in-post/cg-ex2-phong.png)
![img](/img/in-post/cg-ex2-blinn-phong.png)




