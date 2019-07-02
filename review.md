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

###高阶线性微分方程
$$郎斯基行列式$$
