[toc]

# 第九章 重积分

## 第1节 曲顶柱体的体积

### 一、实例

==平面区域直径==：区域$\sigma$上任意两端距离最大值。

### 二、二重积分的定义

设函数$f(x, y)$是定义在平面有界闭区域$D$上的有界函数，如果$\lim_{\lambda \to 0}\sum_i^n f(\xi_i, \eta_i)\Delta\sigma_i$存在（则称$f(x, y)$在$D$上可积），极限值为$I$，且$I$的值与对$D$的分法无关，也与$N_i(\xi_i, \eta_i)$在$\sigma_i$上的取法无关，则称$I$为$f(x, y)$在有界闭区域$D$上的二重积分。记为$\iint_{D} f(x, y)d\sigma$。其中$f(x, y)$称为被积函数，$D$称为积分区域，$d\sigma$称为面积元素，$f(x, y)d\sigma$称为被积表达式。

### 三、二重积分的性质

6. ==中值定理==：设$f(x, y)$在有界闭区域$D$上连续，$S$表示$D$的面积，则至少存在一点$(\xi, \eta) \in D$ 使得$\iint_D f(x, y)d\sigma = f(\xi, \eta)S$。



## 第2节 二重积分的计算

### 一、在直角坐标系下

==简单区域==：平行于$x$轴或$y$轴的直线与区域$D$的边界的交点不多于两个。

==X型区域==：与$y$轴平行的直线与$D$的边界交点不多于两个。$\iint_D f(x,y)d\sigma = \int_a^b dx \int_c^d f(x, y)dy$

==Y型区域==：与$x$轴平行的直线与$D$的边界交点不多于两个。$\iint_D f(x,y)d\sigma = \int_c^d dy \int_a^b f(x, y)dx$

若区域$D$是简单区域，则将积分化成两次单积分进行求解；若区域$D$不是简单区域，利用平行于$y$轴或$x$轴的直线把$D$分为若干个简单区域$D_1, D_2, \cdots, D_n$再分别求解，最后相加。

二重积分$\iint_D f(x, y)d\sigma = \iint_D f(x, y)dxdy$

### 二、在极坐标系下

1. 二重积分由直角坐标变换为极坐标的变换公式：

   假设有界闭区域$D$满足：从极点出发的半直线与$D$的边界的交点不多于两个。

   $\iint_D f(x, y)d\sigma = \lim_{\lambda \to 0}\sum_{i=1}^n f(x_i, y_i)\Delta \sigma_i \\ = \lim_{\lambda \to 0}\sum_{i=1}^n f(\rho_i\cos\theta_i, \rho_i\sin\theta_i)\rho_i \Delta\rho_i\Delta\theta_i \\ = \iint_D f(\rho\cos\theta, \rho\sin\theta)\rho d\rho d\theta$

2. 极坐标系下的累次积分

   假设有界闭区域$D$满足：从极点出发的半直线与$D$的边界的交点不多于两个。

   （1）极点$O$在积分区域外部

   $D = \{(\rho, \theta) | \rho_1(\theta) \le \rho \le \rho_2(\theta), \alpha \le \theta \le \beta\}$

   $\iint_D f(\rho\cos\theta, \rho\sin\theta)\rho d\rho d\theta = \int_\alpha^\beta d\theta \int_{\rho_1(\theta)}^{\rho_2(\theta)} f(\rho\cos\theta, \rho\sin\theta)\rho d\rho$

   

   （2）极点$O$在积分区域边界上

   $D = \{(\rho, \theta) | 0 \le \rho \le \rho(\theta), \alpha \le \theta \le \beta\}$

    $\iint_D f(\rho\cos\theta, \rho\sin\theta)\rho d\rho d\theta = \int_\alpha^\beta d\theta \int_0^{\rho(\theta)} f(\rho\cos\theta, \rho\sin\theta)\rho d\rho$

   （3）极点$O$在积分区域内部

   $D = \{(\rho, \theta) | 0 \le \rho \le \rho(\theta), 0 \le \theta \le 2\pi\}$

   $\iint_D f(\rho\cos\theta, \rho\sin\theta)\rho d\rho d\theta = \int_0^{2\pi} d\theta \int_0^{\rho(\theta)} f(\rho\cos\theta, \rho\sin\theta)\rho d\rho$

例：计算$\int_0^{+\infty}e^{-x^2}dx$。

构造两个圆域和一个矩形域，分别记为$D_1, D_2, S$，利用夹逼准则，求出极限为$\frac{\sqrt{\pi}}{2}$。

$\iint_S e^{-x^2-y^2}dxdy = \int_0^R e^{-x^2}dx \int_0^R e^{-y^2}dy = (\int_0^R e^{-x^2}dx)^2$



### 第3节 三重积分

仿照二重积分的定义，把面积元素换成体积元素即可定义三重积分。记为$\iiint_{\Omega} f(x, y, z)dv$。



### 第4节 三重积分的计算

### 一、直角坐标系下

设平行于$z$轴的直线穿过$\Omega$时与$\Omega$的边界曲面交点不多于两个。  

把$f(x, y, z)$中的$x, y$看作常数，对$z$在$[z_1(x, y), z_2(x, y)]$（z_1(x, y), z_2(x, y)分别为区域$\Omega$的上下曲面方程）上作积分，得$\phi(x, y) = \int_{z_1(x, y)}^{z_2(x, y)}f(x, y, z)dz$。设$\phi(x, y)$在$D$上可积，则：

$\iiint_{\Omega} f(x, y, z) dx dy dz = \iint_D \phi(x, y)dx dy = \iint_D [\int_{z_1(x, y)}^{z_2(x, y)}f(x, y, z)dz]dx dy$。其中$D$是区域$\Omega$沿着平行于$z$轴方向的投影得到的区域。



类似地，可以沿着其他坐标轴进行投影。

思想：先对其中一个轴进行积分，将其他两个变量当作==常数== 。



方法二：$\iiint_\Omega f(x, y, z) dx dy dz = \int_{c_1}^{c_2}dz \iint_D f(x, y, z)dx dy$。

### 二、在柱面坐标系下

==柱面坐标==：在直角坐标系下点$M(x, y, z)$，在$xoy$面上以原点$O$为极点，$x$轴为极轴，建立极坐标系，再以$z$轴为数轴，构成了一个柱面坐标系。表示形式为$P(\rho, \theta, z)$。

==柱面坐标与直角坐标的关系==：$x = \rho \cos \theta, y = \rho \sin \theta, z = z$。

$\iiint_\Omega f(x, y, z)dx dy dz = \iiint_\Omega f(\rho\cos\theta, \rho\sin\theta, z)\rho d\rho d\theta dz$

### 三、在球面坐标系下

==球面坐标==：设空间一点$M$在直角坐标下的坐标为$M(x, y, z)$。

$x = r\sin\phi\cos\theta, y = r\sin\phi\sin\theta, z = r\cos\phi$。

$\iiint_\Omega f(x, y, z)dx dy dz = \iiint_\Omega f(r\sin\phi\cos\theta, r\sin\phi\sin\theta, r\cos\phi)r^2 \sin\phi dr d\phi d\theta$

$V = \iiint_\Omega 1 dx dy dz = \int_a^b d\theta \int_c^d d\phi \int_e^f  r^2\sin\phi dr$



## 第5节 重积分的应用

1. 曲面的面积

   设曲面$\Sigma: z = f(x, y)$，$\Sigma$在$xoy$面上投影区域为$D$，$f(x, y)$在$D$上有连续的偏导数$f_x^\prime(x, y), f_y^\prime(x, y)$，用切平面的面积近似代替小曲面的面积。

   $dA$与$d\sigma$有如下关系：$d\sigma = dA \cdot |\cos\gamma|$其中$\gamma$是曲面在点$M$的法线与$z$轴正向的夹角。所以$dA = \frac{1}{|\cos\gamma|}d\sigma$。其中$|\cos\gamma| = \frac{1}{\sqrt{1+{f_x^\prime}^2+{f_y^\prime}^2}}$，因此$dA = \frac{1}{|\cos\gamma|}d\sigma = \sqrt{1+{f_x^\prime}^2+{f_y^\prime}^2}d\sigma$。所以曲面的面积$S = \iint_D \sqrt{1+{f_x^\prime}^2+{f_y^\prime}^2} d\sigma$