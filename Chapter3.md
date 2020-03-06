[toc]

# 第三章 导数与微分

1. 由于自变量$x$的变化引起函数$y = f(x)$变化的“快慢”问题——函数的变化率——导数。
2. 由于自变量的微小改变（增量$|\Delta x|$很小时）引起$y = f(x)$的改变量$\Delta y$的近似值问题，微分问题。
3. 求导数或求微分。

## 第1节 导数概念

### 一、导数定义

==定义1==：设$y = f(x)$在$N(x_0, \delta), (\delta > 0)$内有定义，当自变量$x$在$x_0$点有增量$\Delta x, x_0 + \Delta x \in N(x_0, \delta)$，函数$y = f(x)$相应的增量$\Delta y = f(x_0 + \Delta x) - f(x_0)$，如果$\lim_{\Delta x \to 0}\frac{\Delta y}{\Delta x} = \lim_{\Delta x \to 0}\frac{f(x_0 + \Delta x) - f(x_0)}{\Delta x}$存在，则称$y = f(x)$在$x_0$点可导，并称此极限为$y = f(x)$在$x_0$点的导数，记为$y^\prime |_{x = x_0}, f^\prime(x_0), \frac{d_y}{d_x} |_{x = x_0}, \frac{d_{f(x)}}{d_x} |_{x = x_0}$，即$f^\prime(x_0) = \lim_{\Delta x \to 0}\frac{f(x_0 + \Delta x)-f(x_0)}{\Delta x}$。

==导数定义的另一种形式==：记$x = x_0 + \Delta x, \Delta x = x - x_0$，当$\Delta x \to 0$时$x \to x_0$，$\Delta y = f(x_0 + \Delta x) - f(x_0) = f(x) - f(x_0)$，$f^\prime(x_0) = \lim_{\Delta x \to 0}\frac{f(x_0 + \Delta x) - f(x_0)}{\Delta x} = \lim_{x \to x_0}\frac{f(x) - f(x_0)}{x - x_0}$。



若$y = f(x)$在$x_0$点可导，记为$f(x) \in D\{x_0\}$；若$y = f(x)$在$(a, b)$每一点处都可导，则称$y = f(x)$在$(a, b)$内可导，记为$f(x) \in D(a, b)$；若$y = f(x)$在区间$I$上每一点处都可导，则称$y = f(x)$在$I$内可导，记为$f(x) \in D(I)$。

若$y = f(x)$在$(a, b)$内可导，$\forall_x \in (a, b)$，就有$f^\prime(x)$与$x$对应，由函数的定义，可知$f^\prime(x)$是定义在区间$(a, b)$的函数，$f^\prime(x)$为==导函数==，简称为==导数==。



例1、求$y = \frac{1}{x^2},(x \neq 0)$的导数。

解：$y = \frac{1}{x^2}$的定义域为$(-\infty, 0) \cap (0, +\infty)$。$\forall_x \in (-\infty, 0) \cap (0, +\infty)$，自变量有增量$\Delta x, x + \Delta x \in (-\infty, 0) \cap (0, +\infty)$，函数$y = \frac{1}{x^2}$对应得增量$\Delta y = \frac{1}{(x + \Delta x)^2} - \frac{1}{x^2} = \frac{-2x \Delta x - (\Delta x)^2}{x^2(x + \Delta x)^2}$，作比值$\frac{\Delta y}{\Delta x} = \frac{-2x - \Delta x}{x^2(x + \Delta x)^2}$，求极限$\lim_{\Delta x \to 0}\frac{\Delta y}{\Delta x} = \lim_{\Delta x \to 0}\frac{-2x - \Delta x}{x^2(x + \Delta x)^2} = \frac{-2}{x^3}$，故$f^\prime(x) = \frac{-2}{x^3}$。



==定义2==：设函数$f(x)$在$x_0$点左侧$[x_0 + \Delta x, x_0], (\Delta x < 0)$上有定义，如果极限$\lim_{\Delta x \to 0^-}\frac{f(x_0 + \Delta x) - f(x_0)}{\Delta x}$存在，则称此极限为$f(x)$在$x_0$点的==左导数==，记为$f_-^\prime(x_0) = \lim_{\Delta x \to 0^-}\frac{f(x_0 + \Delta x) - f(x_0)}{\Delta x}$；类似地有==右导数==$f_+^\prime(x_0) = \lim_{\Delta x \to 0^+}\frac{f(x_0 + \Delta x) - f(x_0)}{\Delta x}$。显然有：==$f(x)$在$x_0$点可导等价于$f_-^\prime(x_0) = f_+^\prime(x_0)$==。

如果$f(x)$在$(a, b)$内可导且$f^\prime_+(a), f^\prime_-(b)$存在，称$f(x)$在$[a, b]$上可导，记为$f(x) \in D[a, b]$。



### 二、导数的几何意义

==导数的几何意义==：曲线上一点处切线的斜率问题及导数的定义，即$f^\prime(x_0) = \lim_{\Delta x \to 0}\frac{\Delta y}{\Delta x}$，可知$f^\prime(x_0)$在几何上表示曲线上一点$P_0(x_0, f(x_0))$上的切线$P_0T$的斜率，即$f^\prime(x_0) = \tan \alpha$（$\alpha$是切线$P_0T$的倾角）。

1. 根据导数的几何意义与平面解析几何关于直线方程的知识可知，切线方程$y - f(x_0) = f^\prime(x_0)(x - x_0)$。
2. 求曲线上点$P_0(x_0, f(x_0))$的法线（过$P_0$且与该点处的切线垂直的直线）方程。已知切线斜率$k_1 = f^\prime(x_0), f^\prime(x_0) \neq 0$，而切线与法线垂直，故法线斜率$k_2 = -\frac{1}{k_1} = -\frac{1}{f^\prime(x_0)}$，则法线方程为$y - f(x_0) = -\frac{1}{f^\prime(x_0)}(x - x_0)$。
3. 若$y = f(x)$在$x_0$点处的导数$f^\prime(x_0) = \infty$，表示切线垂直于$x$轴，切线方程$x = x_0$。



### 三、函数的可导性与连续性的关系

==定理==：如果函数$y = f(x)$在$x_0$点可导，则$f(x)$在$x_0$点一定是连续的。

证：设$y = f(x)$的自变量$x$在$x_0$点有增量$\Delta x$，函数对应的增量$\Delta y = f(x_0 + \Delta x) - f(x_0)$。要证$f(x)$在$x_0$点处连续，亦即要证$\lim_{\Delta x \to 0}\Delta y = 0$。因为$y = f(x)$在$x_0$点可导，从而有$\lim_{\Delta x \to 0}\frac{\Delta y}{\Delta x}$存在且$\lim_{\Delta x \to 0}\frac{\Delta y}{\Delta x} = f^\prime(x_0)$，根据有极限的函数与无穷小的关系有：$\frac{\Delta y}{\Delta x} = f^\prime(x_0) + \alpha$，其中$\lim_{\Delta x \to 0}\alpha = 0$，即$\Delta y = f^\prime(x_0)\Delta x + \alpha \Delta x$，取极限$\lim_{\Delta x \to 0}\Delta y = \lim_{\Delta x \to 0}f^\prime(x_0)\Delta x + \lim_{\Delta x \to 0}\alpha \Delta x = 0$，所以函数$y = f(x)$在$x_0$点处连续。（==连续是可导的必要条件==）

==定理的逆命题不真==

例如：函数$y = \sqrt[3]{x}$，$y = \sqrt{x^2} = |x|$在$x = 0$点连续，但在$x = 0$点不可导。

证：设$y = \sqrt[3]{x}$的自变量$x_0=0$处有增量$\Delta x$，则$\Delta y = \sqrt[3]{x_0 + \Delta x} - \sqrt[3]{x_0} = \sqrt[3]{\Delta x}, (\Delta y)^3 = \Delta x$，$\lim_{\Delta x \to 0}(\Delta y)^3 = (\lim_{\Delta x \to 0}\Delta y)^3 = \lim_{\Delta x \to 0}\Delta x = 0, \therefore \lim_{\Delta x \to 0}\Delta y = 0$，因此$y = \sqrt[3]{x}$在$x = 0$点连续。而$\lim_{\Delta x \to 0}\frac{\Delta y}{\Delta x} = \lim_{\Delta x \to 0}\frac{\sqrt[3]{\Delta x}}{\Delta x} = \lim_{\Delta x \to 0}\frac{1}{(\Delta x)^{\frac{2}{3}}} = \infty$，所以$y = \sqrt[3]{x}$在$x = 0$点不可导。

对于函数：
$$
y = \sqrt{x^2} = |x| = \left\{\begin{array}{cc} &x, &x \ge 0 \\ &-x, &x < 0  \end{array}\right\}
$$
容易证明$y = |x|$在$x = 0$点连续。设自变量$x=0$处有增量$\Delta x$，
$$
\Delta y = |0 + \Delta x| - |0| = |\Delta x| = \left\{\begin{array}{cc} &\Delta x, &\Delta x > 0, \\ &-\Delta x, &\Delta x < 0 \end{array}\right\}
$$
$f_+^\prime(0) = \lim_{\Delta x \to 0^+}\frac{\Delta y}{\Delta x} = \lim_{\Delta x \to 0^+}\frac{\Delta x}{\Delta x} = 1$，$f_-^\prime(0) = \lim_{\Delta x \to 0^-}\frac{\Delta y}{\Delta x} = \lim_{\Delta x \to 0^-}\frac{-\Delta x}{\Delta x} = -1$，因为$f_+^\prime(0) \neq f_-^\prime(0)$，所以$y = f(x) = |x|$在$x = 0$点不可导。



### 四、几个基本初等函数的导数公式

1. 常数$C$：$f(x) \equiv C, -\infty < x < +\infty$。

   证：令$y = f(x) \equiv C$，$\forall_x \in (-\infty, +\infty), \Delta y = f(x + \Delta x) - f(x) = C - C = 0, f^\prime(x) = \lim_{\Delta x \to 0}\frac{\Delta y}{\Delta x} = \lim_{\Delta x \to 0}\frac{0}{\Delta x} = 0$，所以$C^\prime = 0$。

2. 幂函数$y = f(x) = x^\alpha$（$\alpha$为实常数）。

   证：当$\alpha = n, (n \in N)$时，设自变量$x$有增量$\Delta x$，则
   $$
   \Delta y = f(x + \Delta x) - f(x) = (x + \Delta x)^n - (x)^n \\ = [x^n + nx^{n-1}\Delta x + \frac{n(n - 1)}{2!}x^{n - 2}(\Delta x)^2 + \cdots + (\Delta x)^n] - x^n \\ = nx^{n-1}\Delta x + \frac{n(n - 1)}{2!}x^{n - 2}(\Delta x)^2 + \cdots + (\Delta x)^n
   $$
   $\frac{\Delta y}{\Delta x} = nx^{n-1} + \frac{n(n - 1)}{2!}x^{n - 2}\Delta x + \cdots + (\Delta x)^{n - 1}$，$\lim_{\Delta x \to 0}\frac{\Delta y}{\Delta x} = \lim_{\Delta x \to 0}[nx^{n-1} + \frac{n(n - 1)}{2!}x^{n - 2}\Delta x + \cdots + (\Delta x)^{n - 1}] = nx^{n - 1}$，即$(x^n)^\prime = nx^{n - 1}$。

   当$\alpha$为任何实常数时，$(x^\alpha)^\prime = \alpha x^{\alpha - 1}$，==证明将在后面完成==。

3. 正弦、余弦函数$y = f(x) = \sin x, y = f(x) = \cos x$。

   解：$y = \sin x, -\infty < x < +\infty, \forall_x \in (-\infty, +\infty)$。设自变量$x$有增量$\Delta x$，函数$y = \sin x$的增量$\Delta y = \sin(x + \Delta x) - \sin(x) = 2\sin(\frac{\Delta x}{2})\cos(x + \frac{\Delta x}{2})$，$\frac{\Delta y}{\Delta x} = \frac{2\sin(\frac{\Delta x}{2})\cos(x + \frac{\Delta x}{2})}{\Delta x}$，$\lim_{\Delta x \to 0}\frac{\Delta y}{\Delta x} = \lim_{\Delta x \to 0}[\frac{2\sin(\frac{\Delta x}{2})\cos(x + \frac{\Delta x}{2})}{\Delta x}] = \lim_{\Delta x \to 0}\frac{\sin(\frac{\Delta x}{2})}{\frac{\Delta x}{2}} \cdot \lim_{\Delta x \to 0}\cos(x + \frac{\Delta x}{2}) = 1 \cdot \cos x = \cos x$，因此$(\sin x)^\prime = \cos x$。

   $y = \cos x, -\infty < x < +\infty, \forall_x \in (-\infty, +\infty)$。设自变量$x$有增量$\Delta x$，函数$y = \cos x$的增量$\Delta y = \cos(x + \Delta x) - \cos(x) = -2\sin(\frac{\Delta x}{2})\sin(x + \frac{\Delta x}{2})$，$\frac{\Delta y}{\Delta x} = \frac{-2\sin(\frac{\Delta x}{2})\sin(x + \frac{\Delta x}{2})}{\Delta x}$，$\lim_{\Delta x \to 0}\frac{\Delta y}{\Delta x} = \lim_{\Delta x \to 0}[\frac{-2\sin(\frac{\Delta x}{2})\sin(x + \frac{\Delta x}{2})}{\Delta x}] = -\lim_{\Delta x \to 0}\frac{\sin(\frac{\Delta x}{2})}{\frac{\Delta x}{2}} \cdot \lim_{\Delta x \to 0}\sin(x + \frac{\Delta x}{2}) = -1 \cdot \sin x = -\sin x$，因此$(\cos x)^\prime = -\sin x$。

4. 对数函数$y = f(x) = \log_a x, (a > 0, a \neq 1)$。

   解：已知$y = \log_a x, 0 < x < +\infty, \forall_x \in (0, +\infty)$，设自变量$x$有增量$\Delta x$，函数对应增量$\Delta y = \log_a(x + \Delta x) - \log_a x = \log_a \frac{x + \Delta x}{x} = \log_a (1 + \frac{\Delta x}{x})$，$\frac{\Delta y}{\Delta x} = \frac{1}{\Delta x} \cdot \log_a (1 + \frac{\Delta x}{x}) = \frac{1}{x} \cdot \frac{x}{\Delta x} \cdot \log_a (1 + \frac{\Delta x}{x}) = \frac{1}{x} \cdot \log_a (1 + \frac{\Delta x}{x})^{\frac{x}{\Delta x}}$，
   $$
   \lim_{\Delta x \to 0}\frac{\Delta y}{\Delta x} = \lim_{\Delta x \to 0}\frac{1}{x} \cdot \log_a (1 + \frac{\Delta x}{x})^{\frac{x}{\Delta x}} = \frac{1}{x} \cdot \lim_{\Delta x \to 0}[\log_a (1 + \frac{\Delta x}{x})^{\frac{x}{\Delta x}}] = \\ \frac{1}{x} \cdot \log_a[\lim_{\Delta x \to 0}(1 + \frac{\Delta x}{x})^{\frac{x}{\Delta x}}] = \frac{1}{x} \cdot \log_a e = \frac{1}{x} \cdot \frac{1}{\ln a} = \frac{1}{x\ln a}
   $$
   故$(\log_a x)^\prime = \frac{1}{x \ln a}$，特殊地：$(\ln x)^\prime = \frac{1}{x}$。



## 第2节 函数的微分法

### 一、函数的和差积商的求导数公式

1. 设$u = u(x), v = v(x)$在同一点$x$处可导，则$y = u(x) \pm v(x)$在$x$点处可导且$y^\prime = u^\prime(x) \pm v^\prime(x)$。

   证：设自变量在$x$点处有增量$\Delta x$，函数$y$对应的增量$\Delta y = [u(x + \Delta x) \pm v(x + \Delta x)] - [u(x) \pm v(x)] = [u(x + \Delta x) - u(x)] \pm [v(x + \Delta x) - v(x)] = \Delta u \pm \Delta v$，则$\frac{\Delta y}{\Delta x} = \frac{\Delta u \pm \Delta v}{\Delta x} = \frac{\Delta u}{\Delta x} \pm \frac{\Delta v}{\Delta x}$，由假设可知$\lim_{\Delta x \to 0}\frac{\Delta u}{\Delta x} = u^\prime(x), \lim_{\Delta x \to 0}\frac{\Delta v}{\Delta x} = v^\prime(x)$，所以$\lim_{\Delta x \to 0}\frac{\Delta y}{\Delta x} = \lim_{\Delta x \to 0}\frac{\Delta u}{\Delta x} \pm \lim_{\Delta x \to 0}\frac{\Delta v}{\Delta x} = u^\prime(x) \pm v^\prime(x)$，故$[u(x) \pm v(x)]^\prime = u^\prime(x) \pm v^\prime(x)$。

   用数学归纳法原理可将公式推广到有限多个函数和差的导数，即：$[u_1(x) \pm u_2(x) \pm u_3(x) \pm \cdots \pm u_n(x) ]^\prime = u_1^\prime(x) \pm u_2^\prime(x) \pm u_3^\prime(x) \pm \cdots \pm u_n^\prime(x)$。

2. 设$u = u(x), v = v(x)$在同一点$x$处可导，则$y = u(x) \cdot v(x)$在$x$点处可导且$y^\prime = [u(x) \cdot v(x)]^\prime = u^\prime(x) \cdot v(x) + u(x) \cdot v^\prime(x)$。

   证：设自变量在$x$点处有增量$\Delta x$，函数$y$对应的增量
   $$
   \Delta y = u(x + \Delta x) \cdot v(x + \Delta x) - u(x) \cdot v(x) \\ = u(x + \Delta x) \cdot v(x + \Delta x) - u(x) \cdot v(x + \Delta x) + u(x) \cdot v(x + \Delta x) - u(x) \cdot v(x) \\ = [u(x + \Delta x) - u(x)] \cdot v(x + \Delta x) + [v(x + \Delta x) - v(x)] \cdot u(x) \\ = \Delta u \cdot v(x + \Delta x) + \Delta v \cdot u(x)
   $$
   $\frac{\Delta y}{\Delta x} = \frac{\Delta u \cdot v(x + \Delta x) + \Delta v \cdot u(x)}{\Delta x} = \frac{\Delta u}{\Delta x} \cdot v(x + \Delta x) + \frac{\Delta v}{\Delta x} \cdot u(x)$，因为$v = v(x)$在$x$点可导，所以$v(x)$在$x$点连续，即$\lim_{\Delta x \to 0}v(x + \Delta x) = v(x)$，所以$\lim_{\Delta x \to 0}\frac{\Delta y}{\Delta x} = \lim_{\Delta x \to 0}\frac{\Delta u}{\Delta x} \cdot \lim_{\Delta x \to 0}v(x + \Delta x) + \lim_{\Delta x \to 0}\frac{\Delta v}{\Delta x} \cdot \lim_{\Delta x \to 0}u(x) = u^\prime(x) \cdot v(x) + u(x) \cdot v^\prime(x)$，所以$[u(x) \cdot v(x)]^\prime = u^\prime(x) \cdot v(x) + u(x) \cdot v^\prime(x)$。

   若$v(x) = C$（$C$是常数），则$v^\prime(x) = C^\prime = 0$，$[C \cdot u(x)]^\prime = C \cdot u^\prime(x)$。

   有限个函数乘积的导数公式（以四个函数为例）：
   $$
   (u \cdot v \cdot w \cdot z)^\prime = [u \cdot (v \cdot w \cdot z)]^\prime \\ = u^\prime \cdot (v \cdot w \cdot z) + u \cdot (v \cdot w \cdot z)^\prime \\ = u^\prime \cdot v \cdot w \cdot z + u \cdot [v \cdot (w \cdot z)]^\prime \\ = u^\prime \cdot v \cdot w \cdot z + u \cdot [v^\prime \cdot (w \cdot z) + v \cdot (w \cdot z)^\prime] \\ = u^\prime \cdot v \cdot w \cdot z + u \cdot [v^\prime \cdot w \cdot z + v \cdot (w^\prime \cdot z + w \cdot z^\prime)] \\ = u^\prime \cdot v \cdot w \cdot z + u \cdot (v^\prime \cdot w \cdot z + v \cdot w^\prime \cdot z + v \cdot w \cdot z^\prime) \\ = u^\prime \cdot v \cdot w \cdot z + u \cdot v^\prime \cdot w \cdot z + u \
   cdot v \cdot w^\prime \cdot z + u \cdot v \cdot w \cdot z^\prime
   $$
   

   例1、设$y = x^{\frac{1}{5}} - \cos x + \sin \frac{\pi}{180}$，求$y^\prime$。

   解：$y^\prime = (x^{\frac{1}{5}} - \cos x + \sin \frac{\pi}{180})^\prime = (x^{\frac{1}{5}})^\prime - (\cos x)^\prime + (\sin \frac{\pi}{180})^\prime = \frac{1}{5}x^{-\frac{4}{5}} + \sin x + 0$。

   

   例2、设$y = \frac{1 - x}{\sqrt{x}} + \ln(3x)$，求$y^\prime$。

   解：$y = \frac{1}{\sqrt{x}} - \frac{x}{\sqrt{x}} + \ln 3 + \ln x = x^{-\frac{1}{2}} - x^{\frac{1}{2}} + \ln 3 + \ln x$，$y^\prime = (x^{-\frac{1}{2}} - x^{\frac{1}{2}} + \ln 3 + \ln x)^\prime = -\frac{1}{2}x^{-\frac{2}{3}} - \frac{1}{2}x^{-\frac{1}{2}} + 0 + \frac{1}{x} = -\frac{1}{2 \cdot \sqrt[3]{x^2}} - \frac{1}{2\sqrt{x}} + \frac{1}{x}$。

   

   例3、$y = (x - x^3)\ln x + \sin(2x)$，求$y^\prime$。

   解：
   $$
   y^\prime = [(x - x^3)\ln x]^\prime + [\sin(2x)]^\prime \\ = (x - x^3)^\prime \cdot \ln x + (x - x^3) \cdot (\ln x)^\prime + (2 \sin x \cos x)^\prime \\ = (1 - 3x^2) \cdot \ln x + 1 - x^2 + 2[(\sin x)^\prime \cdot \cos x + \sin x \cdot (\cos x)^\prime] \\ = (1 - 3x^2) \cdot \ln x + 1 - x^2 + 2[(\cos x)^2 - (\sin x)^2] \\ = (1 - 3x^2) \cdot \ln x + 1 - x^2 + 2 \cos(2x)
   $$

3. 设$u = u(x), v = v(x)$在同一点$x$处可导，且$v(x) \neq 0$，则$y = \frac{u(x)}{v(x)}$在$x$点处可导，且$[\frac{u(x)}{v(x)}]^\prime = \frac{u^\prime(x) \cdot v(x) - u(x) \cdot v^\prime(x)}{[v(x)]^2}$。

   证：设自变量在$x$点处有增量$\Delta x$，函数$y$有对应增量
   $$
   \Delta y = \frac{u(x + \Delta x)}{v(x + \Delta x)} - \frac{u(x)}{v(x)} \\ = \frac{v(x) \cdot u(x + \Delta x) - u(x) \cdot v(x + \Delta x)}{v(x) \cdot v(x +\Delta x)} \\ = \frac{v(x) \cdot u(x + \Delta x) - u(x) \cdot v(x) + u(x) \cdot v(x) - u(x) \cdot v(x + \Delta x)}{v(x) \cdot v(x +\Delta x)} \\ = \frac{[u(x + \Delta x) - u(x)]v(x) - u(x)[v(x + \Delta x) - v(x)]}{v(x) \cdot v(x +\Delta x)} \\ = \frac{\Delta u \cdot v(x) - u(x) \cdot \Delta v}{v(x) \cdot v(x +\Delta x)}
   $$
   $\frac{\Delta y}{\Delta x} = \frac{\frac{\Delta u}{\Delta x} \cdot v(x) - u(x) \cdot \frac{\Delta v}{\Delta x}}{v(x) \cdot v(x +\Delta x)}$，因为$u(x), v(x)$在$x$点可导，所以$\lim_{\Delta x \to 0}\frac{\Delta u}{\Delta x} = u^\prime(x), \lim_{\Delta x \to 0}\frac{\Delta v}{\Delta x} = v^\prime(x)$又因为$v(x)$在$x$点连续，所以$\lim_{\Delta x \to 0}v(x + \Delta x) = v(x)$，取极限$\lim_{\Delta x \to 0}\frac{\Delta y}{\Delta x} = \frac{v(x) \cdot \lim_{\Delta x \to 0}(\frac{\Delta u}{\Delta x}) - u(x) \cdot \lim_{\Delta x \to 0}(\frac{\Delta v}{\Delta x})}{v(x) \cdot \lim_{\Delta x \to 0}v(x +\Delta x)} = \frac{u^\prime(x) \cdot v(x) - u(x) \cdot v^\prime(x)}{[v(x)]^2}$。当$u = 1$时，$(\frac{1}{v})^\prime = -\frac{v^\prime}{v^2}$。

   

   例1、设$y = \tan x$，$y = \cot x$，求$y^\prime$。

   解：$y = \tan x = \frac{\sin x}{\cos x}$，$y^\prime = (\tan x)^\prime = (\frac{\sin x}{\cos x})^\prime = \frac{(\sin x)^\prime \cdot \cos x - \sin x \cdot (\cos x)^\prime}{(\cos x)^2} = \frac{(\cos x)^2 + (\sin x)^2}{(\cos x)^2} = \frac{1}{(\cos x)^2} = (\sec x)^2$；

   $y = \cot x = \frac{\cos x}{\sin x}$，同理可得$y^\prime = (\cot x)^\prime = (\frac{\cos x}{\sin x})^\prime = -(\csc x)^2$。

   
   
   例2、$y = \sec x$，$y = \csc x$，求$y^\prime$。
   
   解：$y^\prime = (\sec x)^\prime = (\frac{1}{\cos x})^\prime = -\frac{-\sin x}{(\cos x)^2} = \sec x \cdot \tan x$；$y^\prime = (\csc x)^\prime = -\csc x \cdot \cot x$。



### 二、反函数的导数

==反函数的求导法则==——设$x = \phi(y)$在区间$I$上单调且可导，同时$\phi^\prime(y) \neq 0$，则其反函数$y = f(x)$在对应区间$J = \{x | x = \phi(y), y \in I\}$也是可导的且$f^\prime(x) = \frac{1}{\phi^\prime(y)}$。

证：因为$x = \phi(y)$在区间$I$内单调且可导$\Longrightarrow$$x = \phi(y)$在区间$I$上单调且连续$\Longrightarrow$其反函数$y = f(x)$在对应区间$J$上单调且连续。$\forall_x \in J$，设$x$有增量$\Delta x$，反函数$y = f(x)$的增量$\Delta y = f(x + \Delta x) - f(x) \neq 0$，$\frac{\Delta y}{\Delta x} = \frac{1}{\frac{\Delta x}{\Delta y}}$。因为$y = f(x)$是连续函数，由函数连续性的定义，当$\Delta x \to 0$时$\Delta y \to 0$，且注意到$\phi^\prime(y) \neq 0$，从而有$\lim_{\Delta x \to 0}\frac{\Delta y}{\Delta x} = \lim_{\Delta x \to 0}\frac{1}{\frac{\Delta x}{\Delta y}} = \frac{1}{\lim_{\Delta x \to 0}\frac{\Delta x}{\Delta y}} = \frac{1}{\lim_{\Delta y \to 0}\frac{\Delta x}{\Delta y}} = \frac{1}{\phi^\prime(y)}$，所以$f^\prime(x) = \frac{1}{\phi^\prime(y)}$。



例1、设$y = \arcsin x, y = \arccos x$，求$y^\prime$。

解：已知$y = f(x) = \arcsin x, -1 \le x \le 1$是$x = \phi(y) = \sin y, -\frac{\pi}{2} \le y \le \frac{\pi}{2}$的反函数。因为$x = \phi(y) = \sin y$在$-\frac{\pi}{2} \le x \le \frac{\pi}{2}$内是单调增且可导的 ，$x^\prime = \phi^\prime(y) = (\sin y)^\prime = \cos y > 0, (-\frac{\pi}{2} < y < \frac{\pi}{2})$。所以$(\arcsin x)^\prime = \frac{1}{\phi^\prime(y)} = \frac{1}{\cos y} = \frac{1}{\pm \sqrt{1 - (\sin y)^2}} = \frac{1}{\sqrt{1 - (\sin y)^2}} = \frac{1}{\sqrt{1 - x^2}}$。

类似地，可推出$y^\prime = (\arccos x)^\prime = -\frac{1}{\sqrt{1 - x^2}}$。



例2、设$y = \arctan x, y = arccot x$，求$y^\prime$。

解：已知$y = f(x) = \arctan x, -\infty < x < +\infty$是$x = \phi(y) = \tan y, -\frac{\pi}{2} < x < \frac{\pi}{2}$的反函数，且$\phi(y) = \tan y$在$-\frac{\pi}{2} < y < \frac{\pi}{2}$上单调增且可导，所以$\phi^\prime(y) = (\tan y)^\prime = (\sec y)^2 > 0, -\frac{\pi}{2} < y < \frac{\pi}{2}$，所以$(\arctan x)^\prime = \frac{1}{\phi^\prime(y)} = \frac{1}{(\sec y)^2} = \frac{1}{1 + (\tan y)^2} = \frac{1}{1 + x^2}$。

类似地，可推出$y^\prime = (arccot x)^\prime = -\frac{1}{1 + x^2}$。



例3、求$y = a^x, (a > 0, a \neq 1)$的导数。

解：已知$y = f(x) = a^x, -\infty < x < +\infty$是$x = \log_a y$在$(0, +\infty)$内的反函数，$x = \phi(y) = \log_a y$在$(0, +\infty)$内单调且可导，$\phi^\prime(y) = \frac{1}{y \cdot \ln a}, 0 < y < +\infty$，在对应区间$(-\infty, +\infty)$内，$(a^x)^\prime = \frac{1}{(\log_a y)^\prime} = \frac{1}{\frac{1}{y \cdot \ln a}} = y \cdot \ln a = a^x \cdot \ln a$。特殊地，当$a = e$时，$(e^x)^\prime = e^x$。



### 三、复合函数的导数

像$\ln \tan x, e^{x^2}, \sin \frac{2x}{1 + x^2}$都是复合函数。

==复合函数的求导法则==——设$u = \phi(x)$在$x$点可导， 而$y = f(u)$在对应点$u$可导，则复合函数$y = f(u) = f[\phi(x)]$在$x$点可导，且有$\frac{d_y}{d_x} = \frac{d_{f(u)}}{d_u} \cdot \frac{d_u}{d_x} = f^\prime(u) \cdot \phi^\prime(x)$。

证：设自变量在$x$点有增量$\Delta x$，中间变量$u$有对应增量$\Delta u = \phi(x + \Delta x) - \phi(x)$，当$\Delta u \neq 0$时$\lim_{\Delta u \to 0}\frac{\Delta y}{\Delta u} = f^\prime(u)$，根据有极限的函数与无穷小的关系，$\frac{\Delta y}{\Delta u} = f^\prime(u) + \alpha$，其中$\lim_{\Delta u \to 0}\alpha = 0$。所以有$\Delta y = f^\prime(u) \cdot \Delta u + \alpha \cdot \Delta u$；当$\Delta u = 0$时，$\Delta y = f(u + \Delta u) - f(u) = 0$，这时令$\alpha = 0$，则$\Delta y = f^\prime(u) \cdot \Delta u + \alpha \cdot \Delta u$对于$\Delta u \neq 0$或$\Delta u = 0$都是正确的。做比值$\frac{\Delta y}{\Delta x} = f^\prime(u) \cdot \frac{\Delta u}{\Delta x} + \alpha \cdot \frac{\Delta u}{\Delta x}$。因为$u = \phi(x)$在$x$点可导$\Longrightarrow u = \phi(x)$在$x$点连续，由函数连续性的定义可得当$\Delta x \to 0$时有$\Delta u \to 0$。取极限$\lim_{\Delta x \to 0}\frac{\Delta y}{\Delta x} = \lim_{\Delta x \to 0}[f^\prime(u) \cdot \frac{\Delta u}{\Delta x}] + \lim_{\Delta x \to 0}(\alpha \cdot \frac{\Delta u}{\Delta x}) = f^\prime(u) \cdot \frac{d_u}{d_x} = f^\prime(u) \cdot \phi^\prime(x)$。即$\frac{d_y}{d_x} = f^\prime(u) \cdot \phi^\prime(x)$。

例1、设$y = \ln \tan x$，求$\frac{d_y}{d_x}$。

解：设$y = \ln u, u = \tan x$，$\frac{d_y}{d_x} = \frac{d_y}{d_u} \cdot \frac{d_u}{d_x} = \frac{d_{\ln u}}{d_u} \cdot \frac{d_{\tan x}}{d_x} = \frac{1}{u} \cdot (\sec x)^2 = \frac{\cos x}{\sin x} \cdot \frac{1}{(\cos x)^2} = \frac{1}{\sin x \cos x}$。



例2、设$y = x^\alpha$，（$x > 0$，$\alpha$为实常数）,求$\frac{d_y}{d_x}$。

解：两边取对数，得$\ln y = \alpha \ln x$，所以$y = e^{\alpha \ln x} = e^u, u = \alpha \ln x$，$\frac{d_y}{d_x} = \frac{d_{e^u}}{d_u} \cdot \frac{d_{\alpha \ln x}}{d_x} = e^u \cdot \alpha \cdot \frac{1}{x} = e^{\alpha \ln x} \cdot \alpha \cdot \frac{1}{x} = x^\alpha \cdot \alpha \cdot \frac{1}{x} = \alpha \cdot x^{\alpha - 1}$，即$(x^\alpha)^\prime = \alpha \cdot x^{\alpha - 1}$。



例3、设$y = \sin(\frac{2x}{1 + x^2})$，求$\frac{d_y}{d_x}$。

解：设$y = \sin u, u = \frac{2x}{1 + x^2}$，$\frac{d_y}{d_x} = \frac{d_y}{d_u} \cdot \frac{d_u}{d_x} = \frac{d_{\sin u}}{d_u} \cdot \frac{d({\frac{2x}{1 + x^2}})}{d_x} = \cos u \cdot 2 \cdot \frac{1 - x^2}{(1 + x^2)^2} = \frac{2 - 2x^2}{(1 + x^2)^2} \cdot \cos(\frac{2x}{1 + x^2})$。



若$y = f[\phi(\psi(x))] \Longleftrightarrow y = f(u), u = \phi(\psi(x)) = \phi(v), v = \psi(x)$，设$v = \psi(x)$在点$x$可导，而$u = \phi(v)$在对应的$v$可导，$y = f(u)$在对应点$u$可导，则：$\frac{d_y}{d_x} = \frac{d_{f(u)}}{d_u} \cdot \frac{d_u}{d_x} = \frac{d_{f(u)}}{d_u} \cdot \frac{d_u}{d_v} \cdot \frac{d_v}{d_x} = f^\prime(u) \cdot \phi^\prime(v) \cdot \psi^\prime(x)$。



例如：$y = e^{\sin \frac{1}{x}}$，求$\frac{d_y}{d_x}$。

解：$y = e^u, u = \sin \frac{1}{x} = \sin v, v = \frac{1}{x} = x^{-1}$，$\frac{d_y}{d_x} = \frac{d_y}{d_u} \cdot \frac{d_u}{d_x} = \frac{d_y}{d_u} \cdot \frac{d_u}{d_v} \cdot \frac{d_v}{d_x} = e^u \cdot \cos v \cdot (-1)x^{-2} = -e^{\sin \frac{1}{x}} \cdot \cos \frac{1}{x} \cdot \frac{1}{x^2} = -\frac{1}{x^2} \cdot \cos \frac{1}{x} \cdot e^{\sin \frac{1}{x}}$。



初等函数求导数归纳：

1. 记住基本初等函数的导数公式；
2. 记住函数的四则运算的求导公式；
3. 掌握反函数与复合函数的求导规则。



例4、设$y = arsh(x)$，求$\frac{d_y}{d_x}$。

解：$y = arsh(x) = \ln(x + \sqrt{1 + x^2})$，$y = \ln u, u = x + \sqrt{1 + x^2} = v + w, v = x, w = \sqrt{1 + x^2} = z^{\frac{1}{2}}, z = 1 + x^2$。
$$
\frac{d_y}{d_x} = \frac{d_{\ln u}}{d_u} \cdot \frac{d_u}{d_x} \\ = \frac{1}{u} \cdot (\frac{d_v}{d_x} + \frac{d_w}{d_x}) \\ = \frac{1}{u} \cdot (1 + \frac{d_w}{d_z} \cdot \frac{d_z}{d_x}) \\ = \frac{1}{u} \cdot (1 + \frac{1}{2}z^{-\frac{1}{2}} \cdot 2x) \\ = \frac{1}{x + \sqrt{1 + x^2}} \cdot (1 + \frac{x}{\sqrt{1 + x^2}}) \\ = \frac{1}{x + \sqrt{1 + x^2}} \cdot \frac{\sqrt{1 + x^2} + x}{\sqrt{1 + x^2}} \\ = \frac{1}{\sqrt{x + x^2}}
$$



### 四、高阶导数

若$y = f(x)$在区间$I$上可导，则其导数$y^\prime = f^\prime(x)$仍是区间$I$上的函数——导函数，如果$y^\prime = f^\prime(x)$也是可导函数，则称$f^\prime(x)$的导数$[f^\prime(x)]^\prime$为$f(x)$的二阶导数，记为$y^{\prime\prime} = [f^\prime(x)]^\prime = f^{\prime\prime}(x)$，或$\frac{d^2y}{dx^2} = \frac{d(dy)}{dx(dx)}$或$\frac{d^2f(x)}{dx^2}$。类似地，如果$y^{\prime\prime} = f^{\prime\prime}(x)$仍是可导函数，则称$[f^{\prime\prime}(x)]^\prime$为$f(x)$的三阶导数，记为$y^{\prime\prime\prime} = [f^{\prime\prime}(x)]^\prime = f^{\prime\prime\prime}(x)$。如果$f^{(n - 1)}(x)$仍是可导函数，则称$[f^{(n - 1)}f(x)]^\prime$为$f(x)$的$n$阶导数，记为：$[f^{(n - 1)}f(x)]^\prime = f^{(n)}(x) = \frac{d^ny}{dx^n} = \frac{d^nf(x)}{dx^n}$。

若$f(x)$在区间$I$，或$(a, b)$内有$n$阶导数，记为$f(x) \in D^n(I)$或$f(x) \in D^n(a, b)$。



​	例1、求$y = a^x, (a > 0, a \neq 1)$，求$y$的$n$阶导数。

​	解：$y = a^x$，$y^\prime = (a^x)^\prime = a^x \ln a$，$y^{\prime\prime} = a^x [\ln(a)]^2$。设$y^{(n - 1)} = a^x [\ln(a)]^{(n - 1)}$，$y^n = (y^{(n - 1)})^\prime = [a^x (\ln a)^{(n - 1)}]^\prime = (a^x)^\prime (\ln a)^{(n - 1)} = a^x [\ln(a)]^n$，根据数学归纳法原理，得$(a^x)^{(n)} = a^x [\ln(a)]^n$。



​	例2、设$y = \sin x$，求$y^{(n)}$。

​	解：$y^\prime = \cos x = \sin(x + \frac{\pi}{2})$，$y^{\prime\prime} = \cos(x + \frac{\pi}{2}) = \sin((x + \frac{\pi}{2}) + \frac{\pi}{2}) = \sin(x + 2 \cdot \frac{\pi}{2})$，$y^{\prime\prime\prime} = \cos(x + 2 \cdot \frac{\pi}{2}) = \sin((x + 2 \cdot \frac{\pi}{2}) + \frac{\pi}{2}) = \sin(x + 3 \cdot \frac{\pi}{2})$，假设$y^{(n - 1)} = \sin(x + (n - 1) \cdot \frac{\pi}{2})$，则$y^{(n)} = [y^{(n - 1)}]^\prime = \cos(x + (n - 1) \cdot \frac{\pi}{2}) = \sin[(x + (n - 1) \cdot \frac{\pi}{2} + \frac{\pi}{2}] = \sin(x + n \cdot \frac{\pi}{2})$，由数学归纳法原理，得$(\sin x)^{(n)} = \sin(x + n \cdot \frac{\pi}{2})$。



​	例3、设$u = u(x), v = v(x)$在同一点$x$处有直至$n$阶导数（即$u \in D^{(n)}(I), v \in D^{(n)}(I)$），则$(uv)^{(n)} = u^{(n)}v + nu^{(n - 1)}v^\prime + \frac{n(n - 1)}{2!}u^{(n - 1)}v^{\prime\prime} + \cdots + \frac{n(n - 1) \cdots (n - k + 1)}{k!}u^{(n - k)}v^{(k)} + \cdots + uv^{(n)}$（==莱布尼茨公式==）。

​		例如：设$y = x^2 \cdot e^{2x}$，求$y^{(20)}$。

​		解：设$u = e^{2x}, v = x^2$，则$u^\prime = 2e^{2x}, u^{\prime\prime} = 2^2 e^{2x}, \cdots , u^{(k)} = 2^k e^{(2x)}(k = 1, 2, \cdots)$，$v^\prime = 2x, v^{\prime\prime} = 2, v^{(k)} = 0(k = 3, 4, 5, \cdots)$，由莱布尼茨公式，$(uv)^{(n)} = (e^{2x} \cdot x^2)^{(20)} = (e^{2x})^{(20)} \cdot x^2 + 20 \cdot (e^{2x})^{(19)} \cdot (x^2)^\prime + \frac{20 \cdot 19}{2!}(e^{2x})^{(18)} \cdot (x^2)^{\prime\prime} \\ = 2^{20} \cdot e^{2x} \cdot x^2 + 20 \cdot 2^{19} \cdot e^{2x} \cdot 2x + \frac{20 \cdot 19}{2!} \cdot 2^{18} \cdot e^{2x} \cdot 2 = 2^{20} \cdot e^{2x}(x^2 + 20x + 95)$



## 第3节 隐函数、参量函数的导数

### 一、隐函数的导数

函数$f(x)$表示$x$与$y$之间的对应关系，例如：$y = x \cdot \sin x, y = \ln(1 + x^2) \cdots$，因变量$y$已经表示成自变量$x$的明显的数学表达式，这种函数称为==显函数==。

另一种自变量$x$与因变量$y$的对应关系通过$x, y$的方程$(x, y) = 0$来实现。例如：方程$x + y^3 -1 = 0, \forall_x \in (-\infty, +\infty)$。通过这个方程都有确定的$y$值与之对应，这种函数称为==隐函数==。

==隐函数==：对于$x, y$的二元方程$F(x, y) = 0$，如果存在函数$y = f(x)$，使$F[x, f(x)] \equiv 0$，则称$y = f(x)$是由方程$F(x, y) = 0$所确定的隐函数。

例如：$x + y^3 - 1 = 0 \Longrightarrow y = \sqrt[3]{1 - x}$，称此过程为隐函数的==显化==，使得$x + (\sqrt[3]{1 - x})^3 - 1 = 0$，则称$y = \sqrt[3]{1 - x}$是由方程$x + y^3 - 1 = 0$所确定的隐函数。

再如：$xy - e^x + e^y = 0$确定隐函数，但是它不能显化。

==问题==：

1. $F(x, y)$满足什么条件，$F(x, y) = 0$才能够确定一个隐函数？（==下册解决==）
2. $F(x, y) = 0$确定的隐函数是否可导？（==下册解决==）
3. 如果$F(x, y) = 0$所确定的隐函数$y = f(x)$可导，如何求导数$y^\prime = f^\prime(x)$？

==隐函数求导数的方法==：

设$F(x, y) = 0$所确定的隐函数$y = f(x)$可导，把$y = f(x)$代入原方程，得$F[x, f(x)] \equiv 0$，恒等式两边分别对$x$求导，得到含有$f^\prime(x)$的一个等式，从等式中解出$f^\prime(x)$就行了。



​	例1、设方程$e^y - e^x + xy = 0$确定隐函数$y = f(x)$，求$\frac{dy}{dx}|_{x = 0}$。

​	解：把原方程的$y$看作是$x$的函数，把原方程看作恒等式$e^y - e^x + xy \equiv 0$，对恒等式两边分别求导，得：$\frac{d(e^y)}{dx} - \frac{d(e^x)}{dx} + \frac{d(xy)}{x} = 0$，$\frac{d(e^y)}{dy} \cdot \frac{dy}{dx} - e^x + (1 \cdot y + x \cdot \frac{dy}{dx}) = 0$，$e^y \cdot \frac{dy}{dx} - e^x + y + x \cdot \frac{dy}{dx} = 0$，$(e^y + x)\frac{dy}{dx} = e^x - y$，所以$\frac{dy}{dx} = \frac{e^x - y}{e^y + x}$。把$x = 0$代入原方程$e^y - e^x + xy = 0$，得$e^y - 1 = 0 \Longrightarrow y = 0$，所以$\frac{dy}{dx}|_{x = 0} = \frac{e^x - y}{e^y + x}|_{x = 0} = \frac{e^0 - 0}{e^0 + 0} = 1$。

​	

​	例2、（1）求椭圆$\frac{x^2}{4} + y^2 = 1$在点$M(\sqrt{2}, \frac{\sqrt{2}}{2})$处的切线方程。（2）求由方程$\frac{x^2}{4} + y^2 = 1$所确定的隐函数$y = f(x)$的$\frac{d^2y}{dx^2}$。

​	解：（1）把恒等式$\frac{x^2}{4} + y^2 \equiv 1$对$x$求导，$\frac{x}{2} + 2y \cdot y^\prime = 0$，解得$y^\prime = -\frac{x}{4y}$。$y^\prime|_{x = \sqrt{2}} = -\frac{x}{4y}|_{x = \sqrt{2}} = -\frac{\sqrt{2}}{4 \cdot \frac{\sqrt{2}}{2}} = -\frac{1}{2}$。所以过点$M(\sqrt{2}, \frac{\sqrt{2}}{2})$的切线方程为$(y - \frac{\sqrt{2}}{2}) = -\frac{1}{2}(x - \sqrt{2})$，化简得$x + 2y - 2\sqrt{2} = 0$。

​	（2）由（1），已求$\frac{dy}{dx} = -\frac{x}{4y}$，则$\frac{d^2y}{dx^2} = -\frac{1}{4}\frac{d(\frac{x}{y})}{dx} = -\frac{1}{4} \cdot \frac{1 \cdot y - x \cdot \frac{dy}{dx}}{y^2} = -\frac{1}{4}\frac{y - x\cdot (-\frac{x}{4y})}{y^2} = -\frac{4y^2 + x^2}{16y^3}$，由方程$\frac{x^2}{4} + y^2 = 1 \Longrightarrow x^2 + 4y^2 = 4$，所以$\frac{d^2y}{dx^2} = -\frac{1}{4y^3}$。



​	例3、设$y = x^{\sin\frac{x}{2}},(x > 0)$，求$\frac{dy}{dx}$。

​	解：对$y = x^{\sin\frac{x}{2}}$两边取对数得$\ln y = \sin\frac{x}{2} \cdot \ln x$，两边对$x$取导数：$\frac{1}{y} \cdot \frac{dy}{dx} = \frac{1}{2}\cos\frac{x}{2} \cdot \ln x + \sin\frac{x}{2} \cdot \frac{1}{x}$，$\frac{dy}{dx} = y[\frac{1}{2}\cos\frac{x}{2} \cdot \ln x + \sin\frac{x}{2} \cdot \frac{1}{x}] = x^{\sin\frac{x}{2}}[\frac{1}{2}\cos\frac{x}{2} \cdot \ln x + \sin\frac{x}{2} \cdot \frac{1}{x}]$。此法称为==取对数微分法==。



==取对数微分法==：幂指函数$y = [f(x)]^{g(x)}, (f(x) > 0)$，当$f(x), g(x)$可导时，用取对数微分法求$\frac{dy}{dx}$。



​	例4、设$y = x^2 \sqrt{\frac{1 - x}{1 + x}}$，求$\frac{dy}{dx}$。

​	解：取对数$\ln y = 2 \ln x + \frac{1}{2}[\ln(1 - x) - \ln(1 + x)]$，两边对$x$求导数得$\frac{1}{y} \cdot \frac{dy}{dx} = \frac{2}{x} + \frac{1}{2}(-\frac{1}{1 - x} - \frac{1}{1 + x})$，则$\frac{dy}{dx} = x^2 \sqrt{\frac{1 - x}{1 + x}}(\frac{2}{x} - \frac{1}{1 - x^2})$。



### 二、参量函数的导数

例如：在解析几何中，用参量方程讨论动点的几何轨迹：

椭圆的参量方程：
$$
\left\{\begin{array}{ccc} &x &= &a\cos t \\ &y &= &b\cos t \end{array}\right.
$$
其中$a,b$分别为椭圆的长、短半轴。

在力学中，用参量方程讨论质点的运动轨迹，如：一物体以初速度$v_0$，仰角$\phi$抛射出去，忽略空气阻力，得到物体的运动轨迹：
$$
x = v_0 \cos\phi \cdot t \\
y = v_0 \sin\phi \cdot t - \frac{1}{2}gt^2
$$
给定参量$t$一个值，得到对应的一对$x, y$的值，把这对$x, y$的值看作$x$与$y$之间的一种对应，则参量方程确定$y$是$x$的函数。消去参数$t$：由$x = v_0 \cos\phi \cdot t \Longrightarrow t = \frac{x}{v_0 \cos\phi}$代入$y$的方程：$y = v_0 \sin\phi \cdot \frac{x}{v_0 \cos\phi} - \frac{1}{2}g \cdot \frac{x^2}{v_0^2 \cos^2\phi}$，此为==参量函数的显化==。

一般地，设参量方程$x = \phi(x), y = \psi(t), t \in I$，设函数$x = \phi(t)$具有==单调连续==的反函数$t = \phi^{-1}(x)$，将$t$代入$y$的表达式，$y = \psi[\phi^{-1}(x)]$，它是$x$的复合函数，如果$x = \phi(t), y = \psi(t)$都可导，且$\phi^\prime(t) \neq 0$，求参量函数：
$$
\left\{\begin{array}{cccc} &x &= &\phi(t) \\ &&& &,x\in I \\ &y &= &\psi(t) \end{array}\right.
$$
的导数。

由$y = \psi[\phi^{-1}(x)] = \psi(t), t = \phi^{-1}(x)$，则$\frac{dy}{dx} = \frac{d\psi(t)}{dt} \cdot \frac{dt}{dx} = \psi^\prime(t) \cdot \frac{1}{\frac{dx}{dt}} = \frac{\psi^\prime(t)}{\phi^\prime(t)}$。

$\frac{d^2y}{dx^2} = \frac{d(\frac{dy}{dx})}{dx} = \frac{d(\frac{dy}{dx})}{dt} \cdot \frac{dt}{dx} = \frac{d(\frac{\psi^\prime(t)}{\phi^\prime(t)})}{dt} \cdot \frac{1}{\frac{dx}{dt}} = \frac{\psi^{\prime\prime}(t)\phi^\prime(t) - \psi^\prime(t)\phi^{\prime\prime}(t)}{[\phi^\prime(t)]^2} \cdot \frac{1}{\phi^\prime(t)} = \frac{\psi^{\prime\prime}(t)\phi^\prime(t) - \psi^\prime(t)\phi^{\prime\prime}(t)}{[\phi^\prime(t)]^3}$。



例1、求摆线
$$
\left\{\begin{array}{ccc} &x &= &a(t - \sin t) \\ &y &= &a(1 - \cos t) \end{array}\right.
$$
在$t = \frac{\pi}{2}$时的切线方程，并求$\frac{d^2y}{dx^2}$。

解：（1）当$t = \frac{\pi}{2}$时，对应一点$M(a(\frac{\pi}{2} - 1), a)$，$\frac{dy}{dx} = \frac{\frac{dy}{dt}}{\frac{dx}{dt}} = \frac{a\sin t}{a(1 - \cos t)} = \frac{2\sin\frac{t}{2}\cdot\cos\frac{t}{2}}{2\sin^2\frac{t}{2}} = \cot\frac{t}{2}$，$\frac{dy}{dx}|_{t = \frac{\pi}{2}} = \cot\frac{\pi}{4} = 1$。切线方程：$y - a = 1 \cdot (x - a(\frac{\pi}{2} - 1))$，化简得：$x - y + a(2 - \frac{\pi}{2}) = 0$。

（2）$\frac{d^2y}{dx^2} = \frac{d(\frac{dy}{dx})}{dx} = \frac{d(\cot\frac{t}{2})}{dx} = \frac{d(\cot\frac{t}{2})}{dt} \cdot \frac{dt}{dx} = -\csc^2\frac{t}{2} \cdot \frac{1}{2} \cdot \frac{1}{a(1 - \cos t)} = -\frac{1}{2}\frac{1}{\sin^2\frac{t}{2}} \cdot \frac{1}{2a \sin^2\frac{t}{2}} = -\frac{1}{4a}\csc^4\frac{t}{2}, (t \neq 2n\pi)$。



### 三、极坐标系下曲线$\rho = \rho(\theta)$的切线的斜率

设极坐标系下$\rho = \rho(\theta)$可导，利用极坐标与直角坐标的关系：$x = \rho\cos\theta = \rho(\theta)\cos\theta, y = \rho\sin\theta = \rho(\theta)\sin\theta$，其中$\theta$为极角（参量）。

![](images/Figure_4.png)

曲线$\rho = \rho(\theta)$上的一点$(\rho, \theta)$的切线与$x$轴正向的夹角$\alpha$（切线的倾角）。

![](images/Figure_5.png)

由参量函数的微分法：
$$
\frac{dy}{dx} = \frac{[\rho(\theta)\sin\theta)]^\prime}{[\rho(\theta)\cos\theta]^\prime} \\ = \frac{\rho^\prime(\theta)\sin\theta + \rho(\theta)\cos\theta}{\rho^\prime(\theta)\cos\theta - \rho(\theta)\sin\theta} \\ = \frac{\rho^\prime(\theta)\tan\theta + \rho(\theta)}{\rho^\prime(\theta) - \rho(\theta)\tan\theta}
$$
点$M_0(\rho_0, \theta_0) = M(\rho(\theta_0), \theta_0)$，斜率$k = \frac{dy}{dx}|_{\theta = \theta_0}$，然后用直角坐标写切线方程。

​	

​	例1、求心形线$\rho = \alpha(1 - \cos\theta)$在$\theta = \frac{\pi}{4}$的点$M(\alpha(1 - \frac{\sqrt{2}}{2}), \frac{\pi}{4})$的切线的斜率。

​	解：曲线的参量方程：
$$
\left\{\begin{array}{ccccc} &x &= &\rho\cos\theta &= &\alpha(1 - \cos\theta)\cos\theta \\ &y &= &\rho\sin\theta &= &\alpha(1 - \cos\theta)\sin\theta \end{array}\right.
$$
​	$\frac{dy}{dx} = \frac{\alpha(\sin\theta - \sin\theta\cos\theta)^\prime}{\alpha(\cos\theta - \cos^2\theta)^\prime} = \frac{\cos\theta - \cos 2\theta}{\sin 2\theta - \sin\theta}$，$\frac{dy}{dx}|_{\theta = \frac{\pi}{4}} = \frac{\cos\frac{\pi}{4} - \cos\frac{\pi}{2}}{\sin\frac{\pi}{2} - \sin\frac{\pi}{4}} = \frac{1}{\sqrt{2} - 1}$。



### 四、相关变化率

设$x = x(t), y = y(t)$都是可导的，而$x$与$y$存在某种依赖关系，从而导数$\frac{dx}{dt}, \frac{dy}{dx}$也存在某种关系，==这两个相关导数称为相关变化率==。

​	例3、设有深为$8m$，上顶直径为$8m$的正圆锥形容器，现往容器内注水，其速率为$4m^3/min$，问当水深为$5m$时水表面上升的速度是多少？

![](images/Figure_6.png)

​	解：设注水$t$分钟后，水表面上升的高度为$x \ m$。已知$AB = 8m, OE = 8m, OF = x \ m$，因为$\triangle OAB \sim \triangle OCD$，所以$\frac{CD}{AB} = \frac{OF}{OE}$，即$\frac{CD}{8} = \frac{x}{8} \Longrightarrow CD = x$。当注水$t$分钟时，水的体积$V = \frac{1}{3}\pi(\frac{CD}{2})^2 \cdot OF = \frac{\pi}{12}x^3$，$\frac{dv}{dt} = \frac{\pi}{12} \cdot 3x^2 \cdot \frac{dx}{dt}$，解得$\frac{dx}{dt} = \frac{4}{\pi x^2} \cdot \frac{dv}{dt}$，当$x = 5$时，$\frac{dv}{dt} = 4m^3/min, \frac{dx}{dt} = \frac{16}{25\pi} \approx 0.204 m/min$。



## 第4节 函数的微分

### 一、微分的概念

设函数$y = f(x)$在$x_0$点处自变量$x$有增量$\Delta x$，函数$y$对应的增量$\Delta y = f(x_0 + \Delta x) - f(x_0)$，当$y = f(x)$很复杂时，计算$\Delta y$很麻烦，寻找$\Delta y$的一个既简单而又有一定精度的近似表达式。

例1、设有一个正方形的金属薄片，加热之后边长由$x_0$变化到$x_0 + \Delta x$，现求金属薄片面积增加了多少？

![](images/Figure_7.png)

解：设金属薄片的边长为$x$，其面积为$y$，则$y = x^2$，自变量在$x_0$点有增量$\Delta x$，而面积增量为$\Delta y = (x_0 + \Delta x)^2 - x_0^2 = 2x_0\Delta x + (\Delta x)^2$，$\Delta y$由两部分组成：$2x_0\Delta x$是关于$\Delta x$的==线性部分==与$(\Delta x)^2$是关于$\Delta x$的高次幂，当$\Delta x \to 0$时，$(\Delta x)^2 = O(\Delta x)$，此时==可舍去==$\Delta x$的==高阶无穷小==部分（$|\Delta x|$很小时）。取$\Delta y \approx 2x_0\Delta x$。类似地，$y = x^3, \Delta y = (x_0 + \Delta x)^3 - x_0^3 = 3x_0^2\Delta x + [3x_0(\Delta x)^2 + (\Delta x)^3]$，其中：$3x_0^2\Delta x$是关于$\Delta x$的线性部分，当$\Delta x \to 0$时，$3x_0(\Delta x)^2 + (\Delta x)^3 = O(\Delta x)$ ，取$\Delta y \approx 3x_0^2\Delta x$。



==函数微分的定义==：设函数$y = f(x)$在$N(x_0, \delta), (\delta > 0)$有定义，当$x$在$x_0$点有增量$\Delta x, (x_0 + \Delta x \in N(x_0, \delta))$，如果$y = f(x)$在$x_0$点的增量$\Delta y$可以表示为$\Delta y = k\Delta x + \alpha$，其中$k$是不依赖于$\Delta x$的常数，$\alpha = O(\Delta x)$（当$\Delta \to 0$，则称==$k\Delta x$==为$y = f(x)$在$x_0$点的==微分==，称$y = f(x)$在$x_0$点==可微==。）

$dy|_{x = x_0} = k\Delta x$，由定义可知，当$\Delta x \to 0$时，$\Delta y = k\Delta x + \alpha \to 0, dy = k\Delta x \to 0, \lim_{\Delta \to 0}\frac{\Delta y}{dy} = \frac{k\Delta x + \alpha}{k\Delta x} = 1 + \frac{1}{k}\lim_{\Delta x \to 0}\frac{\alpha}{\Delta x} = 1$，说明当$\Delta x \to 0, \Delta y \sim dy$。

==问题==：$y = f(x)$满足什么条件，它才是可微的？

==定理==：函数$y = f(x)$在$x_0$点可微$\Longleftrightarrow$$y = f(x)$在$x_0$点可导。

证：$\Longleftarrow$充分性。设$y = f(x)$在$x_0$点可导，自变量$x$在$x_0$点有增量$\Delta x$，函数$y$对应增量$\Delta y$，则有：$\lim_{\Delta x \to 0}\frac{\Delta y}{\Delta x} = f^\prime(x_0)$。再根据==有极限的函数与无穷小的关系==：$\frac{\Delta y}{\Delta x} = f^\prime(x_0) + \beta, \lim_{\Delta x \to 0}\beta = 0$，$\Delta y = f^\prime(x_0)\Delta x + \beta \cdot \Delta x$，其中$f^\prime(x_0)$是与$\Delta x$无关的常数，$\alpha = \beta \cdot \Delta x$，当$\Delta x \to 0$时，$\lim_{\Delta x \to 0}\frac{\beta \cdot \Delta x}{\Delta x} = \lim_{\Delta x \to 0}\beta = 0$，即$\alpha = O(\Delta x), (\Delta x \to 0)$，按照微分的定义，可知$f(x)$在$x_0$点可微。

再证：$\Longrightarrow$必要性：设$y = f(x)$在$x_0$点可微，根据微分的定义：自变量$x$在$x_0$点有增量$\Delta x$，$\Delta y = k\Delta x + \alpha$，其中$k$与$\Delta x$无关，$\lim_{\Delta x \to 0}\frac{\alpha}{\Delta x} = 0$，$\frac{\Delta y}{\Delta x} = \frac{k\Delta x + \alpha}{\Delta x} = k + \frac{\alpha}{\Delta x}$，$\lim_{\Delta x \to 0}\frac{\Delta y}{\Delta x} = \lim_{\Delta x \to 0}(k + \frac{\alpha}{\Delta x}) = k + 0 = k$，所以$y = f(x)$在$x_0$点可导，且$f^\prime(x_0) = k$。

于是$dy|_{x = x_0} = k\Delta x = f^\prime(x_0)\Delta x$。==规定$\Delta x = dx, dy|_{x = x_0} = f^\prime(x_0)dx$，对于任一点$x$，$y = f(x)$可微，则$dy = f^\prime(x)dx$。==

​	例如：$y = \sin x$在$(-\infty, +\infty)$内可导，$y = \sin x$在$(-\infty, +\infty)$内处处可微。$\forall_x \in (-\infty, +\infty), dy = (\sin x)^\prime dx = \cos x dx$，取$x = \frac{\pi}{3}$，$dy|_{x = \frac{\pi}{3}} = \cos \frac{\pi}{3} dx = 0.5dx$，取$x = \frac{\pi}{3}, dx = 0.01$时，$y = \sin x$的微分：$dy|_{x = \frac{\pi}{3}, dx = 0.01} = 0.5 \times 0.01 = 0.005$，而$\Delta y = f(\frac{\pi}{3} + 0.01) - f(\frac{\pi}{3}) = \sin(\frac{\pi}{3} + 0.01) - \sin(\frac{\pi}{3}) \approx 0.005$。



### 二、微分的几何意义

![](images/Figure_8.png)

设$y = f(x)$在$x_0$点可导，点$P_0$的坐标为$P_0(x_0, f(x_0))$，点$P$的坐标为$P(x_0 + \Delta x, f(x_0 + \Delta x))$，其中$P_0N = \Delta x, NP = \Delta y, NT = P_0N \cdot \tan\alpha = f^\prime(x_0)\Delta x = dy$，可见$y = f(x)$在$x_0$点处的微分$dy|_{x = x_0}$在几何上表示曲线$y = f(x)$在$P_0(x_0, f(x_0))$处==切线的纵坐标的增量==。



### 三、复合函数的微分法则

设$u = \phi(x), y = f(u)$都是可微函数，则复合函数$y = f[\phi(x)]$的微分为$dy = \{f[\phi(x)]\}^\prime dx = f^\prime(u)\phi^\prime(x)dx = f^\prime(u)du$，当$x$为自变量时，$y = f(x)$的微分$dy = f^\prime(x)dx$，当$u$为中间变量时，$y = f(u)$的微分$dy = f^\prime(u)du$，称为==微分形式不变性==，==对于中间变量来说：$\Delta u \neq du, dy \neq f^\prime(u)\Delta u, dy = f^\prime(u)du$。==

