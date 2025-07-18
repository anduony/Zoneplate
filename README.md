## Zoneplate 网页版编写说明
本Zoneplate Html代码是根据https://github.com/mathworks/zone-plate-test-image 中的matlab代码更改而来，目的主要是为了实现在线上直接制作各种分辨率BMP格式的照片用与评测屏幕性能。
可以最大生成5000*5000的分辨率。
![](https://github.com/anduony/Zoneplate/blob/main/ZonePlate-501x501.bmp)

网页界面如下（可以根据需求生成自己需要的尺寸）
![](https://github.com/anduony/Zoneplate/blob/main/%E7%BD%91%E9%A1%B5%E7%95%8C%E9%9D%A2.png)

### 什么是ZonePlate图像？
ZonePlate图像（波带片图像）是一种专业的测试图像，它具有特殊的径向对称结构，在图像中心和边缘具有截然不同的频率特性。这种图像的核心特征在于其频率随着与图像中心距离的增加而线性增加。

#### 数学定义
ZonePlate图像由以下数学公式定义：

g(x,y) = sin( (kₘ * r²) / (2 * rₘ) ) * [0.5 * tanh((rₘ - r)/w) + 0.5]
其中：

r = √(x² + y²) - 像素到图像中心的距离
kₘ - 最大频率参数（通常为0.7π）
rₘ - 图像的有效最大半径
w - 边缘平滑宽度（通常为rₘ/10）


#### 物理意义
ZonePlate图像模拟了光学中的菲涅尔波带片(Fresnel zone plate)概念。在光学领域，波带片是一种衍射光学元件，它可以通过衍射效应而不是折射或反射来聚焦光线。这种结构具有以下特点：

​空间频率变化​：图像中的条纹从中心到边缘由稀疏变得密集
​正弦波动特性​：亮度值按正弦函数变化，与理想光学波动一致
​径向分布​：条纹沿径向分布而非线性分布

