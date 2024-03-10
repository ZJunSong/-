# 浙江大学2023-2024学年秋冬学期

<div align='center'><font size='4'><b>《偏微分方程》课程期末考试试卷</b></font></div>

<div align='center'>
    <font size='3'>
        开课学院：数学科学学院, 考试形式：闭卷、不允许带资料入场
    </font>
    </br>
    <font size='3'>
        考试时间：2024 年 1 月 12 日 10:30 ~ 12:30
    </font>
</div>

   考生姓名：$\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_$  学号：$\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_$ 专业：$\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_$

| 题号 | 一   | 二   | 三   | 四   | 五   | 总分 |
| ---- | ---- | ---- | ---- | ---- | ---- | ---- |
|      |      |      |      |      |      |      |

## 第一题

**(1) (10分)** 考虑如下 *Cauchy* 问题：
$$
\left\{\begin{array}{l}
u_{t}+a (u)u_x = 0 \\
u(0,x) = \varphi(x)
\end{array}\right.
$$
其中 $a(u)$ 是关于 $u$ 的 $C^1$ 函数，$\varphi(x)$ 是 $x\in \R$ 的 $C^1$ 函数且其 $C^1$ 模有界。证明上述 *Cauchy* 问题在上半平面 $\R^+ \times \R$ 上存在唯一的整体 $C^1$ 解的充要条件是：
$$
\frac{\mathbf {d} a(u)}{\mathbf {d} x} \ge 0,\quad \forall x \in \R
$$
**(2) (10分)** 求下述 *Cauchy* 问题解的破裂时间：
$$
\left\{\begin{array}{l}
u_{t}+ u u_x = 0 \\
t=0:\ u = \exp(-x^2)
\end{array}\right.
$$

## 第二题

**(1) (10分)** 求出满足极小曲面方程
$$
\left(1+u_y^2\right) u_{x x}-2 u_x u_y u_{x y}+\left(1+u_x^2\right) u_{y y}=0
$$

的所有绕 $z$ 轴旋转的极小曲面，即具有 $u=f\left(\sqrt{x^2+y^2}\right)$ 形式的极小曲面.

**(2) (10分)** 讨论 *Tricomi* 方程
$$
u_{yy} - yu_{xx} = 0
$$
的类型，并在 $y > 0$ 的上半平面内将其化为标准型.

## 第三题

**(1) (10分)** 求解波动方程 *Cauchy* 问题：
$$
\left\{\begin{array}{l}
u_{t t}-c^2\left(u_{x x}+u_{y y}\right)=0 \\
\left.u\right|_{t=0}=x^2(x+y),\left.\quad u_t\right|_{t=0}=0
\end{array}\right.
$$
**(2) (10分)** 求二维波动方程的**轴对称解**.

## 第四题

**(1) (10分)** 证明方程 $u_t=c^2 u_{x x}+\gamma u$ 具有 *Dirichlet* 边界条件的初边值问题的解的唯一性与稳定性，其中 $\gamma$ 为非负常数.

**(2) (10分)** 求解如下问题：
$$
\left\{\begin{array}{l}
u_{t} = c^2 u_{x x}, & (t>0,\ 0 <x < 1) \\
u(t,0) = u_x(t,1) = 0, & (t > 0) \\
u(0,x) =  f(x), & (0 < x < 1)
\end{array}\right.
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

**(1) (10分)** 利用基本解 $\Phi(x) = (2\pi)^{-1} \log |x|$ 确定上述方程的格林函数 $G(x,y)$. 并由此给出上述方程解的积分表达式.

**(2) (10分)** 使用极值原理证明 **(1)** 中解的唯一性.

**(3) (附加题 10分)** 设 $f \equiv 0$，证明半圆域 $D_1^+$ 内任意半径为 $r$ 的圆盘有：
$$
u(x) = \frac{1}{2\pi r} \int_{|y-x|=r} u(y) d l_y 
$$
其中 $dl_y$ 是圆 $\{y: |y-x|=r \}$ 上的弧微分.

**(4) (附加题 10分)** 在仅假设 $f\in L^2 (D_1^+), g\equiv 0$ 的情形下，证明 $u\in H^2 (D_1^+)$.