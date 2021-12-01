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
