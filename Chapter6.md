[toc]

# 第6章 定积分

## 第1节 定积分的概念

### 一、实例

1. 曲边梯形的面积

==曲边梯形==：$y = f(x) \ge 0, a \le x \le b, y = f(x) \in C[a, b]$在$xoy$平面上，由直线$x=a, x=b, y = 0$和曲线$y=f(x)$所围成的图形。

求曲边梯形的面积：

1. 在$[a, b]$内插入分点：$a = x_0 < x_1 < x_2 < \cdots < x_{i-1} < x_i < \cdots < x_n = b$把$[a, b]$分成$n$个小区间：$[x_0, x_1], [x_1, x_2], \cdots, [x_{i-1}, x_i], \cdots, [x_{n-1}, x_n]$，小区间的长度分别为：$\Delta x_1 = x_1 - x_0, \Delta x_2 = x_2 - x_1, \cdots, \Delta x_i = x_i - x_{i-1}, \cdots \Delta x_n = x_n - x_{n-1}$。过分点$x_1, x_2, \cdots, x_{i-1}, x_i, \cdots, x_{n-1}$作平行于$y$轴的直线，把曲边梯形分割为$n$个窄的曲边梯形，每个窄曲边梯形的面积记为$\Delta s_i, (i=1,2,\cdots, n)$。
2. 在$[x_{i-1}, x_i]$上任取一点$\xi_i$，以$[x_{i-1}, x_i]$为底，$f(\xi_i)$为高的矩形面积近似代替$\Delta s_i$，即$\Delta s_i \approx f(\xi_i)\Delta x_i$。
3. 整个曲边梯形的面积：$S = \sum_i^n \Delta s_i \approx \sum_i^n f(\xi)\Delta x_i$。
4. 记$\lambda = \max(\Delta x_1, \Delta x_2, \cdots, \Delta x_n)$，当$\lambda \to 0$时和式$\sum_i^n f(\xi)\Delta x_i$的极限就定义为曲边梯形的面积。

==总结==：分割-作乘积-求和-取极限。

### 二、定积分的几何意义

例子：应用定积分定义：

（1）求极限$\lim_{n \to \infty}(\frac{1}{\sqrt{4n^2-1^2}} + \frac{1}{\sqrt{4n^2-2^2}} + \cdots + \frac{1}{\sqrt{4n^2-n^2}})$。

（2）把定积分$\int_0^1 \ln(1+x)dx$表示为$n \to \infty$时和式的极限。

解：（1）原式$= \lim_{n \to \infty}\sum_i^n \frac{1}{\sqrt{4n^2-i^2}} = \lim_{n \to \infty}\sum_i^n \frac{1}{\sqrt{4-(\frac{i}{n}^2)}}\cdot \frac{1}{n}$，记$\Delta x_i = \frac{1}{n}$，取$\xi = \frac{i}{n}$，即把$[0, 1]$分成$n$等份，在$[0, 1]$内插入分点：$x_0 = 0 < x_1 = \frac{1}{n} < x_2 = \frac{2}{n} < \cdots < x_i = \frac{i}{n} < \cdots < \frac{n}{n} = 1$，任一子区间长度$\Delta x_i = \frac{i}{n} - \frac{i-1}{n} = \frac{1}{n}$，$\forall_{\xi_i} = \frac{i}{n} \in [\frac{i-1}{n}, \frac{i}{n}], f(\xi_i) = \frac{1}{\sqrt{4-\xi_i^2}} = \frac{1}{\sqrt{4-(\frac{i}{n})^2}}$。选取被积函数$f(x) = \frac{1}{\sqrt{4-x^2}}, \therefore \lim_{n \to \infty}\sum_i^n \frac{1}{\sqrt{4n^2-i^2}} = \lim_{n \to \infty}\sum_i^n \frac{1}{\sqrt{4-(\frac{i}{n}^2)}}\cdot \frac{1}{n} = \lim_{n \to \infty}\sum_i^n\frac{1}{\sqrt{4-\xi_i^2}}\Delta x_i = \int_0^1\frac{1}{\sqrt{4-x^2}}dx$。

（2）$\int_0^1 \ln(1+x)dx$表示为$n \to \infty$时和式的极限，在$[0, 1]$插入分点：$x_0 = 0 < x_1 = \frac{1}{n} < x_2 = \frac{2}{n} < \cdots < x_i = \frac{i}{n} < \cdots < \frac{n}{n} = 1$，把$[0, 1]$分成$n$个子区间：$[0, \frac{1}{n}], [\frac{1}{n}, \frac{2}{n}], \cdots, [\frac{n-1}{n}, 1]$，每个子区间的长度$\Delta x_i = \frac{1}{n}, (i=1, 2, \cdots, n), \forall_{\xi_i} = \frac{i}{n} \in [\frac{i-1}{n}, \frac{i}{n}], \int_0^1 \ln(1+x)dx = \lim_{n\to\infty}\sum_{i=1}^n \ln(1+\frac{i}{n})\cdot\frac{1}{n}$。



## 第2节 定积分的性质，定积分中值定理

### 一、定积分的性质

1. 若$f(x), g(x)$在$[a, b]$上可积，则$f(x) \pm g(x)$在$[a, b]$上也可积，且有$\int_a^b [f(x)\pm g(x)]dx = \int_a^b f(x)dx \pm \int_a^b g(x)dx$。

2. 设$f(x)$在$[a, b]$上可积，$k$为常数，则$kf(x)$也在$[a, b]$区间上可积，且$\int_a^b kf(x)dx = k\int_a^b f(x)dx$。

3. 设$f(x)$在$[\alpha, \beta]$上可积，常数$a, b, c \in [\alpha, \beta]$（==无论$a, b, c$的相对位置如何==）都有：$\int_a^b f(x)dx = \int_a^c f(x)dx + \int_c^b f(x)dx$。

   证：若$a < c < b, [a, c], [c, b] \subseteq [\alpha, \beta]$，$\because f(x)$在$[\alpha, \beta]$上可积，$\therefore f(x)$在$[a, c], [c, b]$上也可积，选取$c$为一个分点，用$\sum_{[a, b]}$表示$f(x)$在$[a, b]$上的分割求和，$\sum_{[a, c]}^\prime$表示$f(x)$在$[a, c]$上的分割求和，$\sum_{[c, b]}^{\prime\prime}$ 表示$f(x)$在$[c, b]$上的分割求和，则有$\sum_{[a, b]}f(\xi_i)\Delta x_i = \sum_{[a, c]}^\prime f(\xi_i)\Delta x_i + \sum_{[c, b]}^{\prime\prime}f(\xi_i)\Delta x_i$，令$\lambda = \max(\Delta x_1, \Delta x_2, \cdots, \Delta x_n), \lim_{\lambda \to 0}\sum_{[a, b]}f(\xi_i)\Delta x_i = \lim_{\lambda \to 0}\sum_{[a, c]}^\prime f(\xi_i)\Delta x_i + \lim_{\lambda \to 0}\sum_{[c, b]}^{\prime\prime}f(\xi_i)\Delta x_i$，$\therefore \int_a^b f(x)dx = \int_a^c f(x)dx + \int_c^b f(x)dx$。

4. 若$f(x), g(x)$在$[a, b]$上可积，且$f(x) \le g(x)$，则$\int_a^b f(x)dx \le \int_a^b g(x) dx, (a < b)$。

   证：对$[a, b]$进行任意划分，$\forall_{\xi_i} \in (x_{i-1}, x_i), (i=1, 2, \cdots, n)$都有$f(\xi_i) \le g(\xi_i)$，$\Delta x_i = x_i - x_{i-1} > 0 \Longrightarrow f(\xi_i)\Delta x_i \le g(\xi_i)\Delta x_i$，$\therefore \sum_{i=1}^n f(\xi_i)\Delta x_i \le \sum_{i=1}^n g(\xi_i)\Delta x_i, \therefore \lim_{\lambda \to 0}\sum_{i=1}^n f(\xi_i)\Delta x_i \le \lim_{\lambda \to 0}\sum_{i=1}^n g(\xi_i)\Delta x_i$，即$\int_a^b f(x)dx \le \int_a^b g(x)dx$。

   由性质4，可推出以下结论：

   ==推论1==：若$f(x)$在$[a, b], (a < b)$上可积，且$f(x) \ge 0$，则$\int_a^b f(x) dx \ge 0$，若$a > b$，则$\int_a^b f(x)dx \le 0$。类似地，若$f(x)$在$[a, b], (a < b)$上可积，且$f(x) \le 0$，则$\int_a^b f(x) dx \le 0$，若$a > b$，则$\int_a^b f(x)dx \ge 0$。

5. 若$f(x)$在$[a, b], (a < b)$上可积，则$|\int_a^b f(x) dx| \le \int_a^b |f(x)| dx$。

   证：已知$-|a| \le a \le |a|$。由上述绝对值性质，有$-|f(x)| \le f(x) \le |f(x)|, (a \le x \le b)$，由性质4，有$-\int_a^b |f(x)| dx \le \int_a^b f(x) dx \le \int_a^b |f(x)| dx, \therefore |\int_a^b f(x)dx| \le \int_a^b |f(x)| dx$。

6. 设$f(x)$在$[a, b], (a < b)$上可积，且$\max_{[a, b]}f(x) = M, \min_{[a, b]}f(x) = m$，则$m(b-a) \le \int_a^b f(x) dx \le M(b-a)$（==定积分估值定理==）。

   证：由假设，有$m \le f(x) \le M, a \le x \le b$，则有$\int_a^b m dx \le \int_a^b f(x)dx \le \int_a^b M dx \Longrightarrow m\int_a^b dx \le \int_a^b f(x)dx \le M \int_a^b dx \Longrightarrow m(b-a) \le \int_a^b f(x)dx \le M(b-a)$



### 二、定积分中值定理

==定理1==：设$f(x), g(x) \in C[a, b]$，且$g(x)$在$[a, b]$上不变号，则至少存在一点$\xi \in [a, b]$，使得$\int_a^b f(x)g(x) dx = f(\xi)\int_a^b g(x)dx$。

证：$\because f(x) \in C[a, b], \therefore f(x)$在$[a, b]$上一定有最大值$M$和最小值$m$，即$m \le f(x) \le M, x \in [a, b]$。由假设，不妨设$g(x) \ge 0$，则有$mg(x) \le f(x)g(x) \le Mg(x), a \le x \le b, \therefore m\int_a^b g(x)dx \le \int_a^b f(x)g(x)dx \le M \int_a^b g(x)dx$， $\because g(x) \ge 0, \therefore \int_a^b g(x) dx \ge 0$。

假若$\int_a^b g(x)dx = 0$，则有$m \cdot 0 \le \int_a^b f(x)g(x) dx \le M \cdot 0, \therefore \int_a^b f(x)g(x) dx = 0$，显然对于任何一点$\xi \in [a, b]$，等式$\int_a^b f(x)g(x)dx = f(\xi)\int_a^b g(x)dx$均成立。

假若$\int_a^b g(x)dx > 0$，则有$m \le \frac{\int_a^b f(x)g(x)dx}{\int_a^b g(x)dx} < M$，设$\mu = \frac{\int_a^b f(x)g(x)dx}{\int_a^b g(x)dx}$，则$m \le \mu \le M$，根据闭区间$[a, b]$上连续函数$f(x)$的介值定理，至少存在一点$\xi \in [a, b]$，使得$f(\xi) = \mu = \frac{\int_a^b f(x)g(x)dx}{\int_a^b g(x)dx}$，故$\int_a^b f(x)g(x) dx = f(\xi)\int_a^b g(x)dx$。

==定理2==：设$f(x) \in C[a, b]$，则至少存在一点$\xi \in [a, b]$，使得$\int_a^b f(x) dx = f(\xi)(b-a)$。



例1：设$f(x) \in C[0, 1], f(x) \in D(0, 1)$，且$3\int_\frac{2}{3}^1 f(x)dx = f(0)$，证明：至少存在一点$\xi \in (0, 1)$，使得$f^\prime(\xi) = 0$。

证：由命题的结论可知，可用Rolle定理来推证。由题设有$3\int_\frac{2}{3}^1 f(x)dx = f(0)$，$\because [\frac{2}{3}, 1] \subset [0, 1]$，由$f(x) \in C[0, 1] \Longrightarrow f(x) \in C[\frac{2}{3}, 1]$。根据定积分中值定理，至少存在一点$\xi^\prime \in [\frac{2}{3}, 1] \subset [0, 1]$，使$3 f(\xi^\prime)(1-\frac{2}{3}) = f(0) \Longrightarrow f(\xi^\prime) = f(0)$，即$f(x) \in C[0, \xi^\prime], f(x) \in D(0, \xi^\prime), f(\xi^\prime) = f(0)$，根据Rolle定理，至少存在一点$\xi \in (0, \xi^\prime) \subset (0, 1)$，使得$f^\prime(\xi) = 0$。



## 第3节 定积分与原函数的关系

### 一、变上限的定积分

设$f(x) \in C[a, b], \forall_x \in [a, b]$，考察定积分：$\int_a^x f(x) dx$。

（1）$\because f(x) \in C[a, x], \therefore \int_a^x f(x)dx$存在，在此积分中积分变量和积分上限用同一字母$x$表示，由于可积函数的积分值与积分变量用什么字母表示无关，现在以$t$表示积分变量，以$x$表示积分上限，就有$\int_a^x f(x) dx = \int_a^x f(t) dt, a \le t \le x \le b$。

（2）如果让积分上限$x$在$[a, b]$上变动，对每一个取定的$x \in [a, b]$，通过定积分$\int_a^x f(t)dt$，有一个确定的值与之对应，由函数的定义，可知，变上限的定积分$\int_a^x f(t)dt$在$[a, b]$上确定了一个$x$的函数，记为：$\Phi(x) = \int_a^x f(t)dt, x \in [a, b]$，称为积分上限的函数。

==定理==：设$f(x) \in C[a, b]$，则$\Phi(x) = \int_a^x f(t)dt$在$[a, b]$上是可导的，且$\frac{d\Phi(x)}{dx} = \frac{d[\int_a^x f(t)dt]}{dx} = f(x), (a \le x \le b)$。

证：$\forall_x \in [a, b]$，$x$有增量$\Delta x, x + \Delta x \in [a, b]$，$\Phi(x+\Delta x) = \int_a^{x+\Delta x}f(t)dt$，函数$\Phi(x)$在$x$点处的增量$\Delta \Phi(x) = \Phi(x+\Delta x) - \Phi(x) = \int_a^{x+\Delta x}f(t)dt - \int_a^x f(t)dt \\ =\int_a^x f(t) dt + \int_x^{x+\Delta x}f(t)dt - \int_a^x f(t)dt = \int_x^{x+\Delta x}f(t)dt = f(\xi)\Delta x$

，其中$\xi$在$[x, x+\Delta x]$或$[x+\Delta x, x]$之间。求极限$\lim_{\Delta x \to 0}\frac{\Delta \Phi(x)}{\Delta x}$，当$\Delta x \to 0$时$\xi \to x$，$\lim_{\Delta x \to 0}\frac{\Delta \Phi(x)}{\Delta x} = \lim_{\Delta x \to 0}\frac{f(\xi)\Delta x}{\Delta x} = \lim_{\xi \to x}f(\xi) = f(x)$，所以$\frac{d[\int_a^x f(t)dt]}{dx} = f(x)$。



由原函数的定义，可知$\int_a^x f(t)dt$是$f(x)$的原函数，那么有：$\int f(x)dx = \int_a^x f(t)dt + C$。

若$f(x) \in C[a,b ]$，$\frac{d[\int_a^x f(t)dt]}{dx} = f(x)$。



例1：求$\frac{d[\int_1^{x^2} e^{-t^2}dt]}{dx}$。

解：令$u = x^2$，$\frac{d[\int_1^{x^2} e^{-t^2}dt]}{dx}$（其上限为$x$的函数，本质上是复合函数），所以$\frac{d[\int_1^{x^2} e^{-t^2}dt]}{dx} = \frac{d[\int_1^{u} e^{-t^2}dt]}{du} \cdot \frac{du}{dx} = e^{-u^2} \cdot 2x = 2x \cdot e^{-x^4}$。



例2：求$\frac{d[\int_{x^2}^{\sin x}e^{-t^2}dt]}{dx}$。

解：$\int_{x^2}^{\sin x}e^{-t^2}dt = \int_{x^2}^a e^{-t^2}dt + \int_a^{\sin x}e^{-t^2}dt$，则$\frac{d[\int_{x^2}^{\sin x}e^{-t^2}dt]}{dx} = -2x \cdot e^{-x^4} + e^{-\sin^2 x} \cdot \cos x$。



### 二、牛顿——莱布尼茨公式

==定理==：设$f(x) \in C[a, b]$，$F(x)$是$f(x)$在$[a, b]$上的一个原函数，则$\int_a^b f(x) dx = F(b) - F(a)$。

证：由上面的定理知：$\Phi(x) = \int_a^x f(t)dt$是$f(x)$在$[a, b]$上的一个原函数，由题设$F(x)$也是$f(x)$在$[a, b]$上的一个原函数，于是$F(x) - \Phi(x) = C \Longrightarrow F(x) = \Phi(x) + C$。则有$F(b) - F(a) = [\Phi(b) + C] - [\Phi(a) + C] = \Phi(b) - \Phi(a) = \int_a^b f(t)dt - \int_a^a f(t)dt = \int_a^b f(t)dt = \int_a^b f(x)dx$，即$\int_a^b f(x)dx = F(b) - F(a)$。



## 第4节 定积分计算法

### 一、求定积分的换元积分法

设$f(x) \in C[a, b]$，单值函数$x = \phi(t)$在$[\alpha, \beta]$上有连续导数，当$t$在$[\alpha, \beta]$上变动时，$\phi(t)$的值在$[a, b]$上变化，并且$\phi(\alpha) = a, \phi(\beta) = b$，则有$\int_a^b f(x)dx = \int_{\alpha}^{\beta} f[\phi(t)]\phi^\prime(t)dt$。

证：因为$f(x) \in C[a, b], f[\phi(t)]\phi^\prime(t) \in C[\alpha, \beta]$，所以上式两边积分都存在。设$F(x)$是$f(x)$在$[a, b]$上的一个原函数，由牛顿-莱布尼茨公式，有$\int_a^b f(x)dx = F(x)|_{a}^{b} = F(b) - F(a)$。

再证明：$F[\phi(t)]$是$f[\phi(t)]\phi^\prime(t)$在$[\alpha, \beta]$上的原函数：$\frac{dF[\phi(t)]}{dt} = \frac{d F(x)}{dx} \cdot \frac{dx}{dt} = f[\phi(t)]\phi^\prime(t)$，所以$F[\phi(t)]$是$f[\phi(t)]\phi^\prime(t)$在$[\alpha, \beta]$上的原函数，因此$\int_\alpha^\beta f[\phi(t)]\phi^\prime(t)dt = F[\phi(t)]|_\alpha^\beta = F[\phi(\beta)] - F[\phi(\alpha)] = F(b) - F(a)$。

所以$\int_a^b f(x)dx = \int_\alpha^\beta f[\phi(t)]\phi^\prime(t)dt$。

==注意==：求出$f[\phi(t)]\phi^\prime(t)$的一个原函数$F[\phi(t)]$不必把$t$换成原来的变量$x$，只要把新的积分限$\alpha, \beta$代入$F[\phi(t)]$中，求差值$F[\phi(\beta)] - F[\phi(\alpha)]$即可。



例1：设$f(x) \in C[-a, a], (a > 0)$。证：

（1）若$f(x)$是奇函数，则$\int_{-a}^{a}f(x)dx = 0$；

（2）若$f(x)$是偶函数，则$\int_{-a}^a f(x)dx = 2\int_0^a f(x)dx$。

证：$\int_{-a}^a f(x)dx = \int_{-a}^0 f(x)dx + \int_0^a f(x)dx$，对$\int_{-a}^0 f(x)dx$，作变换：$x = -t$，当$x = -a$时，$t=a$；当$x=0$时，$t=0$，$\int_{-a}^0 f(x)dx = \int_a^0 -f(-t)dt = \int_0^a f(-t)dt$，$\therefore \int_{-a}^a f(x)dx = \int_0^a f(-t)dt + \int_0^a f(x)dx = \int_0^a f(-x)dx + \int_0^a f(x)dx = \int_0^a[f(-x)+f(x)]dx$。

（1）若$f(x)$为奇函数，则$f(-x) = -f(x) \Longrightarrow f(-x) + f(x) = 0$，$\therefore \int_{-a}^a f(x)dx = \int_0^a [f(-x) + f(x)]dx = \int_0^a 0dx = 0$；

（2）若$f(x)$为偶函数，则$f(-x) = f(x) \Longrightarrow f(-x) + f(x) = 2f(x)$，$\therefore \int_{-a}^a f(x)dx = \int_0^a[f(-x)+f(x)]dx = \int_0^a 2f(x)dx = 2\int_0^a f(x)dx$。



例2：设$f(x)$是定义在$(-\infty, +\infty)$上以$T$为周期的周期函数，$a$为任意常数，证明$\int_a^{a+T}f(x)dx = \int_0^T f(x)dx$。

证：$\because \int_a^{a+T}f(x)dx = \int_a^0 f(x)dx + \int_0^T f(x)dx + \int_T^{a+T}f(x)dx$。要证明$\int_a^{a+T}f(x)dx = \int_0^T f(x)dx$，只须证明$\int_a^0 f(x)dx + \int_T^{a+T}f(x)dx = 0 \Longleftrightarrow -\int_a^0 f(x)dx = \int_T^{a+T}f(x)dx \Longleftrightarrow \int_0^a f(x)dx = \int_T^{a+T}f(x)dx$。

作变换，令$x = t + T$。$\int_T^{a+T}f(x)dx = \int_0^a f(t+T)dt$，$\because f(t+T) = f(t), \therefore \int_0^a f(t+T)dt = \int_0^a f(t)dt = \int_0^a f(x)dx$，$\therefore \int_a^{a+T} f(x)dx = \int_0^T f(x)dx$。



例3：证$\int_0^\pi \sin^n x dx = 2\int_0^\frac{\pi}{2} \sin^n x dx$。

证：$\int_0^\pi \sin^n x dx = \int_0^\frac{\pi}{2} \sin^n x dx + \int_\frac{\pi}{2}^\pi \sin^n x dx$，对$\int_\frac{\pi}{2}^\pi \sin^n x dx$，作变换$x = \pi - t$，$\int_\frac{\pi}{2}^\pi \sin^n x dx = \int_\frac{\pi}{2}^0 -\sin^n(\pi-t)dt = \int_0^\frac{\pi}{2} \sin^n t dt = \int_0^\frac{\pi}{2}\sin^n x dx$，$\therefore \int_0^\pi \sin^n x dx = \int_0^\frac{\pi}{2} \sin^n x dx + \int_\frac{\pi}{2}^\pi \sin^n x dx = 2\int_0^\frac{\pi}{2}\sin^n x dx$。



### 二、定积分的分部积分法

设函数$u(x), v(x)$在$[a, b]$上具有连续的导数$u^\prime(x), v^\prime(x)$，则有$\int_a^b u(x)d[v(x)] = u(x)v(x)|_a^b - \int_a^b v(x)d[u(x)]$。

证：据题设，有$d(uv) = udv + vdu, udv = d(uv) - vdu$，等号两边在$[a, b]$上的积分存在，有$\int_a^b udv = uv|_a^b - \int_a^b vdu$。



例1：证明：

（1）$\int_0^\frac{\pi}{2}\sin^n x dx = \int_0^\frac{\pi}{2}\cos^n x dx$；

（2）$\int_0^\frac{\pi}{2} \sin^n x dx = \left\{\begin{array}{ccc}&\frac{n-1}{n} &\cdot &\frac{n-3}{n-2} &\cdots &\frac{3}{4} &\cdot &\frac{1}{2} &\cdot &\frac{\pi}{2}\quad (n为偶数) \\ &\frac{n-1}{n} &\cdot &\frac{n-3}{n-2} &\cdots &\frac{4}{5} &\cdot &\frac{2}{3} &\  &\ \quad (n为奇数)\end{array}\right.$

证：（1）令$x = \frac{\pi}{2} - t$，$\int_0^\frac{\pi}{2}\sin^n xdx = \int_\frac{\pi}{2}^0 \sin^n(\frac{\pi}{2}-t)(-dt) = \int_0^\frac{\pi}{2} \sin^n(\frac{\pi}{2}-t)dt = \int_0^\frac{\pi}{2} \cos^n t dt = \int_0^\frac{\pi}{2} \cos^n x dx$。

（2）设$I_n = \int_0^\frac{\pi}{2}\sin^n x dx$，$I_n = \int_0^\frac{\pi}{2}\sin^n x dx = \int_0^\frac{\pi}{2}\sin^{n-1} x \sin x dx = \int_0^\frac{\pi}{2}\sin^{n-1} x d(-\cos x) \\ = [\sin^{n-1}x \cdot (-\cos x)]_0^\frac{\pi}{2} - \int_0^\frac{\pi}{2}-\cos x d(\sin^{n-1} x) \\ = 0 + \int_0^\frac{\pi}{2}\cos x \cdot (n-1)\sin^{n-2} x \cos x dx \\ = \int_{0}^\frac{\pi}{2}(n-1)\sin^{n-2}x (1-\sin^2 x)dx \\ = (n-1)[\int_0^\frac{\pi}{2}\sin^{n-2}x dx - \int_0^\frac{\pi}{2}\sin^n x dx] \\ = (n-1)I_{n-2} - (n-1)I_n$

即$nI_n = (n-1)I_{n-2}, \therefore I_n = \frac{n-1}{n}I_{n-2} = \frac{n-1}{n}\frac{n-3}{n-2}I_{n-4} = \frac{n-1}{n}\frac{n-3}{n-2}\frac{n-5}{n-4}I_{n-6}$（递推公式）。

当$n$为正偶数时，$I_n = \frac{n-1}{n}I_{n-2} = \cdots = \frac{n-1}{n}\frac{n-3}{n-2}\cdots\frac{3}{4}\frac{1}{2}I_0$，当$n$为正奇数时，$I_n = \frac{n-1}{n}I_{n-2} = \cdots = \frac{n-1}{n}\frac{n-3}{n-2}\cdots\frac{4}{5}\frac{2}{3}I_1$，$\because I_n = \int_0^\frac{\pi}{2}\sin^n x dx, \therefore I_0 = \int_0^\frac{\pi}{2}1dx = \frac{\pi}{2}, I_1 = \int_0^\frac{\pi}{2}\sin x dx = (-\cos x)_0^\frac{\pi}{2} = 1$，证毕。



例2：设$f(x)$具有连续的二阶导数，$f(\pi) = 2, \int_0^\pi [f(x) + f^{\prime\prime}(x)]\sin x dx = 5$，求$f(0)$。

解：$\int_0^\pi f(x)\sin x dx = \int_0^\pi f(x)d(-\cos x) = [-f(x)\cos x]_0^\pi - \int_0^\pi -\cos x f^\prime(x)dx \\ = f(\pi) + f(0) + \int_0^\pi f^\prime(x)d(\sin x) \\ = f(\pi) + f(0) + f^\prime(x)\sin x |_0^\pi - \int_0^\pi f^{\prime\prime}(x)\sin x dx \\ = f(\pi) + f(0) + [0 - \int_0^\pi f^{\prime\prime}(x)\sin x dx]$

$\therefore \int_0^\pi [f(x) + f^{\prime\prime}(x)]\sin x dx = f(\pi) + f(0) = 5$，$\because f(\pi) = 2, \therefore f(0) = 3$。



## 第6节 广义积分、$\Gamma$函数

定积分中规定：（1）积分区间$[a, b]$是有限区间，即$a, b$是常数；（2）被积函数$f(x) \in C(a, b)$或$f(x)$在$[a, b]$上有界，且至多有有限个间断点。

但是有时积分区间是无限区间、被积函数$f(x)$在$[a, b]$内无界，需要推广积分的概念。



### 一、无穷限的广义积分

==定义==：若$f(x)$在$[a, +\infty)$上是连续函数，取$b > a$，如果极限$\lim_{b \to +\infty}\int_a^b f(x)dx$存在，则称此极限为函数$f(x)$在$[a, \infty)$上的广义积分。

类似地，若$f(x) \in C(-\infty, b]$，取$a < b$，如果极限$\lim_{a \to -\infty}\int_a^b f(x)dx$存在，则称此极限为函数$f(x)$在$(-\infty, b]$上的广义积分。

若$f(x) \in C(-\infty, +\infty)$，任取实数$c$，$-\infty < c < +\infty$，两个广义积分$\int_{-\infty}^c f(x)dx$与$\int_c^{+\infty}f(x)dx$都存在，则称$\int_{-\infty}^c f(x)dx + \int_c^{+\infty}f(x)dx$为$f(x)$在$(-\infty, +\infty)$ 上的广义积分。

记为：

$\int_a^{+\infty}f(x)dx = \lim_{b\to +\infty}\int_a^b f(x)dx$

$\int_{-\infty}^b f(x)dx = \lim_{a \to -\infty}\int_a^b f(x)dx$

$\int_{-\infty}^{+\infty}f(x)dx = \int_{-\infty}^c f(x)dx + \int_c^{+\infty}f(x)dx$



例1：计算广义积分$\int_0^{+\infty}te^{-pt}dt$，其中$p > 0$为常数。

解：$\int_0^{+\infty}te^{-pt}dt = \lim_{b \to +\infty}\int_0^b te^{-pt}dt = \lim_{b \to +\infty}\int_0^b t d(-\frac{e^{-pt}}{p}) \\ = \lim_{b \to +\infty}[-\frac{te^{-pt}}{p}|_0^b - \int_0^b -\frac{e^{-pt}}{p}dt] \\ = -\frac{1}{p}\lim_{b \to +\infty}\frac{b}{e^{pb}} - \frac{1}{p^2}\lim_{b \to +\infty}\int_0^b e^{-pt}d(-pt) = \frac{1}{p^2}$



例2：验证：$\int_a^{+\infty}\frac{1}{x^p}, (a > 0)$，当$p > 1$时，广义积分收敛，$p \le 1$时，广义积分发散。

解：当$p=1$时，$\int_a^{+\infty}\frac{1}{x}dx = \lim_{b \to +\infty}\int_a^b \frac{1}{x}dx = \lim_{b \to +\infty}[\ln x]_a^b = \lim_{b \to +\infty}\ln b - \lim_{b \to +\infty}\ln a = +\infty$，

当$p < 1$时，$\int_a^{+\infty}\frac{1}{x^p}dx = \lim_{b \to +\infty}\int_a^b x^{-p}dx = \lim_{b \to +\infty}[\frac{x^{1-p}}{1-p}]|_a^b \\ = \frac{1}{1-p}[\lim_{b \to +\infty}b^{1-p} - \lim_{b \to \infty}a^{1-p}] = +\infty$

当$p > 1$时，$\int_a^{+\infty}\frac{1}{x^p}dx = \lim_{b \to +\infty}\int_a^b x^{-p}dx = \lim_{b \to +\infty}[\frac{1}{1-p}\frac{1}{x^{p-1}}]|_a^b \\ = \frac{1}{1-p}[\lim_{b \to +\infty}\frac{1}{b^{p-1}} - \lim_{b \to +\infty}\frac{1}{a^{p-1}}] \\ = \frac{1}{1-p}(0-\frac{1}{a^{p-1}}) = \frac{1}{p-1}\frac{1}{a^{p-1}}$

这就验证了题目的结论。



例3：计算$\int_{-\infty}^{+\infty}\frac{1}{1+x^2}dx$。

解：$\int_{-\infty}^{+\infty}\frac{1}{1+x^2}dx = \int_{-\infty}^0 \frac{1}{1+x^2}dx + \int_0^{+\infty}\frac{1}{1+x^2}dx = \lim_{a \to -\infty}\int_a^0 \frac{1}{1+x^2}dx + \lim_{b \to +\infty}\int_0^b \frac{1}{1+x^2}dx \\ = \lim_{a \to -\infty}[\arctan x]|_a^0 + \lim_{b \to +\infty}[\arctan x]|_0^b = -(-\frac{\pi}{2}) + \frac{\pi}{2} = \pi$



==注意==：不能写成$\int_{-\infty}^{+\infty}f(x)dx = \lim_{a \to +\infty}\int_{-a}^{+a}f(x)dx$，若$\lim_{a \to +\infty}\int_{-a}^{+a}f(x)dx$存在，==不能保证==$\int_{-\infty}^{+\infty}f(x)dx$收敛；但如果此极限值存在，则称此极限值为$\int_{-\infty}^{+\infty}f(x)dx$的==柯西主值==。



### 二、无界函数的广义积分

==定义==：设$f(x) \in C(a, b]$，而在点$a$的右邻域内无界，任取一个充分小的$\epsilon > 0$，$f(x)$在$[a + \epsilon, b]$上连续，如果极限$\lim_{\epsilon \to 0^+}\int_{a+\epsilon}^b f(x)dx$存在，则称此极限为$f(x)$在$(a, b]$上的广义积分，记为$\int_a^b f(x)dx = \lim_{\epsilon \to 0^+}\int_{a + \epsilon}^b f(x)dx$。

类似地，设$f(x) \in C[a, b)$，而在点$b$的左邻域内无界，任取一个充分小的整数$\eta > 0$，$f(x)$在$[a, b - \eta]$上连续，如果极限$\lim_{\eta \to 0^+}\int_a^{b-\eta} f(x)dx$存在，则称此极限为$f(x)$在$[a, b)$上的广义积分，记为$\int_a^b f(x)dx = \lim_{\eta \to 0^+}\int_a^{b-\eta} f(x)dx$。

设$f(x)$在$[a, b]$上除点$c, (a < c < b)$外连续，而点$c$的邻域内无界，如果两个广义积分：$\int_a^c f(x)dx, \int_c^b f(x)dx$都收敛，则定义$\int_a^c f(x)dx + \int_c^b f(x)dx$为$f(x)$在$[a, b]$上的广义积分，记为$\int_a^b f(x)dx = \int_a^c f(x)dx + \int_c^b f(x)dx$。



例1：求$\int_0^1 \frac{1}{\sqrt{1-x^2}}dx$。

解：$\because \lim_{x \to 1^-}\frac{1}{\sqrt{1-x^2}} = +\infty$，$\therefore \frac{1}{\sqrt{1-x^2}}$在点$1$的左邻域无界。

$\int_0^1 \frac{1}{\sqrt{1-x^2}}dx = \lim_{\eta \to 0^+}\int_0^{1-\eta}\frac{1}{\sqrt{1-x^2}}dx \\ = \lim_{\eta \to 0^+}[\arcsin x]|_0^{1-\eta} = \lim_{\eta \to 0^+}\arcsin(1-\eta) \\ = \arcsin(1) = \frac{\pi}{2}$



例2：验证广义积分$\int_a^b \frac{1}{(x-a)^p}dx$，当$p < 1$时收敛，当$p \ge 1$时发散。

解：当$p=1$时，$\int_a^b \frac{1}{x-a}dx = \lim_{\epsilon \to 0^+}\int_{a+\epsilon}^b\frac{1}{x-a}dx = \lim_{\epsilon \to 0^+}[\ln(x-a)]|_{a+\epsilon}^b =\lim_{\epsilon \to 0^+}[\ln(b-a) - \ln(\epsilon)] = \infty$

当$p \neq 1$时，$\int_a^b \frac{1}{(x-a)^p}dx = \lim_{\epsilon \to 0^+}\int_{a+\epsilon}^b (x-a)^{-p}dx = \frac{1}{1-p}\lim_{\epsilon \to 0^+}[(x-a)^{1-p}]|_{a+\epsilon}^b \\ = \frac{1}{1-p}[(b-a)^{1-p} - \lim_{\epsilon \to 0^+}\epsilon^{1-p}]$

当$p < 1$时，$\int_a^b \frac{1}{(x-a)^p}dx = \frac{(b-a)^{1-p}}{1-p}$；当$p > 1$时，$\int_a^b \frac{1}{(x-a)^p}dx = \infty$。

这就验证了题目的结论。



==注意==：$\int_{-1}^1 \frac{1}{x^2}dx = [-\frac{1}{x}]|_{-1}^{1} = -1 - 1 = -2$（错误，当$x = 0$时无界）。

正确的做法是：$\int_{-1}^1 \frac{1}{x^2}dx = \int_{-1}^0 \frac{1}{x^2}dx + \int_0^1 \frac{1}{x^2}dx$，其中$\int_{-1}^{0}\frac{1}{x^2}dx = \lim_{\eta \to 0^+}\int_{-1}^{0-\eta}\frac{1}{x^2}dx = \lim_{\eta \to 0^+}[-\frac{1}{x}]|_{-1}^{0-\eta} = \lim_{\eta \to 0^+}(\frac{1}{\eta} - 1) = \infty$，所以$\int_{-1}^1 \frac{1}{x^2}dx$发散。



### 三、$\Gamma$函数

可以证明广义积分：$\int_0^{+\infty} x^{p-1}e^{-x}dx$，当$p > 0$时收敛$\forall_p \in (0, +\infty)$，通过广义积分$\int_0^{+\infty}x^{p-1}e^{-x}dx$有一个确定的实数与之对应，按照函数的定义，就说$\int_0^{+\infty}x^{p-1}e^{-x}dx$定义了一个关于$p$的函数。

==定义==：当$p > 0$时，$\int_0^{+\infty}x^{p-1}e^{-x}dx$所定义的函数$\Gamma(p) = \int_0^{+\infty}x^{p-1}e^{-x}dx$称为$\Gamma$函数。

==性质==：

（1）$\Gamma(1) = 1$。

证：$\Gamma(1) = \int_0^{+\infty}x^{1-1}e^{-x}dx = \int_0^{+\infty}e^{-x}dx = \lim_{b \to +\infty}\int_0^b e^{-x}dx = \lim_{b \to +\infty}[-e^{-x}]|_0^b \\ = \lim_{b \to +\infty}(1 - e^{-b}) = 1 - \lim_{b \to +\infty}e^{-b} = 1 - 0 = 1$

（2）$\Gamma(p+1) = p\Gamma(p)$。

证：$\Gamma(p+1) = \int_0^{+\infty}x^{(p+1)-1}e^{-x}dx = \int_0^{+\infty}x^p e^{-x}dx = \lim_{b \to +\infty}\int_0^b x^p e^{-x}dx \\ = \lim_{b \to +\infty}\int_0^b x^p d(-e^{-x}) = \lim_{b \to +\infty}[-x^p e^{-x}]|_0^b + \lim_{b \to +\infty}p\int_0^b x^{p-1}e^{-x}dx$

$\lim_{b \to +\infty}[-x^p e^{-x}]|_0^b = \lim_{b \to +\infty}(-b^p e^{-b}) = -\lim_{b \to +\infty}\frac{b^p}{e^b} = 0$（根据洛必达法则），所以$\Gamma(p+1) = \lim_{b \to +\infty}[-x^p e^{-x}]|_0^b + \lim_{b \to +\infty}p\int_0^b x^{p-1}e^{-x}dx = \lim_{b \to +\infty}p\int_0^b x^{p-1}e^{-x}dx \\ = p\int_0^{+\infty}x^{p-1}e^{-x}dx = p\Gamma(p)$。

（3）$\Gamma(n + 1) = n!, (n \in N)$。

==$\Gamma$函数的其他形式==：$\Gamma(p) = \int_0^{+\infty}x^{p-1}e^{-x}dx$，现令$x = t^2, (t > 0), dx = 2tdt$，$\Gamma(p) = \int_0^{+\infty} (t^2)^{p-1}e^{-t^2} 2t dt = 2\int_0^{+\infty}t^{2p-1}e^{-t^2}dt = 2\int_0^{+\infty} x^{2p-1}e^{-x^2}dx$。



例1：用$\Gamma$函数表示积分$\int_0^1 (\ln \frac{1}{x})^p dx, (p > 0)$。

解：令$\ln \frac{1}{x} = t, \frac{1}{x} = e^t, x = \frac{1}{e^t}$，当$x = 1$时，$t = 0$，当$x \to 0^+$时，$t \to +\infty$，$\int_0^1 (\ln\frac{1}{x})^p dx = \int_{+\infty}^0 t^p d(e^{-t}) = \int_0^{+\infty} t^p e^{-t}dt = \int_0^{+\infty} t^{(p+1)-1} e^{-t}dt = \Gamma(p + 1)$。



例2：用$\Gamma$函数表示$\int_2^{+\infty}e^2 x e^{-(x-2)^2}dx$，已知$\Gamma(\frac{1}{2}) = \sqrt{\pi}$，计算此积分值。

解：令$x - 2 = t, x = t + 2$，当$x = 2$时，$t = 0$，当$x \to +\infty$时，$t \to +\infty$。

$\int_2^{+\infty}e^2 x e^{-(x-2)^2}dx = \int_0^{+\infty} e^2 (t + 2)e^{-t^2}dt \\ = e^2\int_0^{+\infty}t e^{-t^2}dt + 2e^2\int_0^{+\infty}e^{-t^2}dt \\ = \frac{1}{2} e^2 \cdot 2\int_0^{+\infty}t^{2\cdot 1 - 1} e^{-t^2}dt + 2e^2 \int_0^{+\infty} t^{2 \cdot\frac{1}{2} - 1}e^{-t^2}dt \\ = \frac{1}{2}e^2 \Gamma(1) + e^2 \Gamma(\frac{1}{2}) = \frac{1}{2}e^2 + e^2 \sqrt{\pi} \\ = \frac{e^2}{2}(1+2\sqrt{\pi})$



## 第7节 定积分在几何上的应用

### 一、定积分元素法

所求量（如面积$S$）与$x$变化区间$[a, b]$有关，把$[a, b]$分成一系列部分区间，所求量相应地分成一系列部分量，而且所求量等于部分量的和，称所求量对$[a, b]$具有可加性，$\Delta S_i$与$f(\xi_i)\Delta x$只是差一个高阶无穷小。求部分量的近似值是关键一步。

$\Delta S \approx f(x)dx$， $ds = f(x)dx$——面积元素，则$S = \int_a^b f(x)dx$。



实际问题的所求量$u$符合：

（1）$u$与一个变量$x$的变化区间有关；

（2）$u$对$[a, b]$具有可加性；

（3）$u$的部分量$\Delta u = f(x)dx$；

则可以表示为$u = \int_a^b f(x)dx$。



具体求$u$，先选取积分变量$x$，确定变化区间，在$[a, b]$内任取部分区间$[x, x+dx]$，求此区间对应的所求量的部分量$du = f(x)dx$（$u$的元素），最后求出$u = \int_a^b f(x)dx$。



### 二、平面图形的面积

（1）直角坐标系的情形

例1：求由曲线$y^2 = x, y = x^2$所围成图形的面积。

解：求两条曲线的交点：
$$
\left\{\begin{array}{ccc}&y^2 &= &x \\ &y &= &x^2 \end{array}\right.
$$
求得交点$O(0, 0), A(1, 1)$。

取$x$为积分变量，变化区间$[0, 1]$，任取部分区间$[x, x+dx] \subset [0, 1]$，$ds = (\sqrt{x} - x^2)dx$（面积元素），则$S = \int_0^1 (\sqrt{x} - x^2)dx = \frac{1}{3}$。



一般地，$g(x) \le f(x), x \in [a, b]$，面积元素$ds = [f(x) - g(x)]dx, S = \int_a^b [f(x)-g(x)]dx$。



（2）极坐标的情形

求由极坐标系下曲线$\rho = \rho(\theta)$，两条半直线$\theta = \alpha, \theta = \beta, (\alpha < \beta)$所围成的平面图形的面积（$\rho(\theta)$非负且连续）。选取$\theta$作为积分变量，$\alpha \le \theta \le \beta$，在$\theta$和$\theta + d\theta$之间的曲边扇形近似值（面积元素）$ds = \frac{1}{2}\rho^2(\theta)d\theta$，所以$S = \int_\alpha^\beta \frac{1}{2}\rho^2(\theta)d\theta$。



例3：求心形线$\rho = \alpha(1+\cos\theta), (a > 0)$所围成平面图形的面积。

解：心形线关于极轴对称，所以$S = 2S_1$。面积元素$ds = \frac{1}{2}\alpha^2(1+\cos\theta)^2d\theta$，面积$S = 2S_1 = 2\int_0^\pi \frac{1}{2}\alpha^2(1+\cos\theta)^2d\theta = \alpha^2\int_0^\pi (1+\cos\theta)^2d\theta = \frac{3}{2}\pi\alpha^2$。



例4：求椭圆$\frac{x^2}{a^2} + \frac{y^2}{b^2} = 1$所围成的图形面积。

解：由图形的对称性：$S = 4S_1$，面积元素$ds = y \cdot dx$。
$$
\frac{x^2}{a^2} + \frac{y^2}{b^2} = 1 \Longrightarrow \left\{\begin{array}{ccc}&x &= &a\cos t \\ &y &= &b\sin t\end{array}\right.
$$
故$ds = y \cdot dx = b\sin t(-a\sin t)dt = -ab \sin^2 t dt$。面积$S = 4S_1 = 4\int_0^a y dx = 4\int_\frac{\pi}{2}^0 -ab\sin^2 t dt = 4\int_0^\frac{\pi}{2}ab\sin^2 t dt \\ = 4ab\int_0^\frac{\pi}{2}\frac{1-\cos2t}{2}dt = \pi ab$

当$a = b$时，得到圆的面积$S = \pi a^2$。



### 三、求立体的体积

（1）平行截面面积为已知的立体的体积

设有一曲面和过$x$轴的两点$x = a, x = b, (a < b)$且与$x$轴垂直的平面围成一个立体，过$x$轴上任一点作$x$轴垂直的平面，此平面截此立体，得到一截面，其面积$A(x)$为已知，再求此立体的体积。

取$x$为积分变量：$a \le x \le b$，取部分区间$[x, x + dx] \subset [a, b]$，对应的薄柱体的体积近似看作是$A(x)$为底，高为$dx$的柱体体积。体积元素$dv = A(x)dx$，体积$V = \int_a^b A(x)dx$。



例1：设有底面半径为$R$的圆柱体，现过底圆的一直径作平面，此平面与柱体底面构成二面角为$\alpha$，求这个平面截此圆柱体所得立体的体积。



（2）旋转体的体积

旋转体：一平面图形绕平面上的一条直线旋转得到的立体，叫做旋转体。



（3）平面曲线的弧长

设有连续曲线弧$\overset{\frown}{AB}$的方程$y = f(x), a \le x \le b$，其中$f(x)$在$[a, b]$上有连续的一阶导数，求曲线弧$\overset{\frown}{AB}$的长度。

取$x$为积分变量，$x$的变化区间$[a, b]$，先求小区间$[x, x+dx]$对应的弧长元素$ds = \sqrt{(dx)^2+(dy)^2} = \sqrt{1 + (\frac{dy}{dx})^2}dx$，$\overset{\frown}{AB}$的弧长用定积分表示：$S = \int_a^b ds = \int_a^b \sqrt{1 + (\frac{dy}{dx})^2}dx$。



例2：求悬链线$y = a \cosh\frac{x}{a}$在点$A(-b, a\cosh\frac{-b}{a})$与点$B(b, a\cosh\frac{b}{a})$之间的弧长。

解：$y = a\cosh\frac{x}{a} = a \cdot \frac{e^{\frac{x}{a}} + e^{-\frac{x}{a}}}{2}$是偶函数，$y^\prime = a \sinh\frac{x}{a} \cdot \frac{1}{a} = \sinh \frac{x}{a}$。代公式$S = 2\int_0^b \sqrt{1+(\sinh\frac{x}{a})^2}dx = 2\int_0^b \sqrt{\cosh^2 \frac{x}{a}}dx = 2a\sinh\frac{b}{a}$。


