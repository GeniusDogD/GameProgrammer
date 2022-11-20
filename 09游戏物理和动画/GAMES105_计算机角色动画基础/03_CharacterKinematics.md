# Character Kinematics: Forward and Inverse Kinematics





# Kinematics of a Chain

![image-20221120212912881](Media/03_CharacterKinematics/image-20221120212912881.png)

![image-20221120213256658](Media/03_CharacterKinematics/image-20221120213256658.png)

![image-20221120213430292](Media/03_CharacterKinematics/image-20221120213430292.png)

![image-20221120213620827](Media/03_CharacterKinematics/image-20221120213620827.png)

![image-20221120213640085](Media/03_CharacterKinematics/image-20221120213640085.png)

![image-20221120213719364](Media/03_CharacterKinematics/image-20221120213719364.png)

![image-20221120213924800](Media/03_CharacterKinematics/image-20221120213924800.png)

![image-20221120214000578](Media/03_CharacterKinematics/image-20221120214000578.png)

![image-20221120214015975](Media/03_CharacterKinematics/image-20221120214015975.png)



# Kinematics of a Character

![image-20221120214125687](Media/03_CharacterKinematics/image-20221120214125687.png)

![image-20221120214209669](Media/03_CharacterKinematics/image-20221120214209669.png)

![image-20221120214226483](Media/03_CharacterKinematics/image-20221120214226483.png)

![image-20221120214359978](Media/03_CharacterKinematics/image-20221120214359978.png)

![image-20221120214442951](Media/03_CharacterKinematics/image-20221120214442951.png)



![image-20221120214601637](Media/03_CharacterKinematics/image-20221120214601637.png)

![image-20221120214638822](Media/03_CharacterKinematics/image-20221120214638822.png)

![image-20221120214812787](Media/03_CharacterKinematics/image-20221120214812787.png)

![image-20221120214834368](Media/03_CharacterKinematics/image-20221120214834368.png)

![image-20221120214910393](Media/03_CharacterKinematics/image-20221120214910393.png)

https://research.cs.wisc.edu/graphics/Courses/cs-838-1999/Jeff/BVH.html





# Inverse Kinematics

![image-20221120220900792](Media/03_CharacterKinematics/image-20221120220900792.png)

![image-20221120221009843](Media/03_CharacterKinematics/image-20221120221009843.png)

![image-20221120221131936](Media/03_CharacterKinematics/image-20221120221131936.png)

![image-20221120221147308](Media/03_CharacterKinematics/image-20221120221147308.png)

![image-20221120221203509](Media/03_CharacterKinematics/image-20221120221203509.png)

![image-20221120221222052](Media/03_CharacterKinematics/image-20221120221222052.png)

![image-20221120221334339](Media/03_CharacterKinematics/image-20221120221334339.png)

![image-20221120221347298](Media/03_CharacterKinematics/image-20221120221347298.png)

![image-20221120221355582](Media/03_CharacterKinematics/image-20221120221355582.png)

![image-20221120221424878](Media/03_CharacterKinematics/image-20221120221424878.png)

![image-20221120221522645](Media/03_CharacterKinematics/image-20221120221522645.png)

![image-20221120221532834](Media/03_CharacterKinematics/image-20221120221532834.png)

![image-20221120221540158](Media/03_CharacterKinematics/image-20221120221540158.png)

![image-20221120221601008](Media/03_CharacterKinematics/image-20221120221601008.png)

![image-20221120221650330](Media/03_CharacterKinematics/image-20221120221650330.png)

![image-20221120221659570](Media/03_CharacterKinematics/image-20221120221659570.png)

![image-20221120221813000](Media/03_CharacterKinematics/image-20221120221813000.png)

![image-20221120221902992](Media/03_CharacterKinematics/image-20221120221902992.png)

![image-20221120221947830](Media/03_CharacterKinematics/image-20221120221947830.png)

![image-20221120222008878](Media/03_CharacterKinematics/image-20221120222008878.png)

![image-20221120222112350](Media/03_CharacterKinematics/image-20221120222112350.png)

## 梯度

![image-20221120222143437](Media/03_CharacterKinematics/image-20221120222143437.png)

![image-20221120222203167](Media/03_CharacterKinematics/image-20221120222203167.png)



![image-20221120222245782](Media/03_CharacterKinematics/image-20221120222245782.png)

![image-20221120222307135](Media/03_CharacterKinematics/image-20221120222307135.png)

## Jacobian Transpose

![image-20221120222329451](Media/03_CharacterKinematics/image-20221120222329451.png)

![image-20221120222357283](Media/03_CharacterKinematics/image-20221120222357283.png)

![image-20221120222516126](Media/03_CharacterKinematics/image-20221120222516126.png)

![image-20221120222601165](Media/03_CharacterKinematics/image-20221120222601165.png)

![image-20221120222648336](Media/03_CharacterKinematics/image-20221120222648336.png)

![image-20221120222727967](Media/03_CharacterKinematics/image-20221120222727967.png)

![image-20221120222815417](Media/03_CharacterKinematics/image-20221120222815417.png)

![image-20221120222826343](Media/03_CharacterKinematics/image-20221120222826343.png)

![image-20221120223031635](Media/03_CharacterKinematics/image-20221120223031635.png)

![image-20221120223053995](Media/03_CharacterKinematics/image-20221120223053995.png)

### 收敛速度比 CCD 快，但是每次都要计算 J 贾可比矩阵，计算量爆炸



## 优化

![image-20221120223254889](Media/03_CharacterKinematics/image-20221120223254889.png)

![image-20221120223324549](Media/03_CharacterKinematics/image-20221120223324549.png)

![image-20221120223351853](Media/03_CharacterKinematics/image-20221120223351853.png)

![image-20221120223412196](Media/03_CharacterKinematics/image-20221120223412196.png)

![image-20221120223436624](Media/03_CharacterKinematics/image-20221120223436624.png)

![image-20221120223545163](Media/03_CharacterKinematics/image-20221120223545163.png)

![image-20221120223614869](Media/03_CharacterKinematics/image-20221120223614869.png)

![image-20221120223658765](Media/03_CharacterKinematics/image-20221120223658765.png)

![image-20221120223834170](Media/03_CharacterKinematics/image-20221120223834170.png)

![image-20221120223844009](Media/03_CharacterKinematics/image-20221120223844009.png)

![image-20221120223918993](Media/03_CharacterKinematics/image-20221120223918993.png)

![image-20221120223936743](Media/03_CharacterKinematics/image-20221120223936743.png)



![image-20221120224026777](Media/03_CharacterKinematics/image-20221120224026777.png)

![image-20221120224054034](Media/03_CharacterKinematics/image-20221120224054034.png)

![image-20221120224105052](Media/03_CharacterKinematics/image-20221120224105052.png)



![image-20221120224150146](Media/03_CharacterKinematics/image-20221120224150146.png)





![image-20221120224247783](Media/03_CharacterKinematics/image-20221120224247783.png)

![image-20221120224327146](Media/03_CharacterKinematics/image-20221120224327146.png)

### 用权重来控制，不同关节的旋转程度

![image-20221120224405690](Media/03_CharacterKinematics/image-20221120224405690.png)

![image-20221120224556899](Media/03_CharacterKinematics/image-20221120224556899.png)



# 总结

![image-20221120224637728](Media/03_CharacterKinematics/image-20221120224637728.png)