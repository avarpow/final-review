#高数 7月1日
##二重积分
$$\large 注意要求上限大于下限$$

$$有估值定理估计最大最小值$$

$$二重积分转累次积分直角坐标(扫描线法)$$

$$\int_{y1}^{y2}\int_{y_1(x)}^{y_2(x)}f(x,y)dxdy$$

$$积不出来可以考虑交换积分次序$$

$$\large 极坐标（有{x^2+y^2}时候重点考虑）$$

$$\int_{\theta_0}^{\theta_1}\int_{r_0(\theta)}^{r_1(\theta)}f(rcos\theta,rsin\theta)rdrd\theta$$

$$关注函数关于定义域的对称性的函数值的奇偶性 \& 轮换对称性 \ 能简化计算$$

$$结论\int_0^{+\infty} e^{-x^2}dx=\frac{\sqrt{\pi}}{2} $$

$$一般变量替换公式（一一对应映射）$$

$$\begin{cases}
\xi=\varphi(x,y)\\
\eta=\psi(x,y) 
\end{cases}
$$

$$ \large \iint f(x,y)dxdy=\iint f(x(\xi,\eta),y(\xi,\eta))\begin{vmatrix}
\frac{\partial x}{\partial \xi} & \frac{\partial x}{\partial \eta} \\
\frac{\partial y}{\partial \xi} & \frac{\partial y}{\partial \eta}
\end{vmatrix}d\xi d\eta$$

$$\begin{vmatrix}
\frac{\partial x}{\partial \xi} & \frac{\partial x}{\partial \eta} \\
\frac{\partial y}{\partial \xi} & \frac{\partial y}{\partial \eta}
\end{vmatrix}为雅克比行列式$$

$$椭圆变换(广义极坐标变换)$$

$$x=arcos\theta \ \ \ \ \ y=brsin\theta \ \ \ \ 
雅克比行列式为abr$$
##三重积分
$$投影法 (分为一个个柱，适合凸顶的)$$

$$\iiint f(x,y,z)dxdydz=\iint dxdy \int_{z1(x,y)}^{z2(x,y)}f(x,y,z)dz$$

$$截面法 (分为一层一层，适合平顶的)$$

$$\iiint f(x,y,z)dxdydz=\int_a^bdz\iint f(x,y,z)dxdy$$

$$转换为柱坐标$$

$$\begin{cases}
x=rcos\theta\\
y=rsin\theta\\
z=z\\ 
\end{cases}$$

$$雅克比行列式\frac{D(x,y,z)}{D(rcos\theta,rsin\theta,z)}=r$$

$$转换为球坐标$$

$$\begin{cases}
x=\rho\sin\varphi\cos\theta\\
y=\rho\sin\varphi\sin\theta\\
z=\rho\cos\varphi\\ 
\end{cases} \large其中\theta表示水平偏转角 \ \ \varphi表示俯仰角$$

$$雅克比行列式\frac{D(x,y,z)}{D(\rho\sin\varphi\cos\theta,\rho\sin\varphi\sin\theta,\rho\cos\varphi)}=\rho^2sin\varphi$$

$$一般变量替换类似二重积分$$
##曲线积分与曲面积分
###第一型曲线积分（已知线密度求线的质量）
$$\int_L\rho(x,y,z)ds$$
$$直角坐标形式$$
$$设曲线L方程y=y(x)(a < x < b),线密度\rho=f(x,y)$$
$$线质量m=\int_a^bf(x,y(x))\sqrt{1+y'(x)^2}dx$$
$$参数方程形式$$
$$\begin{cases}
x=\varphi(t)\\
y=\psi(t)
\end{cases}
$$
$$m=\int_{t_0}^{t_1}f(\varphi(t),\psi(t))\sqrt{\varphi'(t)^2+\psi'(t)^2}dt$$
$$空间中曲线类似$$
###第二型曲线积分（向量积分，类似已知力和有向路径求做功）
$$F(x,y)=(P(x,y),Q(x,y))$$

$$\int_{\overgroup{AB}}Pdx+Qdy或者\int_{\overgroup{AB}}F·dr $$

$$参数方程形式$$

$$\begin{cases}
x=\varphi(t)\\
y=\psi(t)
\end{cases}\ \ \ \alpha< t <\beta
$$

$$\int_{\overgroup{AB}}P(x,y)dx+Q(x,y)dy = \int_{\overgroup{AB}}[P(\varphi(t),\psi(t))\varphi'(t)+Q(\varphi(t),\psi(t))\psi'(t)]dt$$

$$空间中类似$$
###格林公式，积分与路径无关的条件（只与起点终点有关）
$$区域积分的顺序（单联通区域逆时针为正）$$

$$L^+为正向边界$$

$$则\oint_{L^+}P(x,y)dx+Q(x,y)dy=\iint(\frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y})dxdy$$

$$对函数有不连续点时候用单独范围包围不连续点$$
#高数 7月2日
$$积分与路径无关的充分必要条件$$

$$1.\oint_{C^+}Pdx+Qdy=0(C是简单光滑闭曲线)$$

$$2.\frac{\partial P}{\partial y} =\frac{\partial Q}{\partial x}在积分区域上成立$$

$$3.存在u(x,y) \ \ du(x,y)=Pdx+Qdy$$

$$推论:\int_{\overgroup{AB}}P(x,y)dx+Q(x,y)dy=\int_A^Bdu=u(B)-u(A)(u称为原函数)$$
###求原函数的方法
$$1.先取特殊点(x_0,y_0)按照特定路线积分(一般是折线)$$

$$2.由\frac{\partial u}{\partial x}=P 对x积分得到P(x,y)关于x的原函数$$

$$记作u_1(x,y) \ \ \ 则\frac{\partial u_1}{\partial x}=P \ \ 令u(x,y)=u_1(x,y)+\varphi(y) \ \ 两边求导得：$$

$$\frac{\partial u_1}{\partial x}+\varphi '(y)=Q 求得\varphi '(y) \ \ 则u(x,y)=u_1(x,y)+\varphi(y)$$

$$3.凑全微分方法(次数相近，注意多项式中x少一次y多一次的，sin和cos的)$$

##第一型曲面积分(曲线网的质量)
$$计算：设曲面S由方程z=g(x,y) \ \ 投影到xoy面上$$

$$\iint f(x,y,z)dS=\iint f(x,y,g(x,y))\sqrt{1+g_x^2+g_y^2}dxdy$$
$$当参数方程给出时\begin{cases}
x=x(u,v)\\
y=y(u,v)\\
z=z(u,v)
\end{cases}则令
\begin{cases}
E=x_u^2+y_u^2+z_u^2\\
F=x_ux_v+y_uy_v+z_uz_v\\
G=x_v^2+y_v^2+z_v^2
\end{cases}$$

$$\iint f(x,y,z)dS=\iint f(x(u,v),y(u,v),z(u,v))\sqrt{EG-F^2}dudv$$

##第二型曲面积分（水流总量积分）
$$曲面的方向：在曲面上一点P(x,y,z)取n=(-f_x,-f_y,1)时，我们称选取了曲面的上侧$$

$$球面和椭球面可分为内侧和外侧$$

$$计算：\iint F·dS=\iint (Pdydz+Qdzdx+Rdxdy)$$

$$设曲面由方程z=f(x,y) \ \ 投影到xoy面上计算,化为二重积分$$

$$计算:\iint (Pdydz+Qdzdx+Rdxdy)=$$

$$\pm\iint (P(x,y,f(x,y))(-f_x)+Q(x,y,f(x,y))(-f_y)+R(x,y,f(x,y)))dxdy（上侧取正，下侧取负）$$
##高斯公式和斯托克斯公式
$$\Omega是空间区域 \ \ S是\Omega的外侧则高斯公式$$

$$\oiint_{S^+} Pdydz+Qdxdz+Rdxdy(S取外侧)=\iiint_\Omega(\frac{\partial P}{\partial x}+\frac{\partial Q}{\partial y}+\frac{\partial R}{\partial z})dV$$
$$斯托克斯公式（空间曲线第二型积分）$$

$$L_+是简单闭曲线，是S_+的边界 \ \ \ 则$$

$$\oint_{L^+}Pdx+Qdy+Rdz=\iint_{S^+}(\frac{\partial R}{\partial y}-\frac{\partial Q}{\partial z})dydz+(\frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y})dxdy+(\frac{\partial P}{\partial z}-\frac{\partial R}{\partial x})dxdz$$

##第八章完

##第九章 常微分方程
###基本概念
$$n阶常微分方程(方程中导数的最高阶为n)$$

$$通解中独立的任意常数恰是方程的阶数$$

$$通解不能表示的解叫奇解$$

$$判断常数是否独立：D(y,y',y'',\dotsb)/D(C_1,C_2,C_3,\dotsb)行列式是否不为0$$
###初等积分法
$$第一类：\Large \frac{dy}{dx}=f(ax+by+c)$$

$$作变量替换z=ax+by+c$$

$$得\frac{dz}{dx}=a+b\frac{dy}{dx}=a+bf(z)是关于z可变量分离的方程$$
$$第二类：\Large \frac{dy}{dx}=f(x,y)(f是关于x,y的齐次函数)$$

$$例如：y'=\frac{x+2y}{2x-y}$$

$$改写为y'=h(\frac{y}{x})$$

$$令u=\frac{y}{x}$$

$$则y'=u+xu'带入上式得\frac{du}{dx}=\frac{h(u)-u}{x}可分分离变量$$
$$第三类：\Large \frac{dy}{dx}=f(\frac{a_1x+b1_y+c_1}{a_2x+b_2y+c_2})$$

$$第一种\Delta=\begin{vmatrix}
a_1 & b_1 \\
a_2 & b_2 
\end{vmatrix}\neq 0$$

$$联立\begin{cases}
a_1x+b1_y+c_1=0\\
a_2x+b_2y+c_2=0
\end{cases} \ \ \ 解得(x_0,y_0)
$$

$$令\begin{cases}
u=x-x_0\\
v=y-y_0
\end{cases}$$

$$原式化为\frac{dv}{du}=f(\frac{a_1u+b_1v}{a_2u+b_2v})是第二种方程$$
$$第二种\Delta=\begin{vmatrix}
a_1 & b_1 \\
a_2 & b_2 
\end{vmatrix}= 0$$

$$令z=a_1x+b_1y$$

$$则\frac{dz}{dx}=a_1+b_1\frac{dy}{dx}=a_1+b_1f(\frac{z+c_1}{kz+c_2})可变量分离$$

###一阶线性微分方程（关于y'和y都是线性的）
$$\Large \frac{dy}{dx}+P(x)y=Q(x)$$

$$第一类：一阶线性其次微分方程（Q(x)\equiv 0）$$

$$直接分离变量得到通解y=Ce^{-\int_{x_0}^xP(t)dt}$$
$$第二类：Q(x) \bcancel{\equiv} 0$$

$$先求出对应其次方程通解，再令通解中的常数C=u(x,y)设出新解：$$

$$\Large \color{#FF0000}{y(x)=u(x)e^{-\int_{x_0}^xP(t)dt}}$$

$$对两边求导 y'(x)=u'(x)e^{-\int_{x_0}^xP(t)dt}+u(x)P(x)e^{-\int_{x_0}^xP(t)dt}$$

$$代入原式有u'(x)e^{-\int_{x_0}^xP(t)dt}=Q(x)$$

$$y(x)=[\int_{x_0}^xQ(t)e^{-\int_{x_0}^xP(t)dt}+C]e^{-\int_{x_0}^xP(t)dt}$$

$$结构为一个特解加上通解$$

####伯努利方程
$$\frac{dy}{dx}=P(x)y=Q(x)y^a \ \ \ 解法：同除以y^a 再令z=y^{1-a}化为一阶线性微分方程$$
###全微分方程（恰当方程）
$$\Large \frac{dy}{dx}=\frac{-P(x,y)}{Q(x,y)}$$

$$可以写成P(x,y)dx+Q(x,y)dy=0的形式$$

$$为某二元函数全微分或者乘适当函数(积分因子)后是某个二元函数全微分$$

$$通积分为u(x,y)=C$$

$$\large 求原函数的方式见第八章$$

$$常见积分因子$$

$$ \color{#FF0000}{\frac{1}{\sqrt{x^2+y^2}}},\color{#FF0000}{\frac{1}{xy},e^x,e^y,\frac{1}{x^2+y^2},\frac{1}{x^2-y^2}}
$$

$$(略过求积分因子的公式法)$$
###可降阶的二阶微分方程
$$\Large F(X,Y',Y'')$$

$$令z=y' \ 化为F(x,z,z')$$
###解决初值问题
$$\begin{cases}
y'=f(x,y)\\
y(x_0)=y_0
\end{cases}$$

####皮卡序列的构造方法
$$令y(x)\equiv y_0$$

$$y_1(x)=y_0+\int_{x_0}^x f(x,y_0(x))dx$$

$$y_2(x)=y_0+\int_{x_0}^x f(x,y_1(x)dx$$

$$\dotsb$$

$$y_n(x)=y_0+\int_{x_0}^x f(x,y_{n-1}(x)dx$$


#高数 七月3日
###高阶线性微分方程
$$郎斯基行列式(判断函数组是否线性相关)$$

$$W(x)= 
    \begin{vmatrix}
    \varphi_1(x) &\dotsb &\varphi_n(x) \\
    \varphi_1'(x) &\dotsb &\varphi_n'(x) \\
    \vdots & \ & \vdots \\
    \varphi_1^{(n-1)}(x) &\dotsb &\varphi_n^{(n-1)}(x) \\
    \end{vmatrix}是否等于0$$

$$根据解的结构 只需求对应齐次方程的通解和一个特解$$
####二阶常系数微分方程
$$对应齐次方程:y''+py'+qy=0$$

$$对应特征方程\lambda^2+p\lambda+q=0$$

$$第一种 \ 两个不相等实根通解为：y=C_1e^{\lambda_1 x}+C_2e^{\lambda_2 x}$$

$$第二种 \ 两个相等实根通解为：y=C_1e^{\lambda x}+C_2xe^{\lambda x}$$

$$第三种 \ 两个共轭复根(\lambda=a\pm\beta i)通解为：y=e^{ax}(C_1cos\beta x+C_2sin\beta x) $$
$$求特解的方式$$

$$第一种：f(x)=P_n(x)e^{ax}时  $$

$$ 设y=x^kQ_n(x)e^{ax} \ \ Q_n(x)为待定系数多项式$$

$$k=\begin{cases}
0,a\neq\lambda_1,a\neq\lambda_2 \\
1,a=\lambda_1或a=\lambda_2 \\
2,a=\lambda_1=\lambda_2
\end{cases}$$
$$第二种：f(x)=e^{ax}[P_m(x)cos\beta x+P_n(x)sin\beta x]时$$

$$设y=x^ke^{ax}[Q_l^{(1)}cos\beta x+Q_l^{(2)}sin\beta x](Q_l^{(1)},Q_l^{(2)}是待定系数多项式)$$

$$k=\begin{cases}
0,a\pm\beta i 不是特征根\\ 
1,a\pm\beta i 是特征根
\end{cases}$$

####欧拉方程
$$\Large x^ny^{(n)}+p_1x^{n-1}y^{(n-1)}+\dotsb+p_{n-1}xy'+p_ny=f(x)$$

$$做变量替换x=e^t \ \ 或 t=ln(x)$$

$$\Large 高阶类似二阶$$
    
##第十章 无穷级数
###基本概念
$$柯西收敛准则：\forall \varepsilon \ \ \exist N \ \ 当n,m>N,|a_m-a_n<\varepsilon|则序列有极限$$

$$部分和极限存在则级数收敛$$

$$级数收敛，通项a_n \rarr 0$$

$$级数前面添加或者删除有限项目，不改变级数的敛散性$$

$$ 收敛级数加括号仍然收敛，级数的和不变 $$
###正向级数的收敛判别方法
####比较判别法
$$u_n < v_n $$

$$\sum_{n=1}^{\infty}v_n收敛则\sum_{n=1}^{\infty}u_n收敛$$

$$\sum_{n=1}^{\infty}u_n发散则\sum_{n=1}^{\infty}v_n发散$$
####p级数
$$\sum_{n=1}^{\infty}\frac{1}{n^p} \ \ \ p>1收敛，p<=1发散$$
####比值法
$$\lim_{n \rarr \infty}\frac{u_n}{v_n}=h$$

$$若0 < h <\infty 则两个级数收敛性相同$$

####达朗贝尔判别法(一般在有阶乘时候用)
$$\lim_{n \rarr \infty}\frac{u_{n+1}}{u_n}=l$$

$$\begin{cases}
l<1时，级数收敛\\
l>1时，级数发散\\
l=1时候，不能判断
\end{cases}$$
####柯西判别法(根值法)(一般用在有n次方时候用)
$$\lim_{n \rarr \infty}\sqrt[n]{u_n}=l$$

$$\begin{cases}
l<1时，级数收敛\\
l>1时，级数发散\\
l=1时候，不能判断
\end{cases}$$

####Raabe判别法(书上说了读者不必记住他)
####积分判别法
$$设\sum_{n=1}^{\infty}u_n为正项级数，若存在单调下降非负函数f(x)使得f(n)=u_n$$

$$则\sum_{n=1}^{\infty}u_n收敛的充分必要条件是无穷积分\int_1^\infty f(x)dx收敛$$

###任意项级数
####莱布尼茨判别法(交错级数，递减趋0)
$$\begin{cases}
u_n>u_{n+1}\\
\lim_{n \rarr \infty}u_n=0
\end{cases}$$

$$则级数收敛$$
####绝对收敛与条件收敛
$$若正项级数\sum_{n=1}^{\infty}|u_n|收敛则\sum_{n=1}^{\infty}u_n收敛$$
####狄里克雷判别法（一个趋0，乘以有界，收敛）
$$级数\sum_{k=1}^{\infty}a_kb_k$$

$$若a_n单调，\lim_{k \rarr \infty}a_k=0且b_k部分和有界，则级数收敛$$
####阿贝尔判别法(一个收敛，乘以单调有界，收敛)
$$级数\sum_{k=1}^{\infty}a_kb_k$$

$$若级数\sum_{k=1}^{\infty}a_k收敛,且级数\sum_{k=1}^{\infty}b_k单调有界则级数收敛$$
##函数项级数（级数每一项都是x的函数）
$$\Large \sum_{n=1}^{\infty}u_n(x)=u_1(x)+\dotsb+u_n(x)+\dotsb$$

$$收敛点：取x_0级数发散则x_0是收敛点$$

$$收敛域：全体收敛点组成的集合$$

$$和函数：记为S(x)$$

$$一致收敛的定义：略 \ \ 符号：f_n(x)\rightrightarrows f(x)$$
###判断是否一致收敛的方法
$$1.若|f_n(x)-f(x)|\leq a_n 且a_n \rarr 0 \ \ \ 则f_n(x)一致收敛$$

$$2.若存在点列x_n,若|f_n(x_n)-f(x_n)| \geq l则f_n(x)不一致收敛$$

$$2.变式\ \ 若存在点列x_n,若|f_n(x_n)-f(x_n)| \rarr k \bcancel{=} 0则f_n(x)不一致收敛$$

$$一致收敛的必要条件：u_n(x) \rarr 0$$

$$一致收的柯西准则(略)$$

####强级数判别法(M判别法):

$$ u_n(x) \leq a_n \ \sum_{n=1}^{\infty}a_n收敛 则\sum_{n=1}^{\infty}u_n(x)一致收敛$$
####狄里克雷判别法
$$u_n(x)=a_n(x)b_n(x)$$

$$若对\forall x,a_n(x)对n单调，且a_n(x)一致收敛于0$$

$$b_n部分和序列一致有界则u_n(x)一致收敛$$

####阿贝尔判别法
$$u_n(x)=a_n(x)b_n(x)$$

$$若\forall x \ a_n(x)对n单调，a_n(x)一致有界，$$

$$且\sum_{n=1}^{\infty}b_n(x)一致收敛,则u_n(x)一致收敛$$

####一致收敛函数的性质
$$\begin{cases}
1.u_n(x)连续，则和函数也连续(反过来可以证明函数不一致收敛)\\
2.可以逐项积分\int_a^b\sum_{k=1}^{\infty}u_k(x)dx=\sum_{k=1}^{\infty}\int_a^bu_k(x)dx
\end{cases}$$

$$\color{FF0000}若\sum_{k=1}^{\infty}u_n(x)点点收敛,\sum_{k=1}^{\infty}u_n'(x)连续且一致收敛则可逐项求导$$

$$\Large 可以利用各种求导积分更容易求得和函数来计算级数的值$$

###幂级数
$$形式：\sum_{n=1}^{\infty}a_n(x-x_0)^n=a_0+a_1(x-x_0)+\dotsb$$

$$收敛半径(幂级数收敛域是一个点或者x_0为中心的区间，区间长度一半叫收敛半径)$$
####求收敛半径
$$1.若幂级数相邻两项的系数之比有极限l$$

$$\large \lim_{n\rarr \infty}|\frac{a_{n+1}}{a_n}|=l$$

$$或者以下极限成立$$

$$\large \lim_{n \rarr \infty}\sqrt[n]{a_n}=l$$

$$则\begin{cases}
当0 < l <+\infty时，& R=\frac{1}{l}\\
当l=0时，& R=+\infty\\
当l=+\infty时，& R=0
\end{cases}$$

$$若有很多项系数为零，可直接换元用比值法$$
####幂级数的性质
$$1.内闭一致性：幂级数在收敛域中任意一个区间上一致收敛$$

$$2.可逐项积分逐项求导，收敛域不变$$

###泰勒级数
$$余项趋0才能泰勒展开$$
$$先把分式化为容易展开的形式$$
$$可以用来估算积分的近似值$$
####初等函数额泰勒展开
$$e^x=1+x+\frac{1}{2!}x^2+\dotsb+\frac{1}{n!}x^n+\dotsb,x \in R$$

$$sinx=x-\frac{x^3}{3!}+\frac{x^5}{5!}+\dotsb+(-1)^{n-1}\frac{x^{2n-1}}{(2n-1)!}$$

$$arctanx=x-\frac{x^3}{3}+\frac{x^5}{5}+\dotsb+(-1)^n\frac{1}{2n+1}x^{2n+1},x \in (-1,1)$$

$$ln(1+x)=x-\frac{x^2}{2}+\frac{x^3}{3}+\dotsb+(-1)^{n-1}\frac{x^n}{n},x \in (-1,1)$$

$$(1+x)^a=1+ax+\frac{a(a-1)}{2!}+\dotsb+\frac{a(a-1)\dotsb(a-n+1)}{n!}x^n,x \in (-1,+\infty)$$

##第十一章 广义积分与含参变量积分
###无穷积分
$$\lim_{A \rarr +\infty}\int_a^Af(x)dx存在则称无穷限积分收敛$$

$$p函数\int_1^{+\infty}\frac{1}{x^p}当p>1时收敛$$
####柯西收敛原理(无穷积分收敛的充要条件)
$$\forall \varepsilon \ \exist A_0>a \ A,A'>A_0|\int_A^{A'}f(x)dx|<\varepsilon$$

$$绝对收敛和条件收敛，比较判别法和级数类似$$

$$比值法：\lim_{x\rarr +\infty}\frac{f(x)}{g(x)}=k$$

$$0<k<+\infty时 两无穷积分收敛性相同$$

####狄里克雷判别法
$$对于\int_a^{+\infty}f(x)g(x)dx$$

$$若\forall A>a \int_a^Af(x)dx有界，g(x)单调趋0则原无穷积分收敛$$

####阿贝尔判别法
$$对于\int_a^{+\infty}f(x)g(x)dx$$

$$若\int_a^{+\infty}f(x)dx收敛，g(x)单调有界，则原无穷积分收敛$$
###瑕积分
$$p函数\int_0^{1}\frac{1}{x^p}当p<1时收敛$$

$$比较判别法，比值判别法，柯西收敛原理类似无穷限积分$$
###含参变量的正常积分
####连续性
$$若二元函数f(x,y)在闭矩形区域上连续，则参变量积分g(y)=\int_a^bf(x,y)dx连续$$

$$有了连续性，可以交换求极限和求积分的顺序$$

$$有了连续性，可以交换x和y的积分顺序$$

$$有了连续性，可以交换求微和积分的顺序$$

$$可以把含有三个参数的积分转换为累次积分(可以考虑交换积分顺序)方便计算$$
###含参变量的广义积分 略
$$\Large \Gamma(\alpha)=\int_0^{+\infty}x^{\alpha-1}e^{-x}dx$$

$$\Large \Gamma(\alpha)=\alpha\Large \Gamma(\alpha-1)$$

$$\Large  \Beta(p,q)=\int_0^1x^{p-1}(1-x)^{q-1}dx$$

$$\Large  \Beta(p,q)=\frac{\Gamma(p)\Gamma(q)}{\Gamma(p+q)}$$
##十二章 傅立叶级数
###三角函数的正交性
####正交
$$(f,g)=\frac{1}{\pi}\int_{-\pi}^{\pi}f(x)g(x)dx=0则f(x),g(x)正交$$

$$函数系： \frac{1}{\sqrt{2}},cosx,sinx,cos2x,sin2x,\dotsb两两正交且范数为1$$

####周期为2pi的函数的傅立叶级数
$$若f(x)在定义上分段连续且分段单调是能傅立叶展开的充分条件$$

$$f(x)=\frac{a_0}{2}+\sum_{n=1}^{+\infty}(a_0cosnx+b_0sinnx)$$

$$其中\begin{cases}
    a_n=\frac{1}{\pi}\int_{-\pi}^{\pi}f(x)cosnxdx\\
    b_n=\frac{1}{\pi}\int_{-\pi}^{\pi}f(x)sinnxdx
\end{cases}$$
####