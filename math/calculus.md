微积分 上册

# 常微分方程
## 线性常微分方程 P217
### 齐次方程
$$y^{(n)}+a_1(x)y^{(n-1)}+a_2(x)y^{(n-2)}+...a_n(x)y=0$$
### 非齐次方程
$$y^{(n)}+a_1(x)y^{(n-1)}+a_2(x)y^{(n-2)}+...a_n(x)y=f(x)$$
### 解的结构
1. 齐次
$$y=C_1y_1+C_2y_2+...+C_ny_n$$
2. 非齐次
$$y=C_1y_1+C_2y_2+...+C_ny_n+y^*$$
$y^*$ 唯一且系数为1

## 常系数微分方程
### 齐次方程 P222
考虑$$y''+ay'+by=0$$
有特征方程$$\lambda^2+a\lambda+b=0$$
有以下情况
1. 方程有互异实根 $\lambda_1\ne\lambda_2$
$$y=C_1e^{\lambda_1x}+C_2e^{\lambda_2x}$$
2. 方程有二重实根
$$y=(C_1+xC_2)e^{\lambda x}$$
3. 方程有共轭虚根 $a+bi$
$$y=(C_1sin bx+C_2cos bx)e^{ax}$$
4. 高阶的情况(详见P224)
    * n重实根(其中n个线性无关解)
    $$(C_1+xC_2+...+x^nC_n)e^{\lambda x}$$
    * 多重共轭复根(其中第i个线性无关解)
    $$(C_1sin bx+C_2cos bx)x^ie^{ax}$$

### 非齐次方程 P225
考虑$$y''+ay'+by=f(x)$$
$P_m(x)$ 为m次多项式
通过判断 特解 $y^*$ 的形式
将 $y^*$ 代入微分方程确定未知系数
从而得到特解
1. $$f(x)=P_m(x)e^{ax}$$$$y^*=Q(x)e^{ax}$$
    1. a 不是特征方程的根
    $$Q(x)=Q_m(x)=b_0+b_1x+...+b_mx^m$$
    2. a 是特征方程的单根
    $$Q(x)=xQ_m(x)$$
    3. a 是特征方程的n重根
    $$Q(x)=x^nQ_m(x)$$
2.  $$f(x)=[P(x)cos bx+Q(x)sin bx]e^{ax}$$$P(x),Q(x)$ 为==最高次为m的多项式==
$$y^*=x^k[A(x)cos bx+B(x)sin bx]e^{ax}$$
$A(x),B(x)$ 均为==m次多项式==
$k$ 为 $\lambda=a+bi$ 在原特征方程的重数

### 欧拉方程 P228
$$x^ny^{(n)}+a_1x^{n-1}y^{(n-1)}+...+a_ny=f(x)$$
通过代换 $x=e^t$ 化为常系数线性微分方程
规定
$$D^iy=\frac{d^iy}{dt}=y^{(i)}$$
$$D^0y=y$$
代换时有
$$xy'=Dy$$
$$x^2y''=D(D-1)y$$
$$x^ky^{(k)}=D(D-1)...(D-k+1)y$$
* 注意, 代换后 f(x) 也会改变为 t 的函数
---
微积分 下册
# 空间几何
## 方向余弦
$$\vec{a} = \{a_x, a_y, a_z\}$$
$$cos\alpha = \frac{a_x}{|\vec{a}|},\;
cos\beta = \frac{a_y}{|\vec{a}|},\;
cos\gamma = \frac{a_z}{|\vec{a}|}$$
角度为$\vec{a}$与对应坐标轴的夹角
### 性质
$$cos^2\alpha + cos^2\beta + cos^2\gamma = 1$$
将一组与 $a_x, a_y, a_z$ 成比例的数称为 $\vec{a}$ 的方向数。
一组方向数非零且与$\vec{a}$共线
## 平面方程
### 一般方程
$$Ax+By+Cz+D=0$$
$\{A,B,C\}$为平面法向量，$D$由平面过的点决定
### 截距式
$$\frac{x}{a}+\frac{y}{b}+\frac{z}{c}=1$$
$\{a,b,c\}$为截距
## 直线方程
### 一般方程
$$A_1x+B_1y+C_1z+D_1=0\\
A_2x+B_2y+C_2z+D_2=0$$
为任意两个不同的过直线的平面
### 点向式
$$\frac{x-x_0}{a}=\frac{y-y_0}{b}=\frac{z-z_0}{c}$$
$\{x_0, y_0, z_0\}$为直线过的点
$\{a,b,c\}$为直线方向矢量
$a = 0$时单独表示$x = x_0$
### 参数方程
$$\vec{r} = \vec{r_0} + \vec{s}t$$
### 转换
一般转点向
$$\{A_1, B_1, C_1\} \times \{A_2, B_2, C_2\} = \{a,b,c\}\\
令x_0 = m 解出\\\{x_0, y_0, z_0\}$$
## 距离问题
### 点到平面
$$d = \frac{|Ax+By+Cz+D|}{\sqrt{A^2+B^2+C^2}}$$
### 点到直线
$$d=\frac{|\vec{s}\times\vec{PP_0}|}{|\vec{s}|}$$
$\vec{s}$ 直线的方向矢量(直角边)
$\vec{PP_0}$ 直线上的一点到计算点的矢量(斜边)
叉乘得到两者夹角乘以$sin\theta$
### 异面直线
$$\frac{|[\vec{s_1}\;\vec{s_2}\;\vec{P_1, P_2}]|}{|\vec{s_1}\times\vec{s_2}|}$$
$\vec{s_1}$ 第一条线的方向矢量
$\vec{s_2}$ 第二条线的方向矢量
$\vec{P_1, P_2}$ 直线上两点的矢量
$\vec{s_1}$，$\vec{s_2}$，$\vec{P_1, P_2}$ 构成一个三棱柱，通过混合积计算出其面积，除以 $\vec{s_1}$，$\vec{s_2}$ 构成的面，得到此面的高，即异面直线距离
## 角度问题
### 两面夹角
$$cos\theta=cos<\vec{n_1},\vec{n_2}>$$
### 两线夹角
$$cos\theta=cos<\vec{s_1},\vec{s_2}>$$
### 线面夹角
$$sin\varphi = |cos<\vec{n},\vec{s}>|$$
注意
$$0\le\varphi\le\frac{\pi}{2}$$
## 直线关系
### 共面
异面距离为0
$$[\vec{s_1}\;\vec{s_2}\;\vec{P_1, P_2}]=0$$
### 平行
$$\vec{s_1}\times\vec{s_2} = 0$$
$\vec{s_1}$ 与 $\vec{s_2}$ 成比例
## 平面束方程 P27
$$A_1x+B_1y+C_1z+D_1+\mu(A_2x+B_2y+C_2z+D_2)=0$$
表示过直线的任意平面
用于求过已知直线的特定平面
## 曲面
### 旋转曲面
求任意曲线绕轴旋转得到的曲线
1. 化为参数方程 或直接令$z=t$
2. $$
z=z(t)\\
x^2(t)+y^2(t)=f^2(t)$$
3. $$
x^2+y^2=f^2(z)$$

### 曲面参数方程
$$x=x(u,v)\\
y=y(u,v)\\
z=z(u,v)$$
二维, 两个参数
## 曲线
###  一般方程
$$f(x,y,z)=0\\
g(x,y,z)=0
$$
两个曲面相交
### 参数方程
$$x=x(t)\\
y=y(t)\\
z=z(t)$$
一维, 一个参数
### 投影曲线
对于曲线L
$$f(x,y,z)=0\\
g(x,y,z)=0$$
消去方程组的z(投影到xy面)得到投影曲线
$$F(x,y)=0\\
z=0(不可少, 表示xy面上的曲线)
$$
## 二次曲线
### 椭球面
$$\frac{x^2}{a^2}+\frac{y^2}{b^2}+\frac{z^2}{c^2}=1
$$
全为正
### 单叶双曲面
$$\frac{x^2}{a^2}+\frac{y^2}{b^2}-\frac{z^2}{c^2}=1
$$
一个为负
zx截面为交于x轴的双曲线
xy截面为椭圆
### 双叶双曲面
$$-\frac{x^2}{a^2}-\frac{y^2}{b^2}+\frac{z^2}{c^2}=1
$$
两个为负
zx截面为交于z轴的双曲线
xy截面为椭圆或无
### 椭圆抛物线
$$\frac{x^2}{a^2}+\frac{y^2}{b^2}=z$$
对照$x^2=y$
没有常数项
### 椭圆锥面
$$\frac{x^2}{a^2}+\frac{y^2}{b^2}=\frac{z^2}{c^2}$$
或
$$\frac{x^2}{a^2}+\frac{y^2}{b^2}-\frac{z^2}{c^2}=0$$
注意区别, 椭圆锥面没有常数项
# 多元函数
## 极限
### 求极限
1. 令$t=x^2+y^2$
2. 分离加法
3. 夹逼
$$\frac{x+y}{2}\ge\sqrt{xy}$$
4. 因式分解
$$\frac{x^3+y^3}{x+y}=x^2-xy+y^2$$
5. $$\lim_{x\to0}(1+x)^{\frac{1}{x}}=e$$
错误注意
$$\lim_{x\to0}(1+\frac{1}{x})^{x}=1$$

### 极限不存在
1. 趋近于无穷(使分母为0)
2. 令y=f(x) (y=0 或 y=kx) 极限结果不唯一, 与k有关

## 微分学
### 偏导
$$f_x=\lim_{\Delta x\to0}\frac{f(x+\Delta x,y)-f(x,y)}{\Delta x}$$
### 连续
$$\lim_{P\to P_0}F(P) = F(P_0)$$
### 偏导存在但不连续
$$f(x,y)=\begin{cases}
\frac{xy}{x^2+y^2}&,\;x^2+y^2\ne 0,\\
0&,\;x^2+y^2=0
\end{cases}$$
令y=kx极限与k有关,不存在
### 连续但偏导不存在
$$f(x,y)=\sqrt{x^2+y^2}\\
$$
$f(0,0)$处x,y偏导均为无穷(不存在)
### 混合偏导
$f_{xy},\;f_{yx}$存在且连续时有
$f_{xy}=f_{yx}$
### 全微分
1. 当$f(P)$可微, 则$f_x(P)与$$f_y(P)$存在且
$$df(P)=f_x(P)dx+f_y(P)dy+o(\rho)$$
2. 当$F_x(P)与$$F_y(P)$存在且==偏导数连续==则F(x, y)与P处可微(==仅充分条件==)
3. 当$F_x(P)与$$F_y(P)$不连续时满足
$$\lim_{\rho\to 0}\frac{[f(x+\Delta x,y+\Delta y)-f(x,y)]-f_x(x,y)\Delta x-f_y(x,y)\Delta y}{\rho}=0$$
$$\rho=\sqrt{\Delta x^2+\Delta y^2}$$
也可微(定义的变形, 用于不连续的情况)
4. 可微则一定有一阶偏导且==原函数连续==, 连续不一定可微

### 复合微分 P60
1. 记号
设 $f(x_1,x_2,...,x_i,...)$
记 $f'_i=\frac{\partial f}{\partial x_i}$
2. 对所有含微分变量的函数求偏导, 乘法注意乘法法则
对于 $f(x,xy)$ $f'_1$ ==也是y的函数==, 不能忽视

### 隐函数微分 P65
* 找出自变量(题目最终要求的偏导的自变量, 其他均看作关于自变量的函数)
* 全微分后对所有式子除以自变量的微分(自变量组则分别除以自变量组中的自变量)
* 除了自变量组以外的==因变量除以自变量的微分时, 变为偏微分, 且不可消去==
1. $$dx=f_1du+f_2dv(草稿纸)\\
1=f_1\frac{\partial u}{\partial x}+f_2\frac{\partial v}{\partial x}$$
2. $$dy=g_1du+g_2dv(草稿纸)\\
0=g_1\frac{\partial u}{\partial x}+g_2\frac{\partial v}{\partial x}$$
3. 结合两个方程解出 $\frac{\partial u}{\partial x}$ 与 $\frac{\partial v}{\partial x}$

## 微分学几何应用
### 方向导数 P69
1. 对于向量 $\vec{n}$
沿 $\vec{n}$ 方向的导数为
$$\frac{\partial f(P)}{\partial n}=\lim_{s\to 0^+}\frac{f(P+s\vec{n})-f(P)}{s\sqrt{a^2+b^2+c^2}}$$
注意, 由于方向导数中 ==$s\to 0^+$== 与偏导不同, 因此轴向的方向导数的值与对应偏导无关
2. 当f(P)可微, 有
$$\frac{\partial f(P)}{\partial n}=\{f_x(P),f_y(P),f_z(P)\}\cdot \vec{n^0}$$

### 梯度
$$grad f(P)=\{f_x(P),f_y(P),f_z(P)\}=\nabla f(P)$$
#### 意义
曲面
$$F(x, y, z)=m$$
1. m的各个取值构成无数个曲面层
2. 取层上的点P处微面 $dS_m$ , $dS_m$ 近似为平面, 且平行于 $dS_{m+dm}$
3. $grad f(P)$ 为使方向导数最大的方向, 在此方向, 到达 $dS_{m+dm}$ 距离最短
4. 两平面间, 垂直线段距离最短
5. $grad f(P)$ 即为法矢量

### 曲线应用 P73
有无数条线垂直于曲线 $\to$ ==唯一法平面== 
曲线上的一点只有==唯一切线==
设$$L:\vec{r} =\vec{s}(t)$$
$$\vec{r}(t)=P\{x_0, y_0, z_0\}$$
有切矢量$$\vec{r'}(t)=\{x'(t),y'(t),z'(t)\}$$
当 $\vec{r'}$ 连续, 存在且 ==$\vec{r'}\ne\vec{0}$== 则 $\vec{r}$ 为光滑曲线
切线(以切矢量为方向矢量), 法平面(以切矢量为法矢量)具体见书
#### 一般方程曲线的切矢量
设曲线方程:
$$F(x,y,z)=0\\
G(x,y,z)=0
$$
曲线于P的切矢量必然垂直于两曲面的法矢量
$$\therefore \vec{r'}(P)=grad F(P) \times grad G(P)$$
### 曲面应用
平面有法矢量 $\to$ 曲面上一微元视为平面, 也有==唯一法线==
有无数条线可以切于平面的一点 $\to$ 有==唯一切平面==
设曲面(两个自由度, 为面)
$$F(x, y, z)=C$$
其切矢量为
$$grad F$$
### 自由极值 P80
#### 驻点
$f_x(P)=f_y(P)=0$
成P为 $f(x,y)$ 的驻点
#### 极值点充分条件
对于驻点 $P_0$ 
$$\Delta = f_{xx}f_{yy}-f_{xy}^2$$
1. $\Delta>0, A<0\;P_0$ 为极小值点 
2. $\Delta>0, A>0\;P_0$ 为极大值点 
3. $\Delta<0$ 不是极值点
4. $\Delta=0$ 不确定

#### 求极值
1. 找出区域内所有驻点
2. 找出区域内==一阶偏导不存在的点==
3. 找出==边界上所有极值点==
4. 比较所有受检点, 得出极值于极值点

### 条件极值 P84
已知 $g(x,y)=0$
求函数 $z=f(x,y)$ 极值 
构造辅助变量 $\lambda$
构造辅助函数
$$L(x,y,\lambda)=f(x,y)+\lambda g(x,y)$$
检验 $L(x,y,\lambda)$ 的所有驻点, 即可求出条件极值
#### 多条件极值
$$L(x,y,\lambda, \mu)=f(x,y)+\lambda g(x,y)+\mu h(x,y)$$
其他同
#### 隐函数极值
已知 $f(x,y,z)=0$ (条件)求 $max\{z\}$ (目标)
即
$$L(x,y,z,\lambda)=z+\lambda f(x,y,z)$$
# 级数
## 级数性质 P187
1. 当级数收敛
$$\lim_{n\to\infty}a_n=0$$
2. 绝对收敛的级数任意改变加的顺序结果不变
条件收敛/发散的数列改变加的顺序结果不唯一
3. $a_n\ge b_n$ 有 $\sum a_n\ge\sum b_n$

## 正项级数 P188
称 $a_n\ge0$ 的级数为正项级数,
==以下判别法仅用于正项级数==
使用以下判别法时必须保证数列上的项大于等于0
$$1.a_n\ge0\;2.|a_n|\;3.a_n^2$$
### 一般比较判别法 P188
* 条件: n足够大时有 $a_n\ge b_n$
* 当 $a_n$ 收敛则 $b_n$ 收敛
* 当 $b_n$ 发散则 $a_n$ 收敛
### 极限比较判别法
$$\lim_{n\to\infty}\frac{a_n}{b_n}=l$$
* $l=\infty$ $a_n$ 收敛则 $b_n$ 收敛
* $l=0$ $a_n$ 发散则 $b_n$ 发散
* 极限存在且不为0 $a_n$ 与 $b_n$ 敛散性相同
### 比值判别法 P189
$$\lim_{n\to\infty}\frac{a_{n+1}}{a_n}=l$$
* $l>1$ 级数发散
* $l<1$ 级数收敛
* $l=1 $ 不确定
* 用于含有阶乘的级数
* 含有积分时可用洛必达法则
### 根值判别法
$$\lim_{n\to\infty}\sqrt[n]{a_n}=l$$
* $l>1$ 级数发散
* $l<1$ 级数收敛
* $l=0$ 不确定
* 用于含有n次方的级数
### 积分判别法 P190
* 条件: ==f(x) 在 $[1, +\infty)$ 非负且单调递减==
* 当 $\int_1^\infty f(x)dx$ 收敛时, 级数 $a_n=f(n)$ 收敛
* 用于级数为分数时
### 比阶判别法 P191
$$\lim_{n\to\infty}n^pa_n=l$$
$$\lim_{n\to\infty}a_n\sim\lim_{n\to\infty}n^{-p}$$
* 级数 $\sum\frac{1}{n}$ 发散
* 要求极限结果 $l$ 存在
* $p>1\;0\le l<\infty$ 级数收敛
* $p\le1\;0<l\le\infty$ 级数发散
* 通过寻找 $a_n$ 的等价无穷小判断p
### 常用等价无穷小
$$x \sim sin x \sim tan x \sim arcsin x\sim arctan x\;(x \to 0)$$
$$1-cos x\sim x^2(x \to 0)$$
$$(1+x)^n - 1 \sim nx\;(x \to 0)$$
$$\lim_{x\to \infty}(1 + \frac{1}{x})^x = \lim_{x\to 0}(1 + x)^{\frac{1}{x}}=e$$
$$a^x - 1 = e^{x lna} - 1 \sim x lna $$
$$ln(1 + x) \sim x(x \to 0)$$
## 变号级数
变号级数为正项与负项有无限多的级数
### 莱布尼兹判别法 P193
$a_n$ 为正项级数
当 $|a_n|$ 严格单调递减且收敛于0时有
$$\sum(-1)^na_n = S$$收敛, 且$S\le a_0$
### 特殊的莱布尼兹判别法
当 $|a_n|$ 从某项开始单调递减且收敛于0时有
$$\sum(-1)^na_n = S$$收敛
但$S\le a_0$==不成立==
### 绝对/条件收敛 P194
$$\sum|a_n|=S$$
$$\sum a_n=S'$$
* $S$ 存在表明 $a_n$ 绝对收敛, 且 $S'$ 存在
* $S'$ 存在, $S$ 不存在表明 $a_n$ 条件收敛
* 仅绝对收敛可以任意改变求和顺序而不影响结果

## 幂级数 P203
幂级数定义
$$\sum a_nx^n$$或
$$\sum a_n(x-x_0)^n$$
$a_n$ 为系数
### 收敛半径
对于幂级数都存在一个收敛半径 R
* 幂级数在 $x\in(-R,R)$ 内级数绝对收敛且一致收敛(可积分求导)
* 幂级数在 $x\notin[-R,R]$ 级数发散
* $x=\pm R$ 时, ==需要单独验证 绝对/条件收敛或发散==
* 推论: 幂级数只会在收敛半径处条件收敛($x_0=0$)
* 收敛半径求法
* 求类幂级数的收敛半径 P204
$$\lim_{n\to\infty}|\frac{a_{n+1}}{a_n}|=\frac{1}{R}$$
### 泰勒级数 P208
$$e^x=\sum_{n=0}^\infty\frac{x^n}{n!}$$
$$sin x=\sum_{n=1}^\infty \frac{(-1)^{n+1}x^{2n-1}}{(2n-1)!}$$
$$cos x=\sum_{n=0}^\infty \frac{(-1)^nx^{2n}}{(2n)!}$$
==级数从0开始==
$$\frac{1}{1-x}=\sum_{n=0}^\infty x^n ;\;x\in(-1,1)$$
错位相减法
注意收敛范围 级数从1开始
$$ln(x+1)=\sum_{n=1}^\infty(-1)^{n+1}\frac{x^n}{n};\;x\in[-1,1)$$
(求导后, 用-x代换得到上式)
#### 求函数的泰勒展开
1. 注意要求展开的 $x_0$
2. $x_0\ne0$ 可令 $t=x-x_0$ 
3. 展开前提出常数 $e^{x+5}=e^5e^x$
4. 展开(对数或分数) $F(x) = g(x) + f(x)$ 新的收敛范围为两个函数收敛范围的交集 

#### 由泰勒展开求函数 P212
1. 对于含有n的项可以整体求导
    * eg $$\frac{d}{dx}(\sum_{n=0}^\infty x^n)=\sum_{n=0}^\infty nx^{n-1}=\frac{1}{(1-x)^2}$$
2. 对于缺少的x可以直接乘上(x视为常数)
    * eg $$\sum_{n=0}^\infty x^{n+1}=x\sum_{n=0}^\infty x^n=\frac{x}{1-x}$$
3. 含 $n!$ 时, 套用 $e^x\;sin x\;cos x$
4. 化为常微分方程 寻找S, S', S'' 等的关系
5. 错位相减
6.  整体代换(n的系数不为1时)
    * eg $$\sum_{n=0}^\infty x^{2n}=\sum_{n=0}^\infty (x^2)^{n}=\frac{1}{1-x^2}$$

### 傅里叶级数 P217
$$\{\frac{1}{\sqrt{2\pi}},\frac{1}{\sqrt{\pi}}cos n\theta,\frac{1}{\sqrt{\pi}}sin m\theta\}$$
函数组中任意两个函数乘积在 $[-\pi,\pi]$ 上的积分结果为0
函数组中相同的函数乘积在 $[-\pi,\pi]$ 上的积分结果为1
$$a_n=\frac{1}{\pi}\int_{-\pi}^{\pi}f(x)cos nx dx$$
$$b_n=\frac{1}{\pi}\int_{-\pi}^{\pi}f(x)sin nx dx$$
$$a_0=\frac{1}{\pi}\int_{-\pi}^{\pi}f(x) dx$$
$$f(x)\sim \frac{a_0}{2}+\sum_{n=1}^\infty(a_n cos nx+b_n sin nx)$$
#### 注意
* ==$a_0$ 有一个系数 $\frac{1}{2}$==
* 级数的下限为1
* 必须使用 $\sim$ 连接
#### Dirichlet条件
1. f(x) 在 $[a,b]$ 上连续或只有==有限个第一类间断点==
    * $\frac{1}{x}$ 在0处为第二类间断点
2. f(x) 在 $[a,b]$ 上分段单调或可微

当函数在 $[-\pi,\pi]$ 满足此条件则其傅里叶级数处处收敛, 周期为 $2\pi$
#### 傅里叶级数的表达式
$$S(x)=\begin{cases}
f(x),x\in(-\pi,\pi)且f在x连续,\\
\frac{f(x^+)+f(x^-)}{2},x\in(-\pi,\pi)且f在x不连续,\\
\frac{f((-\pi)^+)+f((\pi)^-)}{2},x=\pm\pi
\end{cases}$$
当f(x)为==分段函数时特别注意其间断点==应使用左右极限的极值的平均值
#### 正弦/余弦级数
* 当f(x)为奇函数, $a_n=0$ , 级数中仅有正弦函数, 称为正弦级数
* 当f(x)为偶函数, $b_n=0$ , 级数中仅有余弦函数, 称为正弦级数
#### 奇/偶延拓
对于一个函数仅在 $[0,\pi]$ 定义时, 可以假设为奇/偶函数并展开为正弦/余弦级数
即仅计算 $a_n$ / $b_n$
注意:
1. 奇延拓 $S(x)=0,\;x=\pi 或 0$ (奇函数与x=0的值为0)
2. 偶延拓
    * $S(x)=f(0^+),\;x=0$
    * $S(x)=f(\pi^-),\;x=\pi$
3. 注意奇延拓与偶延拓的取值与一般展开的区别
4. ==偶延拓中第一项仍然是 $\frac{a_0}{2}$==
5. 奇延拓
将f(x)直接视为奇函数, 奇函数乘奇函数为偶函数, 使用对称性, ==乘上系数2, 区间变为(0,$\pi$)== $$b_n=\frac{2}{\pi}\int_{0}^{\pi}f(x)sin(nx)dx$$
6. 偶延拓
同上, ==乘上系数2, 区间变为(0,$\pi$)==
 $$a_n=\frac{2}{\pi}\int_0^{\pi}f(x)cos(nx)dx$$

# 重积分
多重积分时不可带入区域方程
仅线面积分时, 才可带入
## 二重积分
### 对称性 P107 P115
计算前优先考虑
1. 区域关于坐标轴的对称性
(带入-x区域不变)
2. x,y,z的轮换性
(交换x,y,z区域不变(球), 则可交换f(x,y,z)中的x,y,z)

### 极坐标代换 P100
$$x=r cos\theta$$
$$y=r sin\theta$$
$$|J|=r$$
1. 注意x, y 是否是标准的圆方程
2. 注意计算 $r$ 与 $\theta$ 的范围(画图)(垂直为 $\frac{\pi}{2}$), 有时 $r$ 可能是 $\theta$ 的函数
    * e.g.
    $$\begin{aligned}
    (x-1)^2+y^2&=1\\
    x^2+y^2&=2x\\
    r^2&=2r cos\theta
    \end{aligned}\\
    \therefore 0\le r\le 2cos\theta\\
    -\frac{\pi}{2}\le\theta\le\frac{\pi}{2}$$
3. ==代换后要乘上代换因子 $|J|$==
4. 其他注意 P122

## 三重积分
### 柱坐标代换
$$x=r cos\theta$$
$$y=r sin\theta$$
$$z=z$$
$$|J|=r$$
### 球坐标代换
$$x=r cos\theta sin\varphi$$
$$y=r cos\theta sin\varphi$$
$$z=r cos\varphi$$
$$|J|=r^2sin\varphi$$
* $\varphi$ 为圆心到球面的矢量==关于z轴的夹角==
* 完整球体中 $\varphi \in [-\frac{\pi}{2},\frac{\pi}{2}]$
## 曲线积分
不可使用对称性
但可以将曲线方程带入被积函数化简
化为相应的多重积分时优先考虑对称性
### 第一型曲线积分 P132
可以使用对称性
积分对象要转化为参数方程
$$dl=\sqrt{x'^2(t)+y'^2(t)+z'^2(t)}dt$$
$$\int_lf(x,y,z)dl=\int_{t_0}^{t_1}f(x(t),y(t),z(t))\sqrt{x'^2(t)+y'^2(t)+z'^2(t)}dt$$
### 第二型曲线积分 P137
不可使用对称性
积分对象要转化为参数方程
规定(==注意P,Q,R是关于x,y,z的函数, x,y,z是关于t的函数==(参数方程))
$$P=P(x,y,z)\;Q=Q(x,y,z)\;R=R(x,y,z)$$
$$\int_L\{P,Q,R\}\cdot d\vec{l}=\int_LPdx+Qdy+Rdz=\int_{t_0}^{t_1}[Px'(t)+Qy'(t)+Rz'(t)]dt$$
### 格林公式 P141
#### 区域概念
设 L 围住区域 D
1. 正向
沿 L 移动时, 如果 D 始终在左侧, 则称 L 的方向为正向
    * L为单连通时, 为逆时针方向
    * L为复连通时, 内部的曲线为顺时针方向
2. 简单闭曲线
分段光滑且不与自身相交的闭曲线
    * 8字型与自身相交不是这种曲线
    * 同心圆不相交, 符合条件

#### 格林公式
仅用于二维
1. L为简单闭曲线 且积分时沿 L 正向
2. D内与L上 ==P,Q有一阶连续偏导== 
$$\oint_L\{P,Q\}\cdot d\vec{l}=\int_D(Q_x-P_y)dx dy$$
#### 普通曲线 P144
1. 添加辅助线段补为闭曲线
2. 减去补充的曲线

### 曲线积分与路径无关的条件 P147
==D 是单连通区域==, ==P Q 在 D 内有一阶连续偏导==, 当在D内满足以下任一条件, 曲线积分与路径无关
(D内可以是任意路径, 仅与初末点的位置有关)
$$du=Pdx+Qdy\iff Q_x=P_y\iff D内曲线积分与路径无关$$
#### 曲线积分与环路路径无关的条件 P149
当存在有限个 $M$ 使 $P,Q$ 没有一阶连续偏导时(==分母为0==)
曲线积分与==环路路径==无关
利用此方法可将复杂环路换为简单环路( $Q_x-P_y$ 的一部分/消去分母)计算
### 全微分方程 P153
$$P(x,y)dx+Q(x,y)dy=0$$
当存在( $ Q_x=P_y$ )
$$du=Pdx+Qdy$$
有通解
$$u(x,y)=C$$
注意通解形式
## 曲面积分
但可以将曲线方程带入被积函数化简
化为相应的多重积分时优先考虑对称性
### 第一型曲面积分 P159
可以使用对称性
$$\iint_S F(x,y,z)dS$$
* 假设曲面由 $z(x,y)-z=0$ 决定
* $dx dy$ 为 $dS$ 在xy平面上的投影
* $D$ 为 $S$ 在xy平面上的投影
* $cos\gamma$ 为 $dS$ 法矢量与z轴的夹角
$$dS=|\frac{dx dy}{cos\gamma}|$$
$$cos\gamma=\frac{-1}{|grad F(x,y,z)|}$$
$$dS=\sqrt{z_x^2+z_y^2+1}dx dy$$
$$\iint_D F(x,y,z(x,y))\sqrt{z_x^2+z_y^2+1}dx dy$$
### 第二型曲面积分
不可使用对称性
$$d\vec{S}=dS\vec{n}=dS\{cos\alpha,cos\beta,cos\gamma\}=\{dy dz,dz dx,dx dy\}$$
$$\iint_S\vec{F}\cdot d\vec{S}=\iint_SPdy dz+Qdz dx+Rdx dy$$
#### 方向定义 P163
* 曲面上微元 $d\vec{S}$ 与Z轴正方向夹角小于 90° 为上侧
* 曲面上微元 $d\vec{S}$ 与Z轴正方向夹角大于 90° 为下侧
* 注意要求的 S 为上侧或下侧, 相反侧要取负号
* 当 S 相对于某个轴可能既有上侧也有下侧, 需要拆分
#### 分散投影法 P166
$$\iint_SRdx dy=\iint_DR(x,y,z(x,y))dx dy$$
#### 统一投影法 P167
假设曲面由 $z(x,y)-z=0$ 决定
$$\vec{n}=\frac{grad F}{|grad F|}=\pm\frac{\{-z_x,-z_y,1\}}{\sqrt{z_x^2+z_y^2+1}}$$
$$dS=\frac{dx dy}{|cos\gamma|}=dx dy\sqrt{z_x^2+z_y^2+1}$$
$$d\vec{S}=\pm\{-z_x,-z_y,1\}dx dy$$
$$\iint_S\vec{F}\cdot d\vec{S}=\iint_D\pm(-z_xP-z_yQ+R)dx dy$$
注意:
1. 当 $d\vec{S}$ 为Z轴上侧时, $cos\gamma>0$ 取正号, 否则取负号
2. $\pm\{-z_x,-z_y,1\}$ 中第==三项的系数为$1$==
3. ==对于平行于xy的平面, 其方程为 $z=n$== , $d\vec{S}=\pm\{0,0,1\}dx dy$ , 带入 R 中时, ==取 $z=n$ , 不是0==

## 积分公式
### 哈密尔顿算子 P170
$$\vec{F}=\{P,Q,R\}$$
$$\nabla=\{\frac{\partial}{\partial x},\frac{\partial}{\partial y},\frac{\partial}{\partial z}\}$$
#### 散度
$$div\vec{F}=\nabla\cdot\vec{F}$$
#### 旋度
$$\vec{rot}\vec{F}=\nabla\times\vec{F}=\begin{vmatrix}\vec{i}&\vec{j}&\vec{k}\\
\frac{\partial}{\partial x}&\frac{\partial}{\partial y}&\frac{\partial}{\partial z}\\P&Q&R\end{vmatrix}$$
==注意叉乘时向量的位置==
#### 梯度
$$grad F(x,y,z)=\nabla F$$
#### 运算规则 P170
见书
### 高斯公式 P172
空间 V 由闭合曲面 S 围成, P,Q,R 在 V 内与 S 上有连续的一阶偏导数
$$\oint_S\vec{F}d\vec{S}=\iiint_V\nabla\vec{F}dV$$
$S$ 取曲面的外侧
#### 普通曲面 P174
1. 添加辅助面补为闭曲面
2. 减去补充的曲面

### Stokes公式 P176
L 为有向闭合曲线
S 为以 L 为边界的任意曲面
P,Q,R在S与边界上一阶偏导连续
积分方向为 L 正向
$$\oint_L\vec{F}\cdot d\vec{l}=\iint_S\nabla\times\vec{F}d\vec{S}=\iint_S\begin{vmatrix}dydz&dzdx&dxdy\\
\frac{\partial}{\partial x}&\frac{\partial}{\partial y}&\frac{\partial}{\partial z}\\P&Q&R\end{vmatrix}$$
#### 积分与路径无关
P,Q,R在V与边界上一阶偏导连续
$$du=Pdx+Qdy+Rdz\iff \nabla\times\vec{F}=\vec{0}\iff V内曲线积分与路径无关$$