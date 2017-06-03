---
layout:     post
title:      "Experiment3: RayTracing II"
subtitle:   "RayTracing in C++: Parameter Matters"
date:       2017-06-03 
author:     "WangXingyu"
header-img: "img/ball.png"
catalog: true
tags:
    - Computer Graphics 
    

---

　　这次实验的任务跟上次差不多，只是因为上次实验大部分人没有实现raytracing而只实现了光照模型，所以这次实验就显得比较尴尬。于是我只能再实现一个c++版本的光线追踪，这次的重点放在参数对图像的影响上。


　　#1.环境光系数对图像的影响

　　环境光系数在代码中是以正比例的方式体现的，即系数越大，物体受到的光越强。
![img](/img/in-post/cg-ex3/1(ambient light factor=0.1).png)
![img](/img/in-post/cg-ex3/1(ambient light factor=0.3).png)
![img](/img/in-post/cg-ex3/1(ambient light factor=0.5).png)

　　#2.最大反射次数对图像的影响

　　为了保证程序运行的时间在可以接受的范围内，必须设置一个最大反射次数，而这个值也直接影响到图像的真实感。
![img](/img/in-post/cg-ex3/2(maximum reflection=1).png)
![img](/img/in-post/cg-ex3/2(maximum reflection=3).png)
![img](/img/in-post/cg-ex3/2(maximum reflection=5).png)

　　可以看出，最大反射次数设置为3与5的效果差距不大，而与1的效果差距较大。

　　#3.超采样系数对图像的影响

　　超采样的原理很简单，就是通过生成一个比原始图像大n倍的图像，再压缩到原来的大小。这种方法生成的图像质量较高，但相应的代价也很大。

![img](/img/in-post/cg-ex3/5(supersampling factor=1).png)
![img](/img/in-post/cg-ex3/5(supersampling factor=4).png)
![img](/img/in-post/cg-ex3/5(supersampling factor=16).png)

　　用肉眼基本看不出这几幅图像的差别，我们借助DiffImg工具查看一下：

![img](/img/in-post/cg-ex3/diff.png)

　　黄点代表差异像素，我们发现集中在中间这个半透明的球以及它在其他三个球的投影上。

　　经过一番参数的调整，最后的结果如下图所示：

![img](/img/in-post/cg-ex3/final.png)







