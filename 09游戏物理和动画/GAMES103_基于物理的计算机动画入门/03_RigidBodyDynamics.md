# Rigid Body Dynamics

游戏引擎都会内置，学习原理，而不是如何使用。

## **Rigid Body Simulation**

![image-20211206002835176](Media/03_RigidBodyDynamics/image-20211206002835176.png)

## **Rigid Body Motion**

刚体只有位移和旋转

![image-20211206002906519](Media/03_RigidBodyDynamics/image-20211206002906519.png)

# **Translational Motion**

![image-20211206003159776](Media/03_RigidBodyDynamics/image-20211206003159776.png)

## **Integration Methods** **Explained**

![image-20211206003218960](Media/03_RigidBodyDynamics/image-20211206003218960.png)

![image-20211206003435321](Media/03_RigidBodyDynamics/image-20211206003435321.png)

二阶精确

![image-20211206003603644](Media/03_RigidBodyDynamics/image-20211206003603644.png)

![image-20211206003738641](Media/03_RigidBodyDynamics/image-20211206003738641.png)

![image-20211206003826688](Media/03_RigidBodyDynamics/image-20211206003826688.png)

速度和位置分别是 2 只青蛙

![image-20211206003844978](Media/03_RigidBodyDynamics/image-20211206003844978.png)

## **Types of Forces** 

![image-20211206004212158](Media/03_RigidBodyDynamics/image-20211206004212158.png)

## **Rigid Body Simulation (Translation Only)**

![image-20211206004259742](Media/03_RigidBodyDynamics/image-20211206004259742.png)

# **Rotational Motion**

![image-20211206004548327](Media/03_RigidBodyDynamics/image-20211206004548327.png)

万向节锁死，时间导数不直观

![image-20211206004630272](Media/03_RigidBodyDynamics/image-20211206004630272.png)

某些情况下，自由度降低。右边出现了轴重合，只有 2 种旋转模式了。

![image-20211206195824986](Media/03_RigidBodyDynamics/image-20211206195824986.png)

## **Rotation Represented by Quaternion** 四元数

复数空间定义了加减乘除，向量只有加减。跟虚数有点像，用 4 维来表示 3 维的加减乘除

![image-20211206200147573](Media/03_RigidBodyDynamics/image-20211206200147573.png)

![image-20211206200409289](Media/03_RigidBodyDynamics/image-20211206200409289.png)

![image-20211206200531907](Media/03_RigidBodyDynamics/image-20211206200531907.png)

![image-20211206200718758](Media/03_RigidBodyDynamics/image-20211206200718758.png)

![image-20211206200855830](Media/03_RigidBodyDynamics/image-20211206200855830.png)

力矩和转动惯量

![image-20211213000800755](Media/03_RigidBodyDynamics/image-20211213000800755.png)

# **Translational and Rotational Motion**

![image-20211213001310067](Media/03_RigidBodyDynamics/image-20211213001310067.png)

![image-20211213001348720](Media/03_RigidBodyDynamics/image-20211213001348720.png)

# **Rigid Body Simulation**

![image-20211213001415867](Media/03_RigidBodyDynamics/image-20211213001415867.png)

![image-20211213002515471](Media/03_RigidBodyDynamics/image-20211213002515471.png)

实现的问题：

位移比较简单，先实现位移

先使用常数的角速度看看效果

重力不会产生任何力矩，如果不受力就不会产生角速度

![image-20211213002533124](Media/03_RigidBodyDynamics/image-20211213002533124.png)

![image-20211213002754965](Media/03_RigidBodyDynamics/image-20211213002754965.png)

https://graphics.pixar.com/pbm2001



# 补充

力矩跟力很像，是造成旋转的趋势。要考虑旋转轴，力矩的大小和夹角，作用点的距离。

![image-20211213005035290](Media/03_RigidBodyDynamics/image-20211213005035290.png)

![image-20211213004533785](Media/03_RigidBodyDynamics/image-20211213004533785.png)

左边更难旋转，右边更容易旋转。不仅跟转动惯量的大小有关，跟方向也有关。

![image-20211213005104680](Media/03_RigidBodyDynamics/image-20211213005104680.png)

当兔子发生旋转的时候，Iref 是一个常量，根据实际角度 R 矩阵来计算当前的值

![image-20211213005404852](Media/03_RigidBodyDynamics/image-20211213005404852.png)

