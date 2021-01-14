[toc]

# 第7章 空间解析几何和矢量代数

平面解析几何：通过坐标法，把平面中的点与坐标$(x, y)$对应起来。把平面中的曲线与方程对应起来，用代数的方法研究几何问题。

空间解析几何：通过坐标法，点$M \Longleftrightarrow (x, y, z)$。空间图形（曲线、曲面）和方程对应起来。用代数的方法研究几何问题。



## 第1节 空间直角坐标系

### 一、空间点的直角坐标

空间直角坐标系的规定：按照右手系确定（右手手指从$x$轴指向$y$轴，大拇指方向为$z$轴方向）。

==坐标面==：三条坐标轴中任何两条可以确定一个平面，称为坐标面。如$xoy, yoz, zox$面。

==卦限==：坐标面$xoy, yoz, zox$把空间分成八个部分——每个部分称为一个卦限。含有$x$轴，$y$轴，$z$轴正向的部分称为第一卦限。在$xoy$面上方，从第一卦限开始按照逆时针方向的顺序确定第二、第三、第四卦限。在$xoy$面下方，位于第一卦限下方的部分称为第五卦限，从第五卦限开始按照逆时针方向的顺序确定第六、第七、第八卦限。



### 二、空间中两点间的距离

已知空间中两点$M_1(x_1, y_1, z_1), M_2(x_2, y_2, z_2)$，距离$|M_1M_2| = \sqrt{(x_2-x_1)^2+(y_2-y_1)^2+(z_2-z_1)^2}$。



## 第2节 矢量代数

### 一、矢量的概念

==矢量==：既有大小又有方向。

==单位矢量、零矢量==：模等于1的矢量称为单位矢量，模等于0的矢量称为零矢量，记为$\overset{\rightarrow}0$。零矢量的方向是任意的。



### 二、矢量的坐标表达式

矢量$\overset{\rightarrow}a$的方向：可以用矢量$\overset{\rightarrow}a$与$x$轴，$y$轴，$z$轴正向的夹角$\alpha, \beta, \gamma$，$0 \le \alpha, \beta, \gamma \le \pi$表示。

$\alpha, \beta, \gamma$的余弦$\cos \alpha, \cos \beta, \cos \gamma$：

$\cos\alpha = \frac{x}{\sqrt{x^2+y^2+z^2}}, \cos\beta = \frac{y}{\sqrt{x^2+y^2+z^2}}, \cos\gamma = \frac{z}{\sqrt{x^2+y^2+z^2}}$。



### 三、数量积和矢量积

（1）==数量积==：设有两个非零矢量$\overset{\rightarrow}a$和$\overset{\rightarrow}b$，$(\overset{\rightarrow}a, \overset{\rightarrow}b) = \theta$，称$|\overset{\rightarrow}a||\overset{\rightarrow}b|\cos\theta$为矢量$\overset{\rightarrow}a$和$\overset{\rightarrow}b$的数量积（点积，内积），记为$\overset{\rightarrow}a \circ \overset{\rightarrow}b = |\overset{\rightarrow}a||\overset{\rightarrow}b|\cos\theta$ 。$\overset{\rightarrow}a \circ \overset{\rightarrow}b = x_1x_2 + y_1y_2 + z_1z_2$。零矢量与任何矢量的数量积都等于0。

（2）==矢量积==： 有两个非零矢量$\overset{\rightarrow}a$和$\overset{\rightarrow}b$，按照下面方式确定一新的矢量$\overset{\rightarrow}c$：1. $|\overset{\rightarrow}c|=|\overset{\rightarrow}a||\overset{\rightarrow}b|\sin\theta$；2. $\overset{\rightarrow}c$垂直于$\overset{\rightarrow}a, \overset{\rightarrow}b$所确定的平面，且$\overset{\rightarrow}a, \overset{\rightarrow}b, \overset{\rightarrow}c$方向构成右手系，则称$\overset{\rightarrow}c$为矢量$\overset{\rightarrow}a$和$\overset{\rightarrow}b$的矢量积（外积，叉积），即$\overset{\rightarrow}c = \overset{\rightarrow}a \times \overset{\rightarrow}b$。
$$
\overset{\rightarrow}a \times \overset{\rightarrow}b = (y_1z_2-z_1y_2)\overset{\rightarrow}i - (x_1z_2-z_1x_2)\overset{\rightarrow}j + (x_1y_2-y_1x_2)\overset{\rightarrow}k = \left|\begin{array}{ccc}\overset{\rightarrow}i &\overset{\rightarrow}j &\overset{\rightarrow}k \\ x_1 &y_1 &z_1 \\ x_2 & y_2 &z_2 \end{array}\right|
$$


矢量即运算规律：

（1）$\overset{\rightarrow}b \times \overset{\rightarrow}a = -(\overset{\rightarrow}a \times \overset{\rightarrow}b)$；

（2）$(\overset{\rightarrow}a + \overset{\rightarrow}b) \times \overset{\rightarrow}c = \overset{\rightarrow}a \times \overset{\rightarrow}c + \overset{\rightarrow}b \times \overset{\rightarrow}c,\overset{\rightarrow}c \times (\overset{\rightarrow}a + \overset{\rightarrow}b) = \overset{\rightarrow}c \times \overset{\rightarrow}a + \overset{\rightarrow}c \times \overset{\rightarrow}b$；

（3）$(\lambda \overset{\rightarrow}a) \times \overset{\rightarrow}b = \overset{\rightarrow}a \times (\lambda \overset{\rightarrow}b) = \lambda(\overset{\rightarrow}a \times \overset{\rightarrow}b)$。



## 第3节 平面及其方程

### 一、曲面方程的概念

平面解析几何中曲线方程概念：如有平面曲线$L$与坐标$x, y$的方程$F(x, y) = 0$有以下关系：（1）凡是$L$上的点$M(x, y)$的坐标都满足$F(x, y) = 0$；（2）凡不是$L$上的点$N(x, y)$的坐标都不满足$F(x, y) = 0$。则称$F(x, y) = 0$是$L$的方程，称$L$为$F(x, y) = 0$的图形。

在空间中把曲面$S$看作动点$M(x, y)$的轨迹，如果曲面$S$与坐标$x, y, z$的方程$F(x, y, z) = 0$有以下关系：（1）凡是$S$上的点$M(x, y, z)$的坐标都满足$F(x, y, z) = 0$；（2）凡不是$S$上的点$N(x, y, z)$的坐标都不满足$F(x, y, z) = 0$。则称$F(x, y, z) = 0$是$S$的方程，称$S$为$F(x, y, z) = 0$的图形。



### 二、平面的点法式方程

==平面的法矢量==：若非零矢量$\overset{\rightarrow}n$垂直于平面$\Pi$，则称$\overset{\rightarrow}n$是平面$\Pi$的法矢量。

设平面$\Pi$的法矢量$\overset{\rightarrow}n = \{A, B, C\} \neq \overset{\rightarrow}0$。且平面$\Pi$过点$M_0(x_0, y_0, z_0)$，建立平面$\Pi$的方程：

解：在平面$\Pi$上任取一点$M(x, y, z)$，作矢量$\overset{\rightarrow}{M_0M}$，$\overset{\rightarrow}{M_0M}$在平面$\Pi$上，则有$\overset{\rightarrow}n \perp \overset{\rightarrow}{M_0M}$，所以$\overset{\rightarrow}n \circ \overset{\rightarrow}{M_0M} = 0$。$\because \overset{\rightarrow}n = \{A, B, C\}, \overset{\rightarrow}{M_0M} = \{x-x_0, y-y_0, z-z_0\}$，$\overset{\rightarrow}n \circ \overset{\rightarrow}{M_0M} = A(x-x_0) + B(y-y_0) + C(z-z_0)$。由$\overset{\rightarrow}n \circ \overset{\rightarrow}{M_0M} = 0$，得$A(x-x_0) + B(y-y_0) + C(z-z_0) = 0$，称为平面的点法式方程。 



### 三、平面的一般式方程

若平面的法矢量$\overset{\rightarrow}n = \{A, B, C\}$。过点$M_0(x_0, y_0, z_0)$，则有平面的点法式方程：$A(x-x_0) + B(y-y_0) + C(z-z_0) = 0$。令$F = Ax+By+Cz+D=0$。平面方程一定是$x, y, z$的一次方程。

反过来，坐标$x, y, z$的一次方程$Ax+By+Cz+D=0$（$A,B,C$不同时为零）的图形是一个平面。

证：取方程$Ax+By+Cz+D=0$的一组解：$Ax_0+By_0+Cz_0+D \equiv 0$，两式相减得$A(x-x_0)+B(y-y_0)+C(z-z_0) = 0$，此方程表示一平面（法矢量$\overset{\rightarrow}n = \{A, B, C\}$。点$M_0(x_0, y_0, z_0)$），且此方程与$Ax+By+Cz+D=0$是等价的，因此方程$Ax+By+Cz+D=0$的图形是一平面。

$Ax+By+Cz+D=0$称为平面的一般式方程。 



### 四、平面的截距式方程

设平面的一般式方程：$Ax+By+Cz+D=0$且$A, B, C, D$都不为0（平面不平行于坐标轴，也不过原点），方程化为$\frac{x}{-\frac{D}{A}}+\frac{y}{-\frac{D}{B}}+\frac{z}{-\frac{D}{C}}=1$，即$\frac{x}{a}+\frac{y}{b}+\frac{z}{c}=1$，此方程称为平面的截距式方程。



### 五、两平面的夹角

两平面的法向量的夹角（指锐角），称为两平面的夹角。

设平面$\Pi_1$：$A_1x+B_1y+C_1z+D_1=0, \overset{\rightarrow}{n_1} = \{A_1, B_1, C_1\}$；平面$\Pi_2$：$A_2x+B_2y+C_2z+D_2=0, \overset{\rightarrow}{n_2} = \{A_2, B_2, C_2\}$。求$\Pi_1, \Pi_2$的夹角$\theta$，即是$\overset{\rightarrow}{n_1}, \overset{\rightarrow}{n_2}$的夹角（指锐角）。$\overset{\rightarrow}{n_1} \circ \overset{\rightarrow}{n_2} = |\overset{\rightarrow}{n_1}| |\overset{\rightarrow}{n_2}|\cos\theta$，即$\cos\theta = \frac{|\overset{\rightarrow}{n_1} \circ \overset{\rightarrow}{n_2}|}{|\overset{\rightarrow}{n_1}| |\overset{\rightarrow}{n_2}|} = \frac{|A_1A_2+B_1B_2+C_1C_2|}{\sqrt{A_1^2+B_1^2+C_1^2}+\sqrt{A_2^2+B_2^2+C_2^2}}$。

（1）平面$\Pi_1 \parallel$平面$\Pi_2 \Longleftrightarrow \overset{\rightarrow}{n_1} \parallel \overset{\rightarrow}{n_2} \Longleftrightarrow \frac{A_1}{A_2} = \frac{B_1}{B_2} = \frac{C_1}{C_2}$。

（2）平面$\Pi_1 \perp$平面$\Pi_2$$ \Longleftrightarrow \overset{\rightarrow}{n_1} \perp \overset{\rightarrow}{n_2} \Longleftrightarrow \overset{\rightarrow}{n_1} \circ \overset{\rightarrow}{n_2} = 0 \Longleftrightarrow A_1A_2+B_1B_2+C_1C_2=0$。



### 六、平面外一点到平面的距离

设有一平面$\Pi$：$Ax+By+Cz+D=0$，$M_0(x_0, y_0, z_0)$是平面外一点，点$M_1(x_1, y_1, z_1)$位于平面上。过$M_0$点作平面的法矢量$\overset{\rightarrow}n$，$\overset{\rightarrow}n$与平面的交点为$N$，作矢量$\overset{\rightarrow}{M_1M_0}$，点$M_0$到平面$\Pi$的距离为$d$，则$d = |NM_0| = |Prj_\overset{\rightarrow}n\overset{\rightarrow}{M_1M_0}|$。

平面$\Pi$的法矢量$\overset{\rightarrow}n = \{A, B, C\}$，有$Ax_1+By_1+Cz_1 + D \equiv 0$，$\overset{\rightarrow}{M_1M_0} = \{x_0-x_1, y_0-y_1, z_0-z_1\}$ 。$d = |Prj_\overset{\rightarrow}n\overset{\rightarrow}{M_1M_0}| = \frac{|A(x_0-x_1)+B(y_0-y_1)+C(z_0-z_1)|}{\sqrt{A^2+B^2+C^2}} = \frac{|Ax_0+By_0+Cz_0-(Ax_1+Bx_1+Cx_1)|}{\sqrt{A^2+B^2+C^2}} = \frac{|Ax_0+By_0+Cz_0+D|}{\sqrt{A^2+B^2+C^2}}$

 

## 第4节 空间直线及其方程

### 一、空间曲线及其方程

把空间曲线看作是两曲面的交线，设曲面$S_1$：$F(x, y, z) = 0$，曲面$S_2$：$G(x, y, z) = 0$，$S_1$与$S_2$的交线$C$——空间曲线。$M(x, y, z) \in C$，点$M \in S_1$，有$F(x, y, z) = 0$，同时$M \in S_2$，有$G(x, y, z) = 0$，从而点$M(x, y, z)$满足：
$$
\left\{\begin{array}{ccc}F(x, y, z) &= &0 \\ G(x, y, z) &= &0\end{array}\right.
$$

### 二、直线的对称式和参量式方程

空间直线的方向矢量：==任何一个与空间直线平行==的非零矢量$\overset{\rightarrow}s$，都称为该直线的方向矢量。

设空间直线$L$过点$M_0(x_0, y_0, z_0)$，其方向矢量$\overset{\rightarrow}s = \{m, n, p\} \neq \overset{\rightarrow}0$，建立直线$L$的方程。

解：在直线$L$上任取一点$M(x, y, z)$，在直线$L$上有矢量$\overset{\rightarrow}{M_0 M} = \{x-x_0, y-y_0, z-z_0\}$，由$\overset{\rightarrow}{M_0 M} \parallel \overset{\rightarrow}s \Longleftrightarrow \frac{x-x_0}{m} = \frac{y-y_0}{n} = \frac{z-z_0}{p}$，称为$L$的对称式方程（标准式方程）。$\overset{\rightarrow}s$的坐标$m, n, p$称为直线$L$的一组方向数，$\overset{\rightarrow}s$的方向余弦称为$L$的方向余弦。

现令$\frac{x-x_0}{m} = \frac{y-y_0}{n} = \frac{z-z_0}{p} = t \Longleftrightarrow x = x_0 + mt, y = y_0 + nt, z = z_0 + pt$，称：
$$
\left\{\begin{array}{ccc}x &= &x_0+mt \\ y &= &y_0+nt \\ z &= &z_0+pt\end{array}\right.
$$
为$L$的参量式方程。



### 三、直线的一般式方程

把空间直线$L$看作两平面$\Pi_1, \Pi_2$的交线，设已知$\Pi_1, \Pi_2$的方程：$A_1x+B_1y+C_1z+D_1=0, A_2x+B_2y+C_2z+D_2=0$，则$\Pi_1, \Pi_2$的交线为直线$L$，其方程为：
$$
\left\{\begin{array}{cc}A_1x+B_1y+C_1z+D_1 &= &0 \\ A_2x+B_2y+C_2z+D_2 &= &0\end{array}\right.
$$
称为直线$L$的一般式方程。



例2：用对称式方程和参量式方程表示直线$L$，已知$L$的一般式方程为：
$$
\left\{\begin{array}{cc}x+y+z+1 &= &0 \\ 2x-y+3z+4 &= &0\end{array}\right.
$$
解：先求出直线$L$上一点$M_0(x_0, y_0, z_0)$，可以取$x_0 = 1$，代入$L$的方程，得：
$$
\left\{\begin{array}{cc}y_0+z_0 &= &-2 \\ -y_0+3z_0 &= &-6\end{array}\right.
$$
解得：$y_0 = 0, z_0 = -2$，得到$L$上一点$M_0(1, 0, -2)$。

再求直线$L$的方向矢量$\overset{\rightarrow}s$。由直线$L$的一般式方程可知两平面的法矢量$\overset{\rightarrow}{n_1} = \{1, 1, 1\}, \overset{\rightarrow}{n_2} = \{2, -1, 3\}$，因为直线$L$在$\Pi_1, \Pi_2$上，所以直线$L \perp \overset{\rightarrow}{n_1}$，$L \perp \overset{\rightarrow}{n_2}$，而方向矢量$\overset{\rightarrow}s \parallel L$。所以$\overset{\rightarrow}s \perp \overset{\rightarrow}{n_1}, \overset{\rightarrow}s \perp \overset{\rightarrow}{n_2}$，根据两个矢量的矢量积定义，可以取$\overset{\rightarrow}s = \overset{\rightarrow}{n_1} \times \overset{\rightarrow}{n_2}$。
$$
\overset{\rightarrow}s = \overset{\rightarrow}{n_1} \times \overset{\rightarrow}{n_2} = \left|\begin{array}{ccc}\overset{\rightarrow}i &\overset{\rightarrow}j &\overset{\rightarrow}k \\ 1 &1 &1 \\ 2 & -1 &3 \end{array}\right| = 4\overset{\rightarrow}i - \overset{\rightarrow}j -3\overset{\rightarrow}k
$$
由$L$上的点$M_0(1, 0, -2)$以及$\overset{\rightarrow}s = \{4, -1, -3\}$，所以直线$L$的对称式方程为：$\frac{x-1}{4} = \frac{y}{-1} = \frac{z+2}{-3}$。参量方程：
$$
\left\{\begin{array}{ccc}x &= &4t+1\\ y &= &-t \\ z &= &-3t-2\end{array}\right.
$$

### 四、直线的相互关系

==两直线的夹角==：两直线的方向矢量的夹角，称为两直线的夹角。

设有两直线，$L1: \frac{x-x_1}{m_1} = \frac{y-y_1}{n_1} = \frac{z-z_1}{p_1}$，方向矢量$\overset{\rightarrow}{s_1} = \{m_1, n_1, p_1\}$；$L2: \frac{x-x_2}{m_2} = \frac{y-y_2}{n_2} = \frac{z-z_2}{p_2}$，方向矢量$\overset{\rightarrow}{s_2} = \{m_2, n_2, p_2\}$。

$\cos \phi = \frac{|m_1m_2+n_1n_2+p_1p_2|}{\sqrt{m_1^2+n_1^2+p_1^2}\cdot\sqrt{m_2^2+n_2^2+p_2^2}}$。

两直线$L_1, L_2$平行、垂直的条件：

1. $L_1 \parallel L_2 \Longleftrightarrow \overset{\rightarrow}{s_1} \parallel \overset{\rightarrow}{s_2} \Longleftrightarrow \frac{m_1}{m_2} = \frac{n_1}{n_2} = \frac{p_1}{p_2}$
2. $L_1 \perp L_2 \Longleftrightarrow \overset{\rightarrow}{s_1} \perp \overset{\rightarrow}{s_2} \Longleftrightarrow m_1m_2+n_1n_2+p_1p_2 = 0$



### 五、直线与平面的夹角

直线$L$与平面$\Pi$的夹角：$l^\prime$是直线$L$在平面$\Pi$上的投影直线，则称直线$L$与$l^\prime$的夹角$\phi (0 \le \phi \le \frac{\pi}{2})$为直线$L$与平面$\Pi$的夹角。

设直线$L$的方程为$\frac{x-x_0}{m} = \frac{y-y_0}{n} = \frac{z-z_0}{p}$，方向矢量$\overset{\rightarrow}{s} = \{m, n, p\}$，平面$\Pi$的方程：$Ax+By+Cz+D=0$，法矢量$\overset{\rightarrow}{n} = \{A, B, C\}$。直线$L$与平面$\Pi$的夹角为$\phi = |\frac{\pi}{2} - (\overset{\rightarrow}{s}, \overset{\rightarrow}{n})|(0 \le \phi \le \frac{\pi}{2})$，$\sin \phi = |\cos(\overset{\rightarrow}{s},\overset{\rightarrow}{n})| = \frac{Am+Bn+Cp}{\sqrt{A^2+B^2+C^2}\cdot\sqrt{m^2+n^2+p^2}}$。

直线$L$与平面$\Pi$平行，垂直的条件：

1. 直线$L$与平面$\Pi$垂直$\Longleftrightarrow$$\overset{\rightarrow}{s} \parallel \overset{\rightarrow}{n}$$\Longleftrightarrow$$\frac{A}{m} = \frac{B}{n} = \frac{C}{p}$
2. 直线$L$与平面$\Pi$平行$\Longleftrightarrow$$\overset{\rightarrow}{s} \perp \overset{\rightarrow}{n}$$\Longleftrightarrow$$Am+Bn+Cp = 0$



## 第5节 曲面与方程

讨论：柱面，旋转曲面的方程

### 一、柱面

平行于定直线并沿着定曲线$C$移动的直线$L$所生成的曲面，称为柱面，定曲线$C$称为准线，平行移动的直线$L$称为母线。

柱面方程的特征：只含有$x, y$而缺少$z$的方程$F(x, y) = 0$表示与$xoy$面以一曲线$F(x, y) = 0$为准线，而母线平行于$z$轴的柱面。

### 二、旋转曲面

一条平面曲线$C$绕着同一平面的一条定直线$l$旋转一周所生成的曲面，叫做==旋转曲面==。

旋转曲面的方程：

设在$yoz$平面上有一已知曲线$C: F(y, z) = 0$，把曲线$C$绕$z$轴旋转，就得到以$z$轴为旋转轴的旋转曲面，求该曲面的方程。

设点$M_1(0, y_1, z_1)$在曲线$C$上，从而有$F(y_1, z_1) = 0$，当曲线$C$绕着$z$轴旋转时，点$M_1$也绕着$z$轴旋转到另一点$M(x, y, z)$。这时，$z = z_1$，且点$M_1$到$z$轴的距离$|y_1|$与点$M(x, y, z)$到$z$轴的距离$d = \sqrt{x^2+y^2}$相等，即：
$$
\left\{\begin{array}{ccc}\sqrt{x^2+y^2} &= &|y_1| \\ z &= &z_1\end{array}\right.
$$
或：
$$
\left\{\begin{array}{ccc} y_1 &= &\pm\sqrt{x^2+y^2} \\ z_1 &= &z\end{array}\right.
$$
代入$F(y_1, z_1) = 0$，得$F(\pm\sqrt{x^2+y^2}, z) = 0$，为旋转曲面的方程。

概括起来：曲线$C: F(y, z) = 0$（$yoz$平面上的曲线）绕$z$轴旋转生成旋转曲面，曲面的方程为：把$F(y, z) = 0$中的$z$保持不变，而把$y$换成$\pm\sqrt{x^2+y^2}$，得到$F(\pm \sqrt{x^2+y^2}, z) = 0$。曲线$C: F(y, z) = 0$（$yoz$平面上的曲线）绕$y$轴旋转生成旋转曲面，曲面的方程为：把$F(y, z) = 0$中的$y$保持不变，而把$z$换成$\pm\sqrt{x^2+z^2}$，得到$F(y, \pm \sqrt{x^2+z^2}) = 0$。



## 第6节 二次曲面

平面解析几何：把二元二次方程所表示的曲线，称为二次曲线。一次方程所表示的曲线称为一次曲线。

空间解析几何：把三元二次方程所表示的曲面，称为二次曲面，平面称为一次曲面。

研究方法：平面截割法——用坐标面或平行于坐标面的平面族去截割二次曲面，考察它们的交线形状，进行综合分析，从而掌握曲面的全貌。

### 一、椭球面

由方程$\frac{x^2}{a^2}+\frac{y^2}{b^2}+\frac{z^2}{c^2}=1(a>0,b>0,c>0)$所确定的曲面称为椭球面。

由方程可知：$\frac{x^2}{a^2} \le 1, \frac{y^2}{b^2} \le 1, \frac{z^2}{c^2} \le 1$，即$|x| \le a, |y| \le b, |z| \le c$。这说明椭球面包含在$x=\pm a, y=\pm b, z=\pm c$所围成的长方体内，且椭球面关于三个坐标轴对称。

椭球面与三个坐标面的交线：
$$
\left\{\begin{array}{ccc} \frac{x^2}{a^2}+\frac{y^2}{b^2}+\frac{z^2}{c^2} &= &1 \\ z &= &0\end{array}\right. \Longleftrightarrow \left\{\begin{array}{ccc} \frac{x^2}{a^2}+\frac{y^2}{b^2} &= &1 \\ z &= &0\end{array}\right.
$$
其表示$xoy$面的椭圆。 

椭球面与平行于$xoy$面的平面族$z = h(|h|\le c)$的交线：
$$
\left\{\begin{array}{ccc} \frac{x^2}{a^2}+\frac{y^2}{b^2}+\frac{z^2}{c^2} &= &1 \\ z &= &h\end{array}\right. \Longleftrightarrow \left\{\begin{array}{ccc} \frac{x^2}{a^2(1-\frac{h^2}{c^2})}+\frac{y^2}{b^2(1-\frac{h^2}{c^2})} &= &1 \\ z &= &h\end{array}\right.
$$
其表示$z=h$平面上的椭圆。椭圆的两个半轴$\frac{a}{c}\sqrt{c^2-h^2}, \frac{b}{c}\sqrt{c^2-h^2}$，椭圆的中心在$z$轴上，当$h$由$0 \to c$时，两个半轴有$\frac{a}{c}\sqrt{c^2-h^2} \to 0, \frac{b}{c}\sqrt{c^2-h^2} \to 0$。

类似地，可讨论平行于$zox$面及平行于$yoz$面的平面族与椭球面的交线也都是椭圆。



### 二、抛物面

1. 由方程$\frac{x^2}{2p} + \frac{y^2}{2q} = z$（其中$p, q$同号）所表示的曲面称为椭圆抛物面。设$p>0,q>0$，由$z = \frac{x^2}{2p} + \frac{y^2}{2q} \ge 0$，椭圆抛物面都在$xoy$面的上方，与$xoy$面交于点$O(0, 0, 0)$，用平面族$z = h > 0$去截曲面，得交线：
   $$
   \left\{\begin{array}{ccc} \frac{x^2}{2p} + \frac{y^2}{2q} &= &z \\ z &= &h>0\end{array}\right. \Longleftrightarrow \left\{\begin{array}{ccc} \frac{x^2}{2ph}+\frac{y^2}{2qh} &= &1 \\ z &= &h\end{array}\right.
   $$
   表示$z=h$平面上的椭圆，两个半轴$\sqrt{2ph}, \sqrt{2qh}$，中心在$z$轴上，当$h > 0$越大，两个半轴也越大。用$zox$坐标面去截曲面，得交线：
   $$
   \left\{\begin{array}{ccc} \frac{x^2}{2p} + \frac{y^2}{2q} &= &z \\ y &= &0\end{array}\right. \Longleftrightarrow \left\{\begin{array}{ccc} x^2 &= &2pz \\ y &= &0\end{array}\right.
   $$
   为$zox$面上的抛物线，顶点在原点，$z$轴为对称轴，开口朝$z$轴正向。

   用平行于$zox$平面的平面$y=h$去截曲面，得交线：
   $$
   \left\{\begin{array}{ccc} \frac{x^2}{2p} + \frac{y^2}{2q} &= &z \\ y &= &h\end{array}\right. \Longleftrightarrow \left\{\begin{array}{ccc} x^2 &= &2p(z-\frac{h^2}{2q}) \\ y &= &h\end{array}\right.
   $$
   为$y=h$平面上的抛物线，对称轴平行于$z$轴，顶点$(0, h, \frac{h^2}{2q})$，开口朝$z$轴的正向。

2. 由方程$-\frac{x^2}{2p}+\frac{y^2}{2q}=z$（其中$p,q$同号）所表示的曲面称为双曲抛物面。讨论曲面的形状：设$p>0,q>0$，考虑用$xoy$平面去截曲面，得交线：
   $$
   \left\{\begin{array}{ccc} -\frac{x^2}{2p} + \frac{y^2}{2q} &= &z \\ z &= &0\end{array}\right. \Longleftrightarrow \left\{\begin{array}{ccc} -\frac{x^2}{2p} + \frac{y^2}{2q} &= &0 \\ z &= &0\end{array}\right. \Longleftrightarrow \left\{\begin{array}{ccc} (\frac{-x}{\sqrt{2p}}+\frac{y}{\sqrt{2q}})(\frac{x}{\sqrt{2p}}+\frac{y}{\sqrt{2q}}) &= &0 \\ z &= &0\end{array}\right. \\ \Longleftrightarrow L1:\left\{\begin{array}{ccc} \frac{-x}{\sqrt{2p}}+\frac{y}{\sqrt{2q}} &= &0 \\ z &= &0\end{array}\right. \quad or \quad L2:\left\{\begin{array}{ccc} \frac{x}{\sqrt{2p}}+\frac{y}{\sqrt{2q}} &= &0 \\ z &= &0\end{array}\right.
   $$
   $L1$是$xoy$面上过原点$O$的一条直线，$L2$是$xoy$面上另一条过原点$O$的一条直线。

   若用平面$z=h(h>0)$去截曲面，得交线：
   $$
   \left\{\begin{array}{ccc} -\frac{x^2}{2p} + \frac{y^2}{2q} &= &z \\ z &= &h>0\end{array}\right. \Longleftrightarrow \left\{\begin{array}{ccc} -\frac{x^2}{2ph}+\frac{y^2}{2qh} &= &1 \\ z &= &h\end{array}\right.
   $$
   交线是$z=h>0$平面的双曲线，实轴平行于$y$轴，虚轴平行于$x$轴，中心在$z$轴上。

   若用平面$z=h(h<0)$去截曲面，得交线：
   $$
   \left\{\begin{array}{ccc} -\frac{x^2}{2p} + \frac{y^2}{2q} &= &z \\ z &= &h<0\end{array}\right. \Longleftrightarrow \left\{\begin{array}{ccc} -\frac{x^2}{2ph}+\frac{y^2}{2qh} &= &1 \\ z &= &h\end{array}\right.
   $$
   交线是$z=h<0$平面的双曲线，实轴平行于$x$轴，虚轴平行于$y$轴，中心在$z$轴上。

   



### 三、双曲面

1. 单叶双曲面

   由方程$\frac{x^2}{a^2}+\frac{y^2}{b^2}-\frac{z^2}{c^2}=1(a>0,b>0,c>0)$所表示的曲面称为单叶双曲面。

   用$z = h$（平行于$xoy$面的平面）与单叶双曲面相交，交线：
   $$
   \left\{\begin{array}{ccc} \frac{x^2}{a^2}+\frac{y^2}{b^2}-\frac{z^2}{c^2} &= &1 \\ z &= &h\end{array}\right. \Longleftrightarrow \left\{\begin{array}{ccc} \frac{x^2}{a^2(1+\frac{h^2}{c^2})}+\frac{y^2}{b^2(1+\frac{h^2}{c^2})} &= &1 \\ z &= &h\end{array}\right.
   $$
   交线是平面$z=h$平面上的椭圆，两个半轴$\frac{a}{c}\sqrt{c^2+h^2}, \frac{b}{c}\sqrt{c^2+h^2}$，随着$|h|$增大，两个半轴也增大，中心在$z$轴上。

   用$zox$坐标面$y = 0$去截单叶双曲面，得交线：
   $$
   \left\{\begin{array}{ccc} \frac{x^2}{a^2}+\frac{y^2}{b^2}-\frac{z^2}{c^2} &= &1 \\ y &= &0\end{array}\right. \Longleftrightarrow \left\{\begin{array}{ccc} \frac{x^2}{a^2}-\frac{z^2}{c^2} &= &1 \\ y &= &0\end{array}\right.
   $$
   交线是$zox$面上的双曲线，其实轴为$x$轴，虚轴为$z$轴，中心在原点。

   用$yoz$坐标面$x = 0$去截单叶双曲面，得交线：
   $$
   \left\{\begin{array}{ccc} \frac{x^2}{a^2}+\frac{y^2}{b^2}-\frac{z^2}{c^2} &= &1 \\ x &= &0\end{array}\right. \Longleftrightarrow \left\{\begin{array}{ccc} \frac{y^2}{b^2}-\frac{z^2}{c^2} &= &1 \\ x &= &0\end{array}\right.
   $$
   交线是$yoz$面上的双曲线，其实轴为$y$轴，虚轴为$z$轴，中心在原点。



2. 双叶双曲面

   由方程$\frac{x^2}{a^2}+\frac{y^2}{b^2}-\frac{z^2}{c^2}=-1(a>0,b>0,c>0)$所表示的曲面称为双叶双曲面。

   用$z = h$（平行于$xoy$面的平面）与双叶双曲面相交，交线：
   $$
   \left\{\begin{array}{ccc} \frac{x^2}{a^2}+\frac{y^2}{b^2}-\frac{z^2}{c^2} &= &-1 \\ z &= &h\end{array}\right. \Longleftrightarrow \left\{\begin{array}{ccc} \frac{x^2}{a^2}+\frac{y^2}{b^2} &= &(\frac{h^2}{c^2}-1) \\ z &= &h\end{array}\right.
   $$
   可以看出，当$|h| < c, (-c < h < c)$时，平面$z=h$与双叶双曲面无交点，即在此范围内双叶双曲面没有图形。

   当$h = \pm c$时：
   $$
   \left\{\begin{array}{ccc} \frac{x^2}{a^2}+\frac{y^2}{b^2}-\frac{z^2}{c^2} &= &-1 \\ z &= &\pm c\end{array}\right. \Longleftrightarrow \left\{\begin{array}{ccc} \frac{x^2}{a^2}+\frac{y^2}{b^2} &= &0 \\ z &= &\pm c\end{array}\right.
   $$
   $z = \pm c$与双叶双曲面相交于两点：$(0, 0, c)$和$(0, 0, -c)$。

   用$zox$坐标面$y = 0$去截双叶双曲面，得交线：
   $$
   \left\{\begin{array}{ccc} \frac{x^2}{a^2}+\frac{y^2}{b^2}-\frac{z^2}{c^2} &= &-1 \\ y &= &0\end{array}\right. \Longleftrightarrow \left\{\begin{array}{ccc} -\frac{x^2}{a^2}+\frac{z^2}{c^2} &= &1 \\ y &= &0\end{array}\right.
   $$
   交线是$zox$面上的双曲线。

   用$yoz$坐标面$x = 0$去截单叶双曲面，得交线：
   $$
   \left\{\begin{array}{ccc} \frac{x^2}{a^2}+\frac{y^2}{b^2}-\frac{z^2}{c^2} &= &-1 \\ x &= &0\end{array}\right. \Longleftrightarrow \left\{\begin{array}{ccc} -\frac{y^2}{b^2}+\frac{z^2}{c^2} &= &1 \\ x &= &0\end{array}\right.
   $$
   交线是$yoz$面上的双曲线。



## 第7节 空间曲线及其方程

### 一、空间曲线的一般方程

### 二、空间曲线的参量方程

将曲线$C$上的动点$(x, y, z)$表示成参量$t$的函数：
$$
\left\{\begin{array}{ccc} x &= &x(t) \\ y &= &y(t) \\ z &= &z(t)\end{array}\right.
$$
称上述方程为曲线$C$的参量方程。

### 三、空间曲线在坐标面上的投影曲线

设空间曲线$C$的一般方程：
$$
\left\{\begin{array}{ccc}F(x, y, z) &= &0 \\ G(x, y, z) &= &0\end{array}\right.
$$
把$C$投影到$xoy$面上，得到投影曲线$C^\prime$，求$xoy$面上$C^\prime$的方程。

==曲线$C$的投影柱面==：以空间曲线$C$为准线，母线平行于$z$轴的柱面，称为曲线$C$关于$xoy$面上的投影柱面。

==曲线$C$在$xoy$面上的投影曲线$C^\prime$==：曲线$C$关于$xoy$面上的投影柱面与$xoy$面的交线$C^\prime$。



解：

（1）先求曲线$C$关于$xoy$面上的投影柱面；

由方程组（27），消去$z$，得到$H(x, y) = 0$，

（2）再求投影柱面与$xoy$面的交线$C^\prime$，即令$z = 0$。