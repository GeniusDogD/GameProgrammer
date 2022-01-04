# Physics-Based Cloth Simulation

![image-20220104155505876](Media/05_PhysicsBasedClothSimulation/image-20220104155505876.png)

弹簧质点系统：显示积分，隐式积分

弯曲问题

非弹簧的方式

# **A Mass Spring System**

![image-20220104161216322](Media/05_PhysicsBasedClothSimulation/image-20220104161216322.png)

![image-20220104161422562](Media/05_PhysicsBasedClothSimulation/image-20220104161422562.png)

![image-20220104161551379](Media/05_PhysicsBasedClothSimulation/image-20220104161551379.png)

![image-20220104161738206](Media/05_PhysicsBasedClothSimulation/image-20220104161738206.png)

![image-20220104161845128](Media/05_PhysicsBasedClothSimulation/image-20220104161845128.png)

![](Media/05_PhysicsBasedClothSimulation/image-20220104161850778.png)

排序后，检测重复，并剔除内部边

![image-20220104161922358](Media/05_PhysicsBasedClothSimulation/image-20220104161922358.png)

# **Explicit Integration of A Mass-Spring System** 显式

![image-20220104162620669](Media/05_PhysicsBasedClothSimulation/image-20220104162620669.png)

缺点：数值不稳定，K 很大或者 时间步长很大的时候。隐式积分通过误差衰减的方式来解决。

![image-20220104162724470](Media/05_PhysicsBasedClothSimulation/image-20220104162724470.png)

![image-20220104163416649](Media/05_PhysicsBasedClothSimulation/image-20220104163416649.png)

隐式积分，消元反推，只跟位置相关。力 f 可能不是线性的，转化为优化问题，利用已有的数值套路。采用了能量优化，而不是解放城组的方法。

![image-20220104163827197](Media/05_PhysicsBasedClothSimulation/image-20220104163827197.png)

牛顿法，解非线性优化问题。牛顿法求根类似

![image-20220104164819791](Media/05_PhysicsBasedClothSimulation/image-20220104164819791.png)

![](Media/05_PhysicsBasedClothSimulation/image-20220104165708347.png)

用二阶导数判定开口方向，确定是最大值还是最小值。只能达到局部最优，增加随机扰动。

二阶导数永远大于 0 的话，不存在最大值，就只有一个最小值。

![image-20220104165936865](Media/05_PhysicsBasedClothSimulation/image-20220104165936865.png)

![image-20220104170052876](Media/05_PhysicsBasedClothSimulation/image-20220104170052876.png)

Hessian 二阶导数矩阵，类似拉普拉斯算子。为何讨论是否正定？实数函数如果二阶导数永远为正的话，存在唯一解。

![image-20220104170427835](Media/05_PhysicsBasedClothSimulation/image-20220104170427835.png)

如果 Hessian 永远正定，就有唯一解。不正定的时候，未必没有唯一解。

充分不必要条件

拉伸的时候会稳定很多，压缩的时候容易出问题（非正定）。

![image-20220104171123257](Media/05_PhysicsBasedClothSimulation/image-20220104171123257.png)

压缩的时候非正定，因为不清楚会往哪边翘起。1D  没这个问题，2D 和 3D 有

![image-20220104171311138](Media/05_PhysicsBasedClothSimulation/image-20220104171311138.png)

![image-20220104171428280](Media/05_PhysicsBasedClothSimulation/image-20220104171428280.png)

​	Choi and Ko. 2002. Stable But Responive Cloth. TOG (SIGGRAPH)

![image-20220104171501267](Media/05_PhysicsBasedClothSimulation/image-20220104171501267.png)

![image-20220104171600756](Media/05_PhysicsBasedClothSimulation/image-20220104171600756.png)

直接法和迭代法的区别，除了运算量还有内存量的问题。

![image-20220104171712201](Media/05_PhysicsBasedClothSimulation/image-20220104171712201.png)

![image-20220104171656479](Media/05_PhysicsBasedClothSimulation/image-20220104171656479.png)

等价于只做一次牛顿迭代

# **Bending and Locking Issues** 

![image-20220104192228157](Media/05_PhysicsBasedClothSimulation/image-20220104192228157.png)

二面角模型，拆成方向和大小

![image-20220104192332036](Media/05_PhysicsBasedClothSimulation/image-20220104192332036.png)

![image-20220104192624567](Media/05_PhysicsBasedClothSimulation/image-20220104192624567.png)

![image-20220104192651357](Media/05_PhysicsBasedClothSimulation/image-20220104192651357.png)

![image-20220104192821547](Media/05_PhysicsBasedClothSimulation/image-20220104192821547.png)

可以从头到尾读一下，比较有意思

# **A Quadratic Bending Model**

![image-20220104193137914](Media/05_PhysicsBasedClothSimulation/image-20220104193137914.png)

能量跟曲率有关，平的时候能量为 0。不是物理能量推导，数学拉普拉斯算子曲率。

![image-20220104194627852](Media/05_PhysicsBasedClothSimulation/image-20220104194627852.png)

![image-20220104194712163](Media/05_PhysicsBasedClothSimulation/image-20220104194712163.png)

# **The Locking Issue**

![image-20220104194913491](Media/05_PhysicsBasedClothSimulation/image-20220104194913491.png)

![image-20220104195010720](Media/05_PhysicsBasedClothSimulation/image-20220104195010720.png)

paper 把自由度定义到边上，更复杂了

# **Shape Matching**