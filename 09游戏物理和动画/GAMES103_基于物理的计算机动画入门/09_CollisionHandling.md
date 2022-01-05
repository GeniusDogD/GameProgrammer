# Collision Handling

![image-20220105105601924](Media/09_CollisionHandling/image-20220105105601924.png)

# **Collision Detection**

![image-20220105105801258](Media/09_CollisionHandling/image-20220105105801258.png)

广度上碰撞剔除，避免两两检测运算量过大。

精细碰撞检测

## **Spatial Partitioning**

![image-20220105110010931](Media/09_CollisionHandling/image-20220105110010931.png)

![image-20220105110100190](Media/09_CollisionHandling/image-20220105110100190.png)

![image-20220105110152142](Media/09_CollisionHandling/image-20220105110152142.png)

需要节省空白格子的内存

![image-20220105110252851](Media/09_CollisionHandling/image-20220105110252851.png)

考虑到内存访问的跨度

![image-20220105110701611](Media/09_CollisionHandling/image-20220105110701611.png)

![image-20220105110743047](Media/09_CollisionHandling/image-20220105110743047.png)

## **Bounding Volume Hierarchy**

![image-20220105110826878](Media/09_CollisionHandling/image-20220105110826878.png)

![image-20220105110937600](Media/09_CollisionHandling/image-20220105110937600.png)

![image-20220105111002012](Media/09_CollisionHandling/image-20220105111002012.png)

![image-20220105111021250](Media/09_CollisionHandling/image-20220105111021250.png)

![image-20220105111106720](Media/09_CollisionHandling/image-20220105111106720.png)

检测自相交

![image-20220105111114724](Media/09_CollisionHandling/image-20220105111114724.png)

![image-20220105111213222](Media/09_CollisionHandling/image-20220105111213222.png)

![image-20220105111502049](Media/09_CollisionHandling/image-20220105111502049.png)

![image-20220105111632202](Media/09_CollisionHandling/image-20220105111632202.png)

## **Discrete Collision Detection (DCD)** 检测相交并不是碰撞

利用最基础的边跟三角形相交检测，t 代表相交位置的插值量

![image-20220105111810025](Media/09_CollisionHandling/image-20220105111810025.png)

![image-20220105111908770](Media/09_CollisionHandling/image-20220105111908770.png)

不相交，不代表没有碰撞。

运动比较快导致穿透，大物体难触发，薄的衣服容易出现

## **Continuous Collision Detection (CCD)**

计算运动后的体积，判断是否相交。

需要解一元三次方程，有公式的解（不建议用，开 3 次根号后浮点数误差很大），用牛顿法，二分法比牛顿法更简单。

![image-20220105112026487](Media/09_CollisionHandling/image-20220105112026487.png)

![image-20220105112828707](Media/09_CollisionHandling/image-20220105112828707.png)

![image-20220105112844955](Media/09_CollisionHandling/image-20220105112844955.png)

![image-20220105113218722](Media/09_CollisionHandling/image-20220105113218722.png)

# **Interior Point Methods and Impact Zone Optimization**

内点法，外点法

![image-20220105113403974](Media/09_CollisionHandling/image-20220105113403974.png)

![image-20220105113434478](Media/09_CollisionHandling/image-20220105113434478.png)

![image-20220105150017141](Media/09_CollisionHandling/image-20220105150017141.png)

![image-20220105150039535](Media/09_CollisionHandling/image-20220105150039535.png)

![image-20220105150152852](Media/09_CollisionHandling/image-20220105150152852.png)

## **Augmented Lagrangian**

​	太复杂了不讲

## **Rigid** **Impact** **Zones**

![image-20220105150256763](Media/09_CollisionHandling/image-20220105150256763.png)

一点办法都没有搞不定的时候，就回到上一个没问题的状态

![image-20220105150402063](Media/09_CollisionHandling/image-20220105150402063.png)

# **Untangling Cloth**

## Intersection Elimination

相交解除，兜底的后续方案。用户可能非法操作拽进去了

![image-20220105150548589](Media/09_CollisionHandling/image-20220105150548589.png)

![image-20220105150635942](Media/09_CollisionHandling/image-20220105150635942.png)

![image-20220105150645202](Media/09_CollisionHandling/image-20220105150645202.png)

![image-20220105150801755](Media/09_CollisionHandling/image-20220105150801755.png)

![image-20220105150815346](Media/09_CollisionHandling/image-20220105150815346.png)

![image-20220105150855815](Media/09_CollisionHandling/image-20220105150855815.png)

# 总结

![image-20220105150900655](Media/09_CollisionHandling/image-20220105150900655.png)

碰撞检测和碰撞响应

碰撞检测：碰撞剔除，碰撞检测。

碰撞检测：离散的 DCD，连续的 CCD

连续碰撞响应： 2 种实现，内点发和外点发，保底策略

离散碰撞响应：把相交解除掉，对于有体积的物体是比较简单。布料的自碰撞比较麻烦。

