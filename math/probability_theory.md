# 随机事件
## 随机事件的运算 P3
### 包含于
若A发生必导致B发生, 则称A包含于B $$A\subset B$$
### 和(并)
当A和B至少一个发生, 记为 $$A\cup B$$当A, B互斥时, 也可记为$$A+B$$
### 交(积)
当A和B同时发生, 记为 $$A\cap B$$ 简记为 $$AB$$

### 差
当A发生而B不发生, 记为 $$A-B=A\overline{B}$$
### 互斥
$$AB=\empty$$
### 互逆
$$AB=\empty\;A\cup B=\Omega$$则称AB互逆$$A=\overline{B}$$
### 并与交的分配律
$$A\cap(B\cup C)=(A\cap B)\cup(A\cap C)$$$$A\cup(B\cap C)=(A\cup B)\cap(A\cup C)$$
#### 计算注意
AB并集中必定有B
$$(A\cup B)\cap B=B$$
### 对偶定律
$$\overline{A\cup B}=\overline{A}\cap\overline{B}$$$$\overline{A\cap B}=\overline{A}\cup\overline{B}$$
## 概率计算 P5
### 基本性质
$$1=P(\Omega)>P(A)\ge0$$
### 有限可加性
若 $A_n$ 两两不相容 $$P(\mathop{\cup}\limits^{n}_{i=1}A_i)=\sum_{i=1}^{n}P(A_i)$$
eg.
$$A=A\overline{B}+AB\to P(A\overline{B})=P(A)-P(AB)$$
### 逆事件
$$P(A)=1-P(\overline{A})$$
### 单调性
$$A\subset B$$$$P(A)\le P(B)$$
### 事件和公式
$$P(A\cup B\cup C)=P(A)+P(B)+P(C)-P(AB)-P(AC)-P(BC)+P(ABC)$$
### 事件的文字表述
有事件 $A_1,A_2,A_3,...A_n$
#### 至少
1. 至少一个发生 $$C_1=A_1\cup A_2\cup...\cup A_n$$
2. 至少两个发生 $$C_2=A_1A_2\cup ...\cup A_1A_n\cup...\cup A_{n-1}A_n$$
3. 至少n个发生的情况同

#### 恰好
* 假设事件 $B_i$ 为 $A$ 中恰好有i个发生
* 至少一个发生即 $$C_1=B_1\cup  B_2\cup...\cup B_n$$
* 至少两个发生即 $$C_2=B_2\cup  B_3\cup...\cup B_n$$
因此有
* 恰好一个发生
$$B_1=C_1-C_2$$
## 事件的独立性
### 条件概率 P6
在A发生的条件下, B发生的概率记为 $P(B|A)$
$$P(B|A)=\frac{P(AB)}{P(A)}$$
#### 推广
1. $$P(\overline{A}|B)=1-P(A|B)$$
2. $$P(A\overline{B}|C)=P(A|C)-P(AB|C)$$
3. $$P(A\cup B|C)=P(A|C)+P(B|C)-P(AB|C)$$

### 划分 P9
设 $A_n$ 两两互斥, 满足
$$1=P(A_1)+P(A_2)+...+P(A_n)$$
则称 $A_1,A_2,...,A_n$ 为 $\Omega$ 的一个划分
(通过画图理解3b1b)
#### 全概率公式
$$\begin{aligned} P(B)&=P(B|A_1)P(A_1)+P(B|A_2)P(A_2)+...+P(B|A_n)P(A_n)\\
&=\sum_{i=1}^n P(B|A_i)P(A_i)\end{aligned}$$
#### 贝叶斯公式
$$P(A_i|B)=\frac{P(B|A_i)P(A_i)}{P(B)}=\frac{P(B|A_i)P(A_i)}{\sum_{k=1}^n P(B|A_k)P(A_k)}$$
* $P(A_i)$ 先验概率
* $P(A_i|B)$ 后验概率
* 用于知 $P(A_i|B)$ 求 $P(B|A_i)$
### 独立性
==与互斥性区分==
1. A与B独立时有
$$P(AB)=P(A)P(B)\iff P(A|B)=P(A)$$
2. 相互独立
$$P(ABC)=P(A)P(B)P(C)\\P(AB)=P(A)P(B),\;P(AC)=P(A)P(C),\;P(BC)=P(B)P(C)$$
3. 两两独立
$$P(AB)=P(A)P(B),\;P(AC)=P(A)P(C),\;P(BC)=P(B)P(C)$$

## 解题步骤
1. 设事件A
2. P(A)=...
3. 回答
# 一维随机变量
## 分布函数
注意小于等于号
$$F_X(x)=P(X\le x)(x\in\R)$$
### 性质
1. 单调非降
2. 右连续 $$\lim_{x\to a^+}F(x)=F(a)=P(X\le x)$$
    * 间断点取值与右侧相同
    * $x\to a^+$ $x$ 从 $a$ 的右侧趋近
    * $P(X\le a)$ 必定包含a点
3. $$F(-\infty)=0\le F(x)\le F(+\infty)=1$$
通过数轴图理解

### 计算
$$F(b)-F(a)=P(a<X\le b)$$
有等号的地方没有等号, 没有等号的地方有等号时, 取负极限
$$\lim_{x\to a^-}F(x)=P(X<a)=P(X\le a)-P(X=a)=F(a)-P(a)$$
$$\therefore P(a)=F(a)-\lim_{x\to a^-}F(x)$$
## 离散型随机变量
### 分布
#### 二项分布 P16
* $$X\sim B(n,p)$$
* $$P(X=k)=C_n^kp^k(1-p)^{n-k}$$
* $$EX=np$$
* $$DX=np(1-p)$$
* 可用于有多个独立个体做某事A概率相同, 求同一时间内做A的人数
* 当 $np(1-p)$ 较大时, $X\mathop{\sim}\limits^{近似}N(np,np(1-p))$
* 当 $n\ge20\;p\le0.05$, $X\mathop{\sim}\limits^{近似}P(np)$
#### 泊松分布
* $$X\sim P(\lambda)(\lambda>0)$$
* $$P(X=k)=\frac{e^{-\lambda} \lambda^{k}}{k!}(k=0,1,2,...)$$
* $$EX=\lambda$$
* $$DX=\lambda$$
#### 几何分布
* 含义: 重复做实验A, 第k次成功的概率
* $$P(X=k)=p(1-p)^{k-1}$$
* $$EX=\frac{1}{p}$$
* $$DX=\frac{1-p}{p^2}$$
#### 超几何分布
* 含义: 共有N件两种物品, 其中有M件物品A, 从中取n个物品, 求取到的n件物品中, 有k件M的概率
* $$P(X=k)=\frac{C_M^kC_{N-M}^{n-k}}{C_N^n}$$
* $$EX=n\frac{M}{N}$$
## 连续型随机变量
### 密度函数
1. 定义
$$f_x(x)=F_x'(x)$$$$F(x)=\int^{x}_{-\infty}f(x)dx$$
2. 性质
    1. $$f(x)\ge0$$
    2.  $$\int_{-\infty}^{\infty}f(x)dx=1$$
        * 对于已知的密度函数, 可作为条件(求EX)
        * ==换元法 见书P29==

### 分布
#### 均匀分布
* $$X\sim U(a,b)$$
* 长度分之1 $$f(x)=\begin{cases}
\frac{1}{b-a}&,a\le x\le b,\\
0&,其余
\end{cases}$$
* 平均值$$EX=\frac{b+a}{2}$$
* ab的距离$$DX=\frac{(b-a)^2}{12}$$
* 有==连续型==随机变量 $X$, $Y=F_X(X)\sim U(0,1)$
#### 指数分布
* $$X\sim E(\lambda)(\lambda>0)$$
* $$f(x)=\begin{cases}
\lambda e^{-\lambda}&,0\le x,\\
0&,其余
\end{cases}$$
* $$F(x)=\begin{cases}
1-e^{-\lambda}&,0\le x,\\
0&,其余
\end{cases}$$
* $$EX=\frac{1}{\lambda}$$
* $$DX=\frac{1}{\lambda^2}$$
#### 正态分布
* $$X\sim N(\mu,\sigma^2)$$
* $$f(x)=\frac{1}{\sqrt{2\pi}\sigma}e^{\frac{(x-\mu)^2}{2\sigma^2}}$$
* $$EX=\mu$$
* 注意$\sigma$为标准差 $$DX=\sigma^2$$
* 标准化正态分布 $$Y=\frac{X-EX}{\sqrt{DX}}\sim N(0,1)$$
* 标准化正态分布的对称性 $$P(X>0)=P(X<0)=\frac{1}{2}$$
* 标准化正态分布的==分布函数==记为 $$\Phi(x)=\frac{1}{\sqrt{2\pi}}\int_{-\infty}^xe^{-\frac{x^2}{2}}$$
为单调递增函数(分布函数的性质)
## 解题步骤
1. 设随机变量 X
2. X的可能取值为 ...
3. P(X=..)=.., ..
4. 回答

# 多维随机变量
## 联合分布函数 P36
### 计算
* $$P(a<X\le b,c<Y\le d)=F(b,d)+F(a,c)-F(b,c)-F(a,d)$$
* 注意, 不是导数关系 $$F(x,\infty)=F_X(x)\\F(\infty,y)=F_Y(y)$$
### 性质
1. 非负性
$$0\le F(x,y)\le 1$$
2. 单调递增
对于X与Y分别单调递增
3. 右连续
有等号的地方没有等号, 没有等号的地方有等号时, 取负极限
4. $$P(-\infty,y)=P(x,-\infty)=0,\;P(+\infty,+\infty)=1$$
5. $$P(a<X\le b,c<Y\le d)=F(b,d)+F(a,c)-F(b,c)-F(a,d)>0$$

## 联合密度函数 P39
### 性质
1. $$F(\infty,\infty)=\int_{-\infty}^{\infty}\int_{-\infty}^{\infty} f(x,y)dx dy=1$$
2. $$f(x,y)=\frac{\partial^2 F(x,y)}{\partial x\partial y}$$
3.  $$f_x(x)=\int_{-\infty}^{\infty}f(x,y)dy$$$$f_y(y)=\int_{-\infty}^{\infty}f(x,y)dx$$
    * 通过积分消去x/y
    * 将广义积分化为以x/y的分段函数再积分
    * ==不是导数关系==

## 连续型联合分布函数
### 均匀分布
$$f(x,y)=\begin{cases}
\frac{1}{S}&,(x,y)\in S,\\
0&,其余
\end{cases}$$
### 二维正态分布
$$(X,Y)\sim N(\mu_1,\mu_2,\sigma_1^2,\sigma_2^2,\rho)$$
* $\mu_1,\mu_2$ X与Y的平均值
* $\sigma_1^2,\sigma_2^2$ X与Y的方差
* $\rho$ X与Y的相关系数
#### 性质
1. $X\sim N(\mu_1,\sigma_1^2)$ ; $Y\sim N(\mu_2,\sigma_2^2)$
2. $C_1X+C_2Y\sim 一维正态分布$
3. $X,Y独立\iff \rho=0$ (仅有二维正态分布有此性质)
4. 在 $X=x$ 条件下(P43), $$Y|X=x\sim N(\mu_2+\rho\frac{\sigma_2}{\sigma_1}(x-\mu_1),(1-\rho^2)\sigma_2^2)$$
(公式中新期望的记忆方法)$$\frac{Y-EY}{\sqrt{DY}}=\rho\frac{X-EX}{\sqrt{DX}}$$

## 条件分布
记 $P(X\le x|Y=y)=F(x|y)$
### 连续型随机变量 P42
$$\because F(x|y)=\frac{F(x,y)-F(x,y^-)}{f_Y(y)dy}=\frac{\frac{\partial F(x,y)}{\partial y}}{f_Y(y)}$$ $$\therefore f(x|y)=\frac{f(x,y)}{f_Y(y)}$$
### 离散型随机变量
<div id='dtl'></div>

$$P(X+Y<a|Y=b)=\frac{P(X+b<a)}{P(Y=b)}$$
### 独立性
$$X,Y独立\iff f(x,y)=f_x(x)f_y(y)\iff F(x,y)=F_X(x)F_Y(y)$$
技巧
$X,Y$ 独立, 求 $P(G(X,Y)<0)$
可以化为(注意分情况, ==负正得负, 负负得正==) $$P(G(X,Y)<0)=P(f_1(X)f_2(Y)<0)=P(f_1(X)<0)P(f_2(Y)>0)+P(f_1(X)>0)P(f_2(Y)<0)$$
## 多维随机变量函数 P45
### 连续型
#### 加法
$$Z=aX+bY$$
$$f_z(z)=\int_{-\infty}^{\infty}\frac{1}{|b|}f(x,\frac{z-ax}{b})dx$$
1. 用 $z,x$ 表示 $y$ 带入
2. 对 $x$ 积分, 消去 $x$
3. 除以 $z$ 的系数的绝对值

#### 乘法
$$Z=XY$$
$$f_z(z)=\int_{-\infty}^{\infty}\frac{1}{|x|}f(x, \frac{z}{x})dx$$
#### 除法
$$Z=\frac{Y}{X}$$
$$f_z(z)=\int_{-\infty}^{\infty}|x|f(x,zx)dx$$
#### 最大值
设 $X_1,X_2,...,X_n$ 相互独立
$$Z=max\{X_1,X_2,...,X_n\}$$
$$P(Z\le z)=P(max\{X_1,X_2,...,X_n\}\le z) 即大于所有X_n$$
$$P(Z\le z)=P(X_1\le z)P(X_2\le z)...P(X_n\le z)$$
$$\therefore F(z)=F_{X_1}(z)F_{X_2}(z)...F_{X_n}(z)$$
#### 最小值
设 $X_1,X_2,...,X_n$ 相互独立
$$Z=min\{X_1,X_2,...,X_n\}$$
$$P(Z> z)=P(min\{X_1,X_2,...,X_n\}> z) 即小于所有X_n$$
$$P(Z> z)=P(X_1> z)P(X_2> z)...P(X_n> z)$$
$$P(Z\le z)=1-P(Z>z)=1-(1-P(X_1\le z))(1-P(X_2\le z))...(1-P(X_n\le z))$$
$$\therefore F(z)=1-(1-F_{X_1}(z))(1-F_{X_2}(z))...(1-F_{X_n}(z))$$
#### 正态总体的样本
设 $X_1,X_2,...,X_n$ 相互独立且 $X_i\sim N(\mu, \sigma^2)$
$$\sum_{i=1}^nC_iX_i\sim N(\mu\sum_{i=1}^nC_i, \sigma^2\sum_{i=1}^nC_i^2)$$
* 即 $X_i$ 的线性组合仍为正态分布, 参数为新的期望/方差
* 两个独立的不同的正态分布线性组合可以化为标准正态
### 分段
计算多位随机变量函数时, 要注意分段, 以 $(X,Y)\sim U(0\le X,Y\le1)\;Z=X+Y$ 为例
1. 通过 X, Y 得出 Z 的取值范围 ($0\le Z\le2$)
2. 采用消去 Y 的方法, 得到 $y=g(x,y)$ ($y=z-x$)
3. 将$Y$带入取值范围, 得到两个关于$X$的不等式 $$\begin{cases}
&0\le x\le1\\
&z-1\le x\le z
\end{cases}$$
4. 通过移动$Z$的取值, 的到$X$的不同上下限(同时分段), 对$X$上下限积分, 得到$f_z(z)$ 

### 含有离散型的多维随机变量函数 P47
1. [消去](#dtl)离散型部分
2. 合理分段(见书)

# 数字特征
## 数学期望
$$EX=\sum_{i=1}^{\infty}x_ip_i=\int_{-\infty}^{\infty}xf(x)dx$$
### 条件
1. 级数绝对收敛
2. x取绝对值时, 积分存在

### 随机变量函数的数学期望
#### 一维
$$Z=g(X)$$
$$EZ=\sum_{i=1}^{\infty}g(x_i)p_i=\int_{-\infty}^{\infty}g(x)f(x)dx$$
#### 二维
$$Z=g(X,Y)$$
$$EZ=\sum_{i=1}^{\infty}\sum_{j=1}^{\infty}g(x_i,y_j)p_{ij}=\int_{-\infty}^{\infty}\int_{-\infty}^{\infty}g(x,y)f(x,y)dx dy$$
* 最大值的处理 $$max(X,Y)=\frac{X+Y}{2}+\frac{|X-Y|}{2}$$$$E[max(X,Y)]=\frac{EX+EY}{2}+\frac{E|X-Y|}{2}$$
* 最小值的处理 $$min(X,Y)=\frac{X+Y}{2}-\frac{|X-Y|}{2}$$
同最大值
### 性质
1. $$EC=C$$
2. $$E(aX+b)=aEX+b$$
3. 当$X_1,X_2,...X_n$ ==相互独立== $$E(X_1X_2...X_n)=EX_1EY_2...EX_n
$$
4. $$[E(XY)]^2\le E(X^2)E(Y^2)$$
5. 当 $X\ge0$ 则 $EX\ge0$
当 $X\ge Y$ 则 $EX\ge EY$
6. $$|EX|\le E|X|$$

## 方差
$$DX=E[(X-EX)^2]=E(X^2)-(EX)^2$$
### 条件
$E(X^2)$ 存在(对应级数/积分存在)
### 切比雪夫不等式 P59
$$P(|X-EX|\ge\varepsilon)\le\frac{DX}{\varepsilon^2}$$
### 性质
1. $$DC=0$$
2. $$D(aX+b)=a^2X$$
3. 当$X_1,X_2,...X_n$ ==相互独立== $$D(X_1+X_2+...+X_n)=DX_1+DX_2+...+DX_n$$

## 协方差
$$Cov(X,Y)=E[(X-EX)(Y-EY)]=E(XY)-EX EY$$
### 性质
1. 当X, Y 相互独立$$Cov(X,Y)=0$$
2. 分配律$$Cov(X_1+X_2,Y_1+Y_2)=Cov(X_1,Y_1)+Cov(X_1,Y_2)+Cov(X_2,Y_1)+Cov(X_2,Y_2)$$
3. $$Cov(aX,bY)=abCov(X,Y)$$
4. 对称性$$Cov(X,Y)=Cov(Y,X)$$
## 相关系数 P65
$$\rho=\frac{Cov(X,Y)}{\sqrt{DX}\sqrt{DY}}$$
### 性质
1. $\rho\in(-1,1)$ 相关系数的绝对值越接近1, XY越成线性关系
2. $\rho=\pm1$ $XY$ 成一条直线($X+kY=n$), 斜率 $>0(\rho=1)/<0(\rho=-1)$
$$\to P(\frac{X-EX}{\sqrt{DX}}=\pm\frac{Y-EY}{\sqrt{DY}})=1$$
3. $\rho=0$ $XY$ 不成直线关系(==不能说明$XY$独立==, 可能$1=X^2+Y^2$)
4. $XY$ 独立则 $\rho=0$

## 标准化随机变量
$$Y=\frac{X-EX}{\sqrt{DX}}$$
此时 $EY=0$ $DY=1$
# 大数定理
## 基础 p76
对于随机变量序列 $$X_1,X_2,...,X_n$$
设 $$\overline{X}=\frac{1}{n}\sum_{i=1}^nX_i$$
### 大数定律
对于任意 $\varepsilon>0$
$$\lim_{n\to\infty}P(|\overline{X}-a_n|<\varepsilon)=1$$
序列的均值与已知数列的误差不断减小
表明n趋于无限时, 序列的均值==几乎必然==趋于一个已知数列
### 依概率收敛
对于任意 $\varepsilon>0$
$$\lim_{n\to\infty}P(|X_n-a|<\varepsilon)=1$$
表明n趋于无限时, 序列将==几乎必然==趋于一个常数
记为 $X_n\xrightarrow{P}a$
#### 性质
已知$$X_n\xrightarrow{P}a\;Y_n\xrightarrow{P}b\;Z_n=g(X_n,Y_n)$$
有$$Z_n\xrightarrow{P}g(a,b)(g(a,b)连续)$$
## 切比雪夫大数定理 P77
对于==不相关/相互独立==的随机变量序列 $X_1,X_2,...,X_n$ 有相同的方差与期望时, 此随机变量序列服从大数定律
## 辛钦大数定律 P78
对于==独立同分布==的随机变量序列 $X_1,X_2,...,X_n$, 且期望$EX=\mu$存在时
对于任意 $\varepsilon>0$
$$\lim_{n\to\infty}P(|\frac{1}{n}\sum_{i=1}^{n}X_i-\mu|<\varepsilon)=1$$
注意$\frac{1}{n}\sum_{i=1}^{n}X_i$ 是一个 ${X_i}$ 的算数平均值的的随机变量序列
表明 ${X_i}$ 的算数平均值依概率收敛于 $\mu$
## 伯努利大数定律 P78
做 $n$ 次独立重复实验, 事件 $A$ 发生次数为 $n_A$, 单次实验中 $P(A)=p$
对于任意 $\varepsilon>0$
$$\lim_{n\to\infty}P(|\frac{n_A}{n}-p|<\varepsilon)=1$$
$A$ 发生的频率 $\frac{n_A}{n}$ 也是一个随机变量序列
表明在多次重复实验中, ==$A$ 发生的频率== 依概率趋近于 $A$ 发生的概率
## 中心极限定理 P80
对于==独立同分布==的随机变量序列 $X_1,X_2,...,X_n$, 且存在期望 $EX_i=\mu$, 方差 $DX_i=\sigma^2$
$\sum_{i=1}^{n}X_i$ 的标准化随机变量
$$Y_n=\frac{\sum_{i=1}^{n}X_i-E(\sum_{i=1}^{n}X_i)}{\sqrt{D(\sum_{i=1}^{n}X_i)}}=\frac{\sum_{i=1}^{n}X_i-n\mu}{\sqrt{n}\sigma}$$
当n充分大时
$$Y_n\mathop{\sim}\limits^{近似}N(0,1)$$
推论
$$\frac{\overline{X}-\mu}{\sigma/\sqrt{n}}\mathop{\sim}\limits^{近似}N(0,1)$$
# 数理统计
## 总体与个体
### 概念 P89
1. 总体: 研究对象全体的集合
2. 个体: 组成总体的元素

### 关系 P90
设总体$X$的分布函数$F(x)$, 若 $X_1,X_2,...,X_n$ ==相互独立且与总体同分布==, 则称 $X_1,X_2,...,X_n$ 是总体 $X$ 的容量为 $n$ 的样本
## 统计量 P92
设 $g(x_1,x_2,...,x_n)$ 不含未知参数, 有 $$Z=g(X_1,X_2,...,X_n)$$ 则称==随机变量 $Z$== 为统计量
### 样本均值
$$\overline{X}=\frac{1}{n}\sum_{i=1}^nX_i$$
### 样本方差
注意 $n-1$ , 此时样本方差为总体方差的无偏估计
$$S^2=\frac{1}{n-1}\sum_{i=1}^n(X_i-\overline{X})^2$$
### 样本标准差
$$S=\sqrt{\frac{1}{n-1}\sum_{i=1}^n(X_i-\overline{X})^2}$$
## 抽样分布 P93
### $\chi^2$ (卡方)分布
设 $(X_1,X_2,...,X_n)$ 是总体 $X\sim N(0,1)$ 的样本, 称统计量
$$\chi^2=X_1^2+X_2^2+...+X_n^2$$
服从自由度为n的卡方分布, 记为 $\chi^2\sim\chi^2(n)$
==要求 $(X_1,X_2,...,X_n)$ 相互独立==, 或仅有一个自由度(变量)时, 没有要求
#### 概率密度
$$f(x)=\begin{cases}
\frac{1}{2^{n/2}\Gamma(n/2)}x^{\frac{n}{2}-1}e^{-\frac{x}{2}}&,x\ge0\\
0&,x<0
\end{cases}$$
#### 性质
1. $$E\chi^2=n$$
2. $$D\chi^2=2n$$
3. $$\chi_1^2\sim\chi^2(n)\;\chi_2^2\sim\chi^2(m)\\(\chi_1^2+\chi_2^2)\sim\chi^2(n+m)\;$$
4. 设 $\chi^2\sim\chi^2(n)$ ==常数 $\chi^2_\alpha(n)$==, $\alpha\in(0,1)$, 满足
$$\int_{\chi^2_\alpha(n)}^{+\infty}f_{\chi^2}(x)dx=P(\chi^2>\chi^2_\alpha(n))=\alpha$$
则称 $\chi^2_\alpha(n)$ 为 $\chi^2(n)$ 分布的上侧 $\alpha$ 分位点

#### 特例
$X\sim N(0,1)$ 则 $X^2\sim\chi^2(1)$
### t 分布
设 $X\sim N(0,1)\;Y\sim\chi^2(n)$, 且 ==$X,Y$ 相互独立==, 则称 
$$T=(上下均匀, 同次)\frac{X}{\sqrt{Y/n}}\sim t(n)$$
表明 $T$ 服从自由度为 $n$ 的 $t$ 分布
#### 性质
1. $t$ 分布的概率密度函数为偶函数
2. 当 $n\to\infty$, $t(n)$ 分布趋近于标准正态分布
3. 设 $T\sim t(n)$ ==常数 $t_\alpha(n)$==, $\alpha\in(0,1)$, 满足
$$\int_{t_\alpha(n)}^{+\infty}f_{T}(x)dx=P(T>t_\alpha(n))=\alpha$$
则称 $t_\alpha(n)$ 为 $t(n)$ 分布的上侧 $\alpha$ 分位点
4. 特征 分子分母为一次

#### 特例
$X,Y$ 来自总体 $N(0,1)$
$\because|Y|=\sqrt{Y^2} \; Y^2\sim\chi^2(1)$
$\therefore \frac{X}{|Y|}\sim t(1)$
### F 分布
设 $X\sim\chi^2(n)\;Y\sim\chi^2(m)$, 且 $X,Y$ 相互独立, 则称
$$F=(上下均匀, 同次)\frac{X/n}{Y/m}\sim F(n,m)$$
表明 $F$ 服从自由度为 $(n,m)$ 的 $F$ 分布
#### 性质
1. $$F\sim F(n,m)\to\frac{1}{F}\sim F(m,n)$$
2. 设 $F\sim F(n,m)$ ==常数 $F_\alpha(n)$==, $\alpha\in(0,1)$, 满足
$$\int_{F_\alpha(n,m)}^{+\infty}f_{F}(x)dx=P(F>F_\alpha(n,m))=\alpha$$
则称 $F_\alpha(n,m)$ 为 $F(n,m)$ 分布的上侧 $\alpha$ 分位点
3. $$F_{1-\alpha}(n,m)=\frac{1}{F_\alpha(m,n)}$$
4. 特征 分子分母为二次

## 正态总体的统计量分布 P95
==前提条件: 设 $(X_1,X_2,...,X_n)$ 是总体 $X\sim N(\mu, \sigma^2)$ 的样本==
### 性质
1. $\overline{X}$ 与 $S^2$ 独立
2. $$\bar{X}\sim N(\mu,\frac{\sigma^2}{n})$$
3. $S$ 中分母为 $n-1$, 减去的值为随机变量 $\bar{X}$
$$(n-1)\frac{S^2}{\sigma^2}\sim\chi^2(n-1)$$
4. 将 $X_i$ 标准化后求平方和, 即卡方分布
$$\frac{1}{\sigma^2}\sum_{i=1}^n(X_i-\mu)^2\sim\chi^2(n)$$

### 统计量分布 P95
#### 单随机变量序列
<div id='sztd'></div>

标准化的 $\overline{X}$ ==与化为 $\chi^2(n-1)$ 的 $S^2$== 转换为 $t$ 分布时, ==要除以 $n-1$ 并开方==
$$T=(\frac{\overline{X}-\mu}{\sigma/\sqrt{n}})/\sqrt{\frac{n-1}{n-1}\frac{S^2}{\sigma^2}}=\frac{\bar{X}-\mu}{S/\sqrt{n}}\sim t(n-1)$$

#### 双变量
设 $(X_1,X_2,...,X_n)$ 是总体 $X\sim N(\mu_x, \sigma_x^2)$ 的样本
$(Y_1,Y_2,...,Y_m)$ 是与 $X$ 独立的总体 $Y\sim N(\mu_y, \sigma_y^2)$ 的样本
$$F=\frac{S_x^2/\sigma_x^2}{S_y^2/\sigma_y^2}\sim F(n-1,m-1)$$
# 参数估计
## 概念
已知总体分布类型, 与容量为 n 的样本的值 $x_1, x_2, ..., x_n$, 但参数未知 $\theta_i$, 通过特定估计量(统计量), 估计未知参数
## 矩估计法 P100
### 单个参数
1. 使用 $\overline{X}=\frac{1}{n}\sum_{i=1}^nX_i$ 估计总体均值 $EX$
2. 寻找参数与总体期望的关系 $EX=g(\theta_i)$
3. 解方程($x_i$ 为已知量/常数) $$\frac{1}{n}\sum_{i=1}^nx_i=g(\hat{\theta_i})$$

### 双参数
1. 使用 $\overline{X}=\frac{1}{n}\sum_{i=1}^nX_i^2$ 估计总体均值 $E(X^2)$
2. 寻找参数与总体期望以及平方期望的关系 $$\begin{aligned}EX&=g(\theta_1,\theta_2)\\E(X^2)&=f(\theta_1,\theta_2)\end{aligned}$$
3. 解方程
4. 可使用 $$S^{*2}=\frac{1}{n}\sum_{i=1}^n(X_i-\overline{X})^2$$
估计 $DX$, 代替 $E(X^2)$ , 注意不是 $S^2$, 此处分母为 $n$

### 不变性
未知参数 $\theta$ 有矩估计 $\hat{\theta}(x_1,x_2,...,x_n)$ , 对于未知参数 $\theta'=g(\theta)$, $g(\theta)$ ==单值单调==(有单值反函数)(概率分布函数符合这一性质), 则 $\theta'$ 的矩估计 $\hat{\theta'}=g(\hat{\theta})$
## 极大似然估计 P103
### 概念
1. 假设实验结果出现的概率极大, 因此分布的参数应使实验结果出现的概率达到最大值, 以符合这一要求
2. ==各个样本之间独立同分布==
3. 求 $\theta$ 使 L 取得最大值 $$L(\theta)=P(X_1=x_1,X_2=x_2,...,X_n=x_n)=P(X_1=x_1)P(X_2=x_2)...P(X_n=x_n)$$

#### 连续型
1. 使用概率密度观察该点的函数值
2. 此时 $\theta$ 为密度函数内的一个未知参数, ==将这个参数作为变量, 随机变量的取值为已知量(常量)==
$$L(\theta)=f(x_1;\theta)f(x_2;\theta)...f(x_n;\theta)$$
3. 求使 $L(\theta)$ 达到最大值的 $\hat{\theta}$ , 等价于使 $ln[L(\theta
)]$ 达到最大值, 可用于简化求值
$$ln[L(\theta)]=ln[f(x_1;\theta)]+ln[f(x_2;\theta)]+...+ln[f(x_n;\theta)]$$
4. ==对 $\theta$ 求导, $x_i$ 为常量==, 求出最大值点, 得到 $\hat{\theta}$
5. 多个未知参数则求偏导
6. 导数不为零时, 结合 ==$x_i$ 对未知参数的限制==, 分析得出未知参数 P105

#### 离散型
1. $$L(\theta)=P(X_1=x_1;\theta)P(X_2=x_2;\theta)...P(X_n=x_n;\theta)$$
2. 同连续型, 取对数求导

### 性质
1. 不变性 未知参数 $\theta$ 有极大似然估计 $\hat{\theta}(x_1,x_2,...,x_n)$ , 对于未知参数 $\theta'=g(\theta)$, $g(\theta)$ ==单值单调==(有单值反函数)(概率分布函数符合这一性质), 则 $\theta'$ 的极大似然估计 $\hat{\theta'}=g(\hat{\theta})$
2. 正态分布总体的极大似然估计
$$\mu=\overline{X}=\frac{1}{n}\sum_{i=1}^nX_i$$
$$\sigma^2=\frac{1}{n}\sum_{i=1}^n(X_i-\mu)^2$$

## 估计量的选择标准
使用估计量 $Z=f(X_1,X_2,...,X_n)$ 估计参数 $\theta$ 
### 无偏性
1. 当 $EZ=\theta$ 称 $Z$ 为参数 $\theta$ 的无偏估计
2. 当 $\lim_{n\to\infty}(EZ-\theta)=0$ 称 $Z$ 为参数 $\theta$ 的渐近无偏估计
3. 否则称 $Z$ 为参数 $\theta$ 的有偏估计

### 有效性
使用无偏估计量 $Z_1=f(X_1,X_2,...,X_n)$ 与 $Z_2=f(X_1,X_2,...,X_n)$ 估计参数 $\theta$
当 $DZ_1<DZ_2$ 则称 $Z_1$ 比 $Z_2$ 有效
### 一致性
当估计量序列($Z_n=f(X_1,X_2,...,X_n)$) 依概率收敛于 $\theta$, 则称 $Z$ 为参数 $\theta$ 的一致估计量
对于任意 $\varepsilon>0$
$$\lim_{n\to\infty}P(|Z_n-\theta|>\varepsilon)=0$$
## 区间估计
对于参数 $\theta$
$$P(\underline{u}\le\theta\le\overline{u})=1-\alpha$$
1. $\underline{u}$ 置信下限
2. $\overline{u}$ 置信上限
3. $\alpha$ 置信水平
4. $[\underline{u},\overline{u}]$ 置信区间
对于一个置信水平可能有多个置信区间, (正态分布)一般取关于关于均值对称的区间
5. $L=\overline{u}-\underline{u}$ 置信长度

### 正态总体, 已知 $\sigma^2$ 求 $\mu$
根据
$$\frac{\bar{X}-\mu}{\sigma/\sqrt{n}}\sim N(0,1)$$
1. 设未知变量 $a$
$$P(|\frac{\bar{X}-\mu}{\sigma/\sqrt{n}}|<a)=1-\alpha$$
$$P(\bar{X}-\frac{\sigma}{\sqrt{n}}a<\mu<\bar{X}+\frac{\sigma}{\sqrt{n}}a)=1-\alpha$$
2. 求未知变量 $a$
求对立事件
$$P(\frac{\bar{X}-\mu}{\sigma/\sqrt{n}}<-a)+P(\frac{\bar{X}-\mu}{\sigma/\sqrt{n}}>a)=\alpha$$
根据标准正态密度函数的对称性
$$P(\frac{\bar{X}-\mu}{\sigma/\sqrt{n}}<-a)=P(\frac{\bar{X}-\mu}{\sigma/\sqrt{n}}>a)=\frac{\alpha}{2}$$
可得
$$a=N_{\frac{\alpha}{2}}$$
即标准正态分布上侧的 $\frac{\alpha}{2}$ 分位点
3. 结果
置信区间 $$[\bar{X}-\frac{\sigma}{\sqrt{n}}N_{\frac{\alpha}{2}},\bar{X}+\frac{\sigma}{\sqrt{n}}N_{\frac{\alpha}{2}}]$$
置信长度 $$L=2\frac{\sigma}{\sqrt{n}}N_{\frac{\alpha}{2}}$$

### 正态总体, 求 $\mu$
根据 [正态总体的抽样分布](#sztd)
$$\frac{\bar{X}-\mu}{S/\sqrt{n}}\sim t(n-1)$$
1. $\sigma^2$ 使用统计量 $S$ 估计(注意 $S$ 中的分母与 $t$ 分布的 $n-1$)
2. $t$ 分布密度函数具有对称性, 可得 $a=t_{\frac{\alpha}{2}}(n-1)$
3. 同已知 $\sigma^2$ 的方式处理
得到结果
置信区间 $$[\bar{X}-\frac{S}{\sqrt{n}}t_{\frac{\alpha}{2}}(n-1),\bar{X}+\frac{S}{\sqrt{n}}t_{\frac{\alpha}{2}}(n-1)]$$
置信长度 $$L=2\frac{S}{\sqrt{n}}t_{\frac{\alpha}{2}}(n-1)$$

# 注意事项
1. $$E(X^2)\ne(EX)^2$$
2. $$E(\frac{1}{X})\ne\frac{1}{EX}$$
3. 连续型随机变量的分布函数必定无间断点
4. $\bar{X}$ 为连续型总体的样本均值, $\bar{X}$ 也为连续型随机变量
eg. $X\sim E(\lambda)$, $P(\bar{X}=\frac{1}{\lambda})=0$ (连续型随机变量等于固定值时必定为0)
5. 密度/分布函数注意分段
6. 当P(A)=1 A不一定是必然事件; A是必然事件 则P(A)=1
