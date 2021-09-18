# EndoSLAM Dataset and An Unsupervised Monocular Visual Odometry and Depth Estimation Approach for Endoscopic Videos: Endo-SfMLearner

## Note：

这篇论文主要有两个地方值得关注：1.提供了一个内窥镜SLAM的数据集，用于六自由的姿态估计和稠密三维地图重建；2.提出了一种无监督单目视觉里程计和深度估计方法：Endo-SfMLearner

目前只看了数据集的部分（2021.9.18）

## 数据集说明

### 实验装置说明

![实验装置](D:\GIT\Notes\论文1\实验装置.PNG)

a.机械臂：用来提供相机的轨迹和相机的位姿（真值）

d.实验环境：将动物器官固定在高密度泡沫上

g、h.扫描仪：用来提供器官的几何形状的真值

i：高分辨率内窥镜相机，分辨率为1280*720，帧率为20FPS

j：低分辨率内窥镜相机，分辨率为640*480，帧率为20FPS

l：Pillcam：double endoscope camera:256*256每个相机。4FPS到35FPS的可变帧率

m：MiroCam，320*329分辨率，3FPS。

数据集的体外部分共包含42700帧，具体的分类如下图所示：

![数据集说明1](D:\GIT\Notes\论文1\数据集说明1.PNG)

数据集的组织说明如下图所示：

![数据集说明](D:\GIT\Notes\论文1\数据集说明.png)

**Frames**：给定轨迹中内窥镜记录的图像

**Poses：**位姿格式为：四元数的四个参数（x,y,z,w）和三个绝对位置参数（x,y,z）,单位为米

**Calibration：**相机的内外参数校准数据

**3D-Scanners:**6个器官的重建的三维图形和点云数据

