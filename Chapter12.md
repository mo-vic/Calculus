[toc]

# 微分方程

要找变量$x, y$之间的函数关系：$y = f(x)$，实际问题往往不能够直接找出$y=f(x)$，但是可以找到$x, y, y^\prime, \cdots, y^{(n)}$之间的关系。表示这个关系的方程——==微分方程==，解这个方程得到$y=f(x)$。



## 第1节 微分方程的基本概念

例1：已知曲线上任一点$M(x, y)$处切线的斜率等于该点横坐标的2倍，且曲线过点$(2, 2)$，求曲线的方程。

解：根据函数导数的几何意义可知：
$$
\left\{\begin{array}{cccc} \frac{dy}{dx} &= &2x &(a) \\ y|_{x=2} &= & 2 &(b)\end{array}\right.
$$
由$(a)$得：$dy = 2x dx$，两边积分$y = x^2+C$，把$(b)$代入，得$2 = 2^2 + C \Longrightarrow C = -2$。

最终得到曲线方程$y = x^2-2$。



例2：设初速度为$v_0$，质量为$m$的物体自由下落，不计空气阻力，求物体的运动规律。

解：设$s = s(t), \frac{ds}{dt}=s^\prime(t), \frac{d^2s}{dt^2}=s^{\prime\prime}(t)$，所以有：
$$
\left\{\begin{array}{cccc} \frac{d^2s}{dt^2} &= &g &(a) \\ s|_{t=0} &= & 0 &(b) \\ \frac{ds}{dt}|_{t=0} &= &v_0 &(c) \end{array}\right.
$$
由$(a)$式两边积分得$\frac{ds}{dt} = gt + C_1$，再作积分，得$s = \frac{1}{2}gt^2+C_1t+C_2$。分别把$(b), (c)$二式代入，得$C_1 = v_0, C_2 = 0$。所以$s = \frac{1}{2}gt^2 + v_0t$。



==微分方程==：含有自变量，一元未知函数及其导数（或微分）的方程称为（常）微分方程。

==微分方程的阶==：在微分方程中所出现的未知函数的==最高==阶导数的阶数称为微分方程的阶。



==隐式微分方程==：$F(x, y, y^\prime, \cdots, y^{(n)})$

==显式微分方程==：$y^{(n)} = f(x, y, y^\prime, \cdots, y^{(n-1)})$

微分方程的解：设$y = \phi(x)$定义在区间$I$上，且有直至$n$阶导数，使得$F[x, \phi(x), \phi^\prime(x), \cdots, \phi^{(n)}(x)] \equiv 0$。则称$y = \phi(x)$为微分方程$F(x, y, y^\prime, \cdots, y^{(n)}) = 0$的解（在区间$I$上）。

通解：如果微分方程的解中含有独立的任意常数，且任意常数的个数与微分方程的阶数相等，称这个解称为通解。隐函数形式的通解称为==通积分==。

==微分方程的定解条件==：当自变量取特定值时，未知函数及其导数取对应确定值，称为微分方程的定解条件。

==初始条件==：自变量都取同一特定值时的定解条件称为初始条件（如例2中的$t=0$），条件个数应与阶数相等。

==特解==：通过定解条件，确定了通解中的任意常数后的解，称为特解。如例1、例2。

==微分方程的初值问题==：求微分方程满足初始条件的特解，称为微分方程的初值问题。



例3：验证$y = xe^x$是$y^{\prime\prime}-2y^\prime+y=0$的解。

解：$y = xe^x, y^\prime = e^x + xe^x = (1+x)e^x, y^{\prime\prime} = e^x + e^x + xe^x = (2 + x)e^x$，方程左端：$(2+x)e^x-2(1+x)e^x+xe^x = e^x(2+x-2-2x+x) = e^x \cdot 0 \equiv 0$。所以$y = xe^x$是$y^{\prime\prime}-2y^\prime+y=0$的解。



例4：求函数$y = c_1e^{c_2x}$，（$c_1, c_2$为任意常数），求其所满足的微分方程。

解：已知$y = c_1e^{c_2 x}, y^\prime = c_1c_2e^{c_2 x} = c_2 y, y^{\prime\prime} = c_2y^\prime(x)$，则有$\frac{y^\prime}{y^{\prime\prime}} = \frac{c_2y}{c_2y^\prime}$，即$y^{\prime \prime}y - (y^\prime)^2 = 0$。此为所求的微分方程（通过求导消去任意常数$c_1, c_2$）。



## 第2节 一阶微分方程

==隐式==：$F(x, y, y^\prime) = 0$

==显式==：$y^\prime = f(x, y)$或$P(x, y)dx + Q(x, y)dy = 0$

### 一、可分离变量的微分方程

例如：$\frac{dy}{dx} = 2x$或$dy = 2x dx$，$\int dy = \int 2x dx + C, y = x^2 + C$。

又例如：$\frac{dy}{dx} = 2x y^2$或$dy = 2xy^2 dx$。若$y \neq 0$，则$\frac{1}{y^2}dy = 2x dx$，两边作积分$\int \frac{1}{y^2}dy = \int 2x dx + C$。即$-\frac{1}{y} = x^2 + C \Longrightarrow y = -\frac{1}{x^2+c}$。



==情形==：形如$X(x)dx = Y(y)dy$为变量已分离的方程，假设$X(x), Y(y)$为已知的==连续函数==，假若$y = y(x)$是方程的解，则$X(x)dx = Y(y)d y(x)$，即$X(x)dx = Y[y(x)]y^\prime(x)dx$，令$y = y(x), X(x)dx = Y[y(x)]d[y(x)], X(x)dx = Y(y)dy, \int X(x)dx = \int Y(y)dy + C$。即$y(x)$是由$\int X(x)dx = \int Y(y)dy + C$确定的隐函数。

反之，由$\int X(x)dx = \int Y(y)dy + C$确定隐函数$y = y(x)$。令$F(x, y) = \int X(x)dx - \int Y(y)dy - C$，由隐函数微分法：$\frac{dy}{dx} = -\frac{F_x^\prime(x, y)}{F_y^\prime(x, y)} = \frac{X(x)}{Y(y)}$，即$X(x)dx = Y(y)dy \quad (1)$，证明了$y = y(x)$是方程$(1)$的解。



例1：求$\frac{dy}{dx} = 3x^2 y$的通解。

解：把方程变形为$\frac{1}{y}dy = 3x^2dx (y \neq 0)$，两边积分$\int \frac{1}{y} dy = \int 3x^2 dx$。即$\ln(|y|) = x^3 + C_1, |y| = e^{x^3 + C_1} = e^{C_1}e^{x^3}, y = \pm e^{C_1}e^{x^3}$，令$C = \pm e^{C_1}$，则有$y = Ce^{x^3}$是方程的通解。



例2：求$y^\prime = \frac{y\ln y}{x}$的通解。

解：化为$\frac{dy}{y\ln y} = \frac{1}{x}dx, y \neq 1$。$\int \frac{dy}{y\ln y} = \int \frac{1}{x}dx, \int \frac{1}{\ln y}d(\ln y) = \ln(|x|) + C_1$，$\ln(|\ln y|) = \ln |x| + C_1, |\ln y| = e^{\ln |x|} \cdot e^{C_1} = |x|e^{C_1}, \ln y = \pm e^{C_1}|x|$，令$C = \pm e^{C_1}$，则$\ln y = C|x|$，即$y = e^{C|x|}$，设$C$为任意常数，则$y = e^{Cx}$是微分方程的通解。



例3：求$\frac{dy}{dx} = f(ax+by+c), (b \neq 0)$的通解。

解：令$u = ax+by+c, \frac{du}{dx} = a + b\frac{dy}{dx} \Longrightarrow \frac{dy}{dx} = \frac{1}{b}(\frac{du}{dx}-a)$，代入原方程得$\frac{1}{b}(\frac{du}{dx}-a) = f(u) \Longrightarrow \frac{du}{dx} = bf(u)+a$，则$\frac{1}{bf(u)+a}du = dx$，解出未知函数$u$后，再换回$u = ax+by+c$。



例4：求$\frac{dy}{dx} = \frac{1}{x-y}+1$的通解。

解：$\frac{dy}{dx} = \frac{1+(x-y)}{x-y}$，$f(x-y) = \frac{1+(x-y)}{x-y}$，令$x-y = u, 1 - \frac{dy}{dx} = \frac{du}{dx}, \Longrightarrow \frac{dy}{dx} = 1 - \frac{du}{dx}$。将$\frac{dy}{dx}, u = x-y$代入原方程得$1-\frac{du}{dx}=\frac{1}{u}+1 \Longrightarrow \frac{du}{dx} = -\frac{1}{u}$，则$u du = -dx$，等式两边积分得$\frac{1}{2}u^2 = -x + C$，所以$u^2 = -2x + 2C \Longrightarrow (x-y)^2 = -2x + C_1$（通积分），其中$C_1 = 2C$是任意常数。



### 二、一阶齐次方程

如果一阶微分方程$\frac{dy}{dx} = \phi(x, y)$，而$\phi(x, y)$可以写成$\phi(x, y) = f(\frac{y}{x})$（如果$\phi(x, y)$满足：$\phi(tx, ty) = \phi(x, y)$），则称该一阶微分方程为一阶齐次微分方程。

例如：$(x^2+4y^2)dx-3xydy=0 \Longrightarrow \frac{dy}{dx} = \frac{x^2+4y^2}{3xy}$，即$\phi(x, y) = \frac{x^2+4y^2}{3xy}$，$\phi(tx, ty) = \frac{(tx)^2+4(ty)^2}{3(tx)(ty)} = \frac{x^2+4y^2}{3xy} = \phi(x, y)$，亦即$\frac{dy}{dx} = \frac{1+4(\frac{y}{x})^2}{3(\frac{y}{x})} = f(\frac{y}{x})$。

解$\frac{dy}{dx} = f(\frac{y}{x})$，令$\frac{y}{x} = u \Longrightarrow y = ux$，两边求导得$\frac{dy}{dx} = u + x\cdot\frac{du}{dx}$，代入原微分方程得$u + x\cdot\frac{du}{dx} = f(u) \Longrightarrow x\cdot\frac{du}{dx}=f(u)-u \Longrightarrow \frac{1}{f(u)-u}du = \frac{1}{x}dx$。两边积分得$\int \frac{1}{f(u)-u}du = \ln |x| + C$（通积分），最后再把$u = \frac{y}{x}$换回原来的变量，就得到原微分方程的通解。



例1：$xydx-(x^2-y^2)dy=0$的通解。

解：$\frac{dy}{dx} = \frac{xy}{x^2-y^2}$，令$y = ux$，$\frac{dy}{dx} = u + x\frac{du}{dx}$，代入原微分方程得$u + x\frac{du}{dx} = \frac{u}{1-u^2}$，移项得$x\frac{du}{dx} = \frac{u}{1+u^2} - u = \frac{u^3}{1-u^2}$，分离变量得$\frac{1-u^2}{u^3}du = \frac{1}{x}dx$，两端积分得$-\frac{1}{2u^2} - \ln |u| = \ln x - \ln C$，即$\ln |\frac{ux}{C}| = -\frac{1}{2u^2}$，脱去对数符号，$|\frac{ux}{C}| = e^{-\frac{1}{2u^2}}$，即$|ux| = |y| = |C|e^{-\frac{1}{2u^2}}, y = \pm|C|e^{-\frac{1}{2u^2}} = Ce^{-\frac{1}{2u^2}}$。（其中$C$为任意常数）。



例2：求$(1+e^{-\frac{x}{y}})ydx+(y-x)dy=0$的通解。

解：把原方程化为$\frac{dy}{dx} = \frac{(1+e^{-\frac{x}{y}})y}{x-y}$，分子分母同时除以$y$得$\frac{dy}{dx} = \frac{1+e^{-\frac{x}{y}}}{\frac{x}{y}-1} = f(\frac{x}{y})$。令$\frac{x}{y} = u \Longrightarrow x = uy \Longrightarrow dx = udy+ydu$，代入原方程得$(1+e^{-u})y (udy+ydu)+(y-uy)dy = 0$，整理得$\frac{1+e^{-u}}{1+ue^{-u}}du+\frac{1}{y}dy=0$。

由上式的第一项的分子分母同乘$e^u$，$\frac{e^u+1}{e^u+u}du+\frac{1}{y}dy=0$，注意到$(e^u+u)^\prime = e^u+1$，等式两边同时积分$\ln |e^u+u| + \ln |y| = \ln C$，化简得$|y (e^u + u)| = C \Longleftrightarrow ye^{\frac{x}{y}} + \frac{x}{y} = C$。



形如$\frac{dy}{dx} = f(\frac{a_1x+b_1y+c_1}{a_2x+b_2y+c_2})$方程：当$c_1=c_2=0$时，它是齐次方程，若$c_1,c_2$不全为零时，它不是齐次方程，但可以转化为齐次方程，具体的做法为：

（1）解方程组：
$$
\left\{\begin{array}{ccc}a_1x+b_1y+c_1 &= &0 \\ a_2x+b_2x+c_2 &= &0\end{array}\right.
$$
解得$x = x_0, y = y_0$

（2）作变量替换：
$$
\left\{\begin{array}{ccc}x &= &X+x_0 \\ y &= &Y+y_0\end{array}\right. \Longrightarrow \frac{dy}{dx} = \frac{dY}{dX}
$$
（3）代入原方程得齐次方程：

$\frac{dY}{dX} = f(\frac{a_1(X+x_0)+b_1(Y+y_0)+c_1}{a_2(X+x_0)+b_2(Y+y_0)+c_2}) = f(\frac{a_1X+b_1Y+a_1x_0+b_1y_0+c_1}{a_2X+b_2Y+a_2x_0+b_2y_0+c_2}) = f(\frac{a_1X+b_1Y}{a_2X+b_2Y})$

（4）把$X, Y$换成$x, y$。



例3：求$\frac{dy}{dx} = \frac{y+2}{x+y+1}$的通解。

解：解方程组
$$
\left\{\begin{array}{ccc}y+2 &= &0 \\ x+y+1 &= &0\end{array}\right.
$$
解得$x_0=3,y_0=-2$，作变量替换$x = X+3, y = Y-2$，$\frac{dy}{dx} = \frac{dY}{dX}$，代入原方程：$\frac{dY}{dX} = \frac{Y}{X+Y}$，令$Y = uX$，$\frac{dY}{dX} = \frac{du}{dX}X + u$，$X\frac{du}{dX} + u = \frac{uX}{X + uX} = \frac{1}{1+u}$，$X\frac{du}{dX} = -\frac{u^2}{1+u}$，最终解得$\frac{X}{Y}-\ln\frac{Y}{X}=\ln(CX)$，$\frac{x-3}{y+2}=\ln[C(y+2)]$。



### 三、一阶线性方程

形如$\frac{dy}{dx} + P(x)y = Q(x)$的微分方程称为一阶的线性方程。其中$Q(x)$称为自由项。

若$P(x),Q(x)$连续，则方程的解存在。

（1）若$Q(x) \equiv 0$，则方程$\frac{dy}{dx} + P(x)y = 0$称为一阶线性齐次方程，为可分离变量的微分方程。

（2）若$Q(X) \not \equiv 0$，则方程$\frac{dy}{dx} + P(x)y = Q(x)$称为一阶线性非齐次方程。

​	常数变易法：已知在（1）中，方程$\frac{dy}{dx} + P(x)y = 0$的通解为$y=Ce^{-\int P(x)dx}$，设$y = u(x)e^{-\int P(x)dx}$是非齐次方程$\frac{dy}{dx} + P(x)y = Q(x)$的解，两边求导数得$\frac{dy}{dx} = u^\prime(x)e^{-\int P(x)dx}+u(x)e^{-\int P(x)dx}[-P(x)] = u^\prime(x)e^{-\int P(x)dx}-u(x)P(x)e^{-\int P(x)dx}$

代入非齐次方程得：$u^\prime(x)e^{-\int P(x)dx}-u(x)P(x)e^{-\int P(x)dx} + P(x)u(x)e^{-\int P(x)dx} = Q(x)$

即$u^\prime(x) = Q(x)e^{\int P(x)dx}$，$u(x) = \int Q(x)e^{\int P(x)dx} dx + C$，整理得一阶线性非齐次微分方程的通解：$y = u(x)e^{-\int P(x)dx} = e^{-\int P(x)dx}[\int Q(x)e^{\int P(x)dx} dx + C]$。



例1：求$\frac{dy}{dx} - \frac{2y}{x+1} = (x+1)^{\frac{5}{2}}$的通解。

解：$P(x) = -\frac{2}{x+1}, Q(x) = (x+1)^{\frac{5}{2}}$，套公式$y = e^{-\int P(x)dx}[\int Q(x)e^{\int P(x)dx} + C] = e^{\int \frac{2}{x+1}dx}[\int (x+1)^{\frac{5}{2}} \cdot e^{\int -\frac{2}{x+1}dx}dx + C] \\ = e^{\ln(x+1)^2}[\int (x+1)^{\frac{5}{2}} \cdot e^{-\ln(x+1)^2}dx + C] \\ = (x+1)^2[\int (x+1)^{\frac{5}{2}} \cdot \frac{1}{(x+1)^2}dx + C] \\ = (x+1)^2[\int(x+1)^{\frac{1}{2}}dx + C] = (x+1)^2[\frac{2}{3}(x+1)^{\frac{3}{2}}+C]$



例2：求$(\sin x)y^\prime - y \cos x = 2x\sin^3x$的通解。

解：原方程变形为$y^\prime - y\frac{\cos x}{sin x} = 2x\sin^2x$，$P(x) = -\frac{\cos x}{\sin x}, Q(x) = 2x\sin^2x$，套公式$y = e^{-\int P(x)dx}[\int Q(x)e^{\int P(x)dx} + C] = e^{\int \frac{\cos x}{\sin x}dx}[\int 2x\sin^2x \cdot e^{\int -\frac{\cos x}{\sin x}dx}dx + C] \\ = e^{\ln \sin x}[\int 2x\sin^2x \cdot e^{-\ln \sin x}dx + C] = \sin x[\int 2x\sin^2x \cdot \frac{1}{\sin x}dx + C] \\ = \sin x [\int 2x \sin x dx + C] = \sin x [-2x \cos x + 2\sin x +C]$



### 四、伯努利方程

方程$\frac{dy}{dx} + P(x)y = Q(x)y^n, (n \neq 0, 1)$称为伯努利方程。

解法：通过变量替换，化为一阶线性方程求解。

把方程变形为：$y^{-n}\frac{dy}{dx} + P(x)y^{1-n} = Q(x)$，$\because \frac{d(y^{1-n})}{dx} = (1-n) \cdot y^{-n} \frac{dy}{dx} \Longleftrightarrow y^{-n}\frac{dy}{dx} = \frac{1}{1-n}\frac{d(y^{1-n})}{dx}$，令$z = y^{1-n}, y^{-n}\frac{dy}{dx} = \frac{1}{1-n} \cdot \frac{dz}{dx}$，代入上面的方程，得$\frac{1}{1-n} \cdot \frac{dz}{dx} + P(x)z = Q(x) \Longrightarrow \frac{dz}{dx} + (1-n)P(x)z = (1-n)Q(x)$为一阶线性微分方程。求出通解后，把$z$换回$y^{1-n}$，得到原方程的通解。



例1：求$y^\prime + \frac{y}{x} = (\ln x)y^2$的通解。

解：原方程式伯努利方程。把原方程化为$y^{-2} \cdot \frac{dy}{dx} + \frac{1}{x}y^{-1} = \ln x$，令$z = y^{-1}$，$\frac{dz}{dx} = -y^{-2} \cdot \frac{dy}{dx} \Longrightarrow y^{-2} \cdot \frac{dy}{dx} = -\frac{dz}{dx}$，代入上面方程$-\frac{dz}{dx} + \frac{1}{x}z = \ln x \Longrightarrow \frac{dz}{dx} - \frac{1}{x} = -\ln x$，解得$z = x[-\frac{1}{2}(\ln x)^2 + C]$，$\therefore y^{-1} = x[C - \frac{1}{2}(\ln x)^2] \Longrightarrow xy[C-\frac{1}{2}(\ln x)^2]=1$



### 五、全微分方程

如果微分方程$P(x, y)dx + Q(x, y)dy = 0$，若方程的左端恰好式某二元函数$u(x, y)$的全微分，即$du(x, y) = P(x, y)dx+Q(x, y)dy$，则称$P(x, y)dx + Q(x, y)dy = 0$为全微分方程。

问题：怎样判定$P(x, y)dx + Q(x, y)dy = 0$是全微分方程？

在曲线积分那一章中讲到：$P(x, y)dx + Q(x, y)dy$是某函数的全微分$\Longleftrightarrow$$\frac{\partial P(x, y)}{\partial y} = \frac{\partial Q(x, y)}{\partial x}$

求解全微分方程：如果存在二元函数$u(x, y)$的全微分为$du(x, y) = P(x, y)dx+Q(x, y)dy$，则$u(x, y) = C$。

假定$P(x, y)dx + Q(x, y)dy = 0$是全微分方程，那么有$\frac{\partial P}{\partial y} = \frac{\partial Q}{\partial x}$，曲线积分$\int_L P(x, y)dx + Q(x, y)dy$与路径无关，其中$L$是由$(x_0, y_0)$到$(x, y)$的曲线弧。

$u(x, y) = \int_{(x_0, y_0)}^{(x, y)} P(x, y)dx + Q(x, y)dy = \int_{x_0}^x P(x_, y_0)dx + \int_{y_0}^y Q(x, y)dy$，令$u(x, y) = C$，得通解。



例1：求$(x^2+y)dx-(y-x)dy=0$的通解。

解：$P(x, y) = x^2+y, Q(x, y) = x - y$，$\frac{\partial P}{\partial y} = 1, \frac{\partial Q}{\partial x} = 1$，所以原方程是全微分方程，$u(x, y) = \int_{(0, 0)}^{(x, y)}(x^2+y)dx-(y-x)dy = \int_0^x x^2dx + \int_0^y (x-y)dy = \frac{1}{3}x^3 + xy - \frac{1}{2}y^2$，令$u(x, y) = C$，原方程的通解为$\frac{1}{3}x^3 + xy - \frac{1}{2}y^2 = C$。



另一种方法：用不定积分法求解。

设有全微分方程$P(x, y)dx + Q(x, y)dy = 0$，一定存在二元函数$u(x, y)$使$du(x, y) = P(x, y)dx+Q(x, y)dy$，$du(x, y) = \frac{\partial u}{\partial x}dx + \frac{\partial u}{\partial y}dy$，由全微分的唯一性，从而$\frac{\partial u}{\partial x} = P(x, y), \frac{\partial u}{\partial y} = Q(x, y)$，$u(x, y) = \int P(x, y)dx + \phi(y)$，$\frac{\partial u}{\partial y} = \frac{\partial}{\partial y}[\int P(x, y)dx] + \phi^\prime(y)$，所以$\phi^\prime(y) = \frac{\partial u}{\partial y} - \frac{\partial}{\partial y}[\int P(x, y)dx] = Q(x, y) - \frac{\partial}{\partial y}[\int P(x, y)dx]$。

验证等号右端函数与$x$无关，$\frac{\partial Q}{\partial x} - \frac{\partial}{\partial x}\{\frac{\partial}{\partial y}[\int P(x, y)dx]\} = \frac{\partial Q}{\partial x} - \frac{\partial}{\partial y}\{\frac{\partial}{\partial x}[\int P(x, y)dx]\} = \frac{\partial Q}{\partial x} - \frac{\partial P}{\partial y} = 0$

$\therefore \phi(y) = \int \phi^\prime(y)dy = \int \{Q(x, y) - \frac{\partial}{\partial y}[\int P(x, y)dx]\}dy$，代入$u(x, y) = \int P(x, y)dx + \phi(y)$，从而$u(x, y) = C$为全微分方程的通解。



例2：求$\frac{2x}{y^3}dx+\frac{y^2-3x^2}{y^4}dy=0$的通解。

解：$P = \frac{2x}{y^3}, Q = \frac{y^2-3x^2}{y^4} = \frac{1}{y^2} - \frac{3x^2}{y^4}$，$\frac{\partial Q}{\partial x} = -\frac{6x}{y^4} = \frac{\partial P}{\partial y}$，原方程是全微分方程。

由$\frac{\partial u}{\partial x} = P(x, y) = \frac{2x}{y^3}, \frac{\partial u}{\partial y} = Q(x, y) = \frac{1}{y^2} - \frac{3x^2}{y^4}$，$u(x, y) = \int \frac{2x}{y^3}dx = \frac{x^2}{y^3} + \phi(y)$，$\frac{\partial u}{\partial y} = Q(x, y) = \frac{1}{y^2} - \frac{3x^2}{y^4} = -\frac{3x^2}{y^4} + \phi^\prime(y)$，从而$\phi^\prime(y) = \frac{1}{y^2}$，$\phi(y) = \int \frac{1}{y^2}dy = -\frac{1}{y}$（取一个函数就行），$u(x, y) = \frac{x^2}{y^3} - \frac{1}{y}$，所以全微分方程的通解为$\frac{x^2}{y^3} - \frac{1}{y} = C$。



### 六、一阶微分方程的应用举例

1. 瞬态法：根据已知的科学规律，在任意瞬时（或任一点处）去寻求未知函数及其导数与自变量之间的关系，并整理成微分方程。（如：冷却问题或者反射问题）
2. 微量法：在任一时间间隔内（或在任一局部范围内），去寻求未知函数及其微分与自变量微分之间的关系，整理成微分方程。



## 第3节 可降阶的高阶方程

### 一、$y^{(n)} = f(x)$型的方程

方程右端$f(x)$是已知的连续函数，令$y^{(n-1)} = u \Longrightarrow y^{(n)} = [y^{(n-1)}]^\prime = u^\prime$，方程可化为$u^\prime = f(x)$，则$u = \int f(x)dx + C$。反复进行积分降阶，连续作$n$次积分，就得到含有$n$个任意常数的通解。



例1：求$y^{\prime\prime\prime} = e^{2x} - \cos x$的通解。

解：$y^{\prime\prime} = \int (e^{2x} - \cos x)dx + C_1 = \frac{1}{2}e^{2x} - \sin x + C_1$，$y^\prime = \int (\frac{1}{2}e^{2x} - \sin x)dx + C_1x + C_2 = \frac{1}{4} e^{2x} + \cos x + C_1x + C_2$，$y = \frac{1}{8}e^{2x}+\sin x+\frac{C_1}{2}x^2+C_2x+C_3=\frac{1}{8}e^{2x}+\sin x+\frac{C_1}{2}x^2+C_2x+C_3$。



### 二、$y^{\prime\prime} = f(x, y^\prime)$型的方程

方程的特点：方程右端不显含未知函数$y$。

作变量替换：$y^\prime = P, y^{\prime\prime} = \frac{dP}{dx}$，代入原方程得$\frac{dP}{dx} = f(x, P)$，该方程是以$P$为未知函数，$x$为自变量的一阶微分方程。设方程的通解$P = \phi(x, C_1)$，又得到一阶方程$y^\prime = \phi(x, C_1)$，$y = \int \phi(x, C_1)dx + C_2$。



例1：求$(1+x^2)y^{\prime\prime} = 2xy^\prime$满足初始条件$y|_{x=0}=1, y^\prime|_{x=0}=3$的特解。

解：原方程化为$y^{\prime\prime} = \frac{2x}{1+x^2}y^\prime$，方程右端不显含$y$，作变量替换，$y^\prime = P, y^{\prime\prime} = \frac{dP}{dx}$，代入上面的方程$\frac{dP}{dx} = \frac{2x}{1+x^2}P$，分离变量：$\frac{dP}{P} = \frac{2x}{1+x^2}dx$，两边积分$\ln P = \ln(1+x^2)+\ln C_1$，$P = C_1(1+x^2)$，即$y^\prime = C_1(1+x^2)$，由$y^\prime|_{x=0} = 3 \Longrightarrow C_1 = 3$，$y^\prime = 3(1+x^2)$，$y = \int 3(1+x^2)dx + C_2 = 3(x+\frac{1}{3}x^3) + C_2$，由$y|_{x=0} = 1 \Longrightarrow C_2 = 1$，所以$y = x^3 + 3x + 1$。



### 三、$y^{\prime\prime} = f(y, y^\prime)$型方程

方程的特点：方程的右端不显含自变量$x$。

作变量替换：$y^\prime = P, y^{\prime\prime} = \frac{dP}{dx} = \frac{dP}{dy} \cdot \frac{dy}{dx} = P \frac{dP}{dy}$，代入原方程，得$P\frac{dP}{dy} = f(y, P)$是一阶微分方程。设其通解为$P = \psi(y, C_1), y^\prime = \psi(y, C_1), \frac{dy}{\psi(y, C_1)} = dx, \int \frac{1}{\psi(y, C_1)}dy = x + C_2$。



例1：求$1+(y^\prime)^2 = 2yy^{\prime\prime}$的通解。

解：原方程可化为$y^{\prime\prime} = \frac{1+(y^\prime)^2}{2y}$，作变量替换，$y^\prime = P, y^{\prime\prime}=P\frac{dP}{dy}$，代入原方程，得$P\frac{dP}{dy} = \frac{1+P^2}{2y}$，分离变量$\frac{2P}{1+P^2}dP = \frac{1}{y}dy$，两端积分得$\ln(1+P^2)=\ln y + \ln C_1$，$1+P^2 = C_1y \Longrightarrow P = \pm\sqrt{C_1y - 1}$。还原成原变量，$y^\prime = \pm\sqrt{C_y - 1}$，分离变量$\frac{1}{\pm\sqrt{C_1y-1}}dy = dx$，两端积分后，$\pm \frac{2}{C_1}(C_1y-1)^{\frac{1}{2}}=x+C_2$，两边平方得$C_1y = \frac{C_1^2}{4}(x+C_2)^2+1$。



## 第4节 线性微分方程解的结构

$n$阶线性微分方程的一般形式：$y^{(n)} + P_1(x)y^{(n-1)} + P_2(x)y^{(n-2)} + \cdots + P_{n-1}(x)y^\prime + P_n(x)y = f(x)$，其中$P_i(x), (i=1,2,\cdots,n)$，$f(x)$为已知的连续函数，也称为自由项。如果$f(x) \equiv 0$，则方程称为$n$阶线性齐次方程。如果$f(x) \not \equiv 0$，则方程称为$n$阶线性非齐次方程。



### 一、线性齐次方程解的结构——以二阶线性齐次方程为例

$y^{\prime\prime} + p(x)y^\prime + q(x)y = 0$，$p(x), q(x)$是已知的连续函数。显然可知$y = 0$是方程的解——==平凡解==。其它的解——==非平凡解==。

==定理==：设函数$y_1, y_2$是齐次方程的两个解，则$y=C_1 y_1 + C_2 y_2$也是方程的解（其中$C_1, C_2$是任意常数）。

证：由假设，有
$$
y_1^{\prime\prime} = p(x)y_1^\prime + q(x)y_1 = 0 \\ y_2^{\prime\prime} = p(x)y_2^\prime + q(x)y_2 = 0
$$
将$y=C_1 y_1 + C_2 y_2$代入方程的左端中，得$(C_1 y_1 + C_2 y_2)^{\prime\prime}+p(x)(C_1 y_1 + C_2 y_2)^\prime+q(x)(C_1 y_1 + C_2 y_2) \\ = C_1[y_1^{\prime\prime}+p(x)y_1^\prime+q(x)y_1^\prime] + C_2[y_2^{\prime\prime}+p(x)y_2^\prime+q(x)y_2^\prime] = 0$

所以$y=C_1 y_1 + C_2 y_2$也是方程的解



当$y_1, y_2$满足什么条件时？$y = C_1y_1 + C_2y_2$才是方程的通解？

==函数线性无关==：设有$y_1, y_2, \cdots, y_n$是在$(a, b)$内的$n$个函数，如果存在不全为零的$n$个常数$k_1, k_2, \cdots, k_n$，使得$k_1y_1 + k_2y_2 + \cdots + k_ny_n = 0$，则称$y_1, y_2, \cdots, y_n$在$(a, b)$内是线性相关的，否则称$y_1, y_2, \cdots, y_n$在$(a, b)$内是线性无关的。



判定两个函数$y_1, y_2$在$x \in I$内线性无关或相关的方法：

1. $\frac{y_2}{y_1} = k$（$k$为常数），则$y_1, y_2$线性相关；
2. $\frac{y_2}{y_1} \neq k$（$k$为常数），则$y_1, y_2$线性无关。



==定理==：如果$y_1, y_2$是齐次方程的两个线性无关的解，则$y = C_1y_1 + C_2y_2$是齐次方程的通解，其中$C_1, C_2$为任意常数。



### 二、线性非齐次方程解的结构——以二阶线性非齐次方程为例

$y^{\prime\prime} + p(x)y^\prime + q(x)y = f(x)$，$p(x), q(x)$是已知的连续函数。



==定理==：设$y^\star$是方程的一特解，而$\bar{y} = C_1y_1+C_2y_2$是方程所对应的齐次方程的通解，则$y = \bar{y} + y^\star$是非齐次方程的通解。

解：由定理的假设，有$(y^\star)^{\prime\prime} + p(x)(y^\star)^\prime + q(x)y^\star = f(x)$，$(\bar{y})^{\prime\prime}+p(x)(\bar{y})^\prime+q(x)\bar{y}=0$，把$y = \bar{y} + y^\star$代入非齐次方程的左端$(\bar{y} + y^\star)^{\prime\prime}+p(x)(\bar{y} + y^\star)^\prime+q(x)(\bar{y} + y^\star) \\ = [\bar{y}^{\prime\prime}+p(x)\bar{y}^\prime+q(x)\bar{y}]+[(y^\star)^{\prime\prime} + p(x)(y^\star)^\prime + q(x)y^\star] = f(x)$

所以$y = \bar{y} + y^\star$是非齐次方程的解。而$y = C_1y_1+C_2y_2 + y^\star$中含有两个任意常数，所以$y = \bar{y} + y^\star$是非齐次方程的通解。



==定理==：设有二阶线性非齐次方程$y^{\prime\prime} + p(x)y^\prime + q(x)y = f_1(x) + f_2(x)$，其中$p(x), q(x), f_1(x), f_2(x)$是连续函数，而$y_1^\star$是$y^{\prime\prime} + p(x)y^\prime + q(x)y = f_1(x)$的一个特解，$y_2^\star$是$y^{\prime\prime} + p(x)y^\prime + q(x)y = f_2(x)$的一个特解。则$y^\star = y_1^\star+y_2^\star$是方程$y^{\prime\prime} + p(x)y^\prime + q(x)y = f_1(x) + f_2(x)$的特解。



## 第5节 常系数线性微分方程

$y^{(n)}+p_1y^{(n-1)}+p_2y^{(n-1)}+\cdots+p_{n-1}y^\prime+p_ny=f(x)$，其中（$p_i, i=1,2\cdots,n$）是常数。



### 一、常系数线性微分方程——以二阶常系数线性齐次微分方程为例

$y^{\prime\prime} + py^\prime + qy = 0$，$p, q$是常数。

由方程结构可知，解$y$及$y^\prime, y^{\prime\prime}$必须是同一类函数，才有可能使$y^{\prime\prime} + py^\prime + qy \equiv 0$。

可知指数函数$y = e^{rx}, y^\prime = re^{rx}, y^{\prime\prime} = r^2e^{rx}$是同一类函数。 

假设$y = e^{rx}$是方程的解，代入方程得：$r^2e^{rx}+pre^{rx}+qe^{rx}=0 \Longrightarrow (r^2+pr+q)e^{rx} \equiv 0$，$\because e^{rx} > 0, \therefore r^2+pr+q=0$，说明$y = e^{rx}$中的$r$是二次方程$r^2+pr+q=0$的根。以上推导过程步步可逆，从而可知，由二次方程$r^2+pr+q=0$的根$r$，写出$y = e^{rx}$就是微分方程的解。

方程$r^2+pr+q=0$称为微分方程的特征方程。特征方程的根$r_1, r_2$称为微分方程的特征根。

（1）不相等的实根，$p^2-4q>0$，特征根$r_1 = \frac{-p-\sqrt{p^2-4q}}{2}, r_2 = \frac{-p+\sqrt{p^2-4q}}{2}$，微分方程的两个解$y_1 = e^{r_1x}, y_2 = e^{r_2x}$，因为$\frac{y_2}{y_1} = e^{(r_2-r_1)x}$，其中$r_2 - r_1 \neq 0$（因为实根不相等），可见$y_1, y_2$线性无关，则$y = C_1y_1+C_2y_2 = C_1e^{r_1x}+C_2e^{r_2x}$是微分方程的通解。

（2）相等实根，$p^2-4q=0$，$r_1 = r_2 = -\frac{p}{2}$，得到齐次方程的一个解：$y_1 = e^{r_1x}$，为了求得另一个与$y_1$线性无关的解$y_2$，可令$\frac{y_2}{y_1} = u(x), y_2 = u(x)y_1$，求导数$y_2^\prime = u^\prime(x)y_1+u(x)y_1^\prime = u^\prime(x)e^{r_1x}+r_1u(x)e^{r_1x}$，$y_2^{\prime\prime}=u^{\prime\prime}(x)y_1+2u^\prime(x)y_1^\prime+u(x)y_1^{\prime\prime} = u^{\prime\prime}(x)e^{r_1x}+2r_1u^\prime(x)e^{r_1x}+r^2u(x)e^{r_1x}$，把$y_2, y_2^\prime, y_2^{\prime\prime}$代入齐次方程，得$e^{r_1x}[u^{\prime\prime}(x)+(2r_1+p)u^\prime(x)+(r_1^2+pr_1+q)u(x)] \equiv 0$，$\because e^{r_1x} > 0$，$\therefore u^{\prime\prime}(x)+(2r_1+p)u^\prime(x)+(r_1^2+pr_1+q)u(x) \equiv 0$，$\because r_1 = -\frac{p}{2} \Longrightarrow 2r_1+p=0$，$r_1$是特征根，$r_1^2+pr_1+q=0$，$\therefore u^{\prime\prime}(x) = 0$，$u(x) = C_1x+C_2$，取$C_1 = 1, C_2 = 0$，得$u(x) = x$，$\therefore y_2 = u(x)y_1 = xy_1 = xe^{r_1x}$，因此原微分方程的通解为$y = C_1y_1+C_2y_2=(C_1+C_2x)e^{r_1x}$。

（3）共轭复数根，$p^2-4q<0$，$r_1 = -\frac{p}{2}-\frac{\sqrt{4q-p^2}}{2}i, r_2 = -\frac{p}{2}+\frac{\sqrt{4q-p^2}}{2}i$，令$\alpha = -\frac{p}{2}, \beta = \frac{\sqrt{4q-p^2}}{2}$，$r_1=\alpha-i\beta, r_2=\alpha+i\beta$，得到两个复函数解：$y_1 = e^{(\alpha-i\beta)x}, y_2 = e^{(\alpha+i\beta)x}$，由欧拉公式，有$y_1 = e^{\alpha x} \cdot e^{-i\beta x} = e^{\alpha x}(\cos \beta x - i\sin\beta x)$，$y_2 = e^{\alpha x} \cdot e^{i\beta x} = e^{\alpha x}(\cos \beta x + i\sin\beta x)$，$y_1+y_2=2e^{\alpha x}\cos\beta x, y_2-y_1=2i e^{\alpha x}\sin\beta x$，得到$Y_1 = \frac{y_1+y_2}{2}=e^{\alpha x}\cos\beta x, Y_2 = \frac{y_2-y_1}{2i}=e^{\alpha x}\sin\beta x$。

$Y_1, Y_2$是齐次方程的两个解，$\frac{Y_2}{Y_1}=\tan\beta x$，因此$Y_1, Y_2$是线性无关的，则$y = C_1Y_1+C_2Y_2 = e^{\alpha x}(C_1\cos\beta x+C_2\sin\beta x)$是原微分方程的通解。



例1：求$y^{\prime\prime}-2y^\prime-3y=0$的通解。

解：特征方程$r^2-2r-3=0$，解得$r_1=-1, r_2=3$，通解$y = C_1e^{-x}+C_2e^{3x}$。



例2：求初值问题：
$$
\left\{\begin{array}{ccc}\frac{d^2s}{dt^2}+2\frac{ds}{dt}+s &= &0 \\ s|_{t=0}=4,\frac{ds}{dt}|_{t=0}=-2 \end{array}\right.
$$
解特征方程：$r^2+2r+1=0$，特征根$r_1=r_2=-1$，通解$s = (C_1+C_2t)e^{-t}$，由$s|_{t=0}=4,\frac{ds}{dt}|_{t=0}=-2$，有$C_1=4, C_2=2$，求得特解$s = (4+2t)e^{-t}$。



设有$n$阶常系数齐次方程：$y^{(n)}+p_1y^{(n-1)}+p_2y^{(n-1)}+\cdots+p_{n-1}y^\prime+p_ny=0$，写出特征方程$r^n+p_1r^{n-1}+p_2r^{n-2}+\cdots+p_{n-1}r+p_n=0$，求出$n$个特征根，求出对应的线性无关的解：

（1）单实根$r$，$y = e^{rx}$；

（2）一对共轭复根，$r_1=\alpha-i\beta, r_2=\alpha+i\beta, y_1 = e^{\alpha x}\cos\beta x, y_2 = e^{\alpha x}\sin\beta x$；

（3）$k$重实根，$r_1=r_2=\cdots=r_k=r$，$y_1=e^{rx}, y_2=xe^{rx}, y_3=x^2e^{rx}, \cdots, y_k=x^{k-1}e^{rx}$

（4）一对$m$重复根，$r_1=r_2=\cdots=r_m=\alpha-i\beta$，$r_{m+1}=r_{m+2}=\cdots=r_{2m}=\alpha+i\beta$，$y_1 = e^{\alpha x}\cos\beta x, y_2 = xe^{\alpha x}\cos\beta x, \cdots y_m = x^{m-1}e^{\alpha x}\cos\beta x$，

$y_{m+1} = e^{\alpha x}\sin\beta x, y_{m+2} = x^2e^{\alpha x}\sin\beta x \cdots y_{2m} = x^{m-1}e^{\alpha x}\sin\beta x$



例4：求$y^{(4)}-6y^{\prime\prime\prime}+12y^{\prime\prime}-8y^\prime=0$的通解。

解：特征方程：$r^4-6r^3+12r^2-8r=0$或$r(r-2)^3 = 0$，解得特征根$r_1=0, r_2=r_3=r_4=2$，线性无关的解：$y_1=1, y_2=e^{2x}, y_3=xe^{2x}, y_4=x^2e^{2x}$，通解$y = C_1+C_2e^{2x}+C_3xe^{2x}+C_4x^2e^{2x}$。



例5：求$y^{(5)}+y^{(4)}+2y^{\prime\prime\prime}+2y^{\prime\prime}+y^\prime+y=0$的通解。

解：特征方程：$r^5+r^4+2r^3+2r^2+r+1=0$或$(r^2+1)^2(r+1)=0$，特征根：$r_1=r_2=-i, r_3=r_4=i, r_5=-1$，写出线性无关的解：$y_1=\cos x, y_2=x\cos x$，$y_3=\sin x, y_4=x\sin x, y_5=e^{-x}$。通解：$y=(C_1+C_1x)\cos x+(C_3+C_4x)\sin x+C_5e^{-x}$。



### 二、常系数线性非齐次微分方程——以二阶方程为例

$y^{\prime\prime}+py^\prime+qy=f(x)$

步骤：

（1）求方程对应的齐次方程$y^{\prime\prime}+py^\prime+qy=0$的通解，$\bar{y}=C_1y_1+C_2y_2$；

（2）求非齐次方程的特解$y^\star$;

（3）写出非齐次方程的通解$y = \bar{y}+y^\star = C_1y_1+C_2y_2 + y^\star$。



讨论以下两种情况：

（1）$f(x) = P_n(x)e^{\lambda x}$，其中$\lambda$是一实常数，$P_n(x)$表示实系数的$n$次多项式，即$P_n(x)=a_0x^n+a_1x^{n-1}+\cdots+a_{n-1}x+a_n$；

设方程的解的一般形式$y^\star = Q(x)e^{\lambda x}$，$Q(x)$是多项式，它的次数、系数待定。

求导数：$(y^\star)^\prime = Q^\prime(x)e^{\lambda x}+\lambda Q(x)e^{\lambda x}$，$(y^\star)^{\prime\prime} = Q^{\prime\prime}e^{\lambda x}+2\lambda Q^\prime(x)e^{\lambda x}+\lambda^2 Q(x)e^{\lambda x}$。

把$y^\star, (y^\star)^\prime, (y^\star)^{\prime\prime}$代入方程，$e^{\lambda x}[Q^{\prime\prime}(x)+2\lambda Q^\prime(x)+\lambda^2 Q(x)] + p e^{\lambda x}[Q^\prime(x)+\lambda Q(x)]+q Q(x)e^{\lambda}x = P_n(x)e^{\lambda x}$

消去$e^{\lambda x}$，整理成$Q^{\prime\prime}(x)+(2\lambda+p)Q^\prime(x)+(\lambda^2+p\lambda+q)Q(x)=P_n(x)$。

（1）如果$\lambda$不是特征方程的特征根，则$\lambda^2+p\lambda+q \neq 0$，比较左右两边多项式的次数，可知$Q(x)$是$n$次多项式。$Q(x)=Q_n(x)=b_0x^n+b_1x^{n-1}+\cdots+b_{n-1}x+b_n$，把$Q_n(x)$，$Q^\prime(x), Q^{\prime\prime}(x)$代入$Q^{\prime\prime}(x)+(2\lambda+p)Q^\prime(x)+(\lambda^2+p\lambda+q)Q(x)=P_n(x)$中，比较$x$的同次幂的系数，求出$b_i, (i=0, 1, \cdots, n)$。得到方程的特解$y^\star = Q_n(x)e^{\lambda x}$；

（2）如果$\lambda$是特征方程的单根，有$\lambda^2+p\lambda+q=0, 2\lambda+p \neq 0$（单根处的导数值不等于零），$Q^{\prime\prime}(x)+(2\lambda+p)Q^\prime(x)=P_n(x)$，比较等号两端$x$的次数，可知$Q^\prime(x)$应是$n$次多项式，从而$Q(x)$应是$n+1$次多项式，可设$Q(x)=xQ_n(x)$（$Q_n(x)$是$n$次完全多项式）。把$Q_n(x)$，$Q^\prime(x), Q^{\prime\prime}(x)$代入$Q^{\prime\prime}(x)+(2\lambda+p)Q^\prime(x)+(\lambda^2+p\lambda+q)Q(x)=P_n(x)$中，比较$x$的同次幂的系数，求出$Q_n(x)$的系数，从而求出$Q(x)$，得到方程的特解$y^\star = Q(x)e^{\lambda x} = xQ_n(x)e^{\lambda x}$；

（3）如果$\lambda$是特征方程的重根，有$\lambda^2+p\lambda+q=0, 2\lambda+p = 0$，$Q^{\prime\prime}(x)=P_n(x)$，应有$Q^{\prime\prime}(x)$是$n$次多项式，$Q(x)$应是$n+2$次多项式，设$Q(x)=x^2Q_n(x)$，把$Q_n(x)$，$Q^\prime(x), Q^{\prime\prime}(x)$代入$Q^{\prime\prime}(x)+(2\lambda+p)Q^\prime(x)+(\lambda^2+p\lambda+q)Q(x)=P_n(x)$中，比较$x$的同次幂的系数，求出$Q_n(x)$的系数，从而求出$Q(x)$，得到方程的特解$y^\star = Q(x)e^{\lambda x} = x^2Q_n(x)e^{\lambda x}$。



推广到$n$阶常系数线性非齐次微分方程：

$y^{(n)}+p_1y^{(n-1)}+\cdots+p_{n-1}y^\prime+p_ny=P_m(x)e^{\lambda x}$，特征方程$r^n+p_1r^{n-1}+\cdots+p_{n-1}r+p_n=0$，

（1）若$\lambda$不是特征根，$y^\star=Q_m(x)e^{\lambda x}$；

（2）若$\lambda$是$s$重特征根，$y^\star=x^s Q_m(x)e^{\lambda x}$。



例1：求$y^{\prime\prime}-5y^\prime+6y=xe^{2x}$的通解。

解：特征方程$r^2-5r+3=0$，$(r-2)(r-3)=0$，解得特征根$r_1=2,r_2=3$，对应的齐次方程的通解$\bar{y}=C_1e^{2x}+C_2e^{3x}$。自由项$f(x)=xe^{2x}=P_n(x)e^{\lambda x}$，取$n=1, \lambda=2$，$\lambda=2$是单根，特解的一般形式$y^\star=x(Ax+B)e^{2x}$，求$(y^\star)^\prime, (y^\star)^{\prime\prime}$代入原方程，消去$e^{2x}$，整理后得$-2Ax+2A-B=x$，比较等式两端$x$的同次幂系数，得$A=-\frac{1}{2}, B=-1$，所以$y^\star=-(\frac{1}{2}x^2+x)e^{2x}$。因此原方程的通解$y=\bar{y}+y^\star=C_1e^{2x}+C_2e^{3x}-x(\frac{1}{2}x+1)e^{2x}$。



例2：求$y^{\prime\prime}+y^\prime+y=x^2$的一个特解。

解：特征方程：$r^2+r+1=0$，特征根：$r_{1,2}=\frac{-1 \pm \sqrt{1-4}}{2}=-\frac{1}{2} \pm \frac{\sqrt{3}}{2}i$。自由项$f(x)=x^2=x^2e^{0x}$，取$n=2, \lambda=0$，而$\lambda=0$不是特征根，特解的一般形式：$y^\star=Q_n(x)e^{\lambda x}=(Ax^2+Bx+C)$，求$(y^\star)^\prime=2Ax, (y^\star)^{\prime\prime}=2A$，把$y^\star, (y^\star)^\prime, (y^\star)^{\prime\prime}$代入原方程，$2A+(2Ax+B)+(Ax^2+Bx+C)=x^2$，整理得$Ax^2+(2A+B)x+(2A+B+C)=x^2$，比较$x$的同次幂的系数，解得$A=1, B=-2, C=0$。所以$y^\star=x^2-2x$。



例3：求初值问题：
$$
\left\{\begin{array}{c}y^{\prime\prime}-2y^\prime+y=e^x \\ y|_{x=0}=1, y^\prime|_{x=0}=0\end{array}\right.
$$
解：特征方程：$r^2-2r+1=0$，特征根$r_1=r_2=1$，对应齐次方程的通解$\bar{y}=(C_1+C_2x)e^x$。$y^{\prime\prime}-2y^\prime+y=e^x$，自由项$f(x)=e^x=1 \cdot e^x = P_n(x)e^{\lambda x}$，$n=0, \lambda=1$，$\because \lambda=1$是二重特征根，特解一般形式$y^\star=x^2 \cdot A \cdot e^x$，求$(y^\star)^\prime, (y^\star)^{\prime\prime}$代入原方程，消去$e^x$，整理后得$A(x^2+4x+2)-2A(x^2+2x)+Ax^2=1$，解得$2A=1, A=\frac{1}{2}$，所以$y^\star=\frac{1}{2}x^2e^x$。非齐次方程的通解：$y=(C_1+C_2x)e^x+\frac{1}{2}x^2e^x$，由初始条件，解得$C_1=1, C_2=-1$，特解$y=(1-x)e^x+\frac{1}{2}x^2e^x$。



（2）$f(x) = e^{ax}[P_{n_1}(x)\cos bx+Q_{n_2}(x)\sin bx]$，其中$a, b$实常数，$b \neq 0$。$P_{n_1}(x)$是$n_1$次实系数多项式，$P_{n_2}(x)$是$n_2$次的实系数多项式。

讨论$y^{\prime\prime}+py^\prime+qy=e^{ax}[P_{n_1}(x)\cos bx+Q_{n_2}(x)\sin bx]$的特解的一般形式：

$y^\star=x^k e^{ax}[R_n(x)\cos bx + T_n(x)\sin bx]$，其中$n = \max\{n_1, n_2\}, R_n(x), T_n(x)$是$n$次多项式。

当$a+bi$不是特征方程$r^2+pr+q = 0$的根时，$k = 0$；当$a + bi$是特征方程$r^2+pr+q = 0$的根时，$k = 1$。



例1：求$y^{\prime\prime}-2y^\prime+5y=e^x\cos 2x$的通解。

解：特征方程$r^2 - 2r + 5 = 0$，解得特征根$r_1 = 1-2i, r_2 = 1+2i$，对于齐次方程的通解$\bar{y} = e^x(C_1\cos 2x + C_2 \sin 2x)$。自由项$f(x) = e^x\cos 2x = e^x[\cos 2x + 0 \cdot \sin 2x] = e^{ax}[P_{n_1}(x)\cos bx+Q_{n_2}(x)\sin bx]$，$P_{n_1}(x) = 1, Q_{n_2}(x) = 0, a = 1, b = 2$。取$n = 0$（0次多项式，即常数）。因为$a + bi = 1 + 2i$是特征根，所以特解的一般形式$y^\star = xe^x[A\cos 2x + B\sin 2x]$。求$(y^\star)^\prime, (y^\star)^{\prime\prime}$，把$y^\star, (y^\star)^\prime, (y^\star)^{\prime\prime}$代入原方程，消去$e^x$，得到$4B\cos2x - 4A\sin 2x = \cos 2x$，比较等号两边$\cos 2x, \sin 2x$的系数，得$4B = 1, -4A = 0$，即$B = \frac{1}{4}, A = 0$。$y^\star = \frac{xe^x\sin 2x}{4}$。原方程的通解$y = \bar{y} + y^\star = e^x(C_1\cos 2x + C_2 \sin 2x) + \frac{xe^x\sin 2x}{4}$。



例2：求$y^{\prime\prime} + 2y^\prime + y = x\sin x$满足$y|_{x = 0} = 0, y^\prime|_{x=0}=1$的特解。

解：特征方程：$r^2+2r+1=0$，解得特征根：$r_1 = r_2 = -1$，对应的齐次方程的通解$\bar{y} = (C_1 + C_2 x)e^{-x}$。自由项$f(x) = x\sin x = e^{0x}x\sin x = e^{ax}[P_{n_1}(x)\cos bx+Q_{n_2}(x)\sin bx]$，$P_{n_1}(x) = 0, Q_{n_2}(x) = x, a = 0, b = 1$，取$n=1$。$a + bi = i$不是特征根，特解的一般形式$y^\star = (Ax+B)\cos x + (Cx+D)\sin x$，求$(y^\star)^\prime = A\cos x - (Ax+B)\sin x + C\sin x + (Cx + D)\cos x = (Cx + A + D)\cos x + (C - B - Ax)\sin x$，$(y^\star)^{\prime\prime} = (2C-B-Ax)\cos x - (Cx + D + 2A)\sin x$。把$y^\star, (y^\star)^\prime, (y^\star)^{\prime\prime}$代入原方程，整理得$(2Cx+2A+2C+2D)\cos x + (-2Ax-2A-2B+2C)\sin x = x\sin x$。比较等号两边$\cos x, \sin x$的系数，得：
$$
\left\{\begin{array}{c}-2Ax-2A-2B+2C = x \\ 2Cx+2A+2C+2D=0\end{array}\right.
$$
解得$A = -\frac{1}{2}, B = \frac{1}{2}, C = 0, D = \frac{1}{2}$，特解$y^\star = (-\frac{1}{2}x + \frac{1}{2})\cos x  + \frac{1}{2}\sin x$。原方程的通解$y = \bar{y} + y^\star = (C_1 + C_2 x)e^{-x} + (-\frac{1}{2}x + \frac{1}{2})\cos x + \frac{1}{2}\sin x$。由$y|_{x = 0} = 0$，得$0 = C_1 + \frac{1}{2}, C_1 = -\frac{1}{2}$，则$(-\frac{1}{2} + C_2 x)e^{-x} + (-\frac{1}{2}x + \frac{1}{2})\cos x + \frac{1}{2}\sin x$；$y^\prime = C_2 e^{-x} - (-\frac{1}{2}+C_2x)e^{-x} - \frac{1}{2}\cos x - (-\frac{1}{2}x+\frac{1}{2})\sin x + \frac{1}{2}\cos x$，再由$y^\prime|_{x=0}=1$，得$1 = C_2 +\frac{1}{2} - \frac{1}{2} +\frac{1}{2}$，即$C_2 = \frac{1}{2}$。所求特解$y = (-\frac{1}{2} + \frac{1}{2} x)e^{-x} + (-\frac{1}{2}x + \frac{1}{2})\cos x + \frac{1}{2}\sin x$。



例3：写出$y^{(4)}+y^{\prime\prime} = 3x^2+\sin x$特解的一般形式。

解：由原方程，写出：
$$
\left\{\begin{array}{c}y^{(4)} + y^{\prime\prime} = 3x^2 \\ y^{(4)} + y^{\prime\prime} = \sin x\end{array}\right.
$$
对于方程$y^{(4)} + y^{\prime\prime} = 3x^2$：特征方程$r^4+r^2=0, r^2(r^2+1)=0$，解得$r_1 = r_2 = 0, r_3 = -i, r_4 = i$。自由项$f_1(x) = 3x^2 = 3x^2 e^{0x} = P_n(x)e^{\lambda x}$，取$n = 2, \lambda = 0$。$\therefore \lambda = 0$是二重特征根，特解的一般形式$y_1^\star = x^2(Ax^2+Bx+C)$；

对于方程$y^{(4)} + y^{\prime\prime} = \sin x$：特征方程与特征根同上。自由项$f_2(x) = \sin x = e^{0x}\sin x = e^{ax}[P_{n_1}(x)\cos bx + Q_{n_2}(x)\sin bx]$，$P_{n_1}(x) = 0, Q_{n_2}(x) = 1, a = 0, b = 1$，取$n = 0$。$a+bi = 0+i=i$是特征根，特解的一般形式：$y_2^\star = xe^{0x}(D\cos x + E\sin x) = x(D\cos x + E\sin x)$。由非齐次方程解的结构定理，可知原方程的特解的一般形式为：$y^\star = y_1^\star + y_2^\star = x^2(Ax^2+Bx+C) + x(D\cos x + E\sin x)$。求导代入原方程，对比系数即可求出$A, B, C, D, E$的值。



总结：对于$y^{\prime\prime} + py^\prime + qy = f(x)$的特解$y^\star$一般形式的确定方法：

|                      自由项$f(x)$的形式                      |            条件             |             $y^\star$形式             |
| :----------------------------------------------------------: | :-------------------------: | :-----------------------------------: |
|                           $P_n(x)$                           |         0不是特征根         |               $Q_n(x)$                |
|                           $P_n(x)$                           |      0是特征方程的单根      |               $xQ_n(x)$               |
|                           $P_n(x)$                           |     0是特征方程的二重根     |              $x^2Q_n(x)$              |
|                                                              |                             |                                       |
|                    $e^{\lambda x}P_n(x)$                     |     $\lambda$不是特征根     |         $e^{\lambda x}Q_n(x)$         |
|                    $e^{\lambda x}P_n(x)$                     |  $\lambda$是特征方程的单根  |        $xe^{\lambda x}Q_n(x)$         |
|                    $e^{\lambda x}P_n(x)$                     | $\lambda$是特征方程的二重根 |       $x^2e^{\lambda x}Q_n(x)$        |
|                                                              |                             |                                       |
| $e^{ax}[P_{n_1}(x)\cos bx + Q_{n_2}(x)\sin bx], n = \max\{n_1, n_2\}$ |      $a+bi$不是特征根       | $e^{ax}[R_n(x)\cos bx + T_n\sin bx]$  |
| $e^{ax}[P_{n_1}(x)\cos bx + Q_{n_2}(x)\sin bx], n = \max\{n_1, n_2\}$ |       $a+bi$是特征根        | $xe^{ax}[R_n(x)\cos bx + T_n\sin bx]$ |



例1：设$f(x)$有二次连续的导数，使$f(x)y dx + [e^x-f^\prime(x)]dy = 0$是全微分方程，同时，$f(0) = \frac{1}{2}, f^\prime(0) = 1$，（1）求$f(x)$；（2）求全微分方程的通解。

解：（1）方程$f(x)y dx = [e^x-f^\prime(x)]dy = 0$是全微分方程$\Longrightarrow$$\frac{\partial P}{\partial y} = \frac{\partial Q}{\partial x}, [P = f(x)y, Q = e^x - f^\prime(x)]$，则有$\frac{\partial P}{\partial y} = f(x), \frac{\partial Q}{\partial x} = e^x - f^{\prime\prime}(x)$，得到$f(x) = e^x - f^{\prime\prime}(x)$，移项得$f^{\prime\prime}(x)+f(x)=e^x$。
$$
\left\{\begin{array}{c}f^{\prime\prime}(x) + f(x) = e^x \\ f(0) = \frac{1}{2}, f^\prime(0) = 1\end{array}\right.
$$
特征方程$r^2 + 1 = 0$，特征根$r_1 = -i, r_2 = i$，对应齐次方程的通解$\bar{y} = C_1 \sin x + C_2 \cos x$，非齐次方程的特解的一般形式$y^\star = Ae^x$，$(y^\star)^\prime = Ae^x, (y^\star)^{\prime\prime} = Ae^x$，代入非齐次方程，得到$Ae^x + Ae^x = e^x, 2A = 1, A = \frac{1}{2}$，$\therefore y^\star = \frac{1}{2}e^x$。所以通解$f(x) = \bar{y} + y^\star = C_1\sin x + C_2\cos x + \frac{1}{2}e^x$。由条件$f(0) = \frac{1}{2}$，$\frac{1}{2} = C_2 + \frac{1}{2}, \Longrightarrow C_2 = 0$，$f(x) = C_1\sin x + \frac{1}{2}e^x, f^\prime(x) = C_1\cos x + \frac{1}{2}e^x$；则再由条件$f^\prime(0) = 1$，$1 = C_1 + \frac{1}{2} \Longrightarrow C_1 = \frac{1}{2}$。所求函数$f(x) = \frac{1}{2}\sin x + \frac{1}{2}e^x$。

（2）把$f(x)$代入全微分方程，得到$\frac{1}{2}(\sin x + e^x)y dx + [e^x - \frac{1}{2}\cos x - \frac{1}{2}e^x] dy = 0$，方程整体乘以2，$(\sin x + e^x)y dx + [e^x - \cos x] dy = 0$。用曲线积分的方法求$u(x, y)$。$u(x, y) = \int_{(0, 0)}^{(x, y)}(\sin x + e^x)y dx + (e^x - \cos x)dy = 0 + \int_0^y (e^x - \cos x)dy = (e^x - \cos x)y$，全微分方程通解：$u(x, y) = (e^x - \cos x)y = C$。



### 三、常系数线性微分方程应用举例

例1：设有一个弹簧，上端固定，下端挂一个质量为$m$的重物，当物体处于静止状态时，作用在物体上的重力与弹簧的弹性力大小相等，方向相反（这个位置称为平衡位置）。建立以平衡位置为原点$O$，方向同重力方向的坐标轴，给物体初速度$v_0 \neq 0$，这时物体离开平衡位置$O$，作上、下的振动。物体的位置$x$随着时间$t$变化，即$x = x(t)$。求物体振动的规律$x(t)$。

解：在振动的过程中，某一时刻$t$，物体受到弹簧恢复力$f$的作用，$f$的大小与物体离开平衡位置的位移$x$有关，且$f = -kx, (k > 0)$，负号表示弹簧的恢复力与物体的位移方向相反。

（1）无阻尼自由振动，即不考虑介质（如空气）的阻力，根据牛顿第二运动定律（$F = ma$），有$m\frac{d^2 x}{dt^2} = -kx$，$\frac{d^2x}{dt^2} = -\frac{k}{m}x$，令$\frac{k}{m} = \omega_0^2$，$\frac{d^2x}{dt^2} + \omega_0^2 x = 0$，特征方程$r^2+\omega_0^2 = 0$，解得特征根$r_1 = \omega_0 i, r_2 = -\omega_0 i$。方程的通解$x = C_1\cos \omega_0 t + C_2\sin \omega_0 t$，$x = \sqrt{C_1^2 + C_2^2}(\frac{C_1}{\sqrt{C_1^2 + C_2^2}}\cos \omega_0 t + \frac{C_2}{\sqrt{C_1^2 + C_2^2}}\sin \omega_0 t)$，令$\frac{C_1}{\sqrt{C_1^2 + C_2^2}} = \sin \phi, \frac{C_2}{\sqrt{C_1^2 + C_2^2}} = \cos \phi, \sqrt{C_1^2 + C_2^2} = A$，则$x = A(\sin \phi \cos \omega_0 t + \cos \phi \sin \omega_0 t) = A \sin(\omega_0 t + \phi)$——==简谐振动==，周期是$\frac{2\pi}{\omega_0}$， 振幅$A = \sqrt{C_1 + C_2}$。

（2）阻尼自由振动，如上例，假定物体除了受弹簧的恢复力之外，还有介质阻力$R$的作用。$R$的大小与振动的速度$\frac{dx}{dt}$成正比，$R = -h\frac{dx}{dt}, (h > 0)$，其中负号表示阻力的方向与物体的运动方向相反。由牛顿第二运动定律，$m\frac{d^2 x}{dt^2} = -h\frac{dx}{dt} - kx$，$\frac{d^2 x}{dt^2} + \frac{h}{m}\frac{dx}{dt} + \frac{k}{m}x = 0$，令$2\beta = \frac{h}{m}, \frac{k}{m} = \omega_0^2$，则$\frac{d^2x}{dt^2} + 2\beta \frac{dx}{dt} + \omega_0^2 x = 0$。

1. 小阻尼情形（$0 < \beta < \omega_0 $）：微分方程的特征方程$r^2 - 2\beta r + \omega_0^2 = 0$，由求根公式得：$r_1 = -\beta - \sqrt{\beta^2 - \omega_0^2} = -\beta - \sqrt{\omega_0^2 - \beta^2}i, r_2 = -\beta + \sqrt{\beta^2 - \omega_0^2} = -\beta + \sqrt{\omega_0^2 - \beta^2}i$

   方程的通解：$x = e^{-\beta t}(C_1 \cos \sqrt{\omega_0^2-\beta^2}t + C_2 \sin \sqrt{\omega_0^2-\beta^2}t) = Ae^{-\beta t}\sin(\sqrt{\omega_0^2-\beta^2}t + \phi)$，其中$A = \sqrt{C_1^2 + C_2^2}, \phi = \arctan \frac{C_1}{C_2}$，振幅$Ae^{\beta t}, (\beta > 0)$，$\lim_{t \to +\infty}Ae^{-\beta t} = 0$，这说明随着时间$t$的增大，振幅很快地趋于0。

2. 大阻尼情形（$0 < \omega_0 < \beta$）：$r_1 = -\beta - \sqrt{\beta^2 - \omega_0^2}, r_2 = -\beta + \sqrt{\beta^2 - \omega_0^2}$，$x = C_1e^{(-\beta - \sqrt{\beta^2 - \omega_0^2})t} + C_2 e^{(-\beta + \sqrt{\beta^2 - \omega_0^2})t}$，显然$-\beta - \sqrt{\beta^2 - \omega_0^2} < 0$，$\because \beta > \sqrt{\beta^2 - \omega_0^2}, \therefore -\beta + \sqrt{\beta^2 - \omega_0^2} < 0$，$\lim_{t \to +\infty}x = 0$。

3. 临界阻尼情形：$\beta = \omega_0$，特征根$r_1 = r_2 = -\beta$，通解$x = (C_1 + C_2 t)e^{-\beta t} = C_1 e^{-\beta t} + C_2 t e^{-\beta t}$，$\lim_{t \to +\infty}e^{-\beta t} = 0, \lim_{t \to +\infty}t e^{-\beta t} = \lim_{t \to +\infty}\frac{t}{e^{\beta t}} = \lim_{t \to +\infty}\frac{1}{\beta e^{\beta t}} = 0$，$\therefore \lim_{t \to +\infty} x = 0$。



### 四、欧拉方程

形如$x^n y^{(n)} + p_1 x^{n-1}y^{(n-1)} + \cdots + p_{n-1}xy^\prime + p_n y = f(x)$（其中$p_1, p_2, \cdots, p_n$是常数），称为欧拉方程。

作变换$x = e^t$或$t = \ln x$，将自变量$x$换为$t$，$\frac{dy}{dx} = \frac{dy}{dt} \cdot \frac{dt}{dx} = \frac{1}{x}\frac{dy}{dt}$，$\frac{d^2y}{dx^2} = \frac{d}{dx}(\frac{1}{x}\frac{dy}{dt}) = -\frac{1}{x^2}\frac{dy}{dt} + \frac{1}{x}\frac{d^2y}{dt^2}\frac{dt}{dx} = \frac{1}{x^2}(\frac{d^2y}{dt^2}-\frac{dy}{dx})$，$\frac{d3y}{dx^3}=\frac{d}{dx}[\frac{1}{x^2}(\frac{d^2y}{dt^2}-\frac{dy}{dx})]=-\frac{2}{x^3}(\frac{d^2y}{dt^2}-\frac{dy}{dx})+\frac{1}{x^2}(\frac{d^3 y}{dt^3} \cdot \frac{dt}{dx}-\frac{d^2y}{dt} \cdot \frac{dt}{dx}) \\ = \frac{1}{x^3}(\frac{d^3y}{dt^3}-3\frac{d^2y}{dt^2}+2\frac{dy}{dt})$

引进符号$\frac{dy}{dt} = \frac{d}{dt} \cdot y = Dy, (D = \frac{d}{dt})$，则$x \frac{dy}{dx} = \frac{dy}{dt} = Dy$，$x^2 \frac{d^2y}{dx^2} = (\frac{d^2}{dt^2}-\frac{d}{dt})y=(D^2-D)y = D(D-1)y$，$x^3 \frac{d^3y}{dx^3} = (D^3-3D^2 + 2D)y = D(D-1)(D-2)y$，

一般地：$x^k \frac{d^{(k)y}}{dx^{(k)}} = D(D-1)(D-2) \cdots (D-k+1)y, (k = 1,2,\cdots)$，

代入欧拉方程，得到以$t$为自变量的常系数线性微分方程，求得通解后，再把$t$换成$\ln x$，就得到了原方程的通解。



例1：求$x^3 y^{\prime\prime\prime} + 3x^2 y^{\prime\prime} + xy^\prime - y = x^2$的通解。

解：原方程是欧拉方程。作变量替换$x = e^t$，或$t = \ln x$。$x^3 y^{\prime\prime\prime} = D(D-1)(D-2)y$，$x^2y^{\prime\prime}=D(D-1)y$，$xy^\prime = Dy$，代入原方程：$D(D-1)(D-2)y+3D(D-1)y+Dy-y=e^{2t}$，即$(D^3-1)y = e^{2t}, D^3y-y=e^{2t}$，$\frac{d^3y}{dt^3} - y = e^{2t}$。特征方程：$r^3-1=0$，特征根$r_1=1, r_2 = -\frac{1}{2}+\frac{\sqrt{3}}{2}i, r_3 = -\frac{1}{2}-\frac{\sqrt{3}}{2}i$，对应齐次方程的通解：$\bar{y} = C_1 e^t + e^{-\frac{1}{2}t}[C_2\cos\frac{\sqrt{3}}{2}t+C_3\sin\frac{\sqrt{3}}{2}t]$，由$x = e^t$，得$\bar{y}= C_1x+x^{-\frac{1}{2}}[C_2 \cos (\frac{\sqrt{3}}{2}\ln x) + C_3 \sin (\frac{\sqrt{3}}{2}\ln x)]$。非齐次方程：$\frac{d^3y}{dt^3} - y = e^{2t}$的特解一般形式$y^\star = A e^{2t} = A x^2$，$(y^\star)^{\prime} = 2A x, (y^\star)^{\prime\prime} = 2A, (y^\star)^{\prime\prime\prime} = 0$，代入原欧拉方程，$3x^2 \cdot 2A + x \cdot 2A x - Ax^2 = x^2$，即$6A + 2A - A = 1$，解得$A = \frac{1}{7}$。

原欧拉方程的通解$y = \bar{y} + y^\star = C_1x+x^{-\frac{1}{2}}[C_2 \cos (\frac{\sqrt{3}}{2}\ln x) + C_3 \sin (\frac{\sqrt{3}}{2}\ln x)] + \frac{1}{7}x^2$。

