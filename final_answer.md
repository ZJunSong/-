# 《偏微分方程》课程期末考试答案



## 第一题

> **(1) (10分)** 考虑如下 *Cauchy* 问题：
> $$
> \left\{\begin{array}{l}
> u_{t}+a (u)u_x = 0 \\
> u(0,x) = \varphi(x)
> \end{array}\right.
> $$
> 其中 $a(u)$ 是关于 $u$ 的 $C^1$ 函数，$\varphi(x)$ 是 $x\in \R$ 的 $C^1$ 函数且其 $C^1$ 模有界。证明上述 *Cauchy* 问题在上半平面 $\R^+ \times \R$ 上存在唯一的整体 $C^1$ 解的充要条件是：
> $$
> \frac{\mathbf {d} a(\varphi(x))}{\mathbf {d} x} \ge 0,\quad \forall x \in \R
> $$

<img src="C:\Users\17504\AppData\Roaming\Typora\typora-user-images\image-20240112151501967.png" alt="image-20240112151501967" style="zoom:60%;" />

<img src="C:\Users\17504\AppData\Roaming\Typora\typora-user-images\image-20240112151521968.png" alt="image-20240112151521968" style="zoom:67%;" />

<img src="C:\Users\17504\AppData\Roaming\Typora\typora-user-images\image-20240112151548150.png" alt="image-20240112151548150" style="zoom:60%;" />



> **(2) (10分)** 求下述 *Cauchy* 问题解的破裂时间：
> $$
> \left\{\begin{array}{l}
> u_{t}+ u u_x = 0 \\
> t=0:\ u = \exp(-x^2)
> \end{array}\right.
> $$
>

<img src="C:\Users\17504\AppData\Roaming\Typora\typora-user-images\image-20240112151743261.png" alt="image-20240112151743261" style="zoom:60%;" />



## 第二题

> **(1) (10分)** 求出满足极小曲面方程
> $$
> \left(1+u_y^2\right) u_{x x}-2 u_x u_y u_{x y}+\left(1+u_x^2\right) u_{y y}=0
> $$
>
> 的所有绕 $z$ 轴旋转的极小曲面，即具有 $u=f\left(\sqrt{x^2+y^2}\right)$ 形式的极小曲面.

解：令 $r=\sqrt{x^2+y^2}$，有：
$$
u_x = \frac{x}{r} f'(r),\ u_y = \frac{y}{r} f'(r) \\
u_{xx} = \frac{x^2 f''(r)}{r^2}-\frac{x^2 f'(r)}{r^3}+\frac{f'(r)}{r} \\
u_{yy} = \frac{y^2 f''(r)}{r^2}-\frac{y^2 f'(r)}{r^3}+\frac{f'(r)}{r} \\
u_{xy} = \frac{x y f''(r)}{r^2}-\frac{x y f'(r)}{r^3}
$$
代入方程，化简得到原方程等价为：
$$
r f''(r)+f'(r)^3+f'(r) = 0
$$
利用分离变量法求解上述ODE，得到解为：
$$
f(r) = \frac{1}{c_1}\ln \left(\sqrt{\left(c_1r\right){}^2-1}+c_1r\right)+c_2
$$
其中 $c_1 > 0, c_2 \in \R$.



> **(2) (10分)** 讨论 *Tricomi* 方程
> $$
> u_{yy} - yu_{xx} = 0
> $$
> 的类型，并在 $y > 0$ 的上半平面内将其化为标准型.

<img src="C:\Users\17504\AppData\Roaming\Typora\typora-user-images\image-20240112155233771.png" alt="image-20240112155233771" style="zoom:60%;" />

<img src="C:\Users\17504\AppData\Roaming\Typora\typora-user-images\image-20240112155246360.png" alt="image-20240112155246360" style="zoom:60%;" />

<img src="C:\Users\17504\AppData\Roaming\Typora\typora-user-images\image-20240112155308756.png" alt="image-20240112155308756" style="zoom:60%;" />

## 第三题

>**(1) (10分)** 求解波动方程 *Cauchy* 问题：
>$$
>\left\{\begin{array}{l}
>u_{t t}-c^2\left(u_{x x}+u_{y y}\right)=0 \\
>\left.u\right|_{t=0}=x^2(x+y),\left.\quad u_t\right|_{t=0}=0
>\end{array}\right.
>$$

解：

由 *Hadamard* 降维法： 
$$
u(t,x,y) = \frac{1}{2\pi c} \frac{\part}{\part t} \iint\limits_{r<ct} \frac{m^2(m+n)}{\sqrt{c^2t^2 -r^2 }}dmdn 
$$
其中 $r=\sqrt{(x-m)^2+(y-n)^2}$.

上式积分记为 $I$，利用三角换元：
$$
m=r\cos\theta+x \\
n=r\sin\theta+y
$$
有：
$$
\begin{aligned}
I &= \int_0^{ct} \frac{r}{\sqrt{c^2t^2 -r^2}} \int_0^{2\pi} m^2(m+n) d\theta dr \\
  &= \int_0^{ct} \frac{r}{\sqrt{c^2t^2 -r^2}} \int_0^{2\pi} (3x+y)r^2\cos^2\theta +x^2(x+y) d\theta \\ 
  &= \int_0^{ct} \frac{r}{\sqrt{c^2t^2 -r^2}} [ \pi (3x+y)r^2+ 2\pi x^2(x+y) ]dr \\
  &= \frac{2}{3}\pi c^3 t^3 (3x+y) + 2\pi ctx^2(x+y)
\end{aligned}
$$
代入公式得到：
$$
u(t,x,y) = (3x+y) c^2 t^2 + x^2(x+y)
$$


> **(2) (10分)** 求二维波动方程的**轴对称解**.

解: 利用二维波动方程柯西问题的积分表达式
$$
\begin{aligned}
u(x, y, t) & =\frac{1}{2 \pi c}\left[\frac{\partial}{\partial t} \iint_{\sum_{at}^M} \frac{\varphi(\zeta, \eta) d \zeta d \eta}{\sqrt{(c t)^2-(\zeta-x)^2-(\eta-y)^2}}\right. \\
& \left.+\iint_{\sum_{at}^M} \frac{\psi(\zeta, \eta) d \zeta d \eta}{\sqrt{(c t)^2-(\zeta-x)^2-(\eta-y)^2}}\right]
\end{aligned}
$$

由于 $u$ 是轴对称的 $u=u(r, t)$, 故其始值 $\varphi, \psi$ 只是 $r$ 的函数,,$u=\left.\right|_{t=0}=\varphi(r)$, $\left.u_t\right|_{t=0}=\psi(r)$, 又 $\sum_{a t}^M$ 为圆 $(\zeta-x)^2+(\eta-y)^2 \leq a^2 t^2$. 

记圆上任一点 $p(\zeta, \eta)$ 的矢径为 $\rho:$ $\rho=\sqrt{\zeta^2+\eta^2}$ . 圆心 $M(x, y)$ 其矢径为 $r=\sqrt{x^2+y^2}$ .

记 $s=\sqrt{(\zeta-x)^2+(\eta-y)^2}$ 则由余弦定理知, $\rho^2=r^2+s^2-2 r s \cos \theta$, 其中 $\theta$ 为 $o M$ 与 $M p$ 的夹角。选极坐标 $(s, \theta)$ 。
$$
\begin{gathered}
\varphi(\zeta, \eta)=\varphi(\rho)=\varphi\left(\sqrt{r^2+s^2-2 r s \cos \theta}\right), \\
\psi(\zeta, \eta)=\psi(\rho)=\psi\left(\sqrt{r^2+s^2-2 r s \cos \theta} \right)
\end{gathered}
$$

于是以上公式可写成
$$
\begin{aligned}
u(x, y, t)= & \frac{1}{2 \pi a}\left[\frac{\partial}{\partial t} \int_0^{a t} \int_0^{2 \pi} \frac{\varphi\left(\sqrt{r^2+s^2-2 r s \cos \theta}\right)}{\sqrt{(a t)^2-s^2}}\right.s d s d \theta \\
& \left.+\int_0^{a t} \int_0^{2 \pi} \frac{\left.\psi\left(\sqrt{r^2+s^2-2 r s \cos \theta}\right)\right]}{\sqrt{(a t)^2-s^2} }s d s d \theta\right]
\end{aligned}
$$

由上式右端容易看出, 积分结果仅和 $(r, t)$ 有关, 因此所得的解为轴对称解, 即
$$
\begin{array}{r}
u(r, t)=\frac{1}{2 \pi a}\left[\frac{\partial}{\partial t} \int_0^{a t} \int_0^{2 \pi} \frac{\varphi \left(\sqrt{r^2+s^2-2 r s \cos \theta}\right)} {\sqrt{(a t)^2-s^2}} s d s d \theta +\int_0^{a t} \int_0^{2 \pi} \frac{\psi\left(\sqrt{r^2+s^2-2 r \cos \theta}\right)}{\sqrt{(a t)^2-s^2}} s d s d \theta\right]
\end{array}
$$



## 第四题

> **(1) (10分)** 证明方程 $u_t=c^2 u_{x x}+\gamma u$ 具有 *Dirichlet* 边界条件的初边值问题的解的唯一性与稳定性，其中 $\gamma$ 为非负常数.

解: 作变换 $v(x, t)=u(x, t) \mathrm{e}^{-\gamma t}$, 则 $v(x, t)$ 满足方程 $v_t=c^2 v_{x x}$, 且有
$$
\begin{gathered}
\left.|v|_{x=\alpha}|=| u \mathrm{e}^{-\gamma t}\right|_{x=\alpha} \mid \leq B, \\
\left.|v|_{x=\beta}|=| u \mathrm{e}^{-\gamma t}\right|_{x=\beta} \mid \leq B, \\
\left.|v|_{t=0}|=| u\right|_{t=0} \mid \leq M .
\end{gathered}
$$

根据热传导方程的极值原理有
$$
|v(x, t)| \leq \max \{M, B\},
$$

而对任何 $t>0$
$$
|u(x, t)|=\left|v(x, t) \mathrm{e}^{\gamma t}\right| \leq \max \left\{M \mathrm{e}^{\gamma t}, B \mathrm{e}^{\gamma t}\right\} .
$$
为证唯一性只要证明问题
$$
\left\{\begin{array}{l}
u_t=c^2 u_{x x}+\gamma u, \\
\left.u\right|_{x=\alpha}=\left.u\right|_{x=\beta}=0, \\
\left.u\right|_{t=0}=0
\end{array}\right.
$$

只有零解. 事实上, 此时 $M=B=0$, 因此 $|u(x, t)| \leq 0$, 即 $u(x, t) \equiv 0$.

为证稳定性, 只要证明问题
$$
\left\{\begin{array}{l}
u_t=c^2 u_{x x}+\gamma u, \\
\left.u\right|_{x=\alpha}=\eta_1(t),\left.u\right|_{x=\beta}=\eta_2(t), \\
\left.u\right|_{t=0}=\varepsilon(x)
\end{array}\right.
$$

当 $\eta_1(t), \eta_2(t)$ 和 $\varepsilon(x)$ 微小时, 解亦微小. 设当 $t \leq T$ 时,
$$
\left|\eta_1(t)\right|<\eta,\left|\eta_2(t)\right|<\eta, \max |\varepsilon(x)|<\varepsilon,
$$

则对 $t \leq T, \alpha \leq x \leq \beta$, 成立
$$
|u(x, t)| \leq \max \left\{\eta \mathrm{e}^{\gamma t}, \varepsilon \mathrm{e}^{\gamma t}\right\} \leq \max \left\{\eta \mathrm{e}^{\gamma T}, \varepsilon \mathrm{e}^{\gamma T}\right\} .
$$

故此问题是稳定的.



> **(2) (10分)** 求解如下问题：
> $$
> \left\{\begin{array}{l}
> u_{t} = c^2 u_{x x}, & (t>0,\ 0 <x < 1) \\
> u(t,0) = u_x(t,1) = 0, & (t > 0) \\
> u(0,x) =  f(x), & (0 < x < 1)
> \end{array}\right.
> $$
>

解：

分离变量 $u(t,x)=T(t)X(x)$，代入热传导方程得：
$$
T'(t) + \lambda c^2 T(t) = 0 \\
X''(x) + \lambda X(x) = 0
$$
讨论$\lambda$，利用边界条件导出第二个方程的非平凡解为：
$$
X_k(x) = B_k \sin(\sqrt{\lambda_k} x) \\
\cos\sqrt{\lambda_k} = 0
$$
其固有值 $\lambda_k = (\tfrac{\pi}{2}+k\pi)^2, k \ge 0$.

将固有值代入 $T(t)$ 的方程，得：
$$
T_k(t) = C_k e^{-c^2\lambda_k t}
$$
即 $u$ 即按叠加原理写为：
$$
u(t,x) = \sum_{k=0}^{\infty} A_k e^{-c^2 (\tfrac{\pi}{2}+k\pi)^2  t} \sin [(\tfrac{\pi}{2}+k\pi)x],\ 0 < x<1
$$
有三角函数系正交性和初值条件，得待定系数的值为：
$$
A_k = 2\int_0^1 f(\xi) \sin [(\tfrac{\pi}{2}+k\pi)\xi] d\xi
$$


## 第五题

设 $D_1^+$ 表示半圆盘 $\{ (x,y) : x^2+y^2 < 1 ,\ y>0  \}$. 考虑如下带有 *Dirichlet* 边界的 *Poisson* 方程：
$$
\left\{  \begin{aligned}
 -\Delta u = f,\quad &\text{ in }D_1^+ \\
\ u=g,\quad &\text{ on } \part D_1^+
\end{aligned} \right.
$$
其中 $f$ 和 $g$ 分别是 $\overline{D_1^+}$ 和 $\part D_1^+$ 上的光滑函数.

> **(1) (10分)** 利用基本解 $\Phi(x) = (2\pi)^{-1} \log |x|$ 确定上述方程的格林函数 $G(x,y)$. 并由此给出上述方程解的积分表达式.

解：

<img src="C:\Users\17504\AppData\Roaming\Typora\typora-user-images\image-20240112165534568.png" alt="image-20240112165534568" style="zoom:67%;" />

记点 $M_0$ 对圆周的反演点为 $M_1$，对 $y=0$ 的反演点为 $M_0'$，$M_1$ 对 $y=0$ 的反演点为 $M_1'$. 则格林函数可写为：
$$
G(M,M_0) = \Phi(r_{MM_0}) - \Phi( r_0 r_{MM_1}) - \Phi(r_{MM_0'}) + \Phi( r_0' r_{MM_1'})
$$
其中 $r_0 = |OM_0|, r_0'=|OM_0'|$.

则解有 *Poisson* 公式：
$$
u(M_0) = \iint_{D^+_1} G(M, M_0) f(M) dM + \oint_{\part D_1^+} g(M) \frac{\part G(M,M_0)}{\part n} ds
$$


> **(2) (10分)** 使用极值原理证明 **(1)** 中解的唯一性.

证明：

反证，若有两解 $u_1 \ne u_2$，记 $v=u_1-u_2$.
$$
\left\{  \begin{aligned}
 -\Delta v = 0,\quad &\text{ in }D_1^+ \\
\ v=0,\quad &\text{ on } \part D_1^+
\end{aligned} \right.
$$
由极值原理知 $v$ 在区域 $D_1^+$ 上的最大值最小值均为0，则 $v\equiv 0$，矛盾.



> **(3) (附加题 10分)** 设 $f \equiv 0$，证明半圆域 $D_1^+$ 内任意半径为 $r$ 的圆盘有：
> $$
> u(x) = \frac{1}{2\pi r} \int_{|y-x|=r} u(y) d l_y
> $$
> 其中 $dl_y$ 是圆 $\{y: |y-x|=r \}$ 上的弧微分.

证明：

$f \equiv 0$ 意味着解 $u$ 是调和函数。记等式右端为 $I(r)$：
$$
\begin{aligned}
I(r) &= \frac{1}{2\pi r} \int_{|z|=r} u(x+z) d l_z = \frac{1}{2\pi } \int_{|z|=1} u(x+rz) d l_z  \\
I'(r) &= \frac{1}{2\pi } \int_{|z|=1} D u(x+rz)\cdot z d l_z  \\
&= \frac{1}{2\pi r} \int_{|y-x|=r} D u(y)\cdot \frac{y-x}{r} d l_y  \\
&= \frac{1}{2\pi r} \int_{|y-x|=r} \frac{\part u}{\part \nu} d l_y \qquad \text{方向导数}\\
&= \frac{1}{2\pi r} \int_{B_x^r} \Delta u  d S  \qquad \text{格林第一公式}\\
&= 0 \qquad \text{u调和}\\

\end{aligned}
$$
 即有：
$$
I(r) = \lim_{r \to 0} I(r) = \lim_{r \to 0} \frac{1}{2\pi r} \int_{|z|=r} u(x+z) d l_z = u(x)
$$

**(4) (附加题 10分)** 在仅假设 $f\in L^2 (D_1^+), g\equiv 0$ 的情形下，证明 $u\in H^2 (D_1^+)$.

由 如下定理 (Adolfsson, 1992[^1])：

<img src="C:\Users\17504\AppData\Roaming\Typora\typora-user-images\image-20240112215520753.png" alt="image-20240112215520753" style="zoom:50%;" />

仅需验证 $D^+_1$ 是一致Lipschitz区域，容易发现这是显然的（总有外切直线）。从而由先验不等式：
$$
\|u\|_{H^2(D_1^+)} \le C \|f\|_{L^2(D_1^+)}
$$


[^1]: ADOLFSSON, VILHELM. “L2-INTEGRABILITY OF SECOND ORDER DERIVATIVES FOR POISSON’S EQUATION IN NONSMOOTH DOMAINS.” *Mathematica Scandinavica*, vol. 70, no. 1, 1992, pp. 146–60. *JSTOR*, http://www.jstor.org/stable/24492539.