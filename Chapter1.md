[TOC]

# 第一章 函数

## 第1节 函数的概念

### 一、区间与邻域

常用数集：

* 自然数集：N；
* 整数集：Z；
* 有理数集：Q；
* 实数集：R。

建立数轴后：

```sequence
实数->数轴上的点:一一对应
数轴上的点->实数:一一对应
```

建立某一实数集A与数轴上某一区间的对应：

* 开区间：设有数a，b，$a < b$，称实数集$\{x|a < x < b\}$为开区间，记为$(a, b)$。即$(a, b) = \{x|a < x < b\}$，a称为$(a, b)$的左端点，b称为$(a, b)$的右端点，$a\notin(a, b), b\notin(a, b)$。
* 闭区间：$[a, b] = \{x|a \leq x \leq b\}$，$a\in[a, b], b\in[a, b]$。
* 半开区间：$[a, b) = \{x|a \leq x < b\}$，$a\in[a, b), b\notin[a, b)$；$(a, b] = \{x|a < x \leq b\}$，$a\notin(a, b], b\in(a, b]$。

其中，a，b都是实数，称$(a, b)$，$[a, b]$，$[a, b)$，$(a, b]$为==有限区间==，称==$b-a$==为区间长度。

记号：“$+\infty$”表示正无穷大；“$-\infty$”表示负无穷大（==仅仅是一个记号而已==）

区间:$[a, +\infty) = \{x|a \leq x\}$, $(a, +\infty) = \{x|a < x\}$, $(-\infty, b] = \{x|x \leq b\}$, $(-\infty, b) = \{x| x < b\}$。

* 邻域：设有两个数，a，$\delta$, ($\delta > 0$), 则称实数集$\{x|a - \delta < x < a + \delta\}$为点a的$\delta$邻域， 记作$N(a, \delta)$，称$\delta > 0$为邻域$N(a, \delta)$的半径，a为$N(a, \delta)$的中心。
* 去心邻域：把$N(a, \delta)$的中心点a去掉，称为点a的去心邻域，记作$N(\hat{a}, \delta) = \{x|0 < |x - a| < \delta\} = N(a, \delta) \backslash \{a\}$

### 二、 函数的概念

例1、设圆的半径为$x (x > 0)$，它的面积$A = \pi x^2$，当x在$(0, +\infty)$内任取一个数值$\forall{x} \in(0, +\infty)$，由关系式$A = \pi x^2$就可以确定A的对应数值。

例2、设有半径为r的圆，作圆的内接正n边形，每一边对应的圆心角$\alpha = \frac{2\pi } {n}$，周长$S_n = 2nr\sin\frac{\pi}{n}$（正内接n边形的边数为n，周长为$S_n$），当边数n在自然数集$N(n \geq 3)$，任取一个数，通过关系式$S_n = 2nr\sin\frac{\pi}{n}$就会有一个对应的$S_n$数值。

* 函数的定义：设有数集X， Y, $f$是一个确定对应法则， $\forall{x} \in X$，通过对应法则$f$都有唯一的$y \in Y$与x对应，记为$f(x) = y$，称$f$为定义在X上的函数，其中X称为$f$的定义域，常记为$D_f$，x记为自变量，y记为因变量。当x遍取X中的一切数时，那么与之对应的y值构成一个数集：$V_f = \{y|y = f(x), x \in X\}$，称$V_f$为函数$f$的值域。

注意：

1. 一个函数由x与y的==对应法则$f$==与x的==取值范围X==所确定，把“对应法则$f$”，“定义域”称为函数定义的==两个要素==。
2. 函数值域是定义域和对应法则确定的。
3. 确定函数定义域时，注意函数如果有实际意义，依据实际问题是否有意义来确定。函数不代表某实际问题时，函数定义域为自变量所能取得的使得函数$y = f(x)$成立的一切实数构成的数集。

* 函数的几何意义：设函数$y = f(x)$，定义域为$D_f$，$\forall{x \in D_f}$，对应函数值$y = f(x)$在xoy平面上得点（x，y），当x遍取$D_f$中的一切实数时，就得到点集$P = \{(x, y)|y = f(x), x \in D_f\}$，点集P称为函数$y = f(x)$的==图形==。

### 三、函数的几个简单性质

1. 函数的有界性

若$\exist{M} > 0$，使得$|f(x)| \leq M, x \in I$，则称$y = f(x)$在区间$I$上有界，否则，则称$f(x)$在$I$上无界，即对于任何正数$M > 0$（无论多么大），总$\exist{x_1} \in I, s.t. |f(x_1)| > M $。例如：$y = \sin(x)$在$I = (-\infty, +\infty)$上有界（$\because|\sin(x)| \leq 1, x \in (-\infty, +\infty)$）；又例如：$y = \frac{1}{1 + x^2}$在$(-\infty, +\infty)$上有界。

证明：$y = \frac{1}{x}$在(0, 1)内无界。

证：对给定M > 0（不妨设M > 1），无论M多么大，必存在$x_1 = \frac{1}{2M}\in (0, 1)$使$f(x_1) = \frac{1}{\frac{1}{2M}} = 2M > M$。

函数的上界、下界的定义：若$\exist{M}$（==不局限为正数==），$s.t. f(x) \leq M, \forall{x} \in I$，称$f(x)$在区间$I$上有上界，任何一个数$N > M$，N也是$f(x)$的一个上界。若$\exist{P}$，$s.t. f(x) \geq P, \forall{x} \in I$，称$f(x)$在区间$I$上有下界，任何一个数$Q < P$，Q也是f(x)的一个下界。

证明：==若$f(x)$在$I$上有界 $\Longleftrightarrow$ $f(x)$在$I$上既有上界，也有下界。==

证：设$f(x)$在$I$上有界，根据定义$\exist{M} > 0, s.t.$ $|f(x)| \leq M,\forall{x} \in I$，即$-M \leq f(x) \leq M$，因此，$f(x)$既有下界$-M$，也有上界$M$。

设$f(x)$在$I$上既有下界$m$，也有上界$n$，即$m \leq f(x) \leq n$。如果$m = n = 0 \Longrightarrow f(x) \equiv 0, \forall{x} \in I, \therefore f(x)$在$I$上有界；如果$m,n$不同时为零，取$M = \max\{|m|, |n|\}$，则有==$-M \leq -|m| \leq m \leq f(x) \leq n \leq |n| \leq M $==，即$-M \leq f(x) \leq M, |f(x| \leq M, \forall(x) \in I, \therefore f(x)$在$I$上有界。

2. 函数的单调性

若$f(x)$在区间$I$上对任何$x_1, x_2 \in I$，且$x_1 < x_2$，==恒有==$f(x_1) < f(x_2)$，则称$f(x)$在区间$I$上是严格单调增的；若$x_1 < x_2$，==恒有==$f(x_1) \leq f(x_2)$，则称$f(x)$在区间$I$上是广义单调增的（或称单调增，非减的）；

若$x_1 < x_2$，==恒有==$f(x_1) > f(x_2)$，则称$f(x)$在区间$I$上是严格单调减的；类似地，有广义单调减（或称单调减，非增的）。

例1、设有函数$y = x^2, D_f = (-\infty, +\infty)$。在$(0, +\infty)$上单增， 在$(-\infty, 0)$上单减。

例2、==取整函数== $y = [x]$为非减函数（广义单增、单调增）。

3. 函数的奇偶性

若函数$f(x)$在==关于原点对称的区间==$I$上满足$f(-x) = f(x)$，则称$f(x)$为偶函数；满足$f(-x) = -f(x)$，则称$f(x)$为奇函数。偶函数图形关于$y$轴对称，奇函数图形关于原点对称。

4. 函数的周期性

   设函数$f(x)$的定义域为$D_f$，如果存在==非零常数==$T$，$s.t.$对==任意的==$x \in D_f$，有$(x \pm T) \in D_f$，且$f(x + T) = f(x)$，则称$f(x)$为==周期函数==，$T$为$f(x)$的==周期==。

### 四、复合函数与反函数

1. 复合函数

例1、设函数$y = \sqrt{u}$，$u = 1 - x^2$，把$u = 1 - x^2$代入$y = \sqrt{u}$中，得到$y = \sqrt{1 - x^2}$，称为由函数$y = \sqrt{u}$与函数$u = 1 - x^2$复合而成的复合函数。

==一般定义==：

设函数$y = f(u)$是数集$Y$上的函数（$Y$是$y = f(u)$的定义域），$u = \varphi(x)$的定义域为$X$，值域为$Y_{\varphi}$ ，且$Y_{\varphi} \not = \phi, Y_{\varphi} \subseteq Y$，这时$\forall{x} \in X$，通过$u$都有唯一的$y$值与之对应，从而在数集$X$上产生一个新函数，用$f \circ \varphi$表示，称$f \circ \varphi为$$X$上的复合函数。
$$
y = f[\varphi(x)]
$$

 $y = f[\varphi(x)]$的定义域由$u = \varphi(x)$的定义域中使函数$u = \varphi(x)$的值域$Y_\varphi$满足$Y_\varphi \subseteq Y$的那一部分实数构成的。

例2、设$f(x) = \frac{x^2 + 1}{x ^2 - 1}$，$\varphi(x) = \frac{1}{1 + x}$，求$f[\varphi(x)]$，并确定定义域。

解：$f[\varphi(x)] = \frac{[\varphi(x)]^2 + 1}{[\varphi(x)]^2 - 1} = \frac{(\frac{1}{1 + x})^2 + 1}{(\frac{1}{1 + x})^2 - 1} = -\frac{x^2 + 2x + 2}{x(x + 2)}$，当$x \neq -1$，且$x \neq 0, x\neq -2$时，$f[\varphi(x)]$有定义，$f[\varphi(x)]$的定义域为：$(-\infty, -2) \cup (-2, -1) \cup (-1, 0) \cup (0, +\infty) $ 。

2. 反函数

设有函数$y = f(x)$，定义域为$D_f$，值域为$V_f$，$\forall{y} \in V_f$，至少可以确定一个$x \in D_f$，$s.t. f(x) = y$。如果把$y$看作自变量，把$x$看作因变量，由函数的概念，可以得到一个新函数，记为$x = f^{-1}(y)$，称为$y = f(x)$的反函数。反函数的定义域为$V_f$，值域为$D_f$，把$y = f(x)$称为==直接函数==。

注意：

1. 虽然直接函数$y = f(x)$是单值的，但反函数$x = f^{-1}(y)$不一定是单值的。

例如：$y = x^2, D_f = (-\infty, +\infty), V_f = [0, +\infty], x = f^{-1}(y)$不是单值的。$\forall{y} \in [0, +\infty), y \ge 0$，得到$x = \pm\sqrt{y}$有两个值$-\sqrt{y}$和$+\sqrt{y}$的双值函数，可取单值支$x = \sqrt{y}$。

2. 如果直接函数$y = f(x)$严格单调， 则其反函数$x = f^{-1}(y)$ 也是单值单调。

 	3. 直接函数$y = f(x)$与反函数$x = f^{-1}(y)$图形相同。习惯上以$x$表示自变量，$y$表示因变量，则反函数记为$y = f^{-1}(x)$。这时，$y = f(x)$与$y = f^{-1}(x)$的图形关于直线$y = x$对称。

例3、设
$$
y = f(x) = \left\{\begin{array}{cc} &\frac{x}{2} &-2 \lt x \lt 1 \\ &x^2 &1 \le x \le 2\end{array}\right\}
$$
求反函数$y = f^{-1}(x)$。

解：当$-2 \leq x \lt 1$时，$y = \frac{x}{2}, -1 \lt y \lt \frac{1}{2}, x = 2y$，定义域$-1 \lt y \lt \frac{1}{2}$；当$1 \leq x \leq 2$时，$y = x^2, 1 \leq y \leq 4, x = \pm\sqrt{y}$，定义域$-1 \lt y \lt \frac{1}{2}$，定义域$1 \leq y \leq 4$。故反函数：
$$
y = f^{-1}(x) = \left\{\begin{array}{cc} &2x &-1 \lt x \lt \frac{1}{2} \\ &\sqrt{x} &1 \le x \le 4\end{array}\right\}
$$

## 第2节 初等函数

### 一、基本初等函数

6类函数：幂函数、指数函数、对数函数、三角函数、反三角函数以及常量

### 二、初等函数

由基本初等函数经过==有限次==的`四则运算`和==有限次==的`复合步骤`所构成的能够用一个数学式子表达的函数，称为初等函数。

例如：$\arcsin \sqrt {1 - x^2}$，$y = \ln (x + e^x)$

例1、分析$y = \ln(1 + \sqrt{x})$的结构。

解：$y = \ln {u}, u = 1 + \sqrt {x} = 1 + x^{\frac{1}{2}}$，令$u = 1 + x^{\frac{1}{2}}, v = 1, w = x^{\frac{1}{2}}, \therefore y = \ln {u}, u = v + w, v = 1, w = x^{\frac{1}{2}}$。

### 三、双曲函数

双曲正弦函数：$sh \  x = \frac{e^x - e^{-x}}{2}$，双曲余弦函数：$ch \  x = \frac{e^x + e^{-x}}{2}$，双曲正切函数：$th \ x = \frac{sh \ x}{ch \ x} = \frac{e^x - e^{-x}}{e^x + e^{-x}}$。

以上函数与三角函数有类似的性质：
$$
ch ^2 \ x - sh^2 \ x = 1
$$

$$
sh \ 2x = 2sh \ x \ ch \ x
$$

$$
ch \ 2x = ch^2 \ x + sh^2 \ x
$$

反双曲函数及其推导：

反双曲正弦函数：$arsh \  x$；反双曲余弦函数：$arch \ x$；反双曲正切函数$arth \ x$。

反双曲正弦函数的推导：

解：已知反双曲正弦函数的表达式为$y = arsh \ x$，则$x = sh \ y = \frac{e^y - e^{-y}}{2}$，令$u = e^y$，则有$2x = u - \frac{1}{u}$，将等式两边同乘$u$可得：$u^2 - 2ux - 1 = 0$，由二次方程求根公式，得：$u = \frac{2x \pm \sqrt{4x^2 + 4}}{2} = x \pm \sqrt{x^2 + 1}$，即$e^y = x \pm \sqrt{x^2 + 1}, \because e^y > 0, \therefore e^y = x + \sqrt{x^2 + 1}, \therefore y = arsh \ x= \ln{(x + \sqrt{x^2 + 1})}$

类似方法可以推出：
$$
arch \ x = ln{(x + \sqrt{x^2 -1})}
$$

$$
arth \ x = \frac{1}{2} \ln{\frac{1 + x}{1 - x}}
$$

