[toc]

# 第11章 级数

函数项级数：

1. 幂级数
2. 三角级数

## 第1节 常数项级数

内容：常数项级数、级数的性质

### 一、级数的基本概念

==级数定义==：设给一数列$\{u_n\}:u_1, u_2, \cdots, u_n, \cdots$，则称表达式$u_1+u_2+\cdots+u_n+\cdots$为无穷级数，$u_n, (n=1,2,\cdots)$是常数，则称为数项级数。简记为$\sum_{n=1}^{\infty}u_n = u_1+u_2+\cdots+u_n+\cdots$，$u_n$称为通项或一般项。



==定义==：若级数$\sum_{n=1}^{\infty}u_n$的部分和数列$\{S_n\}$的极限$\lim_{n \to \infty}S_n$存在，即$\lim_{n \to \infty}S_n = S$，则称$\sum_{n=1}^{\infty}u_n$收敛，并称$S$为级数的和，即$S = u_1+u_2+\cdots+u_n+\cdots$；若$\lim_{n \to \infty}S_n$不存在，则称$\sum_{n=1}^{\infty}u_n$发散。

$S = u_1+u_2+\cdots+u_n+\cdots$，取$S_n \approx S$，差$S - S_n = u_{n+1} + u_{n+2} + \cdots$，记为$r_n = S - S_n$，误差$|r_n|$，$r_n$称为级数$\sum_{n=1}^{\infty}u_n$的余项。



### 二、级数的基本性质

1. 若级数$\sum_{n=1}^{\infty}u_n$收敛于$S$，$k$是常数，则$\sum_{n=1}^{\infty}ku_n$收敛于$kS$。

2. 设$\sum_{n=1}^{\infty}u_n$收敛于$S$，$\sum_{n=1}^{\infty}v_n$收敛于$\sigma$，则$\sum_{n=1}^{\infty}(u_n+v_n)$收敛于$S+\sigma$。

3. 在级数的前面部分去掉（加上）有限项，不影响级数的敛散性。

4. 收敛级数加括号后所成的级数仍然收敛于原级数的和。

5. （级数收敛的必要条件）设$\sum_{n=1}^{\infty}u_n$收敛，则$\lim_{n \to \infty}u_n = 0$。

   证：设$\sum_{n=1}^{\infty}u_n$收敛于$S$，

   $u_1+u_2+\cdots+u_n+u_{n+1}+\cdots$，

   $s_n = u_1+u_2+\cdots+u_n$，

   $s_{n-1} = u_1+u_2+\cdots+u_{n-1}$，

   $u_n = s_n - s_{n-1}$，

   $\lim_{n \to \infty}u_n = \lim_{n \to \infty}s_n - \lim_{n \to \infty}s_{n-1} = S-S=0$。

   由性质5知：若$\lim_{n \to \infty}u_n \neq 0$，则$\sum_{n=1}^{\infty}u_n$发散。

推论1：级数$\sum_{n=1}^{\infty}u_n$与$\sum_{n=1}^{\infty}ku_n, (k \neq 0)$具有相同的敛散性。

==注意==：

1. 若收敛级数带有括号，则去掉括号后得到的新级数不一定收敛，如：

   $(1-1)+(1-1)+(1-1)+\cdots$，即$0+0+0+\cdots$收敛于$0$，去掉括号后，得$1-1+1-1+\cdots$此级数发散。

2. 若$\sum_{n=1}^{\infty}u_n$加括号后得到的级数发散，则原来的级数发散。



证明：调和级数$1+\frac{1}{2}+\frac{1}{3}+\cdots+\frac{1}{n}+\cdots$是发散的。

证：假设级数$1+\frac{1}{2}+\frac{1}{3}+\cdots+\frac{1}{n}+\cdots$收敛于$S$，$\lim_{n \to \infty}(S_{2n}-S_n) = \lim_{n \to \infty}S_{2n} -\lim_{n \to \infty}S_n = S-S=0$，

但是$S_{2n} - S_n = (1+\cdots+\frac{1}{n}+\cdots+\frac{1}{2n})-(1+\frac{1}{2}+\cdots+\frac{1}{n}) \\ = \frac{1}{n+1}+\frac{1}{n+2}+\cdots+\frac{1}{2n} > \frac{1}{2n}+\frac{1}{2n}+\cdots+\frac{1}{2n} = \frac{1}{2}$

则$\lim_{n \to \infty}(S_{2n}-S_n) = 0$与$S_{2n}-S_n > \frac{1}{2}$是矛盾的。



### 三、正项级数敛散性判别法

==正项级数==：如果在$\sum_{n=1}^\infty u_n$中，$u_n \ge 0$（但$u_n \not \equiv 0$），则称$\sum_{n=1}^\infty u_n$为正项级数。

==正项级数收敛的基本原理==：正项级数收敛$\Longleftrightarrow$它的部分和数列$\{S_n\}$是有界的。

证：$\Longrightarrow$，设正项级数$\sum_{n=1}^\infty u_n$收敛，由级数的定义，部分和数列$\lim_{n \to \infty}S_n = S$，极限存在的数列一定是有界的，即$\exists_M > 0$，使得$S_n \le M$。

$\Longleftarrow$，设$\sum_{n=1}^\infty u_n$的$\{S_n\}$是有界的，因为$u_n \ge 0, (n=1,2,\cdots)$，$S_1 = u_1 \le u_1+u_2 = S_2, S_2 = u_1 + u_2 \le u_1+u_2+u_3 =S_3$，则有$S_1 \le S_2 \le S_3 \le \cdots \le S_n \le \cdots$，$\{S_n\}$是单调增数列，且有界。根据极限存在准则，可知$\lim_{n \to \infty}S_n$存在，即$\sum_{n=1}^\infty u_n$收敛。



正项级数敛散性的判别法：

1. 比较判别法

   设有正项级数$\sum_{n=1}^\infty u_n$和$\sum_{n=1}^\infty v_n$，且存在$k \in N$，对一切满足$n > k$，都有$u_n \le v_n, (n = k, k+1, \cdots)$，则

   （1）若$\sum_{n=1}^\infty v_n$收敛，则$\sum_{n=1}^\infty u_n$收敛；

   （2）若$\sum_{n=1}^\infty u_n$发散，则$\sum_{n=1}^\infty v_n$发散。

   证明：根据级数的性质——在级数前面去掉有限项，级数的敛散性不变，不妨设$u_n \le v_n$对$n=1,2\cdots$成立。$S_n = u_1+u_2+\cdots+u_n, \sigma_n = v_1+v_2+\cdots+v_n$

   （1）若$\sum_{n=1}^\infty v_n$收敛，根据正项级数收敛的基本原理，$\{\sigma_n\}$有界，即$\exists_M > 0$，使得$\sigma_n \le M, (n=1, 2, \cdots)$，$S_n=u_1+u_2+\cdots+u_n \le v_1+v_2+\cdots+v_n=\sigma_n$，即有$S_n \le \sigma_n \le M$，即$\{S_n\}$有界，所以$\sum_{n=1}^\infty u_n$收敛。

   （2）反证法：假若$\sum_{n=1}^\infty v_n$收敛，及$u_n \le v_n$，可知$\sum_{n=1}^\infty u_n$收敛，这与$\sum_{n=1}^\infty u_n$发散的假设矛盾。



例1：讨论$p$-级数$\sum_{n=1}^\infty \frac{1}{n^p}$（$p > 0$为常数）的敛散性。

解：当$p=1$时，得$\sum_{n=1}^\infty \frac{1}{n^p}$——调和级数发散；

当$0 < p < 1$时，有$0 < n^p < n, \frac{1}{n^p}>\frac{1}{n}$，因为$\sum_{n=1}^\infty \frac{1}{n}$发散，且$\frac{1}{n^p}>\frac{1}{n}$，由比较判别法，知$\sum_{n=1}^\infty \frac{1}{n^p}$发散。

当$p > 1$时，对任何$n \ge 2$正整数，必存在连续变量$x$满足$n-1 \le x \le n$，$0 < x^p \le n^p$，可知$\frac{1}{x^p} \ge \frac{1}{n^p}$，作积分$\int_{n-1}^n \frac{1}{n^p}dx = \frac{1}{n^p}\int_{n-1}^{n}dx = \frac{1}{n^p}$，

$\frac{1}{n^p} = \int_{n-1}^n \frac{1}{n^p}dx \le \int_{n-1}^{n}\frac{1}{x^p}dx = \frac{1}{1-p}\frac{1}{x^{p-1}}|_{n-1}^n \\ = \frac{1}{1-p}[\frac{1}{n^{p-1}} - \frac{1}{(n-1)^{p-1}}] = \frac{1}{p-1}[\frac{1}{(n-1)^{p-1}} - \frac{1}{n^{p-1}}]$

考虑$\sum_{n=2}^\infty \frac{1}{p-1}[\frac{1}{(n-1)^{p-1}}-\frac{1}{n^{p-1}}]$的敛散性，它的部分和$\sigma_n = \frac{1}{p-1}[(1-\frac{1}{2^{p-1}})+(\frac{1}{2^{p-1}}-\frac{1}{3^{p-1}}) + \cdots + (\frac{1}{(n-1)^{p-1}}-\frac{1}{n^{p-1}}) + (\frac{1}{n^{p-1}}-\frac{1}{(n+1)^{p-1}})] \\ = \frac{1}{p-1}(1-\frac{1}{(n+1)^{p-1}}) < \frac{1}{p-1}$

这说明正项级数$\sum_{n=2}^\infty \frac{1}{p-1}[\frac{1}{(n-1)^{p-1}}-\frac{1}{n^{p-1}}]$的部分和数列$\{\sigma_n\}$有界，所以该级数收敛，所以$\sum_{n=2}^\infty \frac{1}{n^p}$收敛，即$\sum_{n=1}^\infty \frac{1}{n^p}$收敛。



例2：判别$\sum_{n=1}^\infty \frac{1}{\sqrt{n^2+n+1}}$的敛散性。

解：$\frac{1}{\sqrt{n^2+n+1}} > 0, (n=1,2,\cdots)$。因为$n^2+n+1 < n^2+2n+1 = (n+1)^2$，从而有$\frac{1}{\sqrt{n^2+n+1}} > \frac{1}{\sqrt{(n+1)^2}} = \frac{1}{n+1}$，而$\sum_{n=1}^\infty = \frac{1}{2}+\frac{1}{3}+\cdots+\frac{1}{n+1}+\cdots$是发散的，根据正项级数敛散性的比较判别法，可知$\sum_{n=1}^\infty \frac{1}{\sqrt{n^2+n+1}}$发散。



例3：判别$\sum_{n=1}^\infty \ln(1+\frac{1}{n^2})$的敛散性。

解：因$\frac{1}{n^2} > 0, \ln(1+\frac{1}{n^2}) > 0$，所以$\sum_{n=1}^\infty \ln(1+\frac{1}{n^2})$是正项级数。

先证明：当$x > 0$时，$x > \ln(1+x)$，即证明$x - \ln(1+x)>0$。现令$f(x) = x - \ln(1+x), 0 \le x$，$f^\prime(x) = 1 - \frac{1}{1+x} = \frac{x}{1+x} > 0, (x > 0)$，因此$f(x)$在$[0, +\infty]$上是单调增的，所以$f(x) > f(0), x - \ln(1+x) > 0$，即$x > \ln(1+x)$。

现取$x = \frac{1}{n^2} > 0$代入上述不等式中，得$\frac{1}{n^2} > \ln(1+\frac{1}{n^2})$，由$\sum_{n=1}^\infty \frac{1}{n^2}$收敛，根据正项级数的比较判别法，可知$\sum_{n=1}^\infty \ln(1+\frac{1}{n^2})$收敛。



例4：判别$\sum_{n=1}^\infty \frac{6^n}{7^n-5^n}$的敛散性。

解：$u_n = \frac{6^n}{7^n-5^n} = \frac{(\frac{6}{7})^n}{1-(\frac{5}{7})^n}$，$\because 0 < \frac{5}{7} < 1, 0 < (\frac{5}{7})^n < \frac{5}{7} < 1, \therefore 1 - (\frac{5}{7})^n > 1 - \frac{5}{7} = \frac{2}{7}$，因而有$u_n = \frac{(\frac{6}{7})^n}{1-(\frac{5}{7})^n} < \frac{(\frac{6}{7})^n}{\frac{2}{7}} = \frac{7}{2}(\frac{6}{7})^n$，$\sum_{n=1}^\infty (\frac{6}{7})^n$是等比级数，公比$q = \frac{6}{7} < 1$，所以$\sum_{n=1}^\infty (\frac{6}{7})^n$收敛，从而$\sum_{n=1}^\infty \frac{2}{7}(\frac{6}{7})^n$也收敛，根据正项级数的比较判别法，可知$\sum_{n=1}^\infty \frac{6^n}{7^n-5^n}$收敛。



==技巧==：掌握p-级数的敛散性和几何级数的敛散性，构造不等式，利用正项级数的比较判别法进行敛散性判别。



==比较判别法的极限形式==：设有正项级数$\sum_{n=1}^\infty u_n, \sum_{n=1}^\infty v_n, (v_n > 0)$，满足$\lim_{n \to \infty}\frac{u_n}{v_n} = l, (0 < l < +\infty)$，则$\sum_{n=1}^\infty u_n$与$\sum_{n=1}^\infty v_n$具有相同的敛散性。

证明：因为$\lim_{n \to \infty}\frac{u_n}{v_n} = l, (0 < l < +\infty)$，由数列极限的定义，对给定正数$\epsilon = \frac{l}{2} > 0$，必存在正整数$N$，使得$n > N$，恒有$|\frac{u_n}{v_n} - l| < \frac{l}{2} \Longleftrightarrow -\frac{l}{2} < \frac{u_n}{v_n} - l < \frac{l}{2}, \frac{l}{2} < \frac{u_n}{v_n} < \frac{3l}{2}$，$\frac{l}{2}v_n < u_n < \frac{3l}{2}v_n$

（1）若$\sum_{n=1}^\infty v_n$收敛，则有$u_n < \frac{3l}{2}v_n$及$\sum_{n=1}^\infty \frac{3l}{2}v_n$收敛，根据比较判别法，可知$\sum_{n=1}^\infty u_n$收敛；

（2）若$\sum_{n=1}^\infty v_n$发散，则$\sum_{n=1}^\infty \frac{l}{2}v_n$发散，根据比较判别法可知$\sum_{n=1}^\infty u_n$发散。



==补充==：

（1）若$l = 0$，即$\lim_{n \to \infty}\frac{u_n}{v_n} = 0$，且$\sum_{n=1}^\infty v_n$收敛，则$\sum_{n=1}^\infty u_n$收敛。

（2）若$l = +\infty$，即$\lim_{n \to \infty}\frac{u_n}{v_n} = +\infty$，且$\sum_{n=1}^\infty v_n$发散，则$\sum_{n=1}^\infty u_n$发散。



例1：判别$\sum_{n=1}^\infty \ln(1+\frac{1}{n})$的敛散性。

解：令$u_n = \ln(1+\frac{1}{n})$，找$v_n = \frac{1}{n}$，$\lim_{n \to \infty}\frac{\ln(1+\frac{1}{n})}{\frac{1}{n}} = \lim_{n \to \infty}n\ln(1+\frac{1}{n}) = \lim_{n \to \infty}\ln(1+\frac{1}{n})^n = \ln e = 1$，又因为$\sum_{n=1}^\infty v_n = \sum_{n=1}^\infty \frac{1}{n}$发散，可知$\sum_{n=1}^\infty \ln(1+\frac{1}{n})$发散。



例2：判别$\sum_{n=1}^\infty \frac{1}{n^{1+\frac{1}{n}}}$的敛散性。

解：令$u_n = \frac{1}{n^{1+\frac{1}{n}}} = \frac{1}{n \cdot n^{\frac{1}{n}}}$，找$v_n = \frac{1}{n}$，$\lim_{n \to \infty}\frac{u_n}{v_n} = \lim_{n \to \infty}\frac{\frac{1}{n \cdot n^{\frac{1}{n}}}}{\frac{1}{n}} = \lim_{n \to \infty}\frac{1}{n^{\frac{1}{n}}} = \frac{1}{\lim_{n \to \infty}n^{\frac{1}{n}}} = 1$，因为$\sum_{n=1}^\infty v_n = \sum_{n=1}^\infty \frac{1}{n}$发散，可知$\sum_{n=1}^\infty \frac{1}{n^{1+\frac{1}{n}}}$发散。



例3：判别$\sum_{n=1}^\infty \frac{\ln n}{n^2}$的敛散性。

解：令$u_n = \frac{\ln n}{n^2}$，找$v_n = \frac{1}{n^p}, (p > 0)$。$\lim_{n \to \infty}\frac{u_n}{v_n} = \lim_{n \to \infty}\frac{\frac{\ln n}{n^2}}{\frac{1}{n^p}} = \lim_{n \to \infty}\frac{\ln n}{n^{2-p}}$，
$$
\lim_{n \to \infty}\frac{\ln n}{n^{2-p}} = \left\{\begin{array}{cc}+\infty, &p \ge 2 \\ 0, &p < 2\end{array}\right.
$$
取$p = \frac{3}{2}, 1 < p = \frac{3}{2} < 2$，$\sum_{n=1}^\infty \frac{1}{n^{\frac{3}{2}}}$为p-级数，$p>1$，则$\sum_{n=1}^\infty \frac{1}{n^{\frac{3}{2}}}$收敛。又因为$p=\frac{3}{2}<2$，$\lim_{n \to \infty}\frac{u_n}{v_n} = 0$。由比较判别法的极限形式，可知级数$\sum_{n=1}^\infty \frac{\ln n}{n^2}$收敛。



2. 比值判别法

   设有正项级数，有$\lim_{n \to \infty}\frac{u_{n+1}}{u_n} = \rho$，则：

   （1）当$\rho < 1$时，$\sum_{n=1}^\infty u_n$收敛；

   （2）当$\rho > 1$时，$\sum_{n=1}^\infty u_n$发散；

   （3）当$\rho = 1$时，$\sum_{n=1}^\infty u_n$可能收敛也可能发散。



证明：

当$\rho < 1$时，取一个足够小的$\epsilon > 0$，使得$\rho + \epsilon < 1$，令$q = \rho + \epsilon$，由于$\lim_{n \to \infty}\frac{u_{n+1}}{u_n} = \rho$，根据极限的定义，对上面的$\epsilon > 0$，必存在$N$，当$n > N$时，恒有$|\frac{u_{n+1}}{u_n} - \rho| < \epsilon \Longleftrightarrow -\epsilon < \frac{u_{n+1}}{u_n} - \rho < \epsilon \Longleftrightarrow \rho - \epsilon < \frac{u_{n+1}}{u_n} < \rho + \epsilon = q$（其中$n > N$），取$n = N+1, N+2, \cdots$，$u_{N+1} < q u_N, u_{N+2} < q u_{N+1} < q^2 u_N, u_{N+3} < q u_{N+2} < q^3 u_N, \cdots$，表示级数$u_{N+1}, u_{N+2}, u_{N+3}, \cdots$的对应项小于几何级数$q u_N + q^2 u_N + q^3 u_N + \cdots$，因为$q < 1$所以级数$q u_N + q^2 u_N + q^3 u_N + \cdots$收敛，由比较判别法，可知$u_{N+1}, u_{N+2}, u_{N+3}, \cdots$收敛，由级数的性质，知$\sum_{n=1}^\infty u_n$收敛。

当$\rho > 1$时，取一个足够小的$\epsilon > 0$，使得$\rho - \epsilon > 1$，令$r = \rho - \epsilon > 1$。当$n > N$时，$r = \rho - \epsilon < \frac{u_{n+1}}{u_n} < \rho + \epsilon$，所以$\frac{u_{n+1}}{u_n} > r > 1$，即$u_{n+1}>u_n, (n > N)$，因此数列$\{u_n\}$单调增，从而$\lim_{n \to \infty} u_n \neq 0$，由级数收敛的必要条件，可知$\sum_{n=1}^\infty u_n$发散。

当$\rho = 1$时，通过举例证明。



例1：判别$\sum_{n=1}^\infty \frac{3n}{2^n}$的敛散性。

解：$u_n = \frac{3n}{2^n} > 0$，$\lim_{n \to \infty} \frac{\frac{3(n+1)}{2^{n+1}}}{\frac{3n}{2^n}} = \frac{1}{2}\lim_{n \to \infty}\frac{n+1}{n} = \frac{1}{2} < 1$，由比值判别法，可知$\sum_{n=1}^\infty \frac{3n}{2^n}$收敛。



例2：判别$\sum_{n=1}^\infty \frac{n!}{10^n}$敛散性。

解：$\frac{n!}{10^n} > 0$。$\lim_{n \to \infty}\frac{(n+1)!}{10^{n+1}} \cdot \frac{10^n}{n!} = \lim_{n \to \infty} \frac{n+1}{10} = +\infty$，根据比值判别法，知$\sum_{n=1}^\infty \frac{n!}{10^n}$发散。



例3：判别$\sum_{n=1}^\infty \frac{n^3[\sqrt{2}+(-1)^n]^n}{3^n}$的敛散性。

解：$u_n = \frac{n^3[\sqrt{2}+(-1)^n]^n}{3^n} > 0$。$\frac{u_{n+1}}{u_n} = \frac{(n+1)^3[\sqrt{2}+(-1)^{(n+1)}]^{(n+1)}}{3^{(n+1)}} \cdot \frac{3^n}{n^3[\sqrt{2}+(-1)^n]^n} \\ = \frac{1}{3}(\frac{n+1}{n})^3\frac{[\sqrt{2}+(-1)^{(n+1)}]^{(n+1)}}{[\sqrt{2}+(-1)^n]^n}$

当$n$取奇数时，原式等于$\frac{1}{3}(\frac{n+1}{n})^3(\frac{\sqrt{2}+1}{\sqrt{2}-1})^n(\sqrt{2}+1)$；

当$n$取偶数时$\frac{1}{3}(\frac{n+1}{n})^3(\frac{\sqrt{2}-1}{\sqrt{2}+1})^n(\sqrt{2}-1)$。

当$n$取奇数时，$\lim_{n \to \infty} \frac{u_{n+1}}{u_n} = \infty$，

当$n$取奇数时，$\lim_{n \to \infty} \frac{u_{n+1}}{u_n} = 0$，

因此$\lim_{n \to \infty} \frac{u_{n+1}}{u_n} = 0$不存在。



因为$u_n = \frac{n^3[\sqrt{2}+(-1)^n]^n}{3^n} \le \frac{n^3[\sqrt{2}+1]^n}{3^n}$，令$v_n = \frac{n^3[\sqrt{2}+1]^n}{3^n}$，$\lim_{n \to \infty}\frac{v_{n+1}}{v_n} = \frac{(n+1)^3[\sqrt{2}+1]^{(n+1)}}{3^{(n+1)}} \cdot \frac{3^n}{n^3[\sqrt{2}+1]^n} \\ = \lim_{n \to \infty}\frac{1}{3}(\frac{n+1}{n})^3(\sqrt{2}+1) = \frac{\sqrt{2}+1}{3} < 1$

由比值判别法，知$\sum_{n=1}^\infty v_n$收敛，再由比较判别法，知$\sum_{n=1}^\infty \frac{n^3[\sqrt{2}+(-1)^n]^n}{3^n}$收敛。



3. 根值判别法（柯西判别法）

   设有正项级数$\sum_{n=1}^\infty u_n$，有$\lim_{n \to \infty}\sqrt[n]{u_n} = \rho$，则：

   （1）当$\rho < 1$时，$\sum_{n=1}^\infty u_n$收敛；

   （2）当$\rho > 1$时，$\sum_{n=1}^\infty u_n$发散；

   （3）当$\rho = 1$时，$\sum_{n=1}^\infty u_n$可能收敛也可能发散。

   证：

   当$\rho < 1$时，取足够小的$\epsilon > 0$，使得$\rho + \epsilon = q < 1$。由极限定义，知对上面的$\epsilon$，一定存在$N$，当$n > N$时，恒有$|\sqrt[n]{u_n}-\rho| < \epsilon \Longleftrightarrow -\epsilon < \sqrt[n]{u_n}-\rho < \epsilon$，$\rho - \epsilon < \sqrt[n]{u_n} < \rho + \epsilon = q < 1$，由$\sqrt[n]{u_n} < q \Longrightarrow u_n < q^n$，几何级数$\sum_{n=1}^\infty q^n, (q < 1)$收敛，而$u_n < q^n$，由比较判别法，可知$\sum_{n=1}^\infty u_n$收敛。

   当$\rho > 1$时，取足够小的$\epsilon > 0$，使得$\rho - \epsilon > 1$，由$\sqrt[n]{u_n} > \rho - \epsilon > 1$，$u_n > 1$，于是$\lim_{n \to \infty}u_n \neq 0$，由级数收敛的必要条件，可知$\sum_{n=1}^\infty u_n$发散。

   当$\rho = 1$时，通过举例证明。



例1：判断$\sum_{n=1}^\infty \frac{3^n n^3}{4^n}$的敛散性。

解：$u_n = \frac{3^n n^3}{4^n} > 0$。$\sqrt[n]{u_n} = (\frac{3^n n^3}{4^n})^{\frac{1}{n}} = \frac{3}{4} \cdot n^{\frac{3}{n}}$，$\lim_{n \to \infty}\sqrt[n]{u_n} = \lim_{n \to \infty}\frac{3}{4} n^{\frac{3}{n}} = \frac{3}{4} < 1$，由根值判别法，可知$\sum_{n=1}^\infty \frac{3^n n^3}{4^n}$收敛。



例2：判别$\sum_{n=1}^\infty 2^{-n+(-1)^{n-1}}$的敛散性。

解$u_n = 2^{-n+(-1)^{n-1}} = \frac{1}{2^n} \cdot 2^{(-1)^{n-1}} > 0$ ，$\sqrt[n]{u_n} = (2^{-n+(-1)^{n-1}})^{\frac{1}{n}} = 2^{-1} \cdot 2^{\frac{(-1)^{n-1}}{n}}$，$\lim_{n \to \infty}\sqrt[n]{u_n} = \lim_{n \to \infty}2^{-1} \cdot 2^{\frac{(-1)^{n-1}}{n}} = \frac{1}{2} < 1$，所以$\sum_{n=1}^\infty 2^{-n+(-1)^{n-1}}$收敛。



4. 积分判别法

   设正项级数$\sum_{n=k}^\infty u_n$（$k$是正整数）同时$u_n = f(n)$，且$f(x)$在$[k, +\infty)$上是单调减少的连续函数，则$\sum_{n=k}^\infty u_n = \sum_{n=k}^\infty f(n)$与广义积分$\int_k^{+\infty} f(x)dx$具有相同的敛散性（==不予以证明==）。

   

例1：判别$\sum_{n=2}^\infty \frac{1}{n \ln n}$的敛散性。

解：$u_n = \frac{1}{n \ln n} > 0, (n \ge 2)$，取$f(x) = \frac{1}{x \ln x}, 2 \le x < +\infty$，$u_n = f(n) = \frac{1}{n \ln n}$。$f(x) = \frac{1}{x \ln x}$，分子是常数，而分母$x \ln x$随着$x$的增大而增大，其倒数$\frac{1}{x \ln x}$随着$x$的增大而减少，$f(x)$是单调减少的连续函数。$\int_2^{+\infty}f(x)dx = \lim_{b \to +\infty}\int_2^b \frac{1}{x \ln x}dx = \lim_{b \to +\infty} \ln (\ln x)|_2^b \\ = \lim_{b \to +\infty}[\ln(\ln b) - \ln(\ln 2)] = +\infty$

由$\int_2^{+\infty}f(x)dx$发散，可知$\sum_{n=2}^\infty \frac{1}{n \ln n}$发散。



例2：判别$\sum_{n=2}^\infty \frac{1}{n (\ln n)^2}$的敛散性。

解：$u_n = \frac{1}{n (\ln n)^2} > 0, (n \ge 2)$，取$f(x) = \frac{1}{x (\ln x)^2}, 2 \le x < +\infty$，容易判定$f(x)$在$2 \le x < +\infty$是单调减少的连续函数。$\int_2^{+\infty}\frac{1}{x (\ln x)^2}dx = \lim_{b \to +\infty}\int_2^b \frac{1}{(\ln x)^2}d(\ln x) = \lim_{b \to +\infty}(-\frac{1}{\ln x})|_2^b \\ = \lim_{b \to +\infty}[\frac{1}{\ln 2} - \frac{1}{\ln b}] = \frac{1}{\ln 2}$

由$\int_2^{+\infty}\frac{1}{x (\ln x)^2}dx$收敛，可知$\sum_{n=2}^\infty \frac{1}{n (\ln n)^2}$收敛。



### 四、任意项级数敛散性的判别法

==任意项级数==：级数中有无穷多个正项，也有无穷多个负项，也可能有等于零的项。

1. 交错级数：若$u_n > 0, (n = 1, 2, \cdots)$，则称$\sum_{n=1}^\infty (-1)^{n-1}u_n$为交错级数，即$u_1-u_2+u_3-u_4+\cdots+(-1)^{n-1}u_n+\cdots$正负号相间的级数。

==莱布尼茨定理==：如果交错级数$\sum_{n=1}^\infty (-1)^{n-1}u_n, (u_n > 0)$满足：

（1）$u_{n-1} > u_n, (n=2, 3, \cdots)$

（2）$\lim_{n \to \infty}u_n = 0$

则$\sum_{n=1}^\infty (-1)^{n-1}u_n, (u_n > 0)$收敛，其和$0 \le s \le u_1$。

证：考虑$\sum_{n=1}^\infty (-1)^{n-1}u_n = u_1 - u_2 + u_3 - u_4 + \cdots + (-1)^{n-1}u_n + \cdots$，部分和$S_{2n} = (u_1 - u_2) + (u_3 - u_4) + \cdots + (u_{2n-1} - u_{2n}) = \sum_{k=1}^n(u_{2k-1}-u_{2k})$，由条件（1）可知，$u_{2k-1}>u_{2k}, u_{2k-1}-u_{2k}>0$，所以$S_{2n} = \sum_{k=1}^n (u_{2k-1}-u_{2k}) \ge 0$且单调增加；另一方面，

$S_{2n} = u_1 - (u_2 - u_3) - (u_4-u_5) - \cdots - (u_{2n-2}-u_{2n-1}) - u_{2n} \\ = u_1 - [(u_2 - u_3) + (u_4-u_5) + \cdots + (u_{2n-2}-u_{2n-1}) + u_{2n}]$

由条件（1），$[(u_2 - u_3) + (u_4-u_5) + \cdots + (u_{2n-2}-u_{2n-1}) + u_{2n}] > 0$，所以$S_{2n}  \le u_1$，于是$S_{2n}$单调增加且有界，根据数列极限存在的单调有界准则，知$\lim_{n \to \infty}S_{2n} = S$。

另一方面：$S_{2n+1} = S_{2n}+u_{2n+1}$，由条件（2）知，$\lim_{n \to \infty}u_{2n+1} = 0$，$\lim_{n \to \infty}S_{2n+1} = \lim_{n \to \infty}S_{2n} + \lim_{n \to \infty}u_{2n+1} = S$，于是$\lim_{n \to +\infty}S_n = S$，且$0 \le S \le u_1$。

满足莱布尼茨定理的$\sum_{n=1}^\infty (-1)^{n-1}u_n$称为==莱布尼茨型的交错级数==。



==推论==：对莱布尼茨型交错级数$\sum_{n=1}^\infty (-1)^{n-1}u_n$的余项$|r_n| \le u_{n+1}$。

证：由$r_n = (-1)^n u_{n+1} + (-1)^{n+1}u_{n+2} + \cdots = (-1)^n[u_{n+1}-u_{n+2}+u_{n+3}-\cdots]$，$|r_n| = u_{n+1}-u_{n+2}+u_{n+3}-\cdots \le u_{n+1}$。



例1：判别$\sum_{n=1}^\infty (-1)^{n-1}\frac{1}{n}$的敛散性，估计余项$|r_n|$。

解：$u_n = \frac{1}{n} > 0$满足：

（1）$u_n = \frac{1}{n} < \frac{1}{n-1} = u_{n-1}, (n=2,3\cdots)$；

（2）$\lim_{n \to \infty} u_n = \lim_{n \to \infty}\frac{1}{n} = 0$

由莱布尼茨定理，可知$\sum_{n=1}^\infty (-1)^{n-1}\frac{1}{n}$收敛，且$|r_n| \le u_{n+1} = \frac{1}{n+1}$。



例2：判别$\sum_{n=2}^\infty (-1)^{n-1} \frac{\ln n}{n}$的敛散性。

解：$u_n = \frac{\ln n}{n} > 0$。令$f(x) = \frac{\ln x}{x}, 2 \le x < +\infty$， $f^\prime(x) = (\frac{\ln x}{x})^\prime = \frac{\frac{1}{x} \cdot x - \ln x}{x^2} = \frac{1-\ln x}{x^2}, (2 \le x < +\infty)$，当$x \ge 3$时，$1 - \ln x < 0$，$f^\prime(x) = \frac{1-\ln x}{x^2}<0$，所以$f(x)$在$[3, +\infty)$上单调减少，从而有$u_n = \frac{\ln n}{n} < u_{n-1} = \frac{\ln(n-1)}{n-1}$。$\lim_{x \to +\infty}f(x) = \lim_{x \to +\infty}\frac{\ln x}{x} = \lim_{x \to +\infty}\frac{1}{x} = 0$，即$\lim_{n \to \infty}f(n) = \lim_{n \to \infty}\frac{\ln n}{n} = 0$，即$\lim_{n \to \infty}u_n = 0$，所以$\sum_{n=2}^\infty (-1)^{n-1} \frac{\ln n}{n}$收敛。



2. 绝对收敛、条件收敛

   设$\sum_{n=1}^\infty u_n$是任意项级数，而$\sum_{n=1}^\infty |u_n|$是正项级数。这两个级数的敛散性有以下关系：

   ==定理==：如果$\sum_{n=1}^\infty |u_n|$收敛，则任意项级数$\sum_{n=1}^\infty u_n$也收敛。

   证：
   $$
   |u_n| = \left\{\begin{array}{cc}u_n, &u_n \ge 0 \\ -u_n, &u_n < 0\end{array}\right. \\ |u_n| + u_n = \left\{\begin{array}{cc}2u_n, &u_n \ge 0 \\ 0, &u_n < 0\end{array}\right.
   $$
   所以$|u_n|+u_n \ge 0$总成立。

   令$v_n = \frac{1}{2}(|u_n|+u_n) \ge 0$，$\sum_{n=1}^\infty v_n$是正项级数，$v_n = \frac{1}{2}(|u_n|+u_n) \le \frac{1}{2}(|u_n|+|u_n|) = |u_n|$，因为$\sum_{n=1}^\infty |u_n|$收敛，根据比较判别法，可知$\sum_{n=1}^\infty v_n$收敛。由$v_n = \frac{1}{2}(|u_n|+u_n) \Longrightarrow 2v_n = |u_n|+u_n \Longrightarrow u_n = 2v_n - |u_n|$，$\sum_{n=1}^\infty u_n = \sum_{n=1}^\infty(2v_n - |u_n|)$，而$\sum_{n=1}^\infty 2v_n, \sum_{n=1}^\infty |u_n|$都收敛，而$\sum_{n=1}^\infty u_n$是由收敛级数$\sum_{n=1}^\infty 2v_n, \sum_{n=1}^\infty |u_n|$逐项相减得到。由级数的性质可知$\sum_{n=1}^\infty(2v_n - |u_n|)$收敛，即$\sum_{n=1}^\infty u_n$收敛。

   ==绝对收敛==：若$\sum_{n=1}^\infty |u_n|$收敛，则称$\sum_{n=1}^\infty u_n$绝对收敛；

   ==条件收敛==：若$\sum_{n=1}^\infty |u_n|$发散，而$\sum_{n=1}^\infty u_n$收敛，则称$\sum_{n=1}^\infty u_n$条件收敛。



​	例1：判断以下级数的敛散性。若级数收敛，指出是绝对收敛还是条件收敛？

（1）$\sum_{n=1}^\infty (-1)^{n-1}\frac{1}{n \cdot 2^n}$；（2）$\sum_{n=1}^\infty (-1)^{n-1}\frac{1}{\sqrt{n}}$；（3）$\sum_{n=1}^\infty (-1)^{n-1}\frac{2^n}{2n+1}$；（4）$\sum_{n=1}^\infty \frac{\sin n\alpha}{n^4}$。

解：

（1）$u_n = (-1)^{n-1}\frac{1}{n \cdot 2^n}, |u_n| = \frac{1}{n \cdot 2^n}$，$\lim_{n \to \infty}\frac{|u_{n+1}|}{|u_n|} = \lim_{n \to \infty}\frac{1}{(n+1) \cdot 2^{(n+1)}} \cdot n \cdot 2^n = \lim_{n \to \infty}\frac{1}{2}\frac{n}{n+1} = \frac{1}{2} < 1$，由比值判别法，可知$\sum_{n=1}^\infty (-1)^{n-1}\frac{1}{n \cdot 2^n}$绝对收敛。

（2）$u_n = (-1)^{n-1}\frac{1}{\sqrt{n}}, |u_n| = \frac{1}{\sqrt{n}}$，$\sum_{n=1}^\infty |u_n| = \sum_{n=1}^\infty\frac{1}{\sqrt{n}} = \sum_{n=1}^\infty\frac{1}{n^{\frac{1}{2}}}$是p-级数，$p=\frac{1}{2} < 1$，所以级数$\sum_{n=1}^\infty |u_n| = \sum_{n=1}^\infty\frac{1}{\sqrt{n}}$发散。因为$\frac{1}{\sqrt{n}} < \frac{1}{\sqrt{n-1}}, \lim_{n \to \infty}\frac{1}{\sqrt{n}} = 0$，则级数$\sum_{n=1}^\infty (-1)^{n-1}\frac{1}{\sqrt{n}}$满足莱布尼茨定理，可知$\sum_{n=1}^\infty (-1)^{n-1}\frac{1}{\sqrt{n}}$收敛，从而它是条件收敛。

（3）$u_n = (-1)^{n-1}\frac{2^n}{2n+1}, |u_n| = \frac{2^n}{2n+1}$，设$x$为连续变量，$f(x) = \frac{2^x}{2x+1}, f(n) = \frac{2^n}{2n+1} = |u_n|$，$\lim_{x \to +\infty}f(x) = \lim_{x \to +\infty}\frac{2^x}{2x+1} = \lim_{x \to +\infty}\frac{2^x\ln 2}{2} = +\infty$，则$\lim_{n \to +\infty}f(n) = \lim_{x \to +\infty}f(x) = +\infty, \lim_{n \to \infty}|u_n| = +\infty$。因为$\lim_{n \to \infty}|u_n| \neq 0, \lim_{n \to \infty}u_n \neq 0$，所以$\sum_{n=1}^\infty (-1)^{n-1}\frac{2^n}{2n+1}$发散。

（4）$u_n = \frac{\sin n\alpha}{n^4}, |u_n| = \frac{|\sin n\alpha|}{n^4} \le \frac{1}{n^4}$，$\sum_{n=1}^\infty\frac{1}{n^4}$是p-级数，由$p=4>1$，知$\sum_{n=1}^\infty\frac{1}{n^4}$收敛，从而$\sum_{n=1}^\infty \frac{\sin n\alpha}{n^4}$绝对收敛。



​	==绝对收敛级数的两个性质==：

（1）绝对收敛级数的各项可以任意重排（位置），而不改变它的绝对收敛性，也不改变级数的和。

==柯西乘积==：$(\sum_{n=1}^\infty u_n) \cdot (\sum_{n=1}^\infty v_n) = u_1v_1 + (u_1v_2+u_2v_1) + (u_1v_3+u_2v_2+u_3v_1)+(u_1v_n+u_2v_{n-1}+\cdots+u_nv_1)+\cdots$，也为级数。

（2）设$\sum_{n=1}^\infty u_n, \sum_{n=1}^\infty v_n$都绝对收敛，其和分别为$s, \sigma$，则它们的==柯西乘积==也收敛，且和为$s \cdot \sigma$。



## 第2节 幂级数

==函数项级数==：设有定义在区间$I$上的函数列：$u_1(x), u_2(x), \cdots, u_n(x), \cdots$，则称数学表达式$\sum_{n=1}^\infty u_n(x) = u_1(x) + u_2(x) + \cdots + u_n(x) + \cdots$为定义在区间$I$上的函数项级数。$\forall_{x_0} \in I$，则$\sum_{n=1}^\infty u_n(x_0)$是数项级数。如果$\sum_{n=1}^\infty u_n(x_0)$收敛，则称$x_0$为$\sum_{n=1}^\infty u_n(x)$的一个收敛点。若$\sum_{n=1}^\infty u_n(x_0)$发散，则称$x_0$为$\sum_{n=1}^\infty u_n(x)$的一个发散点。

==收敛域==：$\sum_{n=1}^\infty u_n(x)$的全体收敛点所构成的数集，称为$\sum_{n=1}^\infty u_n(x)$的收敛域。

==发散域==：$\sum_{n=1}^\infty u_n(x)$的全体发散点所构成的数集，称为$\sum_{n=1}^\infty u_n(x)$的发散域。

设$\sum_{n=1}^\infty u_n(x)$的收敛域为$J$，$x_0 \in J$，$\sum_{n=1}^\infty u_n(x_0)$收敛于$s$，$\forall_x \in J$，$\sum_{n=1}^\infty u_n(x)$收敛于$s(x)$，则称$s(x)$为$\sum_{n=1}^\infty u_n(x)$的和函数，$s(x)$的定义域为$J$，称$S_n(x) = u_1(x)+u_2(x)+\cdots+u_n(x)$为$\sum_{n=1}^\infty u_n(x)$的部分和。

显然有：$\lim_{n \to +\infty}s_n(x) = s(x)$，余项$r_n(x) = s(x) - s_n(x)$，$\lim_{n \to \infty}r_n(x) = s(x) - \lim_{n \to \infty}s_n(x) = 0$。



### 一、幂级数及其收敛域

形如：$a_0+a_1x+a_2x^2+\cdots+a_nx^n+\cdots$（其中$a_0,a_1,a_2,\cdots,a_n,\cdots$都是常数），称为$x$的幂级数，记为$\sum_{n=0}^\infty a_n x^n$。

更一般的形式：$a_0+a_1(x-x_0)+a_2(x-x_0)^2+\cdots+a_n(x-x_0)^n+\cdots$称为$(x-x_0)$的幂级数，记为$\sum_{n=0}^\infty a_n(x-x_0)^n$。令$x - x_0 = t$，则$\sum_{n=0}^\infty a_n(x-x_0)^n = \sum_{n=0}^\infty a_n t^n$。



考察$x$的幂级数：$1+x+x^2+\cdots+x^n+\cdots$是几何级数，当$|x| < 1$时，$\sum_{n=0}^\infty x^n$是收敛的，当$|x| \ge 1$时，$\sum_{n=0}^\infty x^n$发散，$\sum_{n=0}^\infty x^n$的收敛域为$(-1, 1)$，其和函数$\sum_{n=0}^\infty x^n = \frac{1}{1-x}$。



==阿贝尔定理==：如果$\sum_{n=0}^\infty a_n x^n$在点$x=x_0, (x_0 \neq 0)$收敛，则凡是适合不等式$|x|<|x_0|$的一切$x$都使得$\sum_{n=0}^\infty a_n x^n$绝对收敛，反之若点$x=x_0$使$\sum_{n=0}^\infty a_n x^n$发散，则适合不等式$|x|>|x_0|$的一切$x$都使$\sum_{n=0}^\infty a_n x^n$发散。

证：

==先证明第一部分==：设$x = x_0, (x_0 \neq 0)$，使$\sum_{n=0}^\infty a_n x^n$收敛，即级数$a_0+a_1x_0+a_2x_0^2+\cdots+a_nx_0^n+\cdots$收敛，由级数收敛的必要条件，$\lim_{n \to \infty}a_n x_0^n = 0$，即数列$\{a_n x_0^n\}$在当$n \to \infty$，有$a_n x_0^n \to 0$，极限存在的数列一定是有界的，即存在$M > 0$，使得$|a_nx_0^n| \le M, (n=0,1,2,\cdots)$。

$|a_n x^n| = |a_n x_0^n \cdot \frac{x^n}{x_0^n}| = |a_n x_0^n| \cdot |\frac{x}{x_0}|^n \le M \cdot |\frac{x}{x_0}|^n$，由条件$|x| < |x_0| \Longrightarrow |\frac{x}{x_0}| < 1$，因此几何级数$\sum_{n=0}^\infty M |\frac{x}{x_0}|^n$收敛，再由$|a_n x^n| < M \cdot |\frac{x}{x_0}|^n$，根据比较判别法，可知$\sum_{n=0}^\infty|a_n x^n|$收敛，故$\sum_{n=0}^\infty a_n x^n$是绝对收敛的。

==再证明第二部分==：假若点$x=x_0$使$\sum_{n=0}^\infty a_n x^n$发散，使用反证法：如果由$x_1$满足$|x_1|>|x_0|$，使得$\sum_{n=0}^\infty a_n x^n$收敛，根据定理的前半部分结论，应有$x_0$是$\sum_{n=0}^\infty a_n x^n$的收敛点，这与假设矛盾。



由阿贝尔定理可知：$x = x_0 \neq 0$，使$\sum_{n=0}^\infty a_n x^n$收敛，则对于$(-|x_0|, |x_0|)$内的一切$x$都使$\sum_{n=0}^\infty a_n x^n$绝对收敛；如果$x = x_0 \neq 0$，使$\sum_{n=0}^\infty a_n x^n$发散，则在$(-|x_0|, |x_0|)$以外的任何值都使$\sum_{n=0}^\infty a_n x^n$发散。



推论：如果$\sum_{n=0}^\infty a_n x^n$不仅在原点处收敛，也不是在整个数轴上收敛，则必存在一个数$R > 0$，具有以下性质：

（1）当$|x| < R$时，使$\sum_{n=0}^\infty a_n x^n$==绝对收敛==；

（2）当$|x| > R$时，使$\sum_{n=0}^\infty a_n x^n$发散；

（3）当$x=\pm R$时，$\sum_{n=0}^\infty a_n R^n, \sum_{n=0}^\infty a_n (-R)^n$可能收敛也可能发散。

则称$R$为幂级数$\sum_{n=0}^\infty a_n x^n$的收敛半径，$(-R, R)$为$\sum_{n=0}^\infty a_n x^n$的收敛区间。考虑$\sum_{n=0}^\infty a_n R^n, \sum_{n=0}^\infty a_n (-R)^n$的敛散性可以得收敛域：$(-R, R), (-R, R], [-R, R), [-R, R]$。

如果$\sum_{n=0}^\infty a_n x^n$只在$x=0$一点收敛，规定收敛半径$R=0$，收敛域只有一点$x=0$。

如果$\sum_{n=0}^\infty a_n x^n$对一切$x$都收敛，规定$R=+\infty$，收敛域为$(-\infty, +\infty)$。

对$\sum_{n=0}^\infty a_n(x-x_0)^n$。令$x - x_0 = t$，则$\sum_{n=0}^\infty a_n(x-x_0)^n = \sum_{n=0}^\infty a_n t^n$。如果$\sum_{n=0}^\infty a_n t^n$的收敛半径为$R > 0$，由$|t| = |x-x_0| < R$，可知收敛区间为$(x_0-R, x_0+R)$。



==收敛半径的求法==：

==定理==：在$\sum_{n=0}^\infty a_n x^n$中，若$\lim_{n \to \infty}|\frac{a_{n+1}}{a_n}| = \rho$，则$\sum_{n=0}^\infty a_n x^n$的收敛半径$R$为：

（1）当$\rho \neq 0$时，$R = \frac{1}{\rho}$；

（2）当$\rho = 0$时，$R = +\infty$；

（3）当$\rho = +\infty$时，$R = 0$。

证：由$\sum_{n=0}^\infty a_n x^n$各项取绝对值，得级数$|a_0|+|a_1x|+|a_2x^2|+\cdots+|a_nx^n|+\cdots$，有$\lim_{n \to \infty}\frac{|a_{n+1}x^{n+1}|}{|a_n x^n|} = \lim_{n \to \infty}|\frac{a_{n+1}}{a_n}| \cdot |x|$，

（1）如果$\lim_{n \to \infty}|\frac{a_{n+1}}{a_n}| = \rho, (\rho \neq 0)$，由比值判别法，当$\rho |x| < 1$时，即$|x| < \frac{1}{\rho}$时，级数$\sum_{n=0}^\infty |a_n x^n|$收敛，从而$\sum_{n=0}^\infty a_n x^n$绝对收敛。当$\rho |x| > 1$时，即$|x| > \frac{1}{\rho}$时，由比值判别法，知$\sum_{n=0}^\infty |a_n x^n|$发散，由$\lim_{n \to \infty}\frac{|a_{n+1}x^{n+1}|}{|a_n x^n|} = \lim_{n \to \infty}|\frac{a_{n+1}}{a_n}| \cdot |x| = \rho |x| > 1$，则一定存在$N$，当$n > N$时，有$\frac{|a_{n+1}x^{n+1}|}{|a_n x^n|} > 1$，即$|a_{n+1}x^{n+1}| > |a_n x^n|$，当$n \to +\infty$时，$\lim_{n \to \infty}|a_n x^n| \neq 0 \Longrightarrow \lim_{n \to \infty}a_n x^n \neq 0$，所以当$|x| > \frac{1}{\rho}$时，$\sum_{n=0}^\infty a_n x^n$发散，于是得到$\sum_{n=0}^\infty a_n x^n$的收敛半径$R = \frac{1}{\rho}$。

（2）如果$\lim_{n \to \infty}|\frac{a_{n+1}}{a_n}| = \rho = 0$，$\lim_{n \to \infty}\frac{|a_{n+1}x^{n+1}|}{|a_n x^n|} = \lim_{n \to \infty}|\frac{a_{n+1}}{a_n}| \cdot |x| = 0 < 1$，由比值判别法，可知对于任何$x$，$\sum_{n=0}^\infty a_n x^n$绝对收敛，因此收敛半径$R = +\infty$。

（3）如果$\lim_{n \to \infty}|\frac{a_{n+1}}{a_n}| = +\infty$，除了$x = 0$外，其他一切$x \neq 0$，都有$\lim_{n \to \infty}\frac{|a_{n+1}x^{n+1}|}{|a_n x^n|} = \lim_{n \to \infty}|\frac{a_{n+1}}{a_n}| \cdot |x| = +\infty$，因而存在$N$，使得当$n > N$时，必有$\frac{|a_{n+1}x^{n+1}|}{|a_n x^n|} > 1$，即$|a_{n+1}x^{n+1}| > |a_n x^n|$，当$n \to +\infty$时，$\lim_{n \to \infty}|a_n x^n| \neq 0 \Longrightarrow \lim_{n \to \infty}a_n x^n \neq 0$，所以$\sum_{n=0}^\infty a_n x^n$发散。因此$\sum_{n=0}^\infty a_n x^n$收敛域只有$x=0$一点，从而收敛半径$R=0$。



例1：求$\sum_{n=1}^\infty (-1)^{n-1}\frac{1}{n}x^n$的收敛半径$R$和收敛域。

解：$\lim_{n \to \infty}|\frac{a_{n+1}}{a_n}| = \lim_{n \to \infty}\frac{\frac{1}{n+1}}{\frac{1}{n}} = \lim_{n \to \infty}\frac{n}{n+1} = 1$，收敛半径$R = \frac{1}{\rho} = 1$，收敛区间为$(-R, R) = (-1, 1)$。

当$x=-1$时，得$\sum_{n=1}^\infty (-1)^{n-1}\frac{1}{n}(-1)^n = \sum_{n=1}^\infty (-1)^{2n-1}\frac{1}{n} = -\sum_{n=1}^\infty \frac{1}{n}$，调和级数$\sum_{n=1}^\infty \frac{1}{n}$发散，因而$\sum_{n=1}^\infty (-1)^{n-1}\frac{1}{n}(-1)^n$发散。

当$x=1$时，得$\sum_{n=1}^\infty (-1)^{n-1}\frac{1}{n} = \sum_{n=1}^\infty (-1)^{n-1}\frac{1}{n}$，级数$\sum_{n=1}^\infty (-1)^{n-1}\frac{1}{n}$是莱布尼茨型交错级数，从而$\sum_{n=1}^\infty (-1)^{n-1}\frac{1}{n}$收敛。

综上，$\sum_{n=1}^\infty (-1)^{n-1}\frac{1}{n}x^n$的收敛域为$(-1, 1]$。



例2：求$\sum_{n=0}^\infty \frac{1}{n!}x^n$的收敛半径$R$和收敛域。

解：$a_n = \frac{1}{n!}$，$\lim_{n \to \infty}|\frac{a_{n+1}}{a_n}| = \lim_{n \to \infty}\frac{\frac{1}{(n+1)!}}{\frac{1}{n!}} = \lim_{n \to \infty}\frac{1}{n+1} = 0$，原级数$\sum_{n=0}^\infty \frac{1}{n!}x^n$的收敛半径$R=+\infty$，收敛域为$(-\infty, +\infty)$。



例3：求$\sum_{n=0}^\infty n!x^n$的收敛半径和收敛域。

解：$a_n = n!, \lim_{n \to \infty}|\frac{a_{n+1}}{a_n}| = \lim_{n \to \infty}\frac{(n+1)!}{n!} = \lim_{n \to \infty}(n+1) = +\infty$，原级数的收敛半径$R = 0$，收敛域为$x=0$一点。



例4：求$\sum_{n=0}^\infty 3^{n+1}x^{2n+1}$的收敛半径和收敛域。

解：分析：原级数对比幂级数缺无穷多项，采用比值判别法确定。

通项$u_n(x) = 3^{n+1}x^{2n+1}$，$\lim_{n \to \infty}\frac{|u_{n+1}(x)|}{|u_n(x)|} = \lim_{n \to \infty}\frac{|3^{n+2}x^{2n+3}|}{|3^{n+1}x^{2n+1}|} = \lim_{n \to \infty}3|x|^2 = 3|x|^2$，当$3|x|^2 < 1$时，即$|x| < \frac{\sqrt{3}}{3}$时，原级数$\sum_{n=0}^\infty 3^{n+1}x^{2n+1}$绝对收敛。当$3|x|^2 > 1$时，即$|x| > \frac{\sqrt{3}}{3}$时，原级数$\sum_{n=0}^\infty 3^{n+1}x^{2n+1}$发散。由此可见，$\sum_{n=0}^\infty 3^{n+1}x^{2n+1}$的收敛半径$R = \frac{\sqrt{3}}{3}$，收敛区间为$(-\frac{\sqrt{3}}{3}, \frac{\sqrt{3}}{3})$。

当$x = -\frac{\sqrt{3}}{3}$时，得$\sum_{n=0}^\infty 3^{n+1}(-\frac{\sqrt{3}}{3})^{2n+1} = -\sum_{n=0}^\infty \sqrt{3}$，$\lim_{n \to \infty}\sqrt{3} = \sqrt{3} \neq 0$，故原级数发散。

当$x = \frac{\sqrt{3}}{3}$时，得$\sum_{n=0}^\infty 3^{n+1}(\frac{\sqrt{3}}{3})^{2n+1} = \sum_{n=0}^\infty \sqrt{3}$，$\lim_{n \to \infty}\sqrt{3} = \sqrt{3} \neq 0$，故原级数发散。

综上，原级数的收敛域为$(-\frac{\sqrt{3}}{3}, \frac{\sqrt{3}}{3})$。



例5：求$\sum_{n=1}^\infty \frac{1}{n \cdot 2^n}(x+1)^n$的收敛半径和收敛域。

解：令$x+1=t$，$\sum_{n=1}^\infty \frac{1}{n \cdot 2^n}t^n$，$a_n = \frac{1}{n \cdot 2^n}$，$\lim_{n \to \infty}|\frac{a_{n+1}}{a_n}| = \lim_{n \to \infty}|\frac{\frac{1}{(n+1) \cdot 2^{n+1}}}{\frac{1}{n \cdot 2^n}}| = \lim_{n \to \infty}\frac{1}{2} \cdot \frac{n}{n+1} = \frac{1}{2}$，则收敛半径$R = 2$，收敛区间为$(-2, 2)$。

当$t = -2$时，得$\sum_{n=1}^\infty \frac{1}{n \cdot 2^n}(-2)^n = \sum_{n=1}^\infty (-1)^n\frac{1}{n}$是莱布尼兹型的交错级数，$\sum_{n=1}^\infty (-1)^n\frac{1}{n}$收敛。

当$t = 2$时，得$\sum_{n=1}^\infty \frac{1}{n \cdot 2^n}2^n = \sum_{n=1}^\infty \frac{1}{n}$是调和级数，$\sum_{n=1}^\infty \frac{1}{n}$发散。

综上，$\sum_{n=1}^\infty \frac{1}{n \cdot 2^n}t^n$的收敛域为$[-2, 2)$，而$\sum_{n=1}^\infty \frac{1}{n \cdot 2^n}(x+1)^n$的收敛域为$-2 \le x+1 < 2 \Longleftrightarrow -3 \le x < 1$，即$[-3, 1)$。



### 二、幂级数的性质

1. 设$\sum_{n=0}^\infty a_n x^n$的收敛区间为$(-R_1, R_1), (R_1 > 0)$，其和函数为$f(x)$；$\sum_{n=0}^\infty b_n x^n$的收敛域为$(-R_2, R_2), (R_2 > 0)$，其和函数为$g(x)$，取$R = \min\{R_1, R_2\}$，则$\sum_{n=0}^\infty a_n x^n, \sum_{n=0}^\infty b_n x^n$在$(-R, R)$内绝对收敛。

   ==四则运算性质==：

   （1）加减法

   $(\sum_{n=0}^\infty a_n x^n) \pm (\sum_{n=0}^\infty b_n x^n) = \sum_{n=0}^\infty (a_n \pm b_n)x^n = f(x) \pm g(x)$

   （2）柯西乘法

   $(\sum_{n=0}^\infty a_n x^n) \cdot (\sum_{n=0}^\infty b_n x^n) = \sum_{n=0}^\infty (a_0b_n+a_1b_{n-1}+\cdots+a_nb_0)x^n = f(x) \cdot g(x)$

   （3）除法：假设$b_0 \neq 0$，
   $$
   \frac{f(x)}{g(x)} = \frac{\sum_{n=0}^\infty a_n x^n}{\sum_{n=0}^\infty b_n x^n} = c_0+c_1x+c_2x^2+\cdots+c_nx^n+\cdots
   $$

   $$
   \sum_{n=0}^\infty a_n x^n = (\sum_{n=0}^\infty b_n x^n) \cdot (\sum_{n=0}^\infty c_n x^n) = \sum_{n=0}^\infty (b_0c_n+b_1c_{n-1}+\cdots+b_nc_0)x^n
   $$

   比较等式两边$x$同次幂的系数应该相等：
   $$
   \left\{\begin{array}{ccc}a_0 &= &b_0 c_0 \\ a_1 &= &b_0c_1 + b_1c_0 \\ a_2 &= &b_0c_2+b_1c_1+b_2c_0 \\ \cdots\cdots\cdots\end{array}\right.
   $$
   依顺序，可解出$c_0, c_1, \cdots, c_n, \cdots$。其收敛区间比$(-R, R)$要==小得多==。

   

   ==幂级数的分析运算性质==：

   （1）如果$\sum_{n=0}^\infty a_n x^n = s(x), x \in (-R, R)$，则$s(x)$在$(-R, R)$内是连续函数。如果$\sum_{n=0}^\infty a_n x^n$在$x=R$处也收敛，则$s(x)$在$x=R$点处左连续，如果$\sum_{n=0}^\infty a_n x^n$在$x=-R$处也收敛，则$s(x)$在$x=-R$点处右连续。

   （2）如果$\sum_{n=0}^\infty a_n x^n = s(x), x \in (-R, R)$，则$s(x)$在$(-R, R)$内可导，且有==逐项求导==公式：
   $$
   s^\prime(x) = (\sum_{n=0}^\infty a_n x^n)^\prime = \sum_{n=0}^\infty (a_n x^n)^\prime = \sum_{n=1}^\infty na_n x^{n-1}, \quad x \in (-R, R)
   $$
   反复使用上面公式，可知$\sum_{n=0}^\infty a_n x^n$在$(-R, R)$内和函数有任意阶导数，且
   $$
   s^{(k)}(x) = \sum_{n=k}^\infty a_n n(n-1) \cdots (n-k+1) x^{n-k}, \quad x \in (-R, R)
   $$
   （3）如果$\sum_{n=0}^\infty a_n x^n = s(x), x \in (-R, R)$，则$s(x)$在$(-R, R)$内可积，且有==逐项积分==公式：
   $$
   \int_0^x s(x)dx = \int_0^x(\sum_{n=0}^\infty a_n x^n)dx = \sum_{n=0}^\infty \int_0^x (a_n x^n)dx = \sum_{n=0}^\infty \frac{a_n}{n+1} x^{n+1}, \quad x \in (-R, R)
   $$



例1：求两个幂级数：

$\sum_{n=1}^\infty (-1)^{n-1}x^{n-1} = 1-x+x^2-x^3+\cdots+(-1)^{n-1}x^{n-1}+\cdots$，

$\sum_{n=1}^\infty \frac{(-1)^{n-1}}{n}x^{n} = x-\frac{x^2}{2}+\frac{x^3}{3}-\cdots+\frac{(-1)^{n-1}}{n}x^{n}+\cdots$

的和。

解：$\sum_{n=1}^\infty (-1)^{n-1}x^{n-1} = 1 + \sum_{n=1}^\infty (-1)^{n}x^{n}$，$\sum_{n=1}^\infty (-1)^{n-1}x^{n-1} + \sum_{n=1}^\infty \frac{(-1)^{n-1}}{n}x^{n} = 1 + \sum_{n=1}^\infty (-1)^{n}x^{n} + \sum_{n=1}^\infty \frac{(-1)^{n-1}}{n}x^{n} \\ = 1 + \sum_{n=1}^\infty [(-1)^{n}+\frac{(-1)^{n-1}}{n}]x^n = 1 + \sum_{n=1}^\infty (-1)^{n}[1-\frac{1}{n}]x^n \\ = 1+\sum_{n=1}^\infty (-1)^{n}[\frac{n-1}{n}]x^n$



例2：已知$\sum_{n=0}^\infty (-1)^n x^n = 1-x+x^2-x^3+\cdots+(-1)^nx^n = \frac{1}{1+x}$，收敛区间为$(-1, 1)$，

逐项求导数：$(\frac{1}{1+x})^\prime = (\sum_{n=0}^\infty (-1)^n x^n)^\prime = \sum_{n=1}^\infty (-1)^n n x^{n-1}$，即$-\frac{1}{(1+x)^2} = \sum_{n=1}^\infty (-1)^n n x^{n-1}, x \in (-1, 1)$。

逐项求积分：$\int_0^x \frac{1}{1+x}dx = \sum_{n=0}^\infty \int_0^x (-1)^n x^n dx = \sum_{n=0}^\infty (-1)^n \frac{1}{n+1}x^{n+1}$，即$\ln(1+x)|_0^x = \ln(1+x) = \sum_{n=0}^\infty (-1)^n \frac{1}{n+1}x^{n+1}, x \in (-1, 1)$。

当$x=1$时，$\sum_{n=0}^\infty (-1)^n \frac{1}{n+1}$收敛，$\lim_{x \to 1^-}\ln(1+x) = \ln 2$，上面级数$\ln(1+x) = \sum_{n=0}^\infty (-1)^n \frac{1}{n+1}x^{n+1}, x \in (-1, 1]$。



$\sum_{n = 0}^\infty a_n (x - x_0)^n$在逐项求积分时， 积分的下限取在$x_0$处，即$\sum_{n = 0}^\infty a_n \int_{x_0}^x(x - x_0)^n dx$



## 第3节 函数的幂级数展开

### 一、泰勒级数

函数在$x_0$点可以展开成幂级数——即对于$f(x)$，若存在邻域$N(x_0, \delta)$及幂级数$\sum_{n=0}^\infty a_n (x-x_0)^n$，使得$f(x) = \sum_{n=0}^\infty a_n (x-x_0)^n, x \in N(x_0, \delta)$。



==定理==：设$f(x)$在$x_0$点可以展开为幂级数$\sum_{n=0}^\infty a_n (x-x_0)^n$，则$f(x)$在邻域$N(x_0, \delta)$内有任意阶导数，且$a_n = \frac{f^{(n)}(x_0)}{n!}, (n=0,1,2,\cdots)$。

证：由定理的假设，有$f(x) = \sum_{n=0}^\infty a_n (x-x_0)^n = a_0+a_1(x-x_0)+a_2(x-x_0)^2+\cdots+a_n(x-x_0)^n+\cdots$

根据幂级数的性质，在收敛区间内可以逐项求导，有$f^\prime(x)=a_1+2a_2(x-x_0)+3a_3(x-x_0)^2+\cdots+na_n(x-x_0)^{n-1}+\cdots$，

$f^{\prime\prime}(x) = 2a_2+3\cdot2 a_3(x-x_0)+\cdots+n(n-1)a_n(x-x_0)^{n-2}+\cdots$，

$\cdots\cdots$

$f^{(n)}(x) = n!a_n+(n+1)n(n-1)\cdots2a_{n+1}(x-x_0)+\cdots$

$\cdots\cdots$



$f(x_0) = a_0$

$f^\prime(x_0) = a_1$

$f^{\prime\prime}(x_0) = 2!a_2$

$\cdots\cdots$

$f^{(n)}(x_0) = n!a_n$

等式两端除以阶乘项，有$a_n = \frac{f^{(n)}(x_0)}{n!}, (n=0,1,2,\cdots)$。



由定理1可知，若$f(x)$在$x_0$点可以展开为$(x-x_0)$的幂级数，这个幂级数是唯一的，就是$f(x) = \sum_{n=0}^\infty a_n(x-x_0)^n = \sum_{n=0}^\infty \frac{f^{(n)}(x_0)}{n!}(x-x_0)^n$

称级数$\sum_{n=0}^\infty \frac{f^{(n)}(x_0)}{n!}(x-x_0)^n$为函数$f(x)$在$x_0$点处的泰勒级数，$a_n = \frac{f^{(n)}(x_0)}{n!}$称为泰勒系数。特别地，当$x_0 = 0$时，$a_n = \frac{f^{(n)}(0)}{n!}, (n=0,1,2,3,\cdots)$，$\sum_{n=0}^\infty \frac{f^{(n)}(0)}{n!}x^n$称为$f(x)$的麦克劳林级数。



反过来，设$f(x)$在$N(x_0, \delta)$内具有任意阶导数$f^\prime(x), f^{\prime\prime}(x), \cdots, f^{(n)}(x), \cdots$都存在，写出泰勒系数$a_n = \frac{f^{(n)}(x_0)}{n!},(n=0,1,2,\cdots)$，再写出泰勒级数：

$f(x_0)+f^\prime(x_0)(x-x_0)+\frac{f^{\prime\prime}(x_0)}{2!}(x-x_0)^2+\cdots+\frac{f^{(n)}(x_0)}{n!}(x-x_0)^n+\cdots$

（1）除$x=x_0$点外，这个泰勒级数是否收敛？

（2）如果在$N(x_0, \delta)$内，泰勒级数$\sum_{n=0}^\infty \frac{f^{(n)}(x_0)}{n!}(x-x_0)^n$收敛于$s(x)$，但$s(x)$是否等于$f(x)$？



==定理2==：设$f(x)$在$N(x_0, \delta)$内具有任意阶导数，则$f(x)$的泰勒级数在$N(x_0, \delta)$内收敛于$f(x)$的充要条件是，$f(x)$在$x_0$点处的泰勒公式中的余项$R_n(x) \to 0$（当$n \to \infty$时）。

证：

必要性$\Longrightarrow$：假设$f(x)$在$x_0$点可以展开称泰勒级数，有$f(x_0)+f^\prime(x_0)(x-x_0)+\frac{f^{\prime\prime}(x_0)}{2!}(x-x_0)^2+\cdots+\frac{f^{(n)}(x_0)}{n!}(x-x_0)^n+\cdots, \quad x \in N(x_0, \delta)$，

而$f(x)$在$x_0$点的泰勒公式为：$f(x_0)+f^\prime(x_0)(x-x_0)+\frac{f^{\prime\prime}(x_0)}{2!}(x-x_0)^2+\cdots+\frac{f^{(n)}(x_0)}{n!}(x-x_0)^n+R_n(x)$，其中$R_n(x) = \frac{f^{(n+1)}(\xi)}{(n+1)!}(x-x_0)^{n+1}$，$\xi$介于$x$和$x_0$之间。

泰勒级数的前$n+1$项$s_{n+1}(x) = f(x_0)+f^\prime(x_0)(x-x_0)+\frac{f^{\prime\prime}(x_0)}{2!}(x-x_0)^2+\cdots+\frac{f^{(n)}(x_0)}{n!}(x-x_0)^n$

从而有$f(x) = s_{n+1} + R_n(x)$，由假设，因为$f(x)$在$x_0$点的泰勒级数收敛于$f(x)$，所以$\lim_{n \to \infty}s_{n+1}(x) = f(x)$。由$R_n(x) = f(x) - s_{n+1}$，则$\lim_{n \to \infty} R_n(x) = f(x) - \lim_{n \to \infty}s_{n+1}(x) = f(x)-f(x)=0$。

充分性$\Longrightarrow$：假设$f(x)$在$x_0$点的泰勒公式余项$R_n(x) \to 0, (n \to \infty)$。由$f(x) = s_{n+1}+R_n(x) \Longrightarrow s_{n+1} = f(x) - R_n(x)$，取极限$\lim_{n \to \infty}s_{n+1} = f(x) = \lim_{n \to \infty}R_n(x) = f(x) - 0 = f(x)$，这就证明了$f(x)$的泰勒级数的和函数为$f(x)$，所以$f(x) = \sum_{n=0}^\infty \frac{f^{(n)}(x_0)}{n!}(x-x_0)^n, \quad x \in N(x_0, \delta)$。



### 二、函数展开为幂级数

把$f(x)$在$x_0$点展开为泰勒级数的方法：

1. 直接展开法

   （1）求$f(x)$的各阶导数：$f^\prime(x), f^{\prime\prime}(x), \cdots, f^{(n)}(x), \cdots$，再求$f^\prime(x_0), f^{\prime\prime}(x_0), \cdots, f^{(n)}(x_0), \cdots$，如果$f(x)$在$x_0$点某阶导数不存在，停止进行展开。

   （2）写出$f(x)$在$x_0$点的泰勒级数，$f(x_0)+f^\prime(x_0)(x-x_0)+\frac{f^{\prime\prime}(x_0)}{2!}(x-x_0)^2+\cdots+\frac{f^{(n)}(x_0)}{n!}(x-x_0)^n+\cdots$

   并求出它的收敛区间$I$。

   （3）讨论在收敛区间$I$内，$f(x)$的泰勒公式的余项$R_n(x)$，其极限$\lim_{n \to \infty}R_n(x)$是否趋于0（当$n \to \infty$）。如果$\lim_{n \to \infty}R_n(x) = \lim_{n \to \infty}\frac{f^{(n+1)}(\xi)}{(n+1)!}(x-x_0)^{n+1}=0$（$\xi$在$x_0$于$x$之间），则$f(x) = \sum_{n=0}^\infty \frac{f^{(n)}(x_0)}{n!}(x-x_0)^n, x \in I$。

   

   例1：将$f(x)=e^x$展开为$x$的幂级数。

   解：$f(x) = e^x, f^{(n)}(x) = e^x, (n=1,2,3,\cdots)$，$f^{(n)}(0)=e^0=1, (n=1,2,3,\cdots)$，写出$f(x)=e^x$的麦克劳林级数：$1+x+\frac{1}{2!}x^2+\frac{1}{3!}x^3+\cdots+\frac{1}{n!}x^n+\cdots$，求$\lim_{n \to \infty}|\frac{a_{n+1}}{a_n}| = \lim_{n \to \infty}\frac{n!}{(n+1)!} = \lim_{n \to \infty}\frac{1}{n+1} = 0$，收敛半径$R = +\infty$，收敛域$(-\infty, +\infty)$。对任何有限数$x \in (-\infty, +\infty)$，$\xi$在$0$与$x$之间，$|R_n(x)| = |\frac{f^{(n+1)}(\xi)}{(n+1)!}x^{n+1}| = \frac{e^\xi}{(n+1)!}|x|^{n+1} \le \frac{e^{|\xi|}}{(n+1)!}|x|^{n+1} \le \frac{e^{|x|}}{(n+1)!}|x|^{n+1}$，$e^{|x|}$是有限值，与$n$无关。因为级数$\sum_{n=0}^\infty \frac{|x|^{n+1}}{(n+1)!}$的收敛域为$(-\infty, +\infty)$，所以其通项的极限必等于0，即$\lim_{n \to \infty}\frac{|x|^{n+1}}{(n+1)!} = 0$。

   从而$\lim_{n \to \infty}\frac{e^{|x|}}{(n+1)!}|x|^{n+1} = e^{|x|}\lim_{n \to \infty}\frac{|x|^{n+1}}{(n+1)!} = e^{|x|} \cdot 0 = 0$，根据极限存在的夹挤准则，$\lim_{n \to \infty}|R_n(x)| = 0$，从而$\lim_{n \to \infty}R_n(x) = 0$。

   所以$e^x = 1+x+\frac{1}{2!}x^2+\frac{1}{3!}x^3+\cdots+\frac{1}{n!}x^n+\cdots, \quad x \in (-\infty, +\infty)$。

   

   例2：将$f(x)=\sin x$展开为$x$的幂级数。

   解：$f(x) = \sin x, f^{(n)}(x) = (\sin x)^{(n)} = \sin(x+\frac{n\pi}{2}), (n=1,2,\cdots)$，$f^{(n)}(0) = \sin\frac{n\pi}{2}, (n=1,2,\cdots)$，

   $f^\prime(0) = \sin\frac{\pi}{2} = 1, f^{\prime\prime}(0) = \sin \pi = 0$

   $f^{\prime\prime\prime}(0) = \sin\frac{3\pi}{2} = -1, f^{(4)}(0) = \sin 2\pi = 0$

   $f^{(5)}(0) = \sin \frac{5\pi}{2} = 1, f^{(6)}(0) = \sin 3\pi = 0$

   $\cdots\cdots\cdots$

   写出$f(x) = \sin x$的麦克劳林级数：

   $x-\frac{1}{3!}x^3+\frac{1}{5!}x^5-\frac{1}{7}x^7+\cdots+(-1)^n\frac{1}{(2n+1)!}x^{2n+1}+\cdots$

   容易求出上面的级数的收敛域为$(-\infty, +\infty)$。

   任取有限数$x \in (-\infty, +\infty)$，$\xi$在$0$与$x$之间

   $|R_n(x)| = |\frac{\sin(\xi+\frac{(n+1)\pi}{2})}{(n+1)!}x^{n+1}| = \frac{|\sin(\xi+\frac{(n+1)\pi}{2})|}{(n+1)!}|x|^{n+1} \le \frac{|x|^{n+1}}{(n+1)!}$

   因为级数$\sum_{n=0}^\infty \frac{|x|^{n+1}}{(n+1)!}$收敛，所以其通项的极限必等于0，即$\lim_{n \to \infty}\frac{|x|^{n+1}}{(n+1)!} = 0$。根据极限存在的夹挤准则，$\lim_{n \to \infty}|R_n(x)| = 0$，从而$\lim_{n \to \infty}R_n(x) = 0$。所以

   $\sin x = x-\frac{1}{3!}x^3+\frac{1}{5!}x^5-\frac{1}{7}x^7+\cdots+(-1)^n\frac{1}{(2n+1)!}x^{2n+1}+\cdots, \quad x \in (-\infty, +\infty)$

2. 间接展开法

   （1）逐项求导法

   例1：将$f(x) = \cos x$展开成$x$的幂级数。

   解：因为$(\sin x)^\prime = \cos x = f(x)$，已知：

   $\sin x = x-\frac{1}{3!}x^3+\frac{1}{5!}x^5-\frac{1}{7}x^7+\cdots+(-1)^n\frac{1}{(2n+1)!}x^{2n+1}+\cdots, \quad x \in (-\infty, +\infty)$

   根据幂级数可以逐项求导的性质：

   $\cos = 1 - \frac{1}{2!}x^2 + \frac{1}{4}x^4 + \cdots + (-1)^n\frac{1}{(2n)!}x^{2n}+\cdots, \quad x \in (-\infty, +\infty)$

   

   （2）逐项积分法

例2：将$f(x) = \ln(1+x)$展开成$x$的幂级数。

解：因为$f^\prime(x) = \frac{1}{1+x}$，由$\frac{1}{1+x}=1-x+x^2-x^3+\cdots+(-1)^nx^n+\cdots, \quad x\in(-1, 1)$，由幂级数可以逐项积分的性质，得：$\int_0^x \frac{1}{1+x}dx = \int_0^x 1dx-\int_0^x xdx+\int_0^x x^2dx-\cdots+(-1)^n\int_0^x x^ndx + \cdots$

即$\ln(1+x)|_0^x = x-\frac{1}{2}x^2+\frac{1}{3}x^3-\cdots+\frac{(-1)^n}{n+1}x^{n+1}+\cdots$

化简得$\ln(1+x) = \sum_{n=0}^\infty (-1)^n \frac{1}{n+1}x^{n+1}$，

当$x=1$时，得$\sum_{n=0}^\infty (-1)^n \frac{1}{n+1}$收敛，$\ln(1+x)$在$x=1$左连续$\ln(1+x)=\sum_{n=0}^\infty (-1)^n \frac{1}{n+1}x^{n+1}, x\in(-1, 1]$。



3. 变量代换法

例1：将$y = f(x) = e^{-x}$展开成$x$的幂级数。

解：已知$e^t = \sum_{n=0}^\infty \frac{1}{n!}t^n, -\infty<t<+\infty$，令$t=-x$代入上式，得$e^{-x}=\sum_{n=0}^\infty\frac{1}{n!}(-x)^n = \sum_{n=0}^\infty\frac{(-1)^n}{n!}x^n, \quad x \in (-\infty, +\infty)$。



例2：将$f(x) = \ln x$展开成$x-2$的幂级数。

解：$f(x) = \ln(x) = \ln(2 + x - 2) = \ln [2(1+\frac{x-2}{2})] = \ln 2 + \ln (1+\frac{x-2}{2})$，已知$\ln(1+t) = \sum_{n=0}^\infty (-1)^n \frac{1}{n+1}t^{n+1}, t\in(-1, 1]$，令$t = \frac{x-2}{2}$，$\ln x = \ln 2 + \sum_{n=0}^\infty (-1)^n \frac{1}{n+1}(\frac{x-2}{2})^{n+1} = \ln 2 + \sum_{n=0}^\infty (-1)^n \frac{1}{(n+1) \cdot 2^{n+1}}(x-2)^{n+1}$，因为$-1 < \frac{x-2}{2} \le 1 \Longrightarrow 0 < x \le 4$。



4. 四则运算法

例1：将$f(x) = \frac{1}{x^2+4x+3}$展开为$(x-1)$的幂级数。

解：$f(x) = \frac{1}{x^2+4x+3} = \frac{1}{(x+1)(x+3)} = \frac{1}{2(1+x)}-\frac{1}{2(3+x)}=\frac{1}{2[2+(x-1)]}-\frac{1}{2[4+(x-1)]} \\ = \frac{1}{4(1+\frac{x-1}{2})} - \frac{1}{8(1+\frac{x-1}{4})}$

已知$\frac{1}{1+x} = \sum_{n=0}^\infty (-1)^n x^n, -1 < t < 1$，$\frac{1}{x^2+4x+3} = \frac{1}{4}\sum_{n=0}^\infty (-1)^n (\frac{x-1}{2})^n - \frac{1}{8}\sum_{n=0}^\infty (-1)^n (\frac{x-1}{4})^n \\ = \frac{1}{4}\sum_{n=0}^\infty \frac{(-1)^n}{2^n} (x-1)^n - \frac{1}{8}\sum_{n=0}^\infty \frac{(-1)^n}{2^{2n}} (x-1)^n \\ = \sum_{n=0}^\infty (-1)^n[\frac{1}{2^{n+2}}-\frac{1}{2^{2n+3}}](x-1)^n$

因为$-1 < \frac{x-1}{2} < 1, -1 < \frac{x-1}{4} < 1$，解不等式并取交集，得$x \in (-1, 3)$。所以：

$f(x) = \frac{1}{x^2+4x+3} = \sum_{n=0}^\infty (-1)^n[\frac{1}{2^{n+2}}-\frac{1}{2^{2n+3}}](x-1)^n, \quad x \in (-1, 3)$。



5. 求和函数法

例1：将$f(x) = (1+x)^\alpha$（$\alpha$为实常数）展开成$x$的幂级数。

解：

$f^\prime(x) = \alpha(1+x)^{\alpha-1}$，

$f^{\prime\prime}(x) = \alpha(\alpha-1)(1+x)^{\alpha-2}$，

$\cdots\cdots\cdots$

$f^{(n)}(x) = \alpha(\alpha-1)(\alpha-2)\cdots(\alpha-n+1)(1+x)^{\alpha-n}$



$f(0) = 1, f^\prime(0) = \alpha, f^{\prime\prime}(0) = \alpha(\alpha-1), f^{(n)}(0) = \alpha(\alpha-1)(\alpha-2)\cdots(\alpha-n+1)$

$f(x) = (1+x)^{\alpha}$的麦克劳林级数：$1 + \alpha x + \frac{\alpha(\alpha-1)}{2!}x^2+\cdots+\frac{\alpha(\alpha-1)(\alpha-2)\cdots(\alpha-n+1)}{n!}x^n+\cdots$，要证明余项$R_n(x)$的极限是否为零比较困难。

问题转成原级数的和函数是否为$f(x)$：

$1 + \alpha x + \frac{\alpha(\alpha-1)}{2!}x^2+\cdots+\frac{\alpha(\alpha-1)(\alpha-2)\cdots(\alpha-n+1)}{n!}x^n+\cdots = 1 + \sum_{n=1}^\infty \frac{\alpha(\alpha-1)(\alpha-2)\cdots(\alpha-n+1)}{n!}x^n$

设$1 + \sum_{n=1}^\infty \frac{\alpha(\alpha-1)(\alpha-2)\cdots(\alpha-n+1)}{n!}x^n = s(x)$，再证明：$s(x) = (1+x)^\alpha$。

求收敛域：

$\lim_{n \to \infty}|\frac{a_{n+1}}{a_n}| = \lim_{n \to \infty}|\frac{\alpha(\alpha-1)(\alpha-2)\cdots(\alpha-n)}{(n+1)!} \cdot \frac{n!}{\alpha(\alpha-1)(\alpha-2)\cdots(\alpha-n+1)}| \\ = \lim_{n \to \infty}|\frac{\alpha-n}{n+1}|=1$

即级数的收敛半径$R = 1$，收敛区间为$(-1, 1)$。

下面要证：在$(-1, 1)$内$s(x) = (1+x)^\alpha$。

因为$(1+x)s^\prime(x) = s^\prime(x)+xs^\prime(x)$，$s(x) = 1 + \sum_{n=1}^\infty \frac{\alpha(\alpha-1)(\alpha-2)\cdots(\alpha-n+1)}{n!}x^n$，$s^\prime(x) = \sum_{n=1}^\infty \frac{\alpha(\alpha-1)(\alpha-2)\cdots(\alpha-n+1)}{(n-1)!}x^{n-1}$

$x s^\prime(x) = \sum_{n=1}^\infty \frac{\alpha(\alpha-1)(\alpha-2)\cdots(\alpha-n+1)}{(n-1)!}x^n$

由$s^\prime(x)$的展开式，知$x^n$的系数为：$\frac{\alpha(\alpha-1)(\alpha-2)\cdots(\alpha-n)}{(n)!}$

由$x s^\prime(x)$的展开式，知$x^n$的系数为：$\frac{\alpha(\alpha-1)(\alpha-2)\cdots(\alpha-n+1)}{(n-1)!}$

$s^\prime(x) + x s^\prime(x)$的展开式中$x^n$的系数为：$\frac{\alpha(\alpha-1)(\alpha-2)\cdots(\alpha-n)}{(n)!} + \frac{\alpha(\alpha-1)(\alpha-2)\cdots(\alpha-n+1)}{(n-1)!} = \alpha \cdot \frac{\alpha(\alpha-1)(\alpha-2)\cdots(\alpha-n+1)}{n!}$

所以$(1+x)s^\prime(x) = s^\prime(x) + x s^\prime(x) = \alpha[1+\sum_{n=1}^\infty \frac{\alpha(\alpha-1)(\alpha-2)\cdots(\alpha-n+1)}{n!}x^n] = \alpha s_(x)$

即$(1+x)s^\prime(x) = \alpha s(x)$。作变形$\frac{s^\prime(x)}{s(x)} = \frac{1}{1+x}\alpha$，两边积分：$\int_0^x \frac{s^\prime(x)}{s(x)}dx = \alpha \int_0^x \frac{1}{1+x}dx, \quad -1 < x < 1$，即$\ln s(x)|_0^x = \alpha \ln (1+x)|_0^x$，

因为$s(0) = 1, \ln s(0) = \ln 1 = 0$，从而$\ln s(x) = \ln (1+x)^\alpha$，等式两边同时去掉$\ln$符号，$s(x) = (1+x)^\alpha, \quad -1 < x < 1$。

所以$(1+x)^\alpha = 1 + \sum_{n=1}^\infty \frac{\alpha(\alpha-1)(\alpha-2)\cdots(\alpha-n+1)}{n!}x^n, \quad -1 < x < 1$。



### 三、求幂级数的和函数

例1：求$\sum_{n=0}^\infty (n+1)x^n$的和函数。

解：$a_n = (n+1)$。$\lim_{n \to \infty}|\frac{a_{n+1}}{a_n}| = \lim_{n \to \infty}\frac{n+2}{n+1} = 1$，其收敛区间为$(-1, 1)$。

$u_n(x) = (n+1)x^n$，因为$\int_0^x u_n(x)dx = \int_0^x (n+1)x^n dx = x^{n+1}$，令$s(x) = \sum_{n=0}^\infty (n+1)x^n$，两边在$[0, x], (|x| < 1)$上作积分，$\int_0^x s(x)dx = \sum_{n=0}^\infty (\int_0^x (n+1)x^n dx) = \sum_{n=0}^\infty x^{n+1} = x \sum_{n=0}^\infty x^n = \frac{1}{1-x} \cdot x = \frac{x}{1-x}$。

等式两边求导$(\int_0^x s(x)dx)^\prime = (\frac{x}{1-x})^\prime$，所以$s(x) = \frac{1}{(1-x)^2}, \quad -1 < x < 1$。



例2：求$\sum_{n=1}^\infty \frac{1}{n}x^{n+1}$的和函数。

解：已求出收敛域$[-1, 1)$。令$s(x) = \sum_{n=1}^\infty \frac{1}{n}x^{n+1} = x \sum_{n=1}^\infty \frac{1}{n}x^n = x \cdot f(x), x \in [-1, 1)$，其中$f(x) = \sum_{n=1}^\infty \frac{1}{n}x^n, x \in [-1, 1)$。

$f^\prime(x) = \sum_{n=1}^\infty x^{n-1} = \frac{1}{1-x}, -1 \le x < 1$，$\int_0^x f^\prime(x)dx = \int_0^x \frac{1}{1-x}dx$，$f(x) - f(0) = -\ln(1-x)|_0^x$。因为$f(0) = 0$，所以$f(x) = -\ln(1-x)$，从而$s(x) = xf(x) = -x\ln(1-x), -1 \le x < 1$。



例3：求$\sum_{n=1}^\infty \frac{2n-1}{2^n}x^{2n-2}$的和函数。

解：求出收敛域：$(-\sqrt{2}, \sqrt{2})$。设和函数$s(x) = \sum_{n=1}^\infty \frac{2n-1}{2^n}x^{2n-2}$，因为$\int_0^x (2n-1)x^{2n-2}dx = x^{2n-1}$，和函数等式两边在$[0, x], (-\sqrt{2} < x < \sqrt{2})$上作积分，$\int_0^x s(x)dx = \sum_{n=1}^\infty \frac{1}{2^n}\int_0^x (2n-1)x^{2n-2}dx = \sum_{n=1}^\infty \frac{1}{2^n}x^{2n-1} = x \cdot \sum_{n=1}^\infty \frac{x^{2n-2}}{2^n} \\ = x \cdot \sum_{n=1}^\infty \frac{(x^2)^{n-1}}{2^n} = \frac{x}{2} \cdot \sum_{n=1}^\infty (\frac{x^2}{2})^{n-1} = \frac{x}{2} \cdot \frac{1}{1-\frac{x^2}{2}} = \frac{x}{2-x^2}$

$(\int_0^x s(x)dx)^\prime = (\frac{x}{2-x^2})^\prime \Longrightarrow s(x) = \frac{2+x^2}{(2-x^2)^2}, \quad \sqrt{2} < x < \sqrt{2}$。



例4：求数项级数$\sum_{n=0}^\infty \frac{(n+1)^2}{n!}$的和。

解：若$\sum_{n=0}^\infty \frac{(n+1)^2}{n!}x^n$在区间$I$上收敛于$s(x)$，如果$x = 1 \in I$，则$s(1) = \sum_{n=0}^\infty \frac{(n+1)^2}{n!}$。

求$\sum_{n=0}^\infty \frac{(n+1)^2}{n!}x^n$的收敛域为$(-\infty, +\infty)$，显然$x = 1 \in (-\infty, +\infty)$。设$s(x) = \sum_{n=0}^\infty \frac{(n+1)^2}{n!}x^n, \quad x \in (-\infty, +\infty)$。

$(n+1)^2 x^n = (n+1)(n+1)x^n, \int_0^x (n+1)^2 x^n dx = (n+1)\int_0^x (n+1)x^n dx = (n+1)x^{n+1}$，所以和函数等式两边作积分：$\int_0^x s(x)dx = \sum_{n=0}^\infty \frac{n+1}{n!} \int_0^x (n+1)x^n dx = \sum_{n=0}^\infty \frac{n+1}{n!}x^{n+1} = x \cdot \sum_{n=0}^\infty \frac{n+1}{n!}x^n$，令$\sum_{n=0}^\infty \frac{n+1}{n!}x^n = f(x)$，则$\int_0^x s(x) = x \cdot f(x)$。

$\int_0^x f(x)dx = \sum_{n=0}^\infty \frac{1}{n!} \int_0^x (n+1)x^n dx = \sum_{n=0}^\infty \frac{1}{n!}x^{n+1} = x \cdot \sum_{n=0}^\infty \frac{1}{n!}x^n = x \cdot e^x$，

$f(x) = (\int_0^x f(x)dx)^\prime = e^x + x \cdot e^x$，

$\int_0^x s(x)dx = x (e^x + x \cdot e^x) = (x+x^2)e^x$，

$s(x) = [(x+x^2)e^x]^\prime = (1+3x+x^2)e^x$，

$s(1) = 5e = \sum_{n=0}^\infty \frac{(n+1)^2}{n!}$。



### 四、欧拉公式

复数的指数形式与三角形式的转换公式：$e^{i\theta} = \cos\theta+i\sin\theta$，其中$\theta$是实数，$i = \sqrt{-1}$是虚数单位。



设有==复数项级数==（1）：$(u_1+iv_1)+(u_2+iv_2)+\cdots+(u_n+iv_n)+\cdots$，其中$u_j, v_j$是实数（$j=1,2,\cdots$），$i = \sqrt{-1}$。

由实部所组成的级数（2）：$u_1+u_2+\cdots+u_n+\cdots$收敛于$u$，由虚部所组成的级数（2）：$v_1+v_2+\cdots+v_n+\cdots$收敛于$v$，则称原==复数项级数==收敛于$u+iv$。



若原==复数项级数==各项的模组成的级数：$\sqrt{u_1^2+v_1^2}+\sqrt{u_2^2+v_2^2}+\cdots+\sqrt{u_n^2+v_n^2}+\cdots$收敛于$s$。原==复数项级数==中各项的实部与虚部满足：$|u_n| \le \sqrt{u_n^2 +v_n^2}, |v_n| \le \sqrt{u_n^2+v_n^2}$，由正项级数的比较判别法，可知实部组成的级数（1）和虚部组成的级数（2）绝对收敛。



考虑复数项级数：$1 + z + \frac{1}{2!}z^2 + \cdots + \frac{1}{n!}z^{n} + \cdots$，其中$z$为复数，它的各项的模组成正项级数$1 + |z| + \frac{1}{2!}|z^2| + \cdots + \frac{1}{n!}|z^n| + \cdots$。



复数$z^n$的共轭复数$\overline{z^n} = \overline{z \cdot z \cdots z} = \overline{z} \cdot \overline{z} \cdots \overline{z} = (\overline{z}^n)$

因为$z$的模的平方：$|z|^2 = z \cdot \overline{z}$，所以$|z^n|^2 = z^n \cdot \overline{z^n} = z^n \cdot (\overline{z})^n = (z \cdot \overline{z})^n = (|z|^2)^n$，等式两边同时开方得$|z^n| = |z|^n$



所以$1 + |z| + \frac{1}{2!}|z^2| + \cdots + \frac{1}{n!}|z^n| + \cdots = 1 + |z| + \frac{1}{2!}|z|^2 + \cdots + \frac{1}{n!}|z|^n + \cdots$，其收敛域为$|z| < +\infty$。

其中$z = x+iy$是复数，当$z = x$时，$1+x+\frac{1}{2!}x^2+\cdots+\frac{1}{n!}x^n+\cdots = e^x$。



根据定义，复数项级数$1 + z + \frac{1}{2!}z^2 + \cdots + \frac{1}{n!}z^{n} + \cdots$收敛，现定义复变量的指数函数：

$e^z = 1 + z + \frac{1}{2!}z^2 + \cdots + \frac{1}{n!}z^{n} + \cdots$。

令$z = iy, i = \sqrt{-1}$，$y$为实数，$e^{iy} = 1+iy+\frac{1}{2!}(iy)^2+\frac{1}{3!}(iy)^3+\frac{1}{4!}(iy)^4+\cdots+\frac{1}{n!}(iy)^n+\cdots \\ = 1 + iy - \frac{1}{2!}y^2 - \frac{1}{3!}iy^3 + \frac{1}{4!}y^4 + \cdots + \frac{1}{n!}i^n y^n + \cdots \\ = (1-\frac{1}{2!}y^2+ \frac{1}{4!}y^4-\cdots)+i(y-\frac{1}{3!}y^3+\cdots) \\ \cos y + i\sin y$

即$e^{iy} = \cos y + i\sin\theta$。

令$y = \theta$，得$e^{i\theta} = \cos\theta+i\sin\theta$，其中$\theta$是实数，$i=\sqrt{-1}$。

换$\theta$为$-\theta$，得$e^{-i\theta} = \cos(-\theta)+i\sin(-\theta)=\cos\theta-i\sin\theta$，所以：

$e^{i\theta}+e^{-i\theta} = 2\cos\theta \Longrightarrow \cos\theta = \frac{e^{i\theta}+e^{-i\theta}}{2}$

$e^{i\theta}-e^{-i\theta} = 2i\sin\theta \Longrightarrow \sin\theta = \frac{e^{i\theta}-e^{-i\theta}}{2i}$

由幂级数乘法（柯西）运算，推证：$e^{z_1} \cdot e^{z_2} = e^{z_1+z_2}$。

证明：$e^{z_1} \cdot e^{z_2} = (1 + z_1 + \frac{1}{2!}z_1^2 + \cdots + \frac{1}{n!}z_1^{n} + \cdots) \cdot (1 + z_2 + \frac{1}{2!}z_2^2 + \cdots + \frac{1}{n!}z_2^{n} + \cdots) \\ = 1+(z_1+z_2)+(\frac{1}{2!}z_2^2+z_1z_2+\frac{1}{2!}z_1^2)+(\frac{1}{3!}z_2^3+\frac{1}{2!}z_2^2z_1+\frac{1}{2!}z_2z_1^2+\frac{1}{3!}z_1^3)+\cdots \\ = 1 + (z_1+z_2)+\frac{1}{2!}(z_1+z_2)^2+\frac{1}{3!}(z_1+z_2)^3+\cdots \\ = e^{z_1+z_2}$



如果复数$z$的模$|z| = r$，幅角$\arg z = \theta$，则$z = r(\cos\theta+i\sin\theta)=re^{i\theta}$。



## 第5节 傅立叶级数

如果$a_0, a_n, b_n,(n=1,2,\cdots)$都是实常数，称$\frac{a_0}{2}+(a_1\cos\omega x+b_1\sin\omega x)+(a_2\cos2\omega x+b_2\sin2\omega x)+\cdots+(a_n\cos n\omega x+b_n\sin n\omega x)+\cdots \\ = \frac{a_0}{2} + \sum_{n=1}^\infty (a_n \cos n\omega x + b_n \sin n \omega x)$

（其中$\omega$为常数），称此级数为三角级数。

$\cos n\omega x = \cos(n\omega x - 2\pi) = \cos[n\omega(x - \frac{2\pi}{n\omega})]$（$\cos n\omega x = \cos[n\omega(x-\frac{2\pi}{n\omega})]$，所以周期为$\frac{2\pi}{n\omega}$，乘以$n$之后，$n \cdot \frac{2\pi}{n\omega} = \frac{2\pi}{\omega}$仍然是周期），可知级数中每一项都以$\frac{2\pi}{\omega}$为周期，则三角级数以$\frac{2\pi}{\omega}$为周期。

当$\omega = 1$时，得到三角级数$\frac{a_0}{2} + \sum_{n=1}^\infty (a_n \cos n x + b_n \sin n x)$，该级数以$2\pi$为周期。



### 一、三角函数系的正交性

==函数系的正交性==：设在$[a, b]$上给定一个==可积==的函数系：$\phi_1(x), \phi_2(x), \cdots, \phi_n(x), \cdots$，记为$\{\phi_n(x)\}$，若函数系在$[a, b]$上满足

（1）$\int_a^b \phi_i^2(x)dx = l_i \neq 0, (i=1,2,\cdots)$；

（2）$\int_a^b \phi_i(x) \cdot \phi_j(x)dx = 0, (i \neq j, i,j = 1, 2, \cdots)$

则称函数项$\{\phi_n(x)\}$在$[a, b]$上正交。

考虑：三角函数系$1, \cos x, \sin x, \cos 2x, \sin 2x, \cdots, \cos nx, \sin nx \cdots$在$[-\pi, +\pi]$上的正交性。

验证：

（1）$\int_{-\pi}^{+\pi} 1^2 dx = 2\pi \neq 0$；

$\int_{-\pi}^{+\pi} \cos^2 nx dx = \int_{-\pi}^{+\pi}\frac{1+\cos 2nx}{2}dx = \int_{-\pi}^{+\pi}\frac{1}{2} dx + \int_{-\pi}^{+\pi}\frac{\cos 2nx}{2}dx = \pi \neq 0$；

$\int_{-\pi}^{+\pi} \sin^2 nx dx = \int_{-\pi}^{+\pi}\frac{1-\cos 2nx}{2}dx = \int_{-\pi}^{+\pi}\frac{1}{2} dx - \int_{-\pi}^{+\pi}\frac{\cos 2nx}{2}dx = \pi \neq 0$

（2）$\int_{-\pi}^{+\pi} 1 \cdot \cos nx dx = \frac{1}{n}\sin nx|_{-\pi}^{+\pi} = 0, (n=1,2,\cdots)$；

$\int_{-\pi}^{+\pi} 1 \cdot \sin nx dx = -\frac{1}{n}\cos nx|_{-\pi}^{+\pi} = 0, (n=1,2,\cdots)$；

$\int_{-\pi}^{+\pi} \sin mx \cdot \cos nx dx = \int_{-\pi}^{+\pi}\frac{1}{2}[\sin (m-n)x + \sin (m+n)x]dx \\ = \frac{1}{2}\int_{-\pi}^{+\pi}\sin (m-n)x dx + \frac{1}{2}\int_{-\pi}^{+\pi}\sin (m+n)x dx = 0, (m, n=1,2,\cdots)$

$\int_{-\pi}^{+\pi} \cos mx \cdot \cos nx dx = \int_{-\pi}^{+\pi}\frac{1}{2}[\cos (m-n)x + \cos (m+n)x]dx \\ = \frac{1}{2}\int_{-\pi}^{+\pi}\cos (m-n)x dx + \frac{1}{2}\int_{-\pi}^{+\pi}\cos (m+n)x dx = 0, (m \neq n, m, n=1,2,\cdots)$

$\int_{-\pi}^{+\pi} \sin mx \cdot \sin nx dx = \int_{-\pi}^{+\pi}\frac{1}{2}[\cos (m-n)x - \cos (m+n)x]dx \\ = \frac{1}{2}\int_{-\pi}^{+\pi}\cos (m-n)x dx - \frac{1}{2}\int_{-\pi}^{+\pi}\cos (m+n)x dx = 0, (m \neq n, m, n=1,2,\cdots)$

所以三角函数系在$[-\pi, +\pi]$上是正交的。

由正弦、余弦函数以$2\pi$为周期，再由周期函数积分的性质：$\int_a^b f(x)dx = \int_0^T f(x)dx$，其中$f(x)$以$T$为周期，$b - a = T$。所以三角函数系在$[a, b]$上正交$(b - a = 2\pi)$。



### 二、傅立叶级数

设$f(x)$是以$2\pi$为周期的函数，能展开为三角级数，即$f(x) = \frac{a_0}{2} + \sum_{n=1}^\infty (a_n \cos nx + b_n \sin nx)$。

问题：系数$a_0, a_n, b_n, (n = 1, 2, \cdots)$与$f(x)$有何关系？

假定三角级数逐项可积，以$\sin nx, \cos nx$乘三角函数之后，仍然是逐项可积。

先求$a_0$：把$f(x) = \frac{a_0}{2} + \sum_{n=1}^\infty (a_n \cos nx + b_n \sin nx)$两边同时在$[-\pi, +\pi]$上作积分，$\int_{-\pi}^{+\pi}f(x)dx = \int_{-\pi}^{+\pi}\frac{a_0}{2}dx + \int_{-\pi}^{+\pi}[\sum_{n=1}^\infty(a_n \cos nx + b_n \sin nx)]dx = a_0 \pi + \sum_{n=1}^\infty(a_n \int_{-\pi}^{+\pi}\cos nx dx + b_n \int_{-\pi}^{+\pi}\sin nx dx) = a_0 \pi + 0 = a_0 \pi$

$\therefore a_0 = \frac{\int_{-\pi}^{+\pi} f(x)dx}{\pi}$

接着求$a_n$：把$f(x) = \frac{a_0}{2} + \sum_{n=1}^\infty (a_n \cos nx + b_n \sin nx)$两边乘上$\cos kx$，得$f(x) \cos kx = \frac{a_0}{2} \cos kx + \sum_{n=1}^\infty (a_n \cos nx \cdot \cos kx + b_n \sin nx \cos kx)$，等式两边同时

在$[-\pi, +\pi]$上作积分，$\int_{-\pi}^{+\pi} f(x) \cos kx dx = \frac{a_0}{2}\int_{-\pi}^{+\pi}\cos kx dx + \sum_{n=1}^\infty(a_n \int_{-\pi}^{+\pi}\cos nx \cos kx dx + b_n \int_{-\pi}^{+\pi}\sin nx \cos kx dx) = a_n \int_{-\pi}^{+\pi}\cos^2 nx dx, (n = k)$

$\therefore \int_{-\pi}^{+\pi}f(x)\cos nx dx = a_n \pi$，$\therefore a_n = \frac{\int_{-\pi}^{+\pi}f(x)\cos nx dx}{\pi}, (n = 1, 2, \cdots)$。

同理，把$f(x) = \frac{a_0}{2} + \sum_{n=1}^\infty (a_n \cos nx + b_n \sin nx)$两边乘上$\sin kx$，得$f(x) \sin kx = \frac{a_0}{2} \sin kx + \sum_{n=1}^\infty (a_n \cos nx \cdot \sin kx + b_n \sin nx \sin kx)$，等式两边同时

在$[-\pi, +\pi]$上作积分，得$\therefore b_n = \frac{\int_{-\pi}^{+\pi}f(x)\sin nx dx}{\pi}, (n = 1, 2, \cdots)$

上式表示的$a_0, a_n, b_n, (n = 1, 2, \cdots)$称为傅里叶系数，把$a_0, a_n, b_n$代入三角级数中，得$\frac{a_0}{2} + \sum_{n=1}^\infty (a_n \cos nx + b_n \sin nx)$，此级数称为傅立叶级数（$f(x)$的傅立叶级数）。



若$f(x)$能展开成三角级数，可以得到$a_0 = \frac{\int_{-\pi}^{+\pi} f(x)dx}{\pi}, a_n = \frac{\int_{-\pi}^{+\pi}f(x)\cos nx dx}{\pi}, b_n = \frac{\int_{-\pi}^{+\pi}f(x)\sin nx dx}{\pi}, (n = 1, 2, \cdots)$，级数$\frac{a_0}{2} + \sum_{n=1}^\infty (a_n \cos nx + b_n \sin nx)$——$f(x)$的傅立叶级数。

设$f(x)$已给定，求出$a_0, a_n, b_n, (n = 1, 2, \cdots)$后即可写出级数$\frac{a_0}{2} + \sum_{n=1}^\infty (a_n \cos nx + b_n \sin nx)$。

问题：$f(x)$满足什么条件，它的傅立叶级数收敛于$f(x)$？

==狄里克雷（Dirichlet）收敛定理==：设$f(x)$是以$2\pi$为周期的周期函数，且$f(x)$满足在一个周期内连续或只有有限个第一类间断点且至多有有限个极值，则$f(x)$可以展开成傅立叶级数，且

（1）当$x$是$f(x)$的连续点时，$\frac{a_0}{2} + \sum_{n=1}^\infty (a_n \cos nx + b_n \sin nx) = f(x)$；

（2）当$x$是$f(x)$的间断点时，$\frac{a_0}{2} + \sum_{n=1}^\infty (a_n \cos nx + b_n \sin nx) = \frac{f(x-0) + f(x+0)}{2}$。



例1：设$f(x)$是以$2\pi$为周期的周期函数，它在一个周期$[-\pi, \pi)$的内的表达式为：
$$
f(x) = \left\{\begin{array}{cc}-\frac{\pi}{2}, &-\pi \le x < 0 \\ \frac{\pi}{2}, & 0 \le x < \pi \end{array}\right.
$$
将$f(x)$展开成以$2\pi$为周期的傅立叶级数。

解：函数$f(x)$在$x = k\pi, (k \in Z)$处有第一类间断点。$f(x)$满足收敛定理条件，可以展开成傅立叶级数。

求$a_0 = \frac{\int_{-\pi}^{+\pi} f(x)dx}{\pi} = \frac{\int_{-\pi}^{0}-\frac{\pi}{2}dx + \int_{0}^{+\pi}\frac{\pi}{2}dx}{\pi} = 0$，$a_n = \frac{\int_{-\pi}^{+\pi}f(x)\cos nx dx}{\pi} = \frac{\int_{-\pi}^{0}-\frac{\pi}{2}\cos nx dx + \int_{0}^{+\pi}\frac{\pi}{2}\cos nx dx}{\pi} = 0, (n = 1, 2, \cdots)$，$b_n = \frac{\int_{-\pi}^{+\pi}f(x)\sin nx dx}{\pi} = \frac{\int_{-\pi}^{0}-\frac{\pi}{2}\sin nx dx + \int_{0}^{+\pi}\frac{\pi}{2}\sin nx dx}{\pi} = \frac{1}{2} \cdot \frac{1}{n} \cos nx|_{-\pi}^0 - \frac{1}{2} \cdot \frac{1}{n} \cos nx|_0^{+\pi} \\ \frac{1}{2n}[1-(-1)^n] - \frac{1}{2n}[(-1)^n-1] = \frac{1}{n}[1 - (-1)^n], (n = 1, 2, \cdots)$

即：
$$
b_n = \left\{\begin{array}{cc}\frac{2}{n}, &n = 1, 3, 5, \cdots \\ 0, &n = 2, 4, 6, \cdots \end{array}\right.
$$
所以傅立叶级数：$\frac{a_0}{2} + \sum_{n=1}^\infty (a_n \cos nx + b_n \sin nx) = 0 + \sum_{n=1}^\infty [0 + \frac{1}{n}[1 - (-1)^n]\sin nx] \\ = \sum_{n=1}^\infty \frac{2}{2n-1}\sin (2n-1)x = 2\sum_{n=1}^\infty \frac{1}{2n-1}\sin (2n-1)x$

根据收敛定理，有$f(x) = 2\sum_{n=1}^\infty \frac{1}{2n-1}\sin (2n-1)x, (x \neq k\pi, k \in Z)$，当$x = k\pi$时，分类讨论：当$k = 0, \pm 2, \pm 4, \cdots$时，$2\sum_{n=1}^\infty \frac{1}{2n-1}\sin (2n-1)x = \frac{f(k\pi-0) + f(k\pi+0)}{2} = \frac{\frac{\pi}{2} - \frac{\pi}{2}}{2} = 0$；当$k = \pm 1, \pm 3, \pm 5 \cdots$时，$2\sum_{n=1}^\infty \frac{1}{2n-1}\sin (2n-1)x = \frac{f(k\pi-0) + f(k\pi+0)}{2} = \frac{-\frac{\pi}{2} + \frac{\pi}{2}}{2} = 0$。



设$f(x)$不是周期函数，$f(x)$定义在$[-\pi, \pi]$上，在$[-\pi, +\pi]$之外，补充$f(x)$的定义，使$f(x)$拓广为以$2\pi$为周期的周期函数$F(x)$，其中$F(x) = f(x), -\pi < x < \pi$。称此操作为把$f(x)$作周期延拓，再把$F(x)$展开成以$2\pi$为周期的傅立叶级数，把自变量$x$限制在$[-\pi,\pi]$内，就得$f(x)$的傅立叶的级数。



例2：已知函数
$$
f(x) = \left\{\begin{array}{cc}0, &-\pi \le x \le 0 \\ x, &0 < x < \pi\end{array}\right.
$$
将其展开成以$2\pi$为周期的傅立叶级数。

解：$f(x)$在$[-\pi, \pi]$内是连续函数，可以展开成以$2\pi$为周期的傅立叶级数。把$f(x)$作周期延拓，得$F(x)$是$2\pi$为周期的函数。

$a_0 = \frac{\int_{-\pi}^{+\pi} f(x)dx}{\pi} = \frac{\int_{0}^{+\pi}x dx}{\pi} = \frac{1}{\pi} \cdot \frac{1}{2}x^2|_0^\pi = \frac{\pi}{2}$，$a_n = \frac{\int_{-\pi}^{+\pi}f(x)\cos nx dx}{\pi} = \frac{\int_{0}^{+\pi}x\cos nx dx}{\pi} = \frac{\int_{0}^{+\pi}x d(\frac{1}{n}\sin nx)}{\pi} \\ = \frac{1}{n\pi}(x\sin nx|_0^\pi - \int_0^\pi \sin nx dx) = \frac{1}{n\pi}(0 + \frac{1}{n}\cos nx|_0^\pi) = \frac{1}{n^2\pi}[(-1)^n - 1], (n = 1, 2, \cdots)$

$b_n = \frac{\int_{-\pi}^{+\pi}f(x)\sin nx dx}{\pi} = \frac{\int_{0}^{+\pi}x\sin nx dx}{\pi} = \frac{\int_{0}^{+\pi}x d(-\frac{1}{n}\cos nx)}{\pi} \\ = -\frac{1}{n\pi}(x\cos nx|_0^\pi - \int_0^\pi \cos nx dx) = -\frac{1}{n\pi}(x\cos nx|_0^\pi - 0) = \frac{(-1)^{n+1}}{n}, (n = 1, 2, \cdots)$

$\frac{a_0}{2} + \sum_{n=1}^\infty (a_n \cos nx + b_n \sin nx) = \frac{\pi}{4} + \sum_{n=1}^\infty \{\frac{1}{n^2\pi}[(-1)^n - 1] \cos nx + \frac{(-1)^{n+1}}{n} \sin nx\} \\ = \frac{\pi}{4} + \sum_{n=1}^\infty[\frac{-2}{(2n-1)^2\pi}\cos(2n-1)x+\frac{(-1)^{n+1}}{n}\sin nx]$

所以$f(x) = \frac{\pi}{4} + \sum_{n=1}^\infty[\frac{-2}{(2n-1)^2\pi}\cos(2n-1)x+\frac{(-1)^{n+1}}{n}\sin nx, x \in (-\pi, \pi)$。当$x = \pm\pi, \pm 3\pi, \pm 5\pi, \cdots$时，和函数$s(x) = \frac{f(x-0)+f(x+0)}{2} = \frac{1}{2}(\pi+0) = \frac{\pi}{2}$。



### 三、正弦级数、余弦级数

1. 奇、偶函数的傅立叶级数

==定理==：设$f(x)$在区间$[-\pi, +\pi]$上满足狄里克雷收敛定理的条件，则：

（1）当$f(x)$为奇函数时，则$f(x)$的傅立叶系数$a_0 = 0, a_n = 0, (n=1,2,\cdots), b_n = \frac{2}{\pi}\int_0^\pi f(x)\sin nx dx, (n=1,2,\cdots)$，其傅立叶级数是只含有正弦的正弦级数$\sum_{n=1}^\infty b_n \sin nx$；

（2）当$f(x)$为偶函数时，则$f(x)$的傅立叶系数$b_n = 0, a_0 = \frac{2}{\pi}\int_{0}^{\pi}f(x)dx, a_n = \frac{2}{\pi}\int_{0}^{\pi}f(x)\cos nx dx, (n=1,2,\cdots)$，其傅立叶级数是只含有余弦的余弦级数$\frac{a_0}{2} + \sum_{n=1}^\infty a_n \cos nx$。

证：设$f(x)$为奇函数，即$f(-x) = -f(x), x \in [-\pi, +\pi]$，由傅立叶系数公式，$a_0 = \frac{\int_{-\pi}^{+\pi} f(x)dx}{\pi} = \frac{\int_{-\pi}^{0} f(x)dx + \int_{0}^{+\pi} f(x)dx}{\pi}$，对积分$\int_{-\pi}^{0} f(x)dx$作变量替换，令$x = -t$，$\int_{-\pi}^{0} f(x)dx = \int_{\pi}^0 f(-t)d(-t) = \int_{\pi}^0 -f(t)(-dt) = -\int_{0}^{\pi} f(t)dt = -\int_0^{\pi}f(x)dx$，$\therefore a_0 = \frac{-\int_{0}^{\pi} f(x)dx + \int_{0}^{+\pi} f(x)dx}{\pi} = 0$；

$a_n = \frac{\int_{-\pi}^{+\pi}f(x)\cos nx dx}{\pi} = \frac{\int_{-\pi}^{0}f(x)\cos nx dx + \int_{0}^{\pi}f(x)\cos nx dx}{\pi}$，对积分$\int_{-\pi}^{0}f(x)\cos nx dx$作变量替换，令$x = -t$，$\int_{-\pi}^{0}f(x)\cos nx dx = \int_{\pi}^{0}f(-t)\cos(-nt) d(-t) = -\int_{0}^{\pi}f(x)\cos nx dx$，$\therefore a_n = \frac{-\int_{0}^{\pi}f(x)\cos nx dx + \int_{0}^{\pi}f(x)\cos nx dx}{\pi} = 0$；

$b_n = \frac{\int_{-\pi}^{+\pi}f(x)\sin nx dx}{\pi} = \frac{\int_{-\pi}^{0}f(x)\sin nx dx + \int_{0}^{\pi}f(x)\sin nx dx}{\pi}$，对积分$\int_{-\pi}^{0}f(x)\sin nx dx$作变量替换，令$x = -t$，$\int_{-\pi}^{0}f(x)\sin nx dx = \int_{\pi}^{0}f(-t)\sin(-nt) d(-t) = \int_{0}^{\pi}f(x)\sin nx dx$，$\therefore b_n = \frac{\int_{0}^{\pi}f(x)\sin nx dx + \int_{0}^{\pi}f(x)\sin nx dx}{\pi} = \frac{2}{\pi}\int_{0}^{\pi}f(x)\sin nx dx$。

所以傅立叶级数为$\sum_{n=1}^\infty b_n \sin nx$。



例1：设$f(x) = x, x \in [-\pi, \pi]$，把$f(x)$展成以$2\pi$为周期的傅立叶级数。

解：$f(x) = x$在$[-\pi, +\pi]$上是连续的奇函数，其傅立叶系数$a_0 = 0, a_n = 0$，$b_n = \frac{2}{\pi}\int_0^\pi f(x)\sin nx dx = \frac{2}{\pi}\int_0^\pi x\sin nx dx = -\frac{2}{n\pi}\int_0^\pi x d(-\cos nx) \\ = -\frac{2}{n\pi}[-x\cos nx|_0^\pi - \int_0^\pi -\cos nx dx] = (-1)^{n+1} \cdot \frac{2}{n}, (n=1,2,\cdots)$

所以傅立叶级数为$x = \sum_{n=1}^\infty (-1)^{n+1} \cdot \frac{2}{n} \cdot \sin nx = 2\sum_{n=1}^\infty (-1)^{n+1} \cdot \frac{1}{n} \cdot \sin nx, x \in (-\pi, \pi)$



例2：把$f(x) = |x|, x \in [-\pi, +\pi]$展开成以$2\pi$为周期的傅立叶级数。

解：$f(x) = |x|$在$[-\pi, +\pi]$上是连续的偶函数，其傅立叶系数$b_n = 0, (n=1,2,\cdots)$，$a_0 = \frac{2}{\pi}\int_0^\pi f(x)dx = \frac{2}{\pi}\int_0^\pi xdx = \pi$，$a_n = \frac{2}{\pi}\int_{0}^{\pi}f(x)\cos nx dx = \frac{2}{\pi}\int_0^{\pi}x \cos nx dx = \frac{2}{n\pi}\int_0^{\pi}xd(\sin nx) \\ = \frac{2}{n\pi}[x\sin nx|_0^{\pi}-\int_0^{\pi}\sin nx dx] = \frac{2}{n^2\pi}[(-1)^n-1], (n=1,2,\cdots)$

所以傅立叶级数为$|x| = \frac{\pi}{2} + \sum_{n=1}^\infty \frac{2}{n^2\pi}[(-1)^n-1]\cos nx = \frac{\pi}{2} - \frac{4}{\pi}\sum_{n=1}^\infty \frac{1}{(2n-1)^2}\cos (2n-1)x, x \in [-\pi, \pi]$

$x = 0 \in [-\pi, \pi]$，把$x = 0$代入上式可得：$0 = \frac{\pi}{2} - \frac{4}{\pi}[1+\frac{1}{3^2}+\frac{1}{5^2}+ \cdots + \frac{1}{(2n-1)^2} + \cdots]$，移项得：$1+\frac{1}{3^2}+\frac{1}{5^2}+ \cdots + \frac{1}{(2n-1)^2} + \cdots = \frac{\pi^2}{8}$。

令$\sigma_1 = 1+\frac{1}{3^2}+\frac{1}{5^2}+ \cdots + \frac{1}{(2n-1)^2} + \cdots = \frac{\pi^2}{8}$，$\sigma_2 = \frac{1}{2^2}+\frac{1}{4^2}+ \cdots + \frac{1}{(2n)^2} + \cdots$，$\sigma_3 = 1 + \frac{1}{2^2} + \frac{1}{3^2} + \frac{1}{4^2} + \cdots +\frac{1}{n^2} + \cdots$，

$\sigma_2 = \frac{1}{2^2}+\frac{1}{4^2}+ \cdots + \frac{1}{(2n)^2} + \cdots = \frac{1}{2^2}(1+\frac{1}{2^2}+\frac{1}{3^2} + \cdots + \frac{1}{n^2} + \cdots) = \frac{1}{4}\sigma_3$，

因此$\sigma_3 = 4\sigma_2, \sigma_3 = \sigma_1+\sigma_2$，解得$\sigma_2 = \frac{\pi^2}{24}, \sigma_3 = \frac{\pi^2}{6}$。



### 四、把函数展开成正弦级数或余弦级数

设$f(x)$定义在上$[0, \pi]$，且满足狄里克雷收敛定理条件，把$f(x)$展开成正弦级数。

在$[-\pi, 0)$上补充$f(x)$的定义，使得补充定义后得到一个在$[-\pi, \pi]$上的奇函数$F(x)$==奇式延拓==：
$$
F(x) = \left\{\begin{array}{cc}f(x), &0 < x \le \pi \\ 0, &x = 0 \\ -f(-x), &-\pi \le x < 0\end{array}\right.
$$
即可把$F(x)$展开为正弦级数，限定$x$在$[0, \pi]$上取值，此时得到$f(x)$在$[0, \pi]$上的正弦级数展开式。

若函数$f(x)$定义在上$[0, \pi]$，且满足狄里克雷收敛定理条件，把$f(x)$展开成余弦级数。在$[-\pi, 0)$上补充$f(x)$的定义，使得补充定义后得到一个在$[-\pi, \pi]$上的偶函数$F(x)$==偶式延拓==：
$$
F(x) = \left\{\begin{array}{cc}f(x), &0 \le x \le \pi \\ f(-x), &-\pi \le x < 0\end{array}\right.
$$
即可把$F(x)$展开为余弦级数，限定$x$在$[0, \pi]$上取值，此时得到$f(x)$在$[0, \pi]$上的余弦级数展开式。



例1：把$f(x) = x + 1, (0 \le x \le \pi)$，展开成正弦级数。

解：$f(x) = x + 1, (0 \le x \le \pi)$是连续函数，满足狄里克雷收敛定理条件，在$[-\pi, 0)$上补充定义，得到奇函数$F(x)$（作奇式延拓），求$F(x)$的傅立叶系数，此时$a_0 = 0, a_n = 0$，$b_n = \frac{2}{\pi}\int_0^{\pi}f(x)\sin nx dx = \frac{2}{\pi}\int_0^{\pi}(x+1)\sin nx dx = -\frac{2}{n\pi}\int_0^\pi(x+1)d(\cos nx) \\ = \cdots = \frac{2}{n\pi}[1 - (-1)^n + (-1)^{n+1}\pi]$

即：
$$
b_n = \left\{\begin{array}{cc}\frac{2(\pi+2)}{n\pi}, &n=1,3,5,\cdots \\ -\frac{2}{n}, &n = 2,4,6,\cdots \end{array}\right.
$$
所以正弦级数展开式为：$\frac{2(\pi+2)}{\pi}\sin x - \frac{2}{2}\sin 2x + \frac{2(\pi+2)}{3\pi}\sin 3x - \frac{2}{4}\sin 4x + \cdots, x \in (0, \pi)$。



### 五、以$2l$为周期的周期函数的傅立叶级数

==定理==：设$f(x)$是以$2l, (l > 0)$为周期的周期函数，如果$f(x)$在$[-l, l]$上$f(x)$是连续函数或只有有限个第一类间断点且只有有限个极值，则$f(x)$的傅立叶级数在$(-\infty, +\infty)$上收敛，其展开式为$\frac{a_0}{2} + \sum_{n=1}^\infty (a_n \cos \frac{n\pi}{l}x + b_n \sin \frac{n\pi}{l}x)$，其中傅立叶系数为：$a_0 = \frac{1}{l}\int_{-l}^{+l}f(x)dx$，$a_n = \frac{1}{l}\int_{-l}^{+l}f(x)\cos\frac{n \pi x}{l}dx, (n=1,2,\cdots)$，$b_n = \frac{1}{l}\int_{-l}^{l}f(x)\sin\frac{n \pi x}{l}dx, (n=1,2,\cdots)$，在$[-l, l]$上，和函数$s(x)$为：

（1）当$x$为连续点时，$s(x) = f(x)$；

（2）当$x$为间断点时，$s(x) = \frac{f(x-0)+f(x+0)}{2}$；

（3）当$x = \pm l$时，$s(l) = \frac{f(l-0)+f(l+0)}{2}$。



例1：设$f(x)$是以4为周期的周期函数，它在$[-2, 2)$上的表达式为：
$$
f(x) = \left\{\begin{array}{cc}0, &-2 \le x < 0 \\ h, &0 \le x < 2\end{array}\right. (h > 0)
$$
将$f(x)$展开为以4为周期的傅立叶级数。

解：$f(x)$在$[-2, 2)$上满足收敛定理条件。$a_0 = \frac{1}{l}\int_{-l}^{+l}f(x)dx = \frac{1}{2}[\int_{-2}^0 0 dx + \int_0^2 h dx] = h$，$a_n = \frac{1}{l}\int_{-l}^{+l}f(x)\cos\frac{n \pi x}{l}dx = \frac{1}{2}\int_0^2 h \cos\frac{n \pi x}{2}dx = \frac{1}{2} \cdot h \cdot \frac{2}{n \pi} \sin \frac{n \pi x}{2}|_0^2 = 0, (n=1,2,\cdots)$，$b_n = \frac{1}{l}\int_{-l}^{l}f(x)\sin\frac{n \pi x}{l}dx = \frac{1}{2}\int_0^2 h \sin\frac{n \pi x}{2} dx = \frac{h}{n \pi}[1 - (-1)^n], (n=1,2,\cdots)$，所以$f(x) = \frac{h}{2} + \frac{2h}{\pi}(\sin\frac{\pi x}{2}+\frac{1}{3}\sin\frac{3\pi x}{2}+\frac{1}{5}\sin\frac{5 \pi x}{2}+\cdots), x \in (-\infty, +\infty), x \neq 2k, k \in Z$。



例2：将
$$
f(x) = \left\{\begin{array}{cc}x, &0 \le x < 1 \\ 2-x, &1 \le x < 2\end{array}\right.
$$
展开成以4为周期的正弦级数。

解：对$f(x)$在$[-2, 0)$之间补充定义，得到$[-2, 2]$上的奇函数$F(x)$（奇式延拓）。先求$F(x)$的傅立叶系数：$a_0 = 0, a_n = 0$，$b_n = \frac{2}{l}\int_0^l f(x)\sin\frac{n \pi x}{l}dx = \frac{2}{2}\int_0^2 f(x)\sin\frac{n \pi x}{2}dx = \int_0^1 x\sin\frac{n \pi x}{2}dx + \int_1^2 (2-x)\sin\frac{n \pi x}{2}dx$，对积分$\int_1^2 (2-x)\sin\frac{n \pi x}{2}dx$，作变换$2-x=t$，$\int_1^2 (2-x)\sin\frac{n \pi x}{2}dx = -\int_1^0 t \sin\frac{(2-t)n\pi}{2}dt = \int_1^0 t \cdot (-1)^n \sin\frac{n \pi t}{2}dt \\ = (-1)^{n+1}\int_0^1 t\sin\frac{n \pi t}{2}dt$

$\therefore b_n = \int_0^1 x\sin\frac{n \pi x}{2}dx + (-1)^{n+1}\int_0^1 x\sin\frac{n \pi x}{2}dx = [1+(-1)^{n+1}]\int_0^1 x\sin\frac{n \pi x}{2}dx$

即：
$$
b_n = \left\{\begin{array}{cc}\frac{8}{n^2\pi^2}\sin\frac{n \pi}{2}, &n=1,3,5\cdots \\ 0, &n=2, 4, 6, \cdots\end{array}\right.
$$
根据收敛定理，得$f(x) = \frac{8}{\pi^2}(\sin\frac{\pi x}{2}-\frac{1}{3^2}\sin\frac{3 \pi x}{2} + \frac{1}{5^2}\sin\frac{5 \pi x}{2} - \cdots) = \frac{8}{\pi^2}\sum_{n-1}^\infty \frac{(-1)^{n+1}}{(2n-1)^2}\sin\frac{(2n-1) \pi x}{2}, x \in [0, 2]$

