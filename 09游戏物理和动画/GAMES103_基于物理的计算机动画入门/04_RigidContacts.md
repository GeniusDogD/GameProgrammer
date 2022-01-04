# Rigid Contacts

![image-20211213010135881](Media/04_RigidContacts/image-20211213010135881.png)

# **Particle Collision  Detection and Response**

## **Penalty Methods**（惩罚）

![image-20211213010238319](Media/04_RigidContacts/image-20211213010238319.png)

![image-20211213010425248](Media/04_RigidContacts/image-20211213010425248.png)

![image-20211213010653233](Media/04_RigidContacts/image-20211213010653233.png)

![image-20211213010707272](Media/04_RigidContacts/image-20211213010707272.png)

![image-20211213011540478](Media/04_RigidContacts/image-20211213011540478.png)

k 太小会穿模，k 太大会弹飞

![image-20211213011640889](Media/04_RigidContacts/image-20211213011640889.png)

k 也跟距离有关，利用小步长来避免穿透

![image-20211213011852082](Media/04_RigidContacts/image-20211213011852082.png)

![image-20211213011903622](Media/04_RigidContacts/image-20211213011903622.png)

## **Impulse Method** (冲动)

Penalty 施加力需要下一帧才生效，Impulse 是立刻生效

![image-20211213012238152](Media/04_RigidContacts/image-20211213012238152.png)

![image-20211213012255892](Media/04_RigidContacts/image-20211213012255892.png)

好处是可以精确控制（摩擦力），缺点是复杂麻烦。

刚体用 Impulse 方法比较多，衣服用 Penalty 方法较多



# **Rigid Body Collision Detection and Response**

![image-20220104152039822](Media/04_RigidContacts/image-20220104152039822.png)

![image-20220104152048311](Media/04_RigidContacts/image-20220104152048311.png)

![image-20220104152158566](Media/04_RigidContacts/image-20220104152158566.png)

只想改速度，直接改位置比较困难。

![image-20220104152247772](Media/04_RigidContacts/image-20220104152247772.png)

![image-20220104152502291](Media/04_RigidContacts/image-20220104152502291.png)

![image-20220104152540262](Media/04_RigidContacts/image-20220104152540262.png)

算法过程，判断单个质点是否碰撞以及速度方向。灰色表示中间变量，实际不存在，用冲量去更新。新的冲量跟 Vi_new 是线性关系，得到冲量后更新整体的 v 和 w

![image-20220104153226935](Media/04_RigidContacts/image-20220104153226935.png)

![image-20220104153725096](Media/04_RigidContacts/image-20220104153725096.png)

多个点取平均值，出现抖动需要特殊处理衰减，更新位置是非线性问题。

![image-20220104153859150](Media/04_RigidContacts/image-20220104153859150.png)

https://graphics.pixar.com/pbm2001

![image-20220104153919774](Media/04_RigidContacts/image-20220104153919774.png)

# **Shape Matching**

![image-20220104153938313](Media/04_RigidContacts/image-20220104153938313.png)

先让每个质点都 Impulse 自己动，最后再聚回一个刚体

 

![image-20220104154218224](Media/04_RigidContacts/image-20220104154218224.png)

![image-20220104154414844](Media/04_RigidContacts/image-20220104154414844.png)

![image-20220104154531237](Media/04_RigidContacts/image-20220104154531237.png)

![image-20220104154546007](Media/04_RigidContacts/image-20220104154546007.png)

![image-20220104154627014](Media/04_RigidContacts/image-20220104154627014.png)

![image-20220104154652642](Media/04_RigidContacts/image-20220104154652642.png)

![image-20220104155047585](Media/04_RigidContacts/image-20220104155047585.png)

优点：没有物理运算在里面，容易模拟衣服和软体

缺点：很难保证约束，同时满足约束（可能需要迭代），适合摩擦力精确度不高的场合

![image-20220104155246460](Media/04_RigidContacts/image-20220104155246460.png)
