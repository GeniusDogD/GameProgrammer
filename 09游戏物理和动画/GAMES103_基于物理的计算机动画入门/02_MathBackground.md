# Math Background: Vector, Matrix and Tensor Calculus

# Vectors 矢量

## **Vector: Definition**

印刷体区分，斜体是标量，黑体是矢量，大写黑体是矩阵。

右手坐标系：手掌从 x 到 y，大拇指指向 Z 方向。OpenGL，研究

左手坐标系：Unity，DirectX

![image-20211201145648202](Media/02_MathBackground/image-20211201145648202.png)

![image-20211201145936363](Media/02_MathBackground/image-20211201145936363.png)

Stacked Vector 没有几何含义，每个顶点都是一个向量

![image-20211201150119614](Media/02_MathBackground/image-20211201150119614.png)

## **Vector Arithematic: Addition and Subtraction**

![image-20211201152725274](Media/02_MathBackground/image-20211201152725274.png)

![image-20211201150437164](Media/02_MathBackground/image-20211201150437164.png)

## **Vector Norm**

![image-20211201151222021](Media/02_MathBackground/image-20211201151222021.png)

![image-20211201151453252](Media/02_MathBackground/image-20211201151453252.png)

## **Vector Arithematic: Dot Product** 点乘

![image-20211201151536525](Media/02_MathBackground/image-20211201151536525.png)

![image-20211201152242145](Media/02_MathBackground/image-20211201152242145.png)

![image-20211201152316767](Media/02_MathBackground/image-20211201152316767.png)

![image-20211201152451447](Media/02_MathBackground/image-20211201152451447.png)

## **Vector Arithematic: Cross Product** 叉乘

![image-20211201152739012](Media/02_MathBackground/image-20211201152739012.png)

![image-20211201152909382](Media/02_MathBackground/image-20211201152909382.png)

拓扑顺序很重要，否则会反向

![image-20211201155247794](Media/02_MathBackground/image-20211201155247794.png)

![image-20211201155353166](Media/02_MathBackground/image-20211201155353166.png)

还有其它方法，重心坐标表示的判断应该更高效。

![image-20211201155657220](Media/02_MathBackground/image-20211201155657220.png)

p 跑到外面去，就会出现负面积。利用重心权重，可以进行重心坐标插值。

![image-20211201160020359](Media/02_MathBackground/image-20211201160020359.png)

![image-20211201160334476](Media/02_MathBackground/image-20211201160334476.png)

![image-20211201162558543](Media/02_MathBackground/image-20211201162558543.png)

![image-20211201162604767](Media/02_MathBackground/image-20211201162604767.png)

本质上和平面三角形的是一样的概念，多了一个点。

![image-20211201162645441](Media/02_MathBackground/image-20211201162645441.png)

# **Matrices**

## **Matrix: Definition**

![image-20211201162856156](Media/02_MathBackground/image-20211201162856156.png)

## **Matrix: Multiplication**

![image-20211201163111034](Media/02_MathBackground/image-20211201163111034.png)

## **Matrix: Orthogonality**

![image-20211201163348849](Media/02_MathBackground/image-20211201163348849.png)

## **Matrix Transformation**

![image-20211201163706992](Media/02_MathBackground/image-20211201163706992.png)

![image-20211201163737625](Media/02_MathBackground/image-20211201163737625.png)

## **Singular Value Decomposition** 奇异值分解

![image-20211201164518757](Media/02_MathBackground/image-20211201164518757.png)

线性变换，可以通过 `旋转-缩放-旋转 `得到

## **Eigenvalue Decomposition** 特征值分解

对称矩阵

![image-20211201164913809](Media/02_MathBackground/image-20211201164913809.png)

对称且正定

![image-20211201170534917](Media/02_MathBackground/image-20211201170534917.png)

通过数值计算特征值分解是很慢的，实际使用。（没有概念有点懵）

![image-20211205230128568](Media/02_MathBackground/image-20211205230128568.png)

![image-20211205230617624](Media/02_MathBackground/image-20211205230617624.png)

# **Linear Solver** 线性问题

很多数值问题最后就是解线性方程

不直接求逆，一般用直接法和迭代法

![image-20211205231203637](Media/02_MathBackground/image-20211205231203637.png)

## **Direct Linear Solver**

LU 分解

![image-20211205231429783](Media/02_MathBackground/image-20211205231429783.png)

![image-20211205231526601](Media/02_MathBackground/image-20211205231526601.png)

## **Iterative Linear Solver** 迭代法

数值分析

![ ](Media/02_MathBackground/image-20211205232714885.png)

直接法可能要写几周，迭代法一天就够了。迭代法比较容易并行，缺点：收敛性问题。relaxation 手动调

![image-20211205234040992](Media/02_MathBackground/image-20211205234040992.png)

# **Tensor Calculus**

![image-20211206000635342](Media/02_MathBackground/image-20211206000635342.png)

![image-20211206000931896](Media/02_MathBackground/image-20211206000931896.png)

![image-20211206001115665](Media/02_MathBackground/image-20211206001115665.png)

前面讲的正定，跟函数的二阶导数有关系

![image-20211206001459166](Media/02_MathBackground/image-20211206001459166.png)

![image-20211206001614414](Media/02_MathBackground/image-20211206001614414.png)

![image-20211206001750316](Media/02_MathBackground/image-20211206001750316.png)

![image-20211206002307134](Media/02_MathBackground/image-20211206002307134.png)

