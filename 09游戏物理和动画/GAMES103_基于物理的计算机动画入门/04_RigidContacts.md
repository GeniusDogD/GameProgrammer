# Rigid Contacts

![image-20211213010135881](Media/04_RigidContacts/image-20211213010135881.png)

# **Particle Collision  Detection and Response**

## **Penalty Methods**

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

## **Impulse Method**

Penalty 施加力需要下一帧才生效，Impulse 是立刻生效

![image-20211213012238152](Media/04_RigidContacts/image-20211213012238152.png)

![image-20211213012255892](Media/04_RigidContacts/image-20211213012255892.png)

好处是可以精确控制，缺点是复杂麻烦



# **Rigid Body Collision Detection and Response**

