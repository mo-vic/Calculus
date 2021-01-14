[toc]

# 第10章 曲线积分与曲面积分

### 第1节 第一类曲线积分

### 一、第一类曲线积分的定义

==第一类曲线积分==：设空间的光滑曲线$L$的两个端点$A, B$，$f(x, y, z)$是定义在$L$上的有界函数，用$L$上的点$A = M_0, M_1, M_2, \cdots, M_n = B$把$L$分成$n$个子弧段$\overset{\frown}{M_{i-1}M_i}, (i=1, \cdots, n)$，$\forall N_i(\xi_i, \eta_i, \zeta_i) \in \overset{\frown}{M_{i-1}M_i}$，$\overset{\frown}{M_{i-1}M_i}$弧长为$\Delta S_i$，作和式$I_n = \sum_{i=1}^n f(\xi_i, \eta_i, \zeta_i)\Delta S_i$，令$\lambda = \max\{\Delta S_1, \Delta S_2, \cdots, \Delta S_n\}$，如果$\lim_{\lambda \to 0}I_n = \lim_{\lambda \to 0}\sum_{i=1}^n f(\xi_i, \eta_i, \eta_i)\Delta S_i$存在，设为$I$。若$I$的值与对$L$的分法无关，也与点$N_i$在$\overset{\frown}{M_{i-1}M_i}$的取法无关，则称$I$为$f(x, y, z)$沿着曲线$L$的第一类曲线积分（对弧长的曲线积分），记为$\int_L f(x, y, z)ds$。

若曲线$L$的两个端点$A, B$，则曲线记为$L(AB)$或$\overset{\frown}{AB}$。

若积分路径$L$是封闭曲线，记为$\oint_L f(x, y, z)ds$。

### 二、第一类曲线积分的计算

1. 设空间曲线$L$由参量方程给出：$x = x(t), y = y(t), z = z(t), \alpha \le t\le  \beta$，其中$x(t), y(t), z(t)$在$[\alpha, \beta]$上有一阶连续的导数，且$x^\prime(t), y^\prime(t), z^\prime(t)$不同时为0。$f(x, y, z)$在曲线$L$是连续的，则$\int_L f(x, y, z)ds = \int_\alpha^\beta f[x(t), y(t), z(t)] \sqrt{{x^\prime(t)}^2 + {y^\prime(t)}^2 + {z^\prime(t)}^2}dt$。

   证明该公式：假设当$t$由$\alpha$变化到$\beta$时，$L$上的点$M(x(t), y(t), z(t))$从端点$A$到端点$B$描绘出曲线$L$，在$L$上取一系列分点$A = M_0, M_1, M_2, \cdots, M_n = B$，对应一系列单调增加的$t$值：$t_0 = \alpha < t_1 < t_2 < \cdots < t_n = \beta$，由定义，由$\int_L f(x, y, z)ds = \lim_{\lambda \to 0}\sum_{i=1}^n f(\xi_i, \eta_i, \zeta_i)\Delta S_i$，点$N(\xi_i, \eta_i, \zeta_i) \in \overset{\frown}{M_{i-1}M_i}$，对应参量值$t = \tau_i$，且$t_{i-1} \le \tau_i \le t_i$，根据定积分的应用，$\Delta S_i = \int_{t_{i-1}}^{t_i}\sqrt{{x^\prime(t)}^2 + {y^\prime(t)}^2 + {z^\prime(t)}^2}dt$，由积分中值定理，$\Delta S_i = \sqrt{{x^\prime(\tau_i^\prime)}^2 + {y^\prime(\tau_i^\prime)}^2 + {z^\prime(\tau_i^\prime)}^2}(t_i - t_{i-1}) = \sqrt{{x^\prime(\tau_i^\prime)}^2 + {y^\prime(\tau_i^\prime)}^2 + {z^\prime(\tau_i^\prime)}^2}\Delta t_i$，其中$t_{i-1} \le \tau_i^\prime \le t_i$，于是有$\sum_{i=1}^n f(\xi_i, \eta_i, \zeta_i)\Delta S_i = \sum_{i=1}^n f[x(\tau_i), y(\tau_i), z(\tau_i)] \sqrt{{x^\prime(\tau_i^\prime)}^2 + {y^\prime(\tau_i^\prime)}^2 + {z^\prime(\tau_i^\prime)}^2}\Delta t_i$

   因为$f(x, y, z)$在$L$上连续，所以$\int_L f(x, y, z)ds$存在，定义中的极限值与$\tau_i$的取法无关，取$\tau_i = \tau_i^\prime$，令$d = \max\{\Delta t_1, \Delta t_2, \cdots, \Delta t_n\}$，当$\lambda \to 0, d \to 0$。所以$\int_L f(x, y, z)ds = \lim_{\lambda \to 0}\sum_{i=1}^n f(\xi_i, \eta_i, \eta_i)\Delta S_i = \\ \lim_{d \to 0}\sum_{i=1}^n f[x(\tau_i^\prime), y(\tau_i^\prime), z(\tau_i^\prime)] \sqrt{{x^\prime(\tau_i^\prime)}^2 + {y^\prime(\tau_i^\prime)}^2 + {z^\prime(\tau_i^\prime)}^2}\Delta t_i \\ = \int_\alpha^\beta f[x(t), y(t), z(t)] \sqrt{{x^\prime(t)}^2 + {y^\prime(t)}^2 + {z^\prime(t)}^2}dt$ 



## 第2节 第二类曲线积分

### 一、第二类曲线积分的定义

==数量场==：若对空间区域$\Omega$上的每一点$M(x, y, z)$，在时刻$t$总存在着一个确定的数值$u = u(x, y, z, t)$与之对应，就说在$\Omega$上确定了一个==数量场==。

==矢量场==：若对空间区域$\Omega$上的每一点$M(x, y, z)$，在时刻$t$总存在着一个确定的矢量$\overset{\rightarrow}{A} = \overset{\rightarrow}{A}(x, y, z, t)$与之对应，就说在$\Omega$上确定了一个==矢量场==。

==稳定场==：与时间$t$无关的场称为==稳定场==，这时数量场$u = u(x, y, z)$，矢量场$\overset{\rightarrow}{A} = \overset{\rightarrow}{A}(x, y, z)$。

矢量场$\overset{\rightarrow}{A} = \overset{\rightarrow}{A}(x, y, z)$在$oxyz$中三个坐标轴上投影分别为$P(x, y, z), Q(x, y, z), R(x, y, z)$，则$\overset{\rightarrow}{A} = \overset{\rightarrow}{A}(x, y, z) = P(x, y, z)\overset{\rightarrow}i + Q(x, y, z)\overset{\rightarrow}j + R(x, y, z)\overset{\rightarrow}k$。



==曲线方向规定==：非封闭曲线$L$两个端点$A, B$，有两个方向$\overset{\frown}{AB}, \overset{\frown}{BA}$，规定一个为正向，记为$L$，另一个则记为$L^-$。对于封闭曲线，在曲线上取三个点，则有两个方向$\overset{\frown}{ABCA}, \overset{\frown}{ACBA}$，规定一个为正向，另一个就为负方向。



==第二类曲线积分==：设$\overset{\rightarrow}{A} = \overset{\rightarrow}{A}(x, y, z)$为一矢量场，$L$是矢量场中一条以$A$为起点，$B$为终点的有向光滑曲线，由起点$A$沿着曲线的正向，用分点$A = M_0, M_1, M_2, \cdots, M_n = B$将$L$任意分成$n$个有向的子弧段，弧段$\overset{\frown}{M_{i-1}M_i}$，弧长为$\Delta S_i$，有向子弧段$\overset{\frown}{M_{i-1}M_i}$对应弦矢量$\overset{\rightarrow}{M_{i-1}M_i}$，若$M_i(x_i, y_i, z_i), M_{i-1}(x_{i-1}, y_{i-1}, z_{i-1})$，则$\overset{\rightarrow}{M_{i-1}M_i} = (x_i - x_{i-1})\overset{\rightarrow}{i} + (y_i - y_{i-1})\overset{\rightarrow}{j} + (z_i - z_{i-1})\overset{\rightarrow}{k} = \Delta x_i\overset{\rightarrow}{i} + \Delta y_i\overset{\rightarrow}{j} + \Delta z_i\overset{\rightarrow}{k}$，任取点$N(\xi_i, \eta_i, \zeta_i) \in \overset{\frown}{M_{i-1}M_i}$，作数量积$\overset{\rightarrow}{F}(\xi_i, \eta_i, \zeta_i) \cdot \overset{\rightarrow}{M_{i-1}M_i}$，当$\lambda = \max\{\Delta S_1, \Delta S_2, \cdots, \Delta S_n\}$，如果和式极限$\lim_{\lambda \to 0}\sum_{i=1}^n \overset{\rightarrow}{F}(\xi_i, \eta_i, \zeta_i) \cdot \overset{\rightarrow}{M_{i-1}M_i}$存在，且极限值与对$L$的分法无关，也与点$N_i$在$\overset{\frown}{M_{i-1}M_i}$的取法无关，则称此极限为矢量函数$\overset{\rightarrow}{A} = \overset{\rightarrow}{A}(x, y, z)$沿着曲线$L(AB)$的第二类曲线积分，记为$\int_L \overset{\rightarrow}A(x, y, z) \cdot d\overset{\rightarrow}s$或$\int_{\overset{\frown}{AB}}\overset{\rightarrow}A(x, y, z) \cdot d\overset{\rightarrow}s$。

$\overset{\rightarrow}{A} = \overset{\rightarrow}{A}(x, y, z) = P(x, y, z)\overset{\rightarrow}i + Q(x, y, z)\overset{\rightarrow}j + R(x, y, z)\overset{\rightarrow}k$，$\overset{\rightarrow}{M_{i-1}M_i} = \Delta x_i\overset{\rightarrow}{i} + \Delta y_i\overset{\rightarrow}{j} + \Delta z_i\overset{\rightarrow}{k}$，$\int_L \overset{\rightarrow}A(x, y, z) \cdot d\overset{\rightarrow}s = \lim_{\lambda \to 0}\sum_{i=1}^n \overset{\rightarrow}{F}(\xi_i, \eta_i, \zeta_i) \cdot \overset{\rightarrow}{M_{i-1}M_i} \\ = \lim_{\lambda \to 0}\sum_{i=1}^n [P(\xi_i, \eta_i, \zeta_i)\Delta x_i + Q(\xi_i, \eta_i, \zeta_i)\Delta y_i + R(\xi_i, \eta_i, \zeta_i)\Delta z_i] \\ = \int_L P(x, y, z)dx + \int_L Q(x, y, z)dy + \int_L R(x, y, z)dz$

==注意==第二类曲线积分与曲线的方向有关。

$\int_{L(AB)}Pdx + Qdy + Rdz = -\int_{L(BA)}Pdx + Qdy + Rdz$



### 二、第二类曲线积分的计算

设空间曲线的参量方程$L(AB): x = x(t), y = y(t), z = z(t)$，其中$x(t), y(t), z(t)$具有一阶连续的导数，起点$A$对应$t = \alpha$，即$A(x(\alpha), y(\alpha), z(\alpha))$，终点$B$对应$t = \beta$，即$B(x(\beta), y(\beta), z(\beta))$，当$t$单调地由$\alpha$变化到$\beta$时，点$M(x(t), y(t), z(t))$从端点$A$到端点$B$描绘出曲线$L(AB)$，$\overset{\rightarrow}{A}(x, y, z) = P(x, y, z)\overset{\rightarrow}i + Q(x, y, z)\overset{\rightarrow}j + R(x, y, z)\overset{\rightarrow}k$在$L(AB)$上连续，在$L(AB)$上，由起点$A$开始任意取一系列点$A = M_0, M_1, M_2, \cdots, M_n = B$把$L(AB)$分成$n$个有向子弧段$\overset{\frown}{M_{i-1}M_i}, (i=1, \cdots, n)$，这些分点对应单调变化的参量值$t_0 = \alpha, t_1, t_2, \cdots, t_n = \beta$，$\forall N_i(\xi_i, \eta_i, \zeta_i) \in \overset{\frown}{M_{i-1}M_i}$，点$N_i$对应参量值为$t = \tau_i$，即$N_i(x(\tau_i), y(\tau_i), z(\tau_i))$（其中$\tau_i$介于$t_{i-1}$和$t_i$之间）；$x_i - x_{i-1} = \Delta x_i$，其$x_i = x(t_i), x_{i-1} = x(t_{i-1}), \Delta x_i = x(t_i) - x(t_{i-1}) = x^\prime(\tau_i^\prime)(t_i - t_{i-1}) = x^\prime(\tau_i^\prime)\Delta t_i$，

$\sum_{i=1}^n P(\xi_i, \eta_i, \zeta_i)\Delta x_i = P[x(\tau_i), y(\tau_i), z(\tau_i)]x^\prime(\tau_i^\prime)\Delta t_i$，因为$P(x, y, z)$在$L(AB)$上连续，积分值与$t = \tau_i$的取法无关，现取$\tau_i = \tau_i^\prime$，$\sum_{i=1}^n P(\xi_i, \eta_i, \zeta_i)\Delta x_i = \sum_{i=1}^n P[x(\tau_i^\prime), y(\tau_i^\prime), z(\tau_i^\prime)]x^\prime(\tau_i^\prime)\Delta t_i$，令$d = \max \{|\Delta t_1|, |\Delta t_2|, \cdots, |\Delta t_n|\}$，当$\lambda \to 0$时，$d \to 0$，$\int_L P(x, y, z)dx = \lim_{\lambda \to 0}\sum_{i=1}^n P[x(\tau_i^\prime), y(\tau_i^\prime), z(\tau_i^\prime)]x^\prime(\tau_i^\prime)\Delta t_i = \int_L P(x, y, z)dx \\ = \lim_{d \to 0}\sum_{i=1}^n P[x(\tau_i^\prime), y(\tau_i^\prime), z(\tau_i^\prime)]x^\prime(\tau_i^\prime)\Delta t_i \\ \int_\alpha^\beta P[x(t), y(t), z(t)]x^\prime(t)dt$



### 三、两类曲线积分的关系

设有向曲线$L(AB)$，起点$A$，终点$B$，在$L(AB)$上任取一点$M(x, y, z)$，过$M$点作切线矢量$\overset{\rightarrow}T$（方向与$L$的正向相一致），取与$\overset{\rightarrow}T$方向相同的单位矢量$\overset{\rightarrow}{T^0}$，若$\overset{\rightarrow}T$与$x$轴，$y$轴，$z$轴正向夹角为$\alpha, \beta, \gamma$，则$\overset{\rightarrow}{T^0} = \{\cos\alpha, \cos\beta, \cos\gamma\}, |\overset{\rightarrow}{T^0}| = \sqrt{\cos^2\alpha+\cos^2\beta+\cos^2\gamma} = \sqrt{1} = 1$。在第二类曲线积分中，$\overset{\rightarrow}{ds} = \{dx, dy, dz\}, |\overset{\rightarrow}{ds}| = \sqrt{(dx)^2+(dy)^2+(dz)^2} = ds$（向量的模等于弧微分），因此有$dx = |\overset{\rightarrow}{ds}|\cos\alpha = \cos\alpha ds, dy = |\overset{\rightarrow}{ds}|\cos\beta = \cos\beta ds, dz = |\overset{\rightarrow}{ds}|\cos\gamma = \cos\gamma ds$（投影），因此$\overset{\rightarrow}{ds} = \{dx, dy, dz\} = \{\cos\alpha ds, \cos\beta ds, \cos\gamma ds\} = \{\cos\alpha, \cos\beta, \cos\gamma\}ds = \overset{\rightarrow}{T^0}ds$，因此$\int_L \overset{\rightarrow}A(x, y, z) \cdot d\overset{\rightarrow}s = \int_L \overset{\rightarrow}A(x, y, z) \cdot \overset{\rightarrow}{T^0}ds = \int_L \overset{\rightarrow}A(x, y, z) \cdot \{\cos\alpha, \cos\beta, \cos\gamma\}ds \\ = \int_L\{P(x, y, z)\cos\alpha+Q(x,y,z)\cos\beta+R(x,y,z)\cos\gamma\}ds \\ = \int_L P(x, y, z)dx + \int_L Q(x, y, z)dy + \int_L R(x, y, z)dz$



## 第3节 格林（Green）公式

格林公式描述了平面上封闭曲线的曲线积分$\oint_L P(x,y)dx + Q(x, y)dy$与平面区域$D$（$L$所围成）上的某一个二重积分关系。

==单连通域==：如果区域$D$中的任何一条封闭曲线所包围的点全都属于$D$，则称$D$为单连通域，否则称$D$为复连通域（如带有空洞的区域）。

==格林公式==：设闭区域$D$由光滑或分段光滑的曲线$L$所围成，两函数$P(x, y), Q(x, y)$在$D$内及其边界$L$上具有连续的一阶偏导数，则有$\oint_L Pdx+Qdy = \iint_D (\frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y})dx dy$，其中$L$是区域$D$的正向边界曲线。

$D$的正向边界曲线：当人沿着$D$的正向边界曲线前进时，区域$D$在人的左侧。

证明：

==情形一==：先证$D$是单连通域、平行于坐标轴的直线穿过区域$D$时，直线与$D$的边界曲线交点不多于两个。

区域$D$对应的曲线：$L = L_1(AB) + L_2(BA)$（上半曲线和下半曲线），有$L_1(AB):y=y_1(x), L_2(BA):y=y_2(x), y_1(x) \le y \le y_2(x), a \le x \le b$。$D = \{(x, y)|y_1(x) \le y \le y_2(x), a \le x \le b\}$，二重积分$\iint_D (\frac{\partial P}{\partial y}) dxdy = \int_a^b dx \int_{y_1(x)}^{y_2(x)}\frac{\partial P}{\partial y}dy = \int_a^b P(x, y)|_{y_1(x)}^{y_2(x)}dx \\ = \int_a^b [P(x, y_2(x))-P(x, y_1(x))]dx = \int_a^b P[x, y_2(x)]dx - \int_a^b P[x, y_1(x)]dx$

$\oint_L P(x, y)dx = \int_{L_1}P(x, y)dx + \int_{L_2} P(x, y)dx = \int_a^b P[x, y_1(x)]dx + \int_b^a P(x, y_2(x))dx = \int_a^b P[x, y_1(x)]dx - \int_a^b P(x, y_2(x))dx$。

==情形二==：$D$是单连通域，但是穿过$D$且与坐标轴平行的直线与$D$的边界曲线的交点多于两个。作线段$MN$把$D$分成区域$D_1, D_2$，$D_1$的边界曲线：$L_1 + \bar{NM}$，$D_2$的边界曲线：$L_2+\bar{MN}$。$D_1, D_2$满足情形一条件，由已证得结论，有$\iint_{D_1}(\frac{\partial Q}{\partial x} - \frac{\partial P}{\partial y})dx dy = \int_{L_1 + \bar{NM}}Pdx + Qdy$，$\iint_{D_2}(\frac{\partial Q}{\partial x} - \frac{\partial P}{\partial y})dx dy = \int_{L_2 + \bar{MN}}Pdx + Qdy$，

两式相加，$\iint_{D_1}(\frac{\partial Q}{\partial x} - \frac{\partial P}{\partial y})dxdy + \iint_{D_2}(\frac{\partial Q}{\partial x} - \frac{\partial P}{\partial y})dxdy = \iint_{D}(\frac{\partial Q}{\partial x} - \frac{\partial P}{\partial y})dx dy = \int_{L_1 + \bar{NM}}Pdx + Qdy + \int_{L_2 + \bar{MN}}Pdx + Qdy$

==情形三==：设$D$是复连通域，$D$为$L_1$与$L_2$所围成。取$L_2$的正向为逆时针方向，$L_1$的正向是顺时针方向。作辅助线段$AB$，则以$L_1 + \bar{AB} + L_2 + \bar{BA}$为边界的区域$D^\prime$，$D^\prime$是单连通域。综合情形一和情形二结果，可知当$D$是复连通域时，格林公式仍然成立。



==格林公式的应用==：

1. 计算曲线围成的区域的面积$A = \frac{1}{2}\oint_L x dy - ydx$，$1 = \frac{1}{2}[(1 - (-1)]$
2. 计算复杂的第二类曲线积分。
3. 已知曲线积分与路径无关，则有$du(x, y) = Pdx+Qdy$，而$u(x, y)$是一个曲线积分定义的函数，从而选取特殊的积分路径，求出$u(x, y) = \int_{(x_0, y_0)}^{(x, y)} Pdx+Qdy$。
4. 已知二元函数的全微分，求原二元函数。



==平面曲线积分与路径无关的条件==：

==定理==：设$P(x, y), Q(x, y)$在==单连通域==（复连通域中不一定成立）$D$上具有连续的偏导数，则以下四个命题是等价的：

（1）在$D$内沿任何一条闭曲线$L$其积分值为零，即$\int_L P dx + Qdy = 0$；

（2）在$D$内$\int_{\overset{\frown}{AB}} Pdx+Qdy$与路径无关，只与起点$A$和终点$B$有关；

（3）在$D$上一定存在函数$u(x, y)$使得被积式$Pdx + Qdy$是$u(x, y)$的全微分，即$du(x, y) = Pdx+Qdy$；

（4）在$D$内任一点$(x, y)$处，恒有$\frac{\partial Q}{\partial x} = \frac{\partial P}{\partial y}$。

证：采用==循环证法==，即$(1) \Longrightarrow (2) \Longrightarrow (3) \Longrightarrow (4) \Longrightarrow (1)$。

$(2) \Longrightarrow (3)$使用偏导数的定义，$(3) \Longrightarrow (4)$利用混合偏导数连续，则两个混合偏导数相等。



## 第4节 第一类曲面积分

假定曲面$\Sigma$是有界的且是光滑的。

### 一、第一类曲面积分的定义

==第一类曲面积分==：设$\Sigma$是光滑曲面，$f(x, y, z)$是定义在$\Sigma$上的有界函数，将$\Sigma$任意地分成$n$个子曲面块$\Delta S_i, (i=1,2,\cdot,n)$，它的面积也记为$\Delta S_i$，$\lambda_i$表示$\Delta S_i$的直径，$\lambda = \max\{\lambda_1, \lambda_2, \cdots, \lambda_n\}, \forall_{N_i}(\xi_i, \eta_i, \zeta_i) \in \Delta S_i$，作和式$I_n = \sum_{i=1}^n f(\xi_i, \eta_i, \zeta_i)\Delta S_i$，如果当$\lim_{\lambda \to 0} I_n = I$，且$I$的值与对$\Sigma$的分法无关，也与点$N_i$在$\Delta S_i$的取法无关，则称$I$为$f(x, y, z)$在$\Sigma$上的第一类曲面积分，或对面积的曲面积分。记为$\iint_\Sigma f(x, y, z)dS$，$dS$称为曲面面积元素，$\Sigma$称为积分曲面。



### 二、第一类曲面积分的计算

设曲面$\Sigma$的方程：$z = z(x, y)$，把$\Sigma$投影到$xoy$面上，得区域$D_{xy}$。设$z = z(x, y)$在$D_{xy}$上具有连续的一阶偏导数$z_x^\prime, z_y^\prime$，$\iint_\Sigma f(x, y, z)dS = \lim_{\lambda \to 0}\sum_{i=1}^n f(\xi_i, \eta_i, \zeta_i)\Delta S_i$，子曲面块

$\Delta S_i$在$xoy$面投影区域$(\Delta \sigma_i)_{xy}$，点$N_i(\xi_i, \eta_i, \zeta_i) \in \Delta S_i$，计算$\Delta S_i$：$\Delta S_i = \iint_{\Delta (\sigma_i)_{xy}}\sqrt{1+(z_x^\prime(x, y))^2+(z_y^\prime(x, y))^2}dxdy \\ = \sqrt{1+(z_x^\prime(\xi_i^\prime, \eta_i^\prime))^2+(z_y^\prime(\xi_i^\prime, \eta_i^\prime))^2}(\Delta \sigma_i)_{xy}$

（应用了二重积分的中值定理），取$\xi_i = \xi_i^\prime, \eta_i = \eta_i^\prime, \zeta_i = z(\xi_i^\prime, \eta_i^\prime)$，所以$\iint_\Sigma = f(x, y, z)dS = \lim_{\lambda \to 0}\sum_{i=1}^n f(\xi_i^\prime, \eta_i^\prime, z(\xi_i^\prime, \eta_i^\prime))\sqrt{1+(z_x^\prime(\xi_i^\prime, \eta_i^\prime))^2+(z_y^\prime(\xi_i^\prime, \eta_i^\prime))^2}(\Delta \sigma_i)_{xy}$

令$d_i$表示$(\Delta \sigma_i)_{xy}$的直径，令$d = \max\{d_1, d_2, \cdots, d_n\}$，当$\lambda \to 0$时，有$d \to 0$，$\iint_\Sigma = f(x, y, z)dS = \lim_{d \to 0}\sum_{i=1}^n f(\xi_i^\prime, \eta_i^\prime, z(\xi_i^\prime, \eta_i^\prime))\sqrt{1+(z_x^\prime(\xi_i^\prime, \eta_i^\prime))^2+(z_y^\prime(\xi_i^\prime, \eta_i^\prime))^2}(\Delta \sigma_i)_{xy} \\ = \iint_{D_{xy}}f(x, y, z(x, y))\sqrt{1+(z_x^\prime(x, y))^2+(z_y^\prime(x, y))^2}(\Delta \sigma_i)_{xy}$



## 第5节 第二类曲面积分

### 一、有向曲面

==双侧曲面==：上侧、下侧，左侧、右侧，前侧、后侧，内侧、外侧。

==有向曲面==：取定曲面的$\Sigma$法矢量的方向，亦即选定了侧的曲面。

==曲面的投影==：曲面$\Sigma$（有向），在$\Sigma$上任取一小块有向曲面$\Delta S$，假设$\Delta S$上各点处的法矢量与$z$轴正向夹角$\gamma$的余弦$\cos\gamma$有相同的符号，$\Delta S \cos\gamma$称为$\Delta S$在$xoy$面上的有向投影。同理有其他两个面的有向投影。



==第二类曲面积分==：设有矢量场$\overset{\rightarrow}{A} = \overset{\rightarrow}{A}(x, y, z) = P(x, y, z)\overset{\rightarrow}i + Q(x, y, z)\overset{\rightarrow}j + R(x, y, z)\overset{\rightarrow}k$，$\Sigma$是矢量场中光滑的有向曲面，指定$\Sigma$的一侧为正侧。将曲面$\Sigma$任意地分成$n$个子曲面块：$\Delta S_1, \Delta S_2, \cdots, \Delta S_n$，它们的面积仍为$\Delta S_i(i=1,2,\cdots,n)$，记$\Delta S_i$的直径为$\lambda_i$，记$\lambda = \max\{\lambda_1, \lambda_2, \cdots, \lambda_n\}$，$\forall_{N_i(\xi_i, \eta_i, \zeta_i)} \in \Delta S_i$，$\Sigma$在点$N_i$的单位法矢量为$\overset{\rightarrow}{n_i} = \cos\alpha_i \overset{\rightarrow}{i}+\cos\beta_i \overset{\rightarrow}{j}+\cos\gamma_i \overset{\rightarrow}{k}$，其中$\alpha_i, \beta_i, \gamma_i$是$\overset{\rightarrow}{n_i}$的方向角。作点积：$\overset{\rightarrow}{A}(\xi_i, \eta_i, \zeta_i) \cdot \overset{\rightarrow}{n_i} \Delta S_i$，作和式$I_n = \sum_{i=1}^n \overset{\rightarrow}{A}(\xi_i, \eta_i, \zeta_i) \cdot \overset{\rightarrow}{n_i} \Delta S_i$，如果$\lim_{\lambda \to 0}I_n = \lim_{\lambda \to 0} \sum_{i=1}^n \overset{\rightarrow}{A}(\xi_i, \eta_i, \zeta_i) \cdot \overset{\rightarrow}{n_i} \Delta S_i$存在，记为$I$，$I$与对$\Sigma$的分法无关，同时$I$与点$N_i$在$\Delta S_i$的取法无关，则称此极限为$\overset{\rightarrow}{A}(x, y, z)$沿着有向曲面$\Sigma$正侧的第二类曲面积分，记为：$\iint_\Sigma \overset{\rightarrow}{A}(x, y, z) \cdot \overset{\rightarrow}{n}ds = \lim_{\lambda \to 0} \sum_{i=1}^n \overset{\rightarrow}{A}(\xi_i, \eta_i, \zeta_i) \cdot \overset{\rightarrow}{n_i} \Delta S_i$。



用坐标表示：

因为$\overset{\rightarrow}{A} = \overset{\rightarrow}{A}(x, y, z) = P(x, y, z)\overset{\rightarrow}i + Q(x, y, z)\overset{\rightarrow}j + R(x, y, z)\overset{\rightarrow}k$，$\overset{\rightarrow}{A}(\xi_i, \eta_i, \zeta_i) = P(\xi_i, \eta_i, \zeta_i)\overset{\rightarrow}i + Q(\xi_i, \eta_i, \zeta_i)\overset{\rightarrow}j + R(\xi_i, \eta_i, \zeta_i)\overset{\rightarrow}k$，$\overset{\rightarrow}{n_i} = \cos\alpha_i \overset{\rightarrow}{i}+\cos\beta_i \overset{\rightarrow}{j}+\cos\gamma_i \overset{\rightarrow}{k}$，$\overset{\rightarrow}{A}(\xi_i, \eta_i, \zeta_i) \cdot \overset{\rightarrow}{n_i} = P(\xi_i, \eta_i, \zeta_i)\cos\alpha_i + Q(\xi_i, \eta_i, \zeta_i)\cos\beta_i + R(\xi_i, \eta_i, \zeta_i)\cos\gamma_i$，

$\iint_\Sigma \overset{\rightarrow}{A}(x, y, z) \cdot \overset{\rightarrow}{n}ds \\ = \lim_{\lambda \to 0} \sum_{i=1}^n [P(\xi_i, \eta_i, \zeta_i)\cos\alpha_i\Delta S_i + Q(\xi_i, \eta_i, \zeta_i)\cos\beta_i\Delta S_i + R(\xi_i, \eta_i, \zeta_i)\cos\gamma_i\Delta S_i]$

称$d\overset{\rightarrow}{s} = \overset{\rightarrow}{n}ds = (\cos\alpha ds) \overset{\rightarrow}{i}+(\cos\beta ds)\overset{\rightarrow}{j}+(\cos\gamma ds) \overset{\rightarrow}{k}$为有向曲面面积微元矢量。记$\cos\alpha ds = dydz, \cos\beta ds = dzdx, \cos\gamma ds = dxdy$，则$d\overset{\rightarrow}{s} = \overset{\rightarrow}{n}ds = (dydz) \overset{\rightarrow}{i}+(dzdx)\overset{\rightarrow}{j}+(dxdy) \overset{\rightarrow}{k}$，$\iint_\Sigma \overset{\rightarrow}{A}(x, y, z) \cdot \overset{\rightarrow}{n}ds = \iint_\Sigma \overset{\rightarrow}{A}(x, y, z) \cdot \overset{\rightarrow}{ds} \\ = \iint_\Sigma \overset{\rightarrow}{A}(x, y, z) \cdot [(dydz) \overset{\rightarrow}{i}+(dzdx)\overset{\rightarrow}{j}+(dxdy) \overset{\rightarrow}{k}] \\ = \iint_\Sigma P(x, y, z)dydz + Q(x, y, z)dzdx + R(x, y, z)dxdy$

其中$\iint_\Sigma P(x, y, z)dydz = \lim_{\lambda \to 0} \sum_{i=1}^n P(\xi_i, \eta_i, \zeta_i)\cos\alpha_i\Delta S_i$。



==应用==：

如果矢量场是流速场，$\overset{\rightarrow}{v}(x, y, z) = P\overset{\rightarrow}{i} + Q\overset{\rightarrow}{j} + R\overset{\rightarrow}{k}$，则$\iint_\Sigma \overset{\rightarrow}{v}\overset{\rightarrow}{ds} = \iint_\Sigma Pdydz + Qdzdx + Rdxdy$表示流速场中流体穿过$\Sigma$正侧的流量。

如果矢量场是磁场，磁感应强度为$\overset{\rightarrow}{B}(x, y, z) = P\overset{\rightarrow}{i} + Q\overset{\rightarrow}{j} + R\overset{\rightarrow}{k}$，$\iint_\Sigma \overset{\rightarrow}{B}\overset{\rightarrow}{ds} = \iint_\Sigma Pdydz + Qdzdx + Rdxdy$表示穿过有向曲面$\Sigma$正侧的磁通量。

一般地说，$\iint_\Sigma \overset{\rightarrow}{A}(x, y, z) \cdot \overset{\rightarrow}{ds} = \iint_\Sigma P(x, y, z)dydz + Q(x, y, z)dzdx + R(x, y, z)dxdy$称为矢量场穿$\overset{\rightarrow}{A}(x, y, z)$穿过$\Sigma$正侧的通量。



用$\Sigma$表示有向曲面的正侧，用$\Sigma^-$表示有向曲面的负侧，则$\iint_\Sigma \overset{\rightarrow}{A}(x, y, z) \cdot \overset{\rightarrow}{ds} = -\iint_{\Sigma^-} \overset{\rightarrow}{A}(x, y, z) \cdot \overset{\rightarrow}{ds}$



==两类曲面积分的关系==：

第一类曲面积分：$\iint_\Sigma = f(x, y, z)dS$

第二类曲面积分：$\iint_\Sigma \overset{\rightarrow}{A}(x, y, z) \cdot \overset{\rightarrow}{ds}$

==关系==：由于$dydz = \cos\alpha ds, dzdx = \cos\beta ds, dxdy = \cos\gamma ds$，$\iint_\Sigma \overset{\rightarrow}{A}(x, y, z) \cdot \overset{\rightarrow}{n}ds = \iint_\Sigma Pdydz+Qdzdx+Rdxdy \\ = \iint_\Sigma (P\cos\alpha+Q\cos\beta+R\cos\gamma)dS$。



### 三、第二类曲面积分计算法

设有向曲面$\Sigma: z = z(x, y)$，它在$xoy$面上投影区域$D_{xy}$，$z = z(x, y)$在$D_{xy}$上具有连续的一阶偏导数，$\gamma$为$\Sigma$上的法矢量与$z$轴正向的夹角，$R(x, y, z)$在$\Sigma$上连续。

（1）当$\Sigma$取上侧为正侧，则$0 \le \gamma < \frac{\pi}{2}, \cos \gamma > 0$，有$\iint_\Sigma R(x, y, z)dxdy = \iint_\Sigma R(x, y, z)\cos\gamma ds$，由前面的假设有：$\cos\gamma = \frac{1}{\sqrt{1+z_x^2+z_y^\prime}}$，所以$\iint_\Sigma R(x, y, z)dxdy = \iint_\Sigma R(x, y, z)\cos\gamma ds = \iint_\Sigma R(x, y, z) \frac{1}{\sqrt{1+z_x^2+z_y^2}} ds \\ = \iint_{D_{xy}}R[x, y, z(x, y)]\frac{1}{\sqrt{1+z_x^2+z_y^2}}\sqrt{1+z_x^2+z_y^2}dxdy \\ = \iint_{D_{xy}} R[x, y, z(x, y)]dxdy$

（2）当$\Sigma$取下侧为正侧，曲面$\Sigma$下侧的法矢量与$z$轴正向的夹角$\frac{\pi}{2} < \gamma \le \pi, \cos\gamma < 0$，$\cos\gamma = -\frac{1}{\sqrt{1+z_x^2+z_y^2}}$，从而$\iint_\Sigma R(x, y, z)dxdy = \iint_\Sigma R(x, y, z)\cos\gamma ds = \iint_\Sigma R(x, y, z) (-\frac{1}{\sqrt{1+z_x^2+z_y^2}}) ds \\ = -\iint_{D_{xy}}R[x, y, z(x, y)]\frac{1}{\sqrt{1+z_x^2+z_y^2}}\sqrt{1+z_x^2+z_y^2}dxdy \\ = -\iint_{D_{xy}} R[x, y, z(x, y)]dxdy$

（3）当$\Sigma$是母线垂直于$xoy$面的柱面时，$\gamma = \frac{\pi}{2}, \cos\gamma = 0$，$\iint_\Sigma R(x, y, z)dxdy = \iint_\Sigma R(x, y, z)\cos\gamma ds = 0$。



## 第6节 高斯公式，曲面积分与曲面无关的条件

### 一、高斯公式

==空间区域的连通性==：如果在空间区域$\Omega$内，任何一张简单的封闭曲面所围成的区域全都属于$\Omega$，则称$\Omega$为二维的单连通域。如果在空间区域$\Omega$内，任意一条闭曲线都可以张成一片完全属于$\Omega$的曲面（圈起来的曲面），则称$\Omega$是一维的单连通域。

==高斯公式==：设空间中有界闭域$\Omega$是二维，其边界曲面为$\Sigma$，函数$P(x, y, z), Q(x, y, z), R(x, y, z)$在$\Omega$内及$\Omega$上具有连续的一阶偏导数，则$\iiint_\Omega (\frac{\partial P}{\partial x}+\frac{\partial Q}{\partial y}+\frac{\partial R}{\partial z}) dxdydz = \oiint_\Sigma Pdydz + Qdzdx + Rdxdy \\ = \oiint_\Sigma (P\cos\alpha+Q\cos\beta+R\cos\gamma)ds$

其中$\Sigma$取外侧，$\cos\alpha, \cos\beta, \cos\gamma$是$\Sigma$外侧的法线的方向余弦。

证明：（等式左右两端各项分别证明相等，设空间$\Omega$由上半曲面$\Sigma_1$，下半曲面$\Sigma_2$，柱面$\Sigma_3$共同围成）假定穿过$\Omega$内部与$z$轴平行的直线与$\Omega$的边界曲面交点恰好为两个，要证$\iiint_\Omega \frac{\partial R}{\partial z} dxdydz = \oiint_\Sigma R dxdy$。

$\iiint_\Omega \frac{\partial R}{\partial z} dxdydz = \iint_{D_{xy}} [\int_{z_1(x,y)}^{z_2(x,y)} \frac{\partial R}{\partial z}dz]dxdy = \iint_{D_{xy}}R(x, y,z)|_{z_1(x,y)}^{z_2(x, y)}dxdy \\ = \iint_{D_{xy}}R[x, y, z_2(x, y)]dxdy - \iint_{D_{xy}}R[x, y, z_1(x, y)]dxdy$

$\oiint_\Sigma Rdxdy = \iint_{\Sigma_2}Rdxdy+\iint_{\Sigma_1}Rdxdy+\iint_{\Sigma_3}Rdxdy \\ = \iint_{D_{xy}}R[x, y, z_2(x, y)]dxdy - \iint_{D_{xy}}R[x, y, z_1(x, y)]dxdy + 0$

所以$\iiint_\Omega \frac{\partial R}{\partial z} dxdydz = \oiint_\Sigma R dxdy$。同理$\iiint_\Omega \frac{\partial P}{\partial x} dxdydz = \oiint_\Sigma P dydz, \iiint_\Omega \frac{\partial Q}{\partial y} dxdydz = \oiint_\Sigma Q dzdx$

因而公式得证。

将公式进行推广，当穿过$\Omega$内部与$z$轴平行的直线与$\Omega$的边界曲面交点多于两个时，公式同样成立。

### 二、曲面积分与路径无关的条件

==定理==：设$\Omega$是空间二维单连通域，$P(x, y, z), Q(x, y, z), R(x, y, z)$在$\Omega$上具有一阶连续的偏导数，则以下三个命题是等价的。

（1）在$\Omega$内，$\frac{\partial P}{\partial x} + \frac{\partial Q}{\partial y} + \frac{\partial R}{\partial z} = 0$

（2）对全部包含在$\Omega$内的一个封闭曲面$\Sigma$，有$\oiint_\Sigma Pdydz+Qdzdx+Rdxdy=0$

（3）对全部包含在$\Omega$内的非封闭曲面$\Sigma_1$的曲面积分$\iint_{\Sigma_1} Pdydz+Qdzdx+Rdxdy$只与曲面$\Sigma_1$的边界曲线有关，而与曲面$\Sigma_1$无关。



## 第7节 Stokes公式，空间曲线积分与路径无关的条件

### 一、Stokes公式

==定理==：设$P(x, y, z), Q(x, y, z), R(x, y, z)$在包含曲面$\Sigma$的某一空间区域$\Omega$内具有一阶连续的偏导数，则$\iint_\Sigma (\frac{\partial R}{\partial y}-\frac{\partial Q}{\partial z})dydz+(\frac{\partial P}{\partial z}-\frac{\partial R}{\partial x})dzdx+(\frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y})dxdy = \oint_L Pdx+Qdy+Rdz$

其中$L$为有向曲面$\Sigma$的正向边界曲线，$L$与$\Sigma$的方向按右手法则确定。

为方便记忆，假如把$\frac{\partial R}{\partial y}$看作是$\frac{\partial}{\partial y}$乘以一个函数$R$，即$\frac{\partial R}{\partial y} = \frac{\partial}{\partial y} \cdot R$，
$$
\oint_L Pdx+Qdy+Rdz = \iint_\Sigma \left|\begin{array}{ccc}dydz &dzdx &dxdy \\ \frac{\partial}{\partial x} &\frac{\partial}{\partial y} &\frac{\partial}{\partial z} \\ P &Q &R\end{array}\right| = \iint_\Sigma \left|\begin{array}{ccc}\cos\alpha ds &\cos\beta ds &\cos\gamma ds \\ \frac{\partial}{\partial x} &\frac{\partial}{\partial y} &\frac{\partial}{\partial z} \\ P &Q &R\end{array}\right|
$$

### 二、空间曲线积分与路径无关的条件：

==定理==：设$P(x, y, z), Q(x, y, z), R(x, y, z)$及其偏导数在一维单连通域$\Omega$上连续，则以下四个命题等价：

（1）在$\Omega$内，曲线积分$\int_{\overset{\frown}{AB}} Pdx+Qdy+Rdz$与路径无关，只与起点$A$和终点$B$有关

（2）在$\Omega$内，沿任意一条封闭曲线$L$的积分为零，即$\oint_L Pdx+Qdy+Rdz=0$

（3）在$\Omega$内任一点$(x, y, z)$处，恒有$\frac{\partial R}{\partial y}-\frac{\partial Q}{\partial z} = 0, \frac{\partial P}{\partial z}-\frac{\partial R}{\partial x} = 0, \frac{\partial Q}{\partial x} - \frac{\partial P}{\partial y} = 0$

（4）在$\Omega$中，存在函数$u(x, y, z)$，$du(x, y, z) = Pdx+Qdy+Rdz$



