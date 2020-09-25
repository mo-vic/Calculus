[toc]

# 第五章 不定积分

在微分学中要解决：已知$F(x)$，求$F^\prime(x) = f(x)$或求$dF(x) = F^\prime(x) dx$；在不定积分中要解决：已知$F^\prime(x) = f(x)$，求$F(x)$。

## 第1节 不定积分的概念

### 一、原函数与不定积分

==原函数的定义==：若$F(x), f(x)$在区间$I$上==均有==$F^\prime(x) = f(x)$（或$d F(x) = f(x) dx$），则称$F(x)$为$f(x)$在$I$上的原函数。

由微分学可知：$F(x) \in D(a, b)$，则$F^\prime(x) = f(x)$是唯一的（因为导数是极限，而极限是唯一的）。



==定理1==：若$f(x)$在区间$I$上有一个原函数，则$f(x)$必有无穷多个原函数。对于任何常数$C$，形如$F(x) + C$函数族包括了$f(x)$的全体原函数。

证：（1）先证$F(x) + C$是$f(x)$在$I$上的原函数；（2）再证对$f(x)$的任一个原函数$G(x)$，都有$G(x) = F(x) + C$。

（1）已知$F(x)$是$f(x)$在$I$上的原函数，有$F^\prime(x) = f(x), \forall_x \in I$。则$[F(x) + C]^\prime = F^\prime(x) + C^\prime = f(x) + 0 = f(x)$，所以$F(x) + C$是$f(x)$的原函数，由$C$的任意性可知$f(x)$有无穷多个原函数。

（2）假设$G(x)$是$f(x)$在区间$I$上的任意原函数，有$G^\prime(x) = f(x), \forall_x \in I$，$[G(x) - F(x)]^\prime = G^\prime(x) - F^\prime(x) = f(x) - f(x) = 0, \forall_x \in I$，所以$G(x) - F(x) = C, \forall_x \in I$，所以$G(x) = F(x) + C$。



==不定积分==：函数$f(x)$的全体原函数叫做$f(x)$的不定积分，记为$\int f(x) dx$。其中$f(x)$是被积函数，$f(x)dx$是被积表达式，$\int$为积分号，$x$为积分变量，$C$为积分常数。



例1：求$\int x^2 dx$。

解：$\because (x^3)^\prime = 3x^2, (\frac{1}{3}x^3)^\prime = x^2, \therefore \int x^2 dx = \frac{1}{3}x^3 + C$。



例2：求$\int \frac{1}{x} dx$。

解：当$x > 0$时，$(\ln x)^\prime = \frac{1}{x}$，$\ln x$是$\frac{1}{x}$在$(0, +\infty)$上的一个原函数，则有$\int \frac{1}{x} dx = \ln x + C, x \in (0, +\infty)$。当$x < 0$时，在$(-\infty, 0)$上，$[\ln(-x)]^\prime = -\frac{1}{-x} = \frac{1}{x}$，则$\ln(-x)$是$\frac{1}{x}$在$(-\infty, 0)$上的一个原函数，即$\int \frac{1}{x} dx = \ln(-x) + C, x \in (-\infty, 0)$。所以$\int \frac{1}{x} dx = \ln(|x|) + C$。



### 二、不定积分的几何意义

在xoy平面上，$f(x)$的一个原函数$F(x)$，$y = F(x)$的图形（曲线）称为$f(x)$的一条积分曲线。由不定积分：$\int f(x) dx = F(x) + C$，得曲线族：$y = F(x) + C$。由$[F(x) + C]^\prime = f(x)$，可知积分曲线上横坐标为$x$的点处的切线平行，切线斜率为$k = f(x)$。



### 三、不定积分的性质

==性质1==：$f(x) \in [a, b]$，如果$F(x)$是$f(x)$的一个原函数，则$[\int f(x) dx]^\prime = f(x)$（$d[\int f(x) dx] = f(x) dx, \int F^\prime(x) dx = F(x) + C, \int d F(x) = F(x) + C$）。

证：假设有$F^\prime(x) = f(x)$，则$[\int f(x) dx]^\prime = [F(x) + C]^\prime = f(x), \int F^\prime(x) dx = \int f(x) dx = F(x) + C$。



==性质2==：若常数$k \neq 0$，则$\int kf(x)dx = k\int f(x)dx$。

证：先证：$k\int f(x)dx$是$kf(x)$的原函数。因为$[k\int f(x)dx]^\prime = kf(x)$，$k\int f(x) dx$含有任意常数，所以$k\int f(x) dx$是$kf(x)$的全体原函数，所以$\int kf(x)dx = k\int f(x)dx$。



==性质3==：$\int [f_1(x) \pm f_2(x)]dx = \int f_1(x)dx + \int f_2(x)dx$。

证：$\because [\int f_1(x)dx \pm \int f_2(x)dx]^\prime = [\int f_1(x)dx]^\prime \pm [\int f_2(x)dx]^\prime =  f_1(x) \pm f_2(x)$，又$\because \int f_1(x)dx \pm \int f_2(x)dx$含有任意常数，$\therefore \int [f_1(x) + f_2(x)]dx = \int f_1(x)dx + \int f_2(x)dx$。



### 四、基本积分表

根据求导数运算与求不定积分运算是互逆运算，由导数公式可得到相应的积分公式。

1. $\int kdx = kx + c$
2. $\int x^\alpha dx = \frac{1}{\alpha + 1}x^{\alpha + 1} + C$
3. $\int \frac{1}{x} dx = \ln(|x|) + C$
4. $\int a^x dx = \frac{1}{\ln a}a^x + C$

$\ \ \ \ \ \ \ \ \vdots$



例1：求$\int \frac{(1 - x)^2}{x\sqrt{x}}dx$。

解：原式$= \int \frac{1 - 2x + x^2}{x\sqrt{x}}dx = \int x^{-\frac{3}{2}}dx - 2\int x^{-\frac{1}{2}}dx + \int x^{\frac{1}{2}}dx \\ = \frac{1}{-\frac{3}{2} + 1}x^{-\frac{3}{2}+1} - 2 \cdot \frac{1}{-\frac{1}{2} + 1}x^{-\frac{1}{2} + 1} + \frac{1}{\frac{1}{2} + 1}x^{\frac{1}{2} + 1} + C \\ = -\frac{2}{\sqrt{x}} - 4\sqrt{x} + \frac{2}{3}x\sqrt{x} + C$



例2：求$\int (e^{\frac{x}{2}} + 2^x)^2 dx$。

解：原式$= \int (e^x + 2e^{\frac{x}{2}}2^x + 2^{2x}) dx = \int e^x dx + 2\int (2e^{\frac{1}{2}})^x dx + \int 4^x dx = e^x + \frac{4e^{\frac{x}{2}}2^x}{1 + 2\ln 2} + \frac{4^x}{2\ln 2} + C$。



例3：求$\int \frac{1 + x + x^2}{x(1 + x^2)}dx$。

解：原式$= \int \frac{(1 + x^2) + x}{x(1 + x^2)}dx = \int \frac{(1 + x^2)}{x(1 + x^2)}dx + \int \frac{x}{x(1 + x^2)}dx = \int \frac{1}{x}dx + \int \frac{1}{1 + x^2}dx = \ln(|x|) + \arctan x + C$。



例4：求$\int \frac{\cos 2x}{\sin^2x \cos^2x}dx$。

解：原式$= \int\frac{\cos^2x - \sin^2x}{\sin^2x \cos^2x}dx = \int\frac{\cos^2x}{\sin^2x \cos^2x}dx - \int\frac{\sin^2x}{\sin^2x \cos^2x}dx = \int\frac{1}{\sin^2x}dx - \int\frac{1}{\cos^2x}dx = -\cot x - \tan x + C$。



例5：求$\int\frac{1}{\sin^2\frac{x}{2} \cos^2\frac{x}{2}}dx$。

解：原式$= \int\frac{4}{(2\sin\frac{x}{2} \cos\frac{x}{2})^2}dx = 4\int\frac{1}{\sin^2x}dx = -4 \cot x + C$。



例6：已知$F^\prime(x) = (2^x + 2^{-x})^2$，且$F(0) = 0$，求$F(x)$。

解：$F^\prime(x) = (2^x)^2 + 2 \cdot 2^x \cdot 2^{-x} + (2^{-x})^2 = 4^x + 2 + (\frac{1}{4})^x$，$F(x) = \int 4^x dx + \int 2 dx + \int (\frac{1}{4})^x dx = \frac{4^x}{2\ln 2} + 2x + \frac{4^{-x}}{-2 \ln 2} + C$。$F(0) = \frac{1}{2\ln 2} + 0 + \frac{1}{-2\ln 2} + C = 0$，所以$C = 0$，于是$F(x) = \frac{4^x}{2\ln 2} + 2x + \frac{4^{-x}}{-2 \ln 2}$。



## 第2节 换元积分法

基本积分方法：

1. ==换元积分法==
   1. 第一换元法
   2. 第二换元法
2. ==分部积分法==



### 一、第一换元积分法

==基本原理==：$F(u)$是$f(u)$的一个原函数，$u = u(x)$有连续的一阶导数$u^\prime(x)$，则$\int f[u(x)]u^\prime(x) dx = F[u(x)] + C$。（==本质上是复合函数求导的逆运算==）

证明：由题设$F^\prime(u) = f(u) \Longrightarrow \int f(u)du = F(u) + C$，由复合函数微分法，有$dF[u(x)] = F^\prime(u)u^\prime(x)dx = f(u)u^\prime(x)dx = f[u(x)]d[u(x)]$。故$\int f[u(x)]u^\prime(x) dx = \int f[u(x)]d[u(x)] = [\int f(u) du]_{u = u(x)} = [F(u) + C]_{u = u(x)} = F[u(x)] + C$。



怎样利用基本原理来求$\int g(x) dx$？

答：考虑把被积函数$g(x)$化为$g(x) = f[u(x)]u^\prime(x)$形式，那么$\int g(x)dx = \int f[u(x)]u^\prime(x) dx = [\int f(u)du]_{u = u(x)}$。检查$\int f(u)du$是不是基本积分表中的积分，如果有$\int f(u)du = F(u) + C$，则有$\int g(x)dx = [\int f(u)du]_{u = u(x)} = [F(u) + C]_{u = u(x)} = F[u(x)] + C$。



例1：求$\int \cos(3x)dx$。

解：令$u = 3x, u^\prime = 3$，被积式中缺少常数3，现解决如下：$\int \cos(3x)dx = \frac{1}{3}\int \cos(3x) \cdot 3 dx = \frac{1}{3}\int \cos (3x) d(3x) = \frac{1}{3}\sin (3x) + C$。



例2：求$\int \frac{1}{3 + 2x}dx$。

解：令$\frac{1}{3 + 3x} = \frac{1}{u}, u = 3 + 2x, u^\prime(x) = 2$。原式$= \frac{1}{2}\int \frac{2}{3 + 2x}dx = \frac{1}{2} \int \frac{1}{u}du = \frac{1}{2} \ln(|u|) + C = \frac{1}{2}\ln(|3 + 2x|) + C$。



例3：求$\int x\sqrt{1 - x^2}dx$。

解：$\sqrt{1 - x^2} = u^{\frac{1}{2}}, u = 1 - x^2, u^\prime(x) = -2x$。被积式中有因式$x$，缺少常数$-2$。原式$= \int -(\frac{1}{2}) \cdot (-2x) \sqrt{1 - x^2}dx = -\frac{1}{2} \int \sqrt{1 - x^2}d(1 - x^2) \overset{u = 1-x^2}{\Longrightarrow} -\frac{1}{2}\int u^{\frac{1}{2}} du \\ = -\frac{1}{3} u^{\frac{3}{2}} + C = -\frac{1}{3}(1 - x^2)^{\frac{3}{2}} + C$



例4：求$\int \tan x dx$。

解：原式$= \int \frac{\sin x}{\cos x}dx = \int \frac{1}{\cos x} \cdot \sin x dx = -\int \frac{1}{\cos x} (\cos x)^\prime dx \overset{u = \cos x}{\Longrightarrow} \int \frac{1}{u} du = -\ln(|\cos x|) + C$。



例5：求$\int \frac{1}{a^2 + x^2}dx$。

解：原式$= \int \frac{1}{a^2} \cdot \frac{1}{1 + (\frac{x}{a})^2}dx$，令$u = \frac{x}{a}, u^\prime(x) = \frac{1}{a}$。则原式$= \int \frac{1}{a} \cdot \frac{1}{1 + (\frac{x}{a})^2} \cdot \frac{1}{a} dx \overset{u = \frac{x}{a}}{\Longrightarrow} \frac{1}{a}\int\frac{1}{1 + u^2}du = \frac{1}{a}\arctan u + C = \frac{1}{a} \arctan \frac{x}{a} + C$。



例6：求$\int \frac{1}{x^2 - a^2}dx$。

解：$\frac{1}{x^2-a^2} = \frac{1}{(x - a)(x + a)} = (\frac{1}{x-a} - \frac{1}{x+a}) \cdot \frac{1}{2a}$。

$\int \frac{1}{x^2-a^2}dx = \frac{1}{2a}\int [\frac{1}{x-a} - \frac{1}{x+a}]dx = \frac{1}{2a}[\int \frac{1}{x-a}dx - \int \frac{1}{x+a}dx] \\ = \frac{1}{2a}[\ln(|x-a|) - \ln(|x+a|)] + C = \frac{1}{2a} \ln(|\frac{x-a}{x+a}|) + C$



例7：求$\int \frac{1}{x^2 + 4x + 8}dx$。

解：原式$ = \int \frac{1}{(x + 2)^2 + 4}dx = \int \frac{1}{(x+2)^2 + 4}d(x+2) = \frac{1}{2}\arctan(\frac{x+2}{2}) + C$（参照例5结论）。



例8：求$\int \csc x dx$。

解：原式$= \int \frac{1}{\sin x}dx = \int \frac{1}{2\sin\frac{x}{2}\cos\frac{x}{2}}dx = \int\frac{1}{2}\cdot \frac{1}{\frac{\sin\frac{x}{2}}{\cos\frac{x}{2}} \cdot \cos^2\frac{x}{2}}dx \\ = \int\frac{1}{\tan\frac{x}{2}}\sec^2\frac{x}{2}d(\frac{x}{2}) = \int \frac{1}{\tan\frac{x}{2}}d(\tan\frac{x}{2}) = \ln(|\tan\frac{x}{2}|) + C$

$\because \tan\frac{x}{2} = \frac{\sin\frac{x}{2}}{\cos\frac{x}{2}} = \frac{2\sin^2\frac{x}{2}}{2\sin\frac{x}{2}\cos\frac{x}{2}} = \frac{1-\cos x}{\sin x} = \csc x - \cot x$，所以$\int \csc x dx = \ln(|\csc x - \cot x|) + C$。



例9： 求$\int \sec x dx$。

解：$\int \sec x dx = \int \frac{1}{\cos x}dx = \int \frac{1}{\sin(x + \frac{\pi}{2})}dx = \int \frac{1}{\sin(x+\frac{\pi}{2})}d(x+\frac{\pi}{2}) = \ln(|\csc(x+\frac{\pi}{2}) - \cot(x+\frac{\pi}{2})|) + C = \ln(|\sec x + \tan x|) + C$。



例10：求$\int \sin^2(x)dx$。

解：原式$ = \int \frac{1 - \cos2x}{2}dx = \int\frac{1}{2}dx - \int\frac{\cos2x}{2}dx = \frac{1}{2}x - \frac{1}{4}\int\cos(2x) d(2x) = \frac{1}{2}x - \frac{1}{4}\sin(2x) + C$。



例11：求$\int \sin^3 (x)dx$。

解：原式$ = \int \sin x \sin^2(x)dx = -\int \sin^2(x)d(\cos x) \\ = -\int[1 - \cos^2(x)]d(\cos x) = -\int d(\cos x) + \int \cos^2(x)d(\cos x) \\ = -\cos x + \frac{1}{3}\cos^3(x) + C$



例12：求$\int \sin^2(x)\cos^3(x)dx$。

解：原式$= \int \sin^2(x)\cos^2(x) \cos(x)dx = \int \sin^2(x)\cos^2(x) d(\sin x) \\ = \int[\sin^2(x)(1 - \sin^2(x)]d(\sin x) = \int\sin^2(x)d(\sin x) - \int\sin^4(x)d(\sin x) = \frac{1}{3}\sin^3(x) - \frac{1}{5}\sin^5(x) + C$



例13：求$\int \sin^2(x) \cos^4(x) dx$。

解：原式$= \int (\sin x \cos x)^2 \cos^2(x) dx = \int\frac{1}{4}\sin^2(2x)(\frac{1 + \cos(2x)}{2}) dx \\ = \frac{1}{8} \int \sin^2(2x) dx + \frac{1}{8}\int \sin^2(2x)\cos(2x)dx \\ = \frac{1}{8}\int\frac{1 - \cos(4x)}{2}dx + \frac{1}{16}\int \sin^2(2x)\cos(2x)d(2x) \\ = \frac{1}{16}\int dx - \frac{1}{16}\int \cos(4x) dx + \frac{1}{16}\int \sin^2(2x)d[\sin(2x)] \\ = \frac{1}{16}x - \frac{1}{64}\sin(4x) + \frac{1}{48}\sin^3(2x) + C$



例4：求$\int \sec^6 x dx$。

解：原式$= \int \sec^4 x \sec^2 x dx = \int\sec^4 x d(\tan x) = \int (\sec^2 x)^2 d(\tan x) = \int (1 + \tan^2 x)^2 d(\tan x) \\ = \int [1 + 2\tan^2 x + \tan^4 x]d(\tan x) = \tan x + \frac{2}{3}\tan^3 x + \frac{1}{5}\tan^5 x + C$



### 二、第二换元积分法

==第一换元法==：通过变量$u = u(x), \int f[u(x)]u^\prime(x)dx = \int f(u)du = F(u) + C = F[u(x)] + C$，有时候$\int f(x)dx$不易求出，用变量替换，即用$x = \phi(t)$代入原式。而$\int f(x)dx = \int f[\phi(t)]\phi^\prime(t)dt$容易求出（==第二换元==）

==基本原理==：设$x = \phi(t)$是==单调的==，有连续的导数，且$\phi^\prime(t) \neq 0$，$f[\phi(t)]\phi^\prime(t)$有原函数$F(t)$，则有$\int f(x) dx = \int f[\phi(t)]\phi^\prime(t)dt = F(t) + C = F[\phi^{-1}(x)] + C$。其中$t = \phi^{-1}(x)$是$x = \phi(t)$的反函数。

证：只须验证$\frac{d(F[\phi^{-1}(x)])}{dx} = f(x)$。因为$x = \phi(t)$单调且连续，所以$x = \phi(t)$的反函数$t = \phi^{-1}(x)$存在且连续，根据复合函数微分法与反函数微分法，令$t = \phi^{-1}(x)$，有$\frac{d(F[\phi^{-1}(x)])}{dx} = \frac{d F(t)}{dt}\cdot\frac{dt}{dx} = f[\phi(t)]\phi^\prime(t)\cdot \frac{1}{\frac{dx}{dt}} = f[\phi(t)]\phi^\prime(t) \frac{1}{\phi^\prime(t)} = f[\phi(t)] = f(x)$。所以$F[\phi^{-1}(x)]$是$f(x)$的一个原函数，于是$\int f(x)dx = F[\phi^{-1}(x)] + C$。



例1：求$\int \frac{1}{1 + \sqrt{1+x}}dx$。

解：令$\sqrt{1 + x} = t, \Longrightarrow x = t^2 - 1, dx = 2t dt$，原式$= \int \frac{1}{1+t}\cdot 2t dt = 2\int\frac{t}{1+t}dt = 2\int\frac{t+1-1}{t+1}dt = 2[\int dt - \int\frac{1}{t+1}dt] \\ = 2[t - \ln(|t+1|)] + C = 2[\sqrt{1+x} - \ln(|1+\sqrt{1+x}|)] + C$



例2：求$\int \sqrt{a^2 - x^2}dx\ (a > 0)$。

解：$\sqrt{a^2 - x^2} = \sqrt{a^2(1 - \frac{x^2}{a^2})} = a\sqrt{1-(\frac{x}{a})^2}$。根据三角公式：$1 - \sin^2 t = \cos^2 t$，令$\frac{x}{a} = \sin t$，即$x = a\sin t, (-\frac{\pi}{2} < t < \frac{\pi}{2})$。于是有$\sqrt{a^2-x^2} = a\sqrt{1-(\frac{x}{a})^2} = a\sqrt{1-\sin^2 t} = a\sqrt{\cos^2 t} = a|\cos t| = a\cos t, (-\frac{\pi}{2} < t < \frac{\pi}{2})$，$dx = d(a\sin t) = a\cos t dt$。所以$\int \sqrt{a^2-x^2}dx = \int a \cos t \cdot a \cos t dt = a^2 \int \cos^2 t dt = a^2\int\frac{1+\cos 2t}{2}dt \\ = \frac{a^2}{2}[t + \frac{1}{2}\int\cos(2t)d(2t)] = \frac{a^2}{2}[t + \frac{1}{2}\sin(2t)] + C$

其中，换变量$t$为变量$x$，有两种方法：

1. 利用三角公式：

   $\because x = a\sin t \Longrightarrow \sin t = \frac{x}{a}, t = \arcsin\frac{x}{a}, \frac{1}{2}\sin(2t) = \frac{1}{2} \cdot 2 \sin t\cos t = \sin t \cos t, \\ \because \cos t = \sqrt{1 - \sin^2 t} = \sqrt{1-\frac{x^2}{a^2}} = \frac{1}{a}\sqrt{a^2-x^2} \\ \therefore \frac{1}{2}\sin(2t) = \frac{x}{a}\cdot\frac{1}{a}\sqrt{a^2-x^2}$

   于是$\int\sqrt{a^2-x^2}dx = \frac{a^2}{2}[\arcsin\frac{x}{\alpha} + \frac{x\sqrt{a^2-x^2}}{a^2}] + C$。

2. 利用直角三角形法：

   $\because x = a\sin t, \sin t = \frac{x}{a} \Longrightarrow t = \arcsin\frac{x}{a}$，由直角三角形，得$\cos t = \frac{\sqrt{a^2-x^2}}{a}$，$\int \sqrt{a^2-x^2}dx = \frac{a^2}{2}[t + \sin t \cos t] + C = \frac{a^2}{2}[\arctan\frac{x}{a} + \frac{x\sqrt{a^2-x^2}}{a^2}] + C$。



例3：求$\int \frac{1}{\sqrt{x^2+a^2}}dx, (a > 0)$。

解：$\sqrt{x^2+a^2} = \sqrt{a^2(1 + \frac{x^2}{a^2})} = a\sqrt{1 + (\frac{x}{a})^2}$，由三角公式，$1 + \tan^2 t = \sec^2 t$，若令$\frac{x}{a} = \tan t \Longrightarrow x = a\tan t, -\frac{\pi}{2} < t < \frac{\pi}{2}$，$\sqrt{x^2 + a^2} = a\sqrt{1 + (\frac{x}{a})^2} = a\sqrt{1+\tan^2 t} = a\sqrt{\sec^2 t} = a|\sec t| = a|\frac{1}{\cos t}| = a\sec t, (\because -\frac{\pi}{2} < t < \frac{\pi}{2})$，

$dx = d(a\tan t) = a\sec^2 t dt$，原式$= \int \frac{1}{a\sec t} a \sec^2 t dt = \int \sec t dt  = \ln(|\sec t + \tan t|) + C$，由$\tan t = \frac{x}{a}$，则原式$= \ln(|\frac{\sqrt{a^2+x^2}}{a} + \frac{x}{a}|) + C = \ln(|\sqrt{a^2+x^2} + x|) + C_1, (C_1 = C + \ln a)$。



例4：求$\int \frac{1}{\sqrt{x^2-a^2}}dx$。

解：注意被积函数$\frac{1}{\sqrt{x^2-a^2}}$的定义域为$|x| > a$。即$x > a > 0$或$x < -a < 0$。

当$x > a > 0$时，$\sqrt{x^2-a^2}=\sqrt{a^2(\frac{x^2}{a^2}-1)} = a\sqrt{(\frac{x}{a})^2 - 1}$。由三角公式：$1 + \tan^2 t = \sec^2 t \Longrightarrow \tan^2 t = \sec^2 t - 1$。令$\frac{x}{a} = \sec t$，即$x = a\sec t, (0 < t < \frac{\pi}{2})$，$\sqrt{x^2-a^2} = a\sqrt{\sec^2 t - 1} = a\sqrt{\tan^2 t} = a\tan t$，$dx = d(a\sec t) = a\sec t \tan t dt$，$\int\frac{1}{\sqrt{x^2-a^2}}dx = \int \frac{1}{a\tan t} a \sec t \tan t dt = \int \sec t dt = \ln(\sec t + \tan t) + C \\ = \ln(\frac{x}{a} + \frac{\sqrt{x^2-a^2}}{a}) + C = \ln(x + \sqrt{x^2-a^2}) + C - \ln a = \ln(x + \sqrt{x^2-a^2}) + C_1$ 

，其中$C_1 = C + \ln a$。

当$x < -a < 0$时，令$u = -x > 0$，$dx = -du$，$\int \frac{1}{\sqrt{x^2-a^2}}dx = \int \frac{-1}{\sqrt{u^2-a^2}}du = -\int \frac{1}{\sqrt{u^2-a^2}}du, \\ \because u = -x > a > 0, \therefore -\int\frac{1}{\sqrt{u^2-a^2}}dx = -\ln(u+\sqrt{u^2-a^2}) + C \\ = -\ln(-x+\sqrt{x^2-a^2}) + C = \ln(\frac{1}{-x+\sqrt{x^2-a^2}}) + C = \ln(\frac{-x-\sqrt{x^2-a^2}}{a^2}) + C = \ln(-x - \sqrt{x^2-a^2})-2\ln a + C \\ = \ln(-x-\sqrt{x^2-a^2}) + C_1$，其中$C_1 = C - 2\ln a$。

以上两个结果综合在一起，得到：$\int\frac{1}{\sqrt(x^2-a^2)}dx = \ln|x+\sqrt{x^2-a^2}| + C$。



==小结==：为了去掉被积函数中的根式，作换元。

1. $\sqrt{1+x}$，令$\sqrt{1+x} = t, x = t^2-1$；
2. $\sqrt{a^2-x^2}$，令$x = a\sin t$；
3. $\sqrt{x^2+a^2}$，令$x = a\tan t$；
4. $\sqrt{x^2-a^2}$，令$x = a\sec t$。



例5：求$\int \frac{1}{\sqrt{x^2+2x+3}}dx$。

解：$\int \frac{1}{\sqrt{x^2+2x+3}}dx = \int \frac{1}{\sqrt{(x+1)^2+(\sqrt{2})^2}}d(x+1)$，令$x+1 = \sqrt{2}\tan t, dx = \sqrt{2}\sec^2 t dt$。原式$= \int \frac{1}{\sqrt{2\tan^2 t + 2}}\sqrt{2}\sec^2 t dt = \int \frac{1}{\sqrt{2}\sqrt{\tan^2 t + 1}}\sqrt{2} \sec^2 tdt = \int \frac{1}{\sec t} \sec^2 t dt \\ = \int \sec t dt = \ln(|\sec t+\tan  t|) + C$

因为$\tan t = \frac{x+1}{\sqrt{2}}$，作直角三角形，原式$= \ln(|\frac{\sqrt{x^2+2x+3}}{\sqrt{2}}+\frac{x+1}{\sqrt{2}}|) + C = \ln(|x+1 + \sqrt{x^2+2x+3}|) + C_1$，其中$C_1 = C - \frac{1}{2}\ln 2$。



例6：求$\int \frac{1}{\sqrt{1+x-x^2}}dx$。

解：$\int \frac{1}{\sqrt{1+x-x^2}}dx = \int \frac{1}{\sqrt{\frac{5}{4}-(\frac{1}{4}-x+x^2)}}dx = \int \frac{1}{\sqrt{\frac{5}{4} - (x-\frac{1}{2})^2}}dx \\ = \int \frac{1}{\frac{\sqrt{5}}{2}\sqrt{1-(\frac{x-\frac{1}{2}}{\frac{\sqrt{5}}{2}})^2}}dx = \int \frac{1}{\sqrt{1-(\frac{x-\frac{1}{2}}{\frac{\sqrt{5}}{2}})^2}}d(\frac{x-\frac{1}{2}}{\frac{\sqrt{5}}{2}})$

令$u = \frac{x-\frac{1}{2}}{\frac{\sqrt{5}}{2}}$，原式$= \int\frac{1}{\sqrt{1-u^2}}du = \arcsin u + C = \arcsin \frac{x-\frac{1}{2}}{\frac{\sqrt{5}}{2}} + C = \arcsin \frac{2x-1}{\sqrt{5}} + C$。

==小结==：三项的话先进行配方，再看具体形式使用上述根式中对应的换元规则。



## 第3节 分部积分法

==基本原理==：设$u = u(x), v = v(x)$具有连续的一阶导数，则$\int u(x)v^\prime(x)dx = u(v)v(x) - \int v(x)u^\prime(x)dx$。即$\int u dv$（难）$=$ $uv - \int v du$（易）。

证明：根据两个函数乘积的导数公式，$[u(x)v(x)]^\prime = u^\prime(x)v(x)+u(x)v^\prime(x) \Longrightarrow u(x)v^\prime(x) = [u(x)v(x)]^\prime - u^\prime(x)v(x)$，作积分$\int u(x)v^\prime(x)dx = \int [u(x)v(x)]^\prime dx - \int u^\prime(x)v(x)dx = u(x)v(x) - \int v(x)u^\prime(x)dx$，即$\int u dv = uv - \int v du$。



例1：求$\int xe^x dx$。

解：令$u = x, dv = e^x dx, du = dx, v = e^x, \int xe^x dx = \int x d(e^x) = xe^x - \int e^x dx = xe^x - e^x + C = e^x(x-1) + C$

==注意==：选择$u$和$dv$：

1. 由$dv$求$v$比较容易；
2. 求$\int v du$比求$\int u dv$容易。



例2：求$\int x \cos x dx$。

解：令$u = x, dv = \cos x dx, du = dx, v = \sin x$，$\int x \cos x dx = \int x d(\sin x) = x \sin x - \int \sin x dx = x \sin x + \cos x + C$。



例3：求$\int \arctan x dx$。

解：$\int \arctan x dx = \arctan x \cdot x - \int x d(\arctan x) = x \arctan x - \int \frac{x}{1 + x^2}dx \\  = x \arctan x - \frac{1}{2}\int \frac{1}{1+x^2}2x dx = x\arctan x - \frac{1}{2}\int \frac{1}{1+x^2}d(1+x^2) = x\arctan x - \frac{1}{2}\ln(1+x^2) + C$



例4：求$\int(x+1)^2\sin x dx$。

解：$\int(x+1)^2\sin x dx = \int (x+1)^2 d(-\cos x) = -(x+1)^2 \cos x + \int \cos x d[(x+1)^2] \\ = -(x+1)^2 \cos x + \int 2(x+1)\cos x dx = -(x+1)^2 \cos x + 2\int (x+1) d(\sin x) \\ = -(x+1)^2 \cos x + 2[(x+1)\sin x - \int \sin x dx] \\ =  -(x+1)^2 \cos x + 2(x+1)\sin x + 2\cos x + C$



有些不定积分，经过两次分部积分后又回到原来的积分，且不能消去，通过==解方程法==，求出不定积分。

例5：$\int \sec^3 x dx$。

解：$\int \sec^3 x dx = \int \sec x \sec^2 x dx = \int \sec x d(\tan x) \\ = \sec x \tan x - \int \tan x d(\sec x) = \sec x \tan x - \int \tan x \sec x \tan x dx \\ = \sec x\tan x - \int\sec x(\sec^2 x - 1) dx = \sec x \tan x - \int \sec^3 x dx + \int \sec x dx$

即$2\int \sec^3 x dx = \sec x \tan x + \int \sec x dx = \sec x \tan x + \ln(|\sec x + \tan x|) + C$，即$\int \sec^3 x dx = \frac{1}{2}[\sec x \tan x + \ln(|\sec x + \tan x|)] + C$。



例6：$\int e^{ax}\sin bx dx$。

解：$\int e^{ax}\sin bx dx = \int e^{ax} d(-\frac{\cos bx}{b}) = -\frac{1}{b}e^{ax}\cos bx + \int \frac{\cos bx}{b}d(e^{ax}) \\ = -\frac{1}{b}e^{ax}\cos bx + \frac{a}{b}\int e^{ax}\cos bx dx = -\frac{1}{b}e^{ax}\cos bx + \frac{a}{b}\int e^{ax}d(\frac{\sin bx}{b}) \\ = -\frac{1}{b}e^{ax}\cos bx + \frac{a}{b}[\frac{e^{ax}\sin bx}{b} - \int \frac{\sin bx}{b} d(e^{ax})] \\ = -\frac{1}{b}e^{ax}\cos bx + \frac{a}{b^2}e^{ax}\sin bx - \frac{a^2}{b^2}\int e^{ax}\sin bx dx$

移项后，得：$(1 + \frac{a^2}{b^2})\int e^{ax}\sin bx dx = -\frac{1}{b}e^{ax}\cos bx + \frac{a}{b^2}e^{ax}\sin bx + C$，所以$\int e^{ax}\sin bx dx = \frac{b^2}{a^2+b^2}[-\frac{1}{b}e^{ax}\cos bx + \frac{a}{b^2}e^{ax}\sin bx + C] \\ = [-\frac{b}{a^2+b^2}\cos bx + \frac{a}{a^2+b^2}\sin bx]e^{ax} + \frac{b^2 C}{a^2+b^2} \\ = \frac{e^{ax}}{a^2+b^2}[a\sin bx - b\cos bx] + C_1$

其中$C_1 = \frac{b^2 C}{a^2+b^2}$。



==小结==：设$n$为正整数：

1. $\int x^n e^{ax} dx, \int x^n \sin bx dx, \int x^n \cos bx dx$，可以令$u = x^n, dv = e^{ax}dx$或$dv = \sin bx dx$或$dv = \cos bx dx$；

2. $\int x^n \ln x dx, \int x^n \arcsin x dx, \int x^n \arctan dx$，可以令$u = \ln x, dv = x^n dx$或$u = \arcsin x, dv = x^n dx$或$u = \arctan x, dv = x^n dx$；



## 第4节 几类函数的积分法

### 一、有理函数的积分

==有理函数==：由两个多项式的商所表示的函数，记为$R(x)$。

$R(x) = \frac{a_0x^m + a_1x^{m-1} +\cdots+ a_{m-1}x + a_m}{b_0x^n + b_1x^{n-1} + \cdots + b_{n-1}x + b_n} = \frac{P_m(x)}{Q_n(x)}$，其中$m, n$是非负的整数，$a_i (i=0,1,\cdots,m), b_j (j=0,1,\cdots,n)$为常数，$a_0 \neq 0, b_0 \neq 0$，且$P_m(x)$与$Q_n(x)$没有公因式。

当$m \ge n$，称$R(x) = \frac{P_m(x)}{Q_n(x)}$为有理假分式；当$m < n$，称$R(x) = \frac{P_m(x)}{Q_n(x)}$为有理真分式。通过多项式除法（长除法），可以把有理假分式化为多项式+有理真分式的形式。



讨论有理真分式的分解问题：

$R(x) = \frac{P_m(x)}{Q_n(x)}$是有理真分式，1. 分母$Q_n(x) = b_0x^n + b_1x^{n-1} + \cdots + b_{n-1}x + b_n$在实数范围内总可以分解为一次因式与二次因式的乘积，即$Q_n(x) = (x - a)^\alpha \cdots (x-b)^\beta (x^2+px+q)^\lambda \cdots (x^2 + \gamma x + s)^\mu$，其中$p^2-4q < 0; \cdots ; \gamma^2 - 4s < 0, \alpha + \cdots + \beta + 2\lambda + \cdots + 2\mu = n$，$\alpha, \cdots, \beta, \cdots, \lambda, \cdots, \mu$是正整数；2. 若$Q_n(x)$有上述的分解式，真分式$R(x) = \frac{P_m(x)}{Q_n(x)}$可以分解为以下的”部分分式“之和：

$R(x) = \frac{P_m(x)}{Q_n(x)} = \frac{A_1}{(x-a)^\alpha} + \frac{A_2}{(x-a)^{\alpha-1}} + \cdots + \frac{A_\alpha}{x-a} + \frac{B_1}{(x-b)^\beta} + \frac{B_2}{(x-b)^{\beta-1}} + \cdots + \frac{B_\beta}{x-b} \\ + \frac{M_1 x + N_1}{(x^2+px+q)^\lambda} + \frac{M_2 x + N_2}{(x^2+px+q)^{\lambda-1}} + \cdots + \frac{M_\lambda x + N_\lambda}{x^2+px+q} + \cdots \\ + \frac{R_1 x + S_1}{(x^2+\gamma x+s)^\mu} + \frac{R_2 x + S_2}{(x^2+\gamma x+s)^{\mu-1}} + \cdots + \frac{M_\mu x + N_\mu}{x^2+\gamma x+s}$

上式右端的分式叫做有理函数的==部分分式==。



具体分解时，要注意：

1. 在分母$Q_n(x)$的分解式中，如果有因式$(x - a)^k$（$k \ge 1$的正整数），在$R(x)$的分解式中有$k$个部分分式：$\frac{A_1}{(x-a)^k} + \frac{A_2}{(x-a)^{k-1}} + \cdots + \frac{A_k}{(x-a)}$；
2. 在分母$Q_n(x)$的分解式中，如果有因式$(x^2 + px + q)^k$（$p^2-4q<0$， $k \ge 1$正整数），在$R(x)$的分解式中有$k$个部分分式：$\frac{M_1x-N_1}{(x^2+px+q)^k} + \frac{M_2x-N_2}{(x^2+px+q)^{k-1}} + \cdots + \frac{M_kx-N_k}{x^2+px+q}$



例1：把$\frac{x+2}{x^3-2x^2+x}$分解为部分分式之和。

解：$x^3-2x^2+x=x(x-1)^2$，$\frac{x+2}{x^3-2x^2+x}=\frac{x+2}{x(x-1)^2} = \frac{A}{x} + \frac{B}{(x-1)^2} + \frac{C}{(x-1)} = \frac{A(x-1)^2+Bx+Cx(x-1)}{x(x-1)^2}$，去分母后得：$x+2 = A(x-1)^2+Bx+Cx(x-1) = (A+C)x^2+(-2A+B-C)x + A$，恒等式两边$x$的同次幂的系数要相等：
$$
\left\{\begin{array}{ccccc}&A+C &= &0 \\ &-2A+B-C &= &1 \\ &A &= &2 \end{array}\right.
$$
 解得$A=2, B=3, C=-2$，所以$\frac{x+2}{x^3-2x^2+x} = \frac{2}{x} + \frac{3}{(x-1)^2} - \frac{2}{(x-1)}$。

也可以根据恒等式：$x+2 = A(x-1)^2+Bx+Cx(x-1)$，令$x = 0 \Longrightarrow A = 2$，令$x=1 \Longrightarrow B = 3$，将$A = 2, B = 3$代入恒等式，得：$x+2 = 2(x-1)^2+3x+Cx(x-1)$，令$x=2 \Longrightarrow C=-2$。



例2：把$\frac{2x}{x^3-x^2+x-1}$分解为部分分式之和。

解：$x^3-x^2+x-1 = x^2(x-1) + (x-1) = (x-1)(x^2+1)$，$\frac{2x}{x^3-x^2+x-1} = \frac{2x}{(x-1)(x^2+1)} = \frac{A}{x-1} + \frac{Bx+C}{x^2+1}$，上式两边去分母，得$2x = A(x^2+1) + (x-1)(Bx+C) = (A+B)x^2+(C-B)x+(A-C)$，比较恒等式$x$的同次幂的系数：
$$
\left\{\begin{array}{ccccc}&A+B &= &0 \\ &C-B &= &2 \\ &A-C &= &0 \end{array}\right.
$$
解得$A = 1, B = -1, C = 1$。所以$\frac{2x}{x^3-x^2+x-1} = \frac{1}{x-1} + \frac{-x+1}{x^2+1}$。



==有理函数$R(x)$的积分==：$R(x) = \frac{P_m(x)}{Q_n(x)}$ = （多项式）+ （有理真分式）= （多项式） + （部分分式之和）

作$\int R(x)dx$= 多项式积分与部分分式的积分之和。



==求部分分式的积分==：$\int \frac{A}{x-a}dx, \int \frac{A}{(x-a)^n} dx, \int \frac{Bx + C}{x^2+px+q}dx, \int \frac{Bx + C}{(x^2+px+q)^n}dx$。



1. $\int \frac{A}{x-a}dx = A\int \frac{1}{x-a}dx = A\ln(|x-a|) + C$。
2. $\int \frac{A}{(x-a)^n}dx = A\int (x-a)^{-n}d(x-a) = \frac{A}{-n+1}(x-a)^{-n+1} + C = \frac{A}{1-n}\frac{1}{(x-a)^{n-1}} + C$。
3. $\int \frac{Bx+C}{x^2+px+q}dx = \frac{1}{2}\int \frac{2Bx + 2C}{x^2+px+q}dx = \frac{1}{2}\int \frac{(2Bx + Bp) + (2C - Bp)}{x^2+px+q}dx = \frac{B}{2}\int \frac{2x+p}{x^2+px+q}dx + \frac{2C-Bp}{2}\int \frac{1}{x^2+px+q}dx \\ = \frac{B}{2}\int\frac{1}{x^2+px+q}d(x^2+px+q) + \frac{2C-Bp}{2}\int \frac{dx}{(x+\frac{p}{2})^2+q-\frac{p^2}{4}} = \frac{B}{2}\ln(x^2+px+q) + \frac{2C-Bp}{2}\int\frac{dx}{(x+\frac{p}{2})^2+(\frac{\sqrt{4q-p^2}}{2})^2} \\ = \frac{B}{2}\ln(x^2+px+q) + \frac{2C-Bp}{2}\frac{1}{\frac{\sqrt{4q-p^2}}{2}}\arctan \frac{x+\frac{p}{2}}{\frac{\sqrt{4q-p^2}}{2}} + C_1 \\ = \frac{B}{2}\ln(x^2+px+q) + \frac{2C-Bp}{\sqrt{4q-p^2}}\arctan \frac{2x+p}{\sqrt{4q-p^2}} + C_1, (p^2+4q < 0)$
4. $\int \frac{Bx + C}{(x^2+px+q)^n}dx, (p^2-4q<0)$：

$\int \frac{Bx + C}{(x^2+px+q)^n}dx = \frac{1}{2}\int\frac{2Bx + Bp + 2C - Bp}{(x^2+px+q)^n}dx = \frac{B}{2}\int \frac{2x + p}{(x^2+px+q)^n}dx + \frac{2C-Bp}{2}\int \frac{1}{(x^2+px+q)^n}dx \\ = \frac{B}{2}\int (x^2+px+q)^{-n}d(x^2+px+q) + \frac{2C-Bp}{2}\int\frac{1}{[(x+\frac{p}{2})^2+(\frac{\sqrt{4q-p^2}}{2})^2]^n}dx \\ = \frac{B}{2(1-n)(x^2+px+q)^{n-1}}+C_1 + \frac{2C-Bp}{2}\int\frac{1}{[(x+\frac{p}{2})^2+(\frac{\sqrt{4q-p^2}}{2})^2]^n}dx$

令$u = (x+\frac{p}{2}), dx = du, a = \frac{\sqrt{4q-p^2}}{2}$，$I_n = \int \frac{1}{(x^2+px+q)^n}dx = \int \frac{1}{(u^2 + a^2)^n}du = \frac{1}{a^2}\int \frac{(u^2 + a^2) - u^2}{(u^2 + a^2)^n}du = \frac{1}{a^2}\int \frac{1}{(u^2+a^2)^{n-1}}du + \frac{1}{a^2}\int \frac{u^2}{(u^2+a^2)^n}du \\ = \frac{1}{a^2}I_{n-1} - \frac{1}{a^2}\int u\frac{1}{(u^2+a^2)^n}u du = \frac{1}{a^2}I_{n-1} - \frac{1}{2a^2}\int u\frac{1}{(u^2+a^2)^n}d(u^2 + a^2) \\ = \frac{1}{a^2}I_{n-1} - \frac{1}{2a^2}\int \frac{1}{1-n}u d[(u^2 + a^2)^{1-n}] = \frac{1}{a^2}I_{n-1} - \frac{1}{2a^2(1-n)}\int u d[(u^2 + a^2)^{1-n}] \\ = \frac{1}{a^2}I_{n-1} - \frac{1}{2a^2(1-n)}[u(u^2 + a^2)^{1-n} - \int (u^2 + a^2)^{1-n} du] \\ = \frac{1}{a^2}I_{n-1} - \frac{1}{2a^2(1-n)}[\frac{u}{(u^2 + a^2)^{n-1}} - \int \frac{1}{(u^2 + a^2)^{n-1}} du] \\ = \frac{1}{a^2}I_{n-1} - \frac{1}{2a^2(1-n)}\frac{u}{(u^2 + a^2)^{n-1}} + \frac{1}{2a^2(1-n)}I_{n-1} = \frac{3-2n}{2a^2(1-n)}I_{n-1} - \frac{u}{2a^2(1-n)(u^2+a^2)^{n-1}}$

当$n = 1$时，$I_1 = \int \frac{1}{u^2 + a^2}du = \frac{1}{a}\arctan \frac{u}{a} + C$。



例3：求$\int \frac{2x}{x^3-x^2+x-1}dx$。

解：$\frac{2x}{x^3-x^2+x-1} = \frac{1}{x-1} + \frac{-x+1}{x^2+1}$，$\int \frac{2x}{x^3-x^2+x-1}dx = \frac{1}{x-1}dx - \int\frac{x-1}{x^2+1}dx = \ln(|x-1|) - \frac{1}{2}\ln(x^2+1)+\arctan x + C$。



### 二、三角函数的有理式

==三角函数的有理式==：由三角函数（$\sin x, \cos x, \tan x, \cot x, \sec x, \csc x$）及常数经过有限次四则运算所构成的数学表达式。

==注意到==：$\tan x = \frac{\sin x}{\cos x}, \cot x = \frac{\cos x}{\sin x}, \sec = \frac{1}{\cos x}, \csc x = \frac{1}{\sin x}$，因此，三角函数有理式可以用正弦函数、余弦函数及常数经过有限次四则运算来表达。

1. 三角函数有理式可表达为$R(\sin x,\cos x)$，其不定积分为$\int R(\sin x, \cos x)dx$。其中的$\sin x, \cos x$都可以用$\tan \frac{x}{2}$的有理式来表达，即$\sin x = 2\sin\frac{x}{2}\cos\frac{x}{2} = 2\frac{\sin\frac{x}{2}}{\cos\frac{x}{2}}\cos^2\frac{x}{2} = 2\tan\frac{x}{2}\frac{1}{\frac{1}{\cos^2 \frac{x}{2}}} = \frac{2\tan\frac{x}{2}}{1+\tan^2\frac{x}{2}}$，$\cos x = \cos^2\frac{x}{2} - \sin^2\frac{x}{2} = \cos^2\frac{x}{2}(1-\frac{\sin^2{\frac{x}{2}}}{\cos^2\frac{x}{2}}) = \frac{1}{\sec^2 \frac{x}{2}}(1 - \tan^2{\frac{x}{2}}) = \frac{1 - \tan^2{\frac{x}{2}}}{1+\tan^2\frac{x}{2}}$，

   如果作变换：$u = \tan{\frac{x}{2}}, x = 2\arctan u, dx = \frac{2}{1+u^2}du, \sin x = \frac{2u}{1+u^2}, \cos x = \frac{1-u^2}{1+u^2}$，$\int R(\sin x,\cos x)dx = \int R(\frac{2u}{1+u^2}, \frac{1-u^2}{1+u^2})\frac{2}{1+u^2}du$为有理函数的积分。



例1：求$\int \frac{1+\sin x}{\sin x(1 + \cos x)}dx$。

解：令$u = \tan\frac{x}{2}$，原式$= \int \frac{1+\frac{2u}{1+u^2}}{\frac{2u}{1+u^2}(1+\frac{1-u^2}{1+u^2})}\frac{2}{1+u^2}du = \int \frac{u^2+2u+1}{2u}du = \int \frac{u}{2}du + \int du + \int \frac{1}{2u}du \\ = \frac{1}{4}u^2 + u + \frac{1}{2}\ln(|u|) + C = \frac{1}{4}\tan^2\frac{x}{2} + \tan\frac{x}{2} + \frac{1}{2}\ln(|\tan \frac{x}{2}|) + C$



2. $\int R(\tan x)dx$，包括$\int R(\tan x)dx, \int R(\sin^2 x, \cos^2 x)dx, \int R(\sin 2x \cos 2x)dx$。用代换$u = \tan x, x = \arctan u, dx = \frac{1}{1+u^2}du$，$\sin^2 x = \frac{\sin^2 x}{\cos^2 x}\cdot\cos^2 x = \tan^2 x \cdot \frac{1}{1+\tan^2 x} = \frac{u^2}{1+u^2}$，$\cos^2 x = 1 - \sin^2x = 1 - \frac{u^2}{1+u^2} = \frac{1}{1+u^2}$，$\sin 2x = \frac{2u}{1+u^2}, \cos2x = \frac{1-u^2}{1+u^2}$。



例2：$\int \frac{\tan^2 x}{5 + 4\cos 2x}dx$。

解：令$u = \tan x$，原式$= \int \frac{u^2}{5 + 4\cdot\frac{1-u^2}{1+u^2}} \frac{1}{1+u^2}du = \int \frac{u^2}{9+u^2}du = \int (1-\frac{9}{9+u^2})du = u - 9\int\frac{1}{3^2+u^2}du \\ = u - 9\cdot \frac{1}{3}\arctan \frac{u}{3} + C= \tan x - 3\arctan(\frac{\tan x}{3}) + C$



### 三、两种无理函数的积分

1. $\int R(x, \sqrt[n]{\frac{ax+b}{cx+h}})dx, n \ge 2, a, b, c, h$为常数，$ac \neq 0$。当$c=0,h=1$时，$\int R(x, \sqrt[n]{ax + b})dx$。令$t = \sqrt[n]{\frac{ax+b}{cx+h}} \Longrightarrow t^n = \frac{ax+b}{cx+h} \Longrightarrow t^n(cx+h) = ax+b \Longrightarrow ht^n - b = (a - t^n c)x$，$\therefore x = \frac{ht^n - b}{a-ct^n} = \phi(t)$（为有理函数），$dx = \phi^\prime(t)dt$，$\phi^\prime(t)$仍为有理函数。

   $\int R(x, \sqrt[n]{\frac{ax+b}{cx+h}})dx = \int R[\phi(t), t]\phi^\prime(t)dt$（有理函数积分）



例1：求$\int\frac{1}{x}\sqrt{\frac{x+1}{x}}dx$。

解：令$t=\sqrt{\frac{x+1}{x}}, t^2 = \frac{x+1}{x}, t^2 x = x+ 1, x = \frac{1}{t^2-1}, dx = \frac{-2t}{(t^2-1)^2}dt$。所以$\int\frac{1}{x}\sqrt{\frac{x+1}{x}}dx = \int(t^2 - 1)t \frac{(-2t)}{(t^2-1)^2}dt = -2\int\frac{t^2}{t^2-1}dt = -2\int\frac{t^2-1+1}{t^2-1}dt = -2\int(1+\frac{1}{t^2-1})dt \\ = -2t + \ln(|\frac{t-1}{t+1}|) + C = -2\sqrt{\frac{x+1}{x}} + \ln(|x(\sqrt{\frac{x+1}{x}} - 1)^2|) + C$



2. $\int R(x, \sqrt{ax^2+bx+c})dx, (a \neq 0)$。

==思路==：先对$ax^2+bx+c$进行配方，然后对根式选择适当的三角变换去掉根式（第二换元法），化为三角函数有理式的积分。



例2： $\int \frac{1}{1+\sqrt{x^2+2x+2}}dx$。

解：原式$= \int \frac{1}{1+\sqrt{(x+1)^2+1}}dx$，令$x + 1 = \tan t, dx = \sec^2 t dt$。原式$= \int \frac{1}{1+\sqrt{\tan^2 t + 1}}\sec^2 t dt = \int \frac{\sec^2 t}{1+\sec t}dt = \int \frac{\frac{1}{\cos^2 t}}{1+\frac{1}{\cos t}}dt \\ = \int \frac{1}{\cos t(1+\cos t)}dt = \int (\frac{1}{\cos t}-\frac{1}{1+\cos t})dt = \int \sec t dt - \int \frac{1}{2\cos^2\frac{t}{2}}dt \\ = \ln(|\sec t + \tan t|) - \int \sec^2\frac{t}{2}d(\frac{t}{2}) = \ln(|\sec t + \tan t|) - \tan\frac{t}{2} + C$

由$x+1=\tan t$，画直角三角形，可得$\sec t = \sqrt{x^2+2x+2}, \tan t = x+1, \tan \frac{t}{2} = \sqrt{\frac{1-\cos t}{1+\cos t}} = \frac{\sqrt{x^2+2x+2}-1}{x+1}$，所以原式$= \ln(|x+1+\sqrt{x^2+2x+2}|) - \frac{\sqrt{x^2+2x+2}-1}{x+1} + C$。





