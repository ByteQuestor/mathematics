# 第二章 一元函数微分学及其应用【1月10日】

# 第一节-导数与微分

## 1，导数的概念及函数的求导法则

1. 导数的定义

   导数可以看成一个**瞬时量**，或者说**斜率**

   > 例如开车，2小时开了120公里，但是如果想知道某一时刻的速度，不能用120除以2算出（那样是平均速度），所以导数可以看作物理中的瞬时速度

   + 导数第一定义
     $$
     \lim\limits_{\Delta x\to 0}\frac{\Delta y}{\Delta x}=\lim\limits_{\Delta x\to 0}\frac{f(x_0+\Delta x)-f(x_0)}{\Delta x}=f^{'}(x_0)
     $$

   + 等价的定义
     $$
     f^{'}(x_0)=\lim\limits_{x\to x_0}\frac{f(x)-f(x_0)}{x-x_0}
     $$

     $$
     f^{'}(x_0)=\lim\limits_{h\to0}\frac{f(x_0+h)-f(x_0)}{h}
     $$

   + 实战技巧

     + 函数`f(x)`在`x=0`处的导数
       $$
       f^{'}(0)=\lim\limits_{x\to 0}\frac{f(x)-f(0)}{x}=\lim\limits_{h\to 0}\frac{f(h)-f(0)}{h}=\lim\limits_{\Delta x\to 0}\frac{f(\Delta x)-f(0)}{\Delta x}
       $$

     + 如果函数`f(x)`满足`f(0)=0`，则
       $$
       f^{'}(0)=\lim\limits_{x\to 0}\frac{f(x)}{x}=\lim\limits_{h\to 0}\frac{f(h)}{h}=\lim\limits_{\Delta x\to 0}\frac{f(\Delta x)}{\Delta x}
       $$

   > 利用导数定义解题，要常用**等价无穷小替换**和**极限的四则运算**等

2. 左导数和右导数

   > 定理1 函数`y=f(x)`在点`x₀`处可导的充分必要条件是函数`f(x)`在点`x₀`处的左、右导数存在且相等

   > 左导和右导统称为**单侧导数**，可导的充分必要条件**常用于判定分段函数**（包括绝对值函数）在**其分段点处的可导性**

3. 可导与连续的关系

   > 定理2 可导**一定**连续，连续**不一定**可导，不连续**一定**不可导，不可导**不一定**不连续

   做题记得代导数定义公式

4. 导数的几何意义
   切线方程，我认为本质上就是一条直线的斜率，对曲线某一点切线的直线的斜率
   $$
   曲线y=f(x)在点M(x_0,f(x_0))处的切线方程为：y-f(x_0)=f^{'}(x_0)(x-x_0)
   $$
   法线方程，过切点且与切线处置的直线叫做曲线在此点处的法线
   $$
   如果f^{'}(x_0)≠0，则曲线y=f(x)在点M(x_0,f(x_0))处的法线方程为：y-f(x_0)=\frac{1}{f^{'}(x_0)}(x-x_0)
   $$

   > 如果曲线在一点处的切线斜率存在且不为0，则该点处**切线斜率✖法线斜率`=-1`**

   求**切线方程**和**法线方程**
   ①先对曲线函数求导（导数就是切线的斜率）

   ②将点代入到切线方程求出斜率（**法线斜率✖切线斜率=`-1`**）

   ③利用点斜式求出方程

## 2，导数的基本公式与求导法则

1. 常用的求导公式

   + 幂函数
     $$
     (x^a)^{'}=ax^{a-1}
     $$

   + 指数函数
     $$
     (a^x)^{'}=a^xlna\\
     (e^x)^{'}=e^x
     $$

   + 对数函数
     $$
     (log_ax)^{'}=\frac{1}{xlna}\\
     (lnx)^{'}=\frac{1}{x}
     $$

   + 三角函数
     $$
     (sinx)^{'}=cosx\\
     (cosx)^{'}=-sinx\\
     (tanx)^{'}=sec^2x\\
     (cotx)^{'}=-csc^2x\\
     (secx)^{'}=secxtanx\\
     (cscx)^{'}=-cscxcotx\\
     $$
     使用六挂图记忆
     ①上互换（六边形上顶点导数为另一个上顶点）

     ②中下方（六边形中顶点导数等于其下顶点）

     ③下中下（下顶点的导数等于自身✖其中顶点）

     > 注意发`“kao”`音的要加负号

   + 反三角函数
     下面的公式，只记反正弦和反正切即可，发`“kao”`音的在前面加个负号
     $$
     (arcsinx)^{'}=\frac{1}{\sqrt{1-x^2}}\\
     (arccosx)^{'}=-\frac{1}{\sqrt{1+x^2}}\\
     (arctanx)^{'}=\frac{1}{1+x^2}\\
     (arccotx)^{'}=-\frac{1}{1+x^2}\\
     $$

   > **先化简再求导**
   >
   > 写题的时候记得先检查是否换成常数，如：`cosΠ/3=1/2`，那么求导直接为0，如果算出`-sinΠ/3`，再算出常数结果就是错误的
   >
   > 优先化成幂函数形式进行求导

2. 函数的四则运算求导法则

   + 四则运算
     $$
     (u±v)^{'}=u^{'}±v^{'}\\
     (Cu)^{'}=Cu{'}，数乘函数，常数可不参与求导\\
     (uv)^{'}=u^{'}v+uv^{'}，前导后不导+前不导后导\\
     推广：(uvw)^{'}=u^{'}vw+uv^{'}w+uvw^{'}\\
     (\frac{u}{v})^{'}=\frac{u^{'}v-uv^{'}}{v^2}，v≠0
     $$
     
   + 复合运算

     > 复合函数的运算，就是，外层导✖内层导，像**递归**一样

     $$
     y=f[g(x)]=
      \begin{cases}
      y=f(u)\\
      u=g(x)\\
      \end{cases}
      ，函数y的求导法则为，y(x)=\frac{dy}{du}*\frac{du}{dx}=f^{'}(u)*u^{'}(x)
     $$

     求导三步骤

     > 注意：诸如`4xcosx`这种，`cosx`是复合函数

     ①复合函数分解/分层(引入了中间变量`u`)

     ②代入公式

     ③替换掉中间变量`u`

3. 复合函数地求导法则
   上面一并记录了，切记公式，不要只写一半

4. 反函数的求导法则
   如果函数`g(x)`某一区间内单调可导，在`g'(x)≠0`处，它的反函数`f(x)`在对应区间内也可导，且**`f(x)`的导数*`g(x)`的导数=1**

5. 奇偶函数的导数

   > 可导偶函数的导数为奇函数，特别的：f(x)为偶函数，且`f'(0)`存在，则`f'(0)=0`
   >
   > 可导奇函数的导数为偶函数

## 3，高阶导数

求一次导数就叫一阶导，求两次导数就叫二阶导数，求三次导数就叫三阶导数...，求`n(n≥4)`阶导数表示为：
$$
f^{(n)}(x)，y^{(n)}，\frac{d^ny}{dx^n}或\frac {d^nf(x)}{dx^n}
$$
常见的`n`阶导数公式主要有以下几个：
$$
(e^x)^{n}=e^x\\
(a^x)^{n}=a^x*ln^na(a>0,a≠1)\\
(cosx)^{(n)}=cos(x+n*\frac{Π}{2})\\
(sinx)^{(n)}=sin(x+n*\frac{Π}{2})\\
(x^m)^{(n)}=0，(正整数m<n)\\
(x^m)^{(n)}=\frac{m!}{(m-n)!}x^{(m-n)}，(正整数m>n)\\
(x^n)^{(n)}=n!\\
[ln(x+a)]^{(n)}=(-1)^{n-1}\frac{(n-1)!}{(x+a)^n}
$$

$$
若函数u=u(x),v=v(x)，具有n阶导数，则(u±v)^{(n)}=u^{(n)}±v^{(n)}
$$

## 4，各类特殊函数的导数

之前碰到的所有因变量和自变量的函数基本上都是显函数，因变量和自变量关系明显，例如：
$$
y=x^2
$$
隐函数就是，`x`和`y`的关系不明显，例如：
$$
e^{tanxy+cosx}+arcsinxy=x
$$

1. 隐函数的导数

   > 注意要用复合函数求导法（因为隐函数你中有我，我中有你）
   >
   > 直接方程两边同时对`x`求导，然后接触`y'`即可，切记是在题中现有方程里
   >
   > 而且求二阶导时，如果结果里有`y'`要将一阶导代入
   >
   > 如果要求值，题中给定一个值，再代入**原函数**求出另一个值

2. 对数求导法

   > 用于解决多个因子的积商、乘方、开方构成的函数的导数

   > 幂指函数的导数

   $$
   对于函数y=\frac{f(x)}{g(x)}，首先确定定义域：\\
   若f(x)有根式，则根号下部分>0\\
   g(x)总体不能为0，综合确定函数的定义域\\
   其次找出f(x)的零点，用这些零点将定义域划分为多个区间\\
   最后在每个区间内分析函数（如正负性、单调性等），这些区间边界点[即f(x)的零点和定义域边界在分析过程中有很重要的作用]
   $$

   

3. 由参数方程所确定的函数的导数
   参数方程的特点是：`x,y`通过中间变量`t`产生函数关系
   $$
   \begin{cases}
    x=\omega(t)\\
    y=\varphi(t)\\
    \end{cases}
    \Longleftrightarrow
    \begin{cases}
    x=t^2+1
    \\
    y=3t^3
    \end{cases}
   $$
   由于y和x没有直接关系，所以不能直接求导

   所以`x`先对`t`求导，`y`也先对`t`求导，然后取将二者的结果的商（注意`dy`在上面）
   $$
   \frac{dy}{dx}=\frac{\omega^{'}(t)}{\varphi^{'}(t)}或\frac{dy}{dx}=\frac{\frac{dy}{dt}}{\frac{dx}{dt}}
   $$
   如果两个参数方程都有二阶导数，则：【下面**不是平方，是二阶导**】
   $$
   \frac{d^2y}{dx^2}=\frac{\omega^{''}(t)\omega^{'}(t)-\omega^{'}(t)\omega^{''}(t)}{[\varphi^{'}(t)]^3}或\frac{d^2y}{dx^2}=\frac{\frac{d}{dt}(\frac{dy}{dx})}{\frac{dx}{dt}}
   $$
   
   $$
   
   $$

   $$
   注意：\frac{d}{dt}表示对t求导，，也就是组成的新的式子，求关于t的导数\\
   上述公式中\frac{d}{dt}(\frac{dy}{dx})表明是对\frac{dy}{dx}的式子进行求导
   $$

## 5，函数的微分

1. 微分的定义
   比如开汽车时，如果导数可以理解为瞬时速度，而微分可以理解为在一个很短的时间内行驶的路程

2. 可导与可微的关系

   > 定理3  函数在一点处可微的充分必要条件是`f(x)`在该点处可导，即可导与可微等价
   > $$
   > dy|_{x=x_0}=f^{'}(x_0)\Delta x=f^{'}(x_0)dx
   > $$

3. 微分的几何意义
   当自变量有很小的变化时，对函数值变化量的描述

## 6，微分的运算

1. 常数和基本初等函数的微分公式【可以看到，与导数的运算法则差不多】
   $$
   dC=0(C为常数)\\
   d(x^n)=nx^{n-1}dx(n为实数)\\
   d(log_ax)=\frac{1}{xlna}dx(a>0,a≠1)\\
   d(lnx)=\frac{1}{x}dx\\
   d(a^x)=a^xlnadx(a>0,a≠1)\\
   d(e^x)=e^xdx\\
   d(sinx)=cosxdx\\
   d(cosx)=-sindx\\
   d(tanx)=\frac{1}{cos^2x}dx=sec^2xdx\\
   d(cotx)=-\frac{1}{sin^2}dx=-csc^2xdx\\
   d(secx)=secxtanxdx\\
   d(cscx)=-cscxcotxdx\\
   d(arcsinx)=\frac{1}{\sqrt{1-x^2}}dx\\
   d(arccosx)=-\frac{1}{\sqrt{1-x^2}}dx\\
   d(arctanx)=\frac{1}{1+x^2}dx\\
   d(arccotx)=-\frac{1}{1+x^2}dx
   $$
   
2. 微分的四则运算法则

   > 前提是`u=u(x)，v=v(x)`可微，则：

   $$
   d(u±v)=du±dv\\
   d(Cu)=Cdu(C为常数)\\
   d(uv)=vdu＋udv\\
   d(\frac{u}{v})=\frac{vdu-udv}{v^2}，(v≠0)
   $$

   

3. 一阶微分形式不变性

   > 复合函数中，如果内外层函数都可微，则：
   > $$
   > y=f[u(x)]的微分为：dy=f^{'}(u)*u^{'}
   > dx
   > $$
   > 

4. 微分在近似计算中的应用

   > 适用于计算那些不规则的数字
   > $$
   > 例如：\sqrt[3]{1.02}\\
   > 先根据给出的多项式列出函数表达式再套公式\\
   > 公式：
   > f(x_0+\Delta x)≈f(x_0)+f^{'}(x_0)\Delta x
   > $$

# 第二节-微分中值定理及导数的应用

> 罗尔定理
>
> 如果一个函数①在其闭区间[a,b]上连续，②在开区间(a,b)内可导，且③两端点值相等，则开区间内必有一点的导数值为`0`
>
> **应用罗尔定理必须满足其三个条件，缺一不可**

证明题：
$$
设函数f(x)在闭区间[0,1]上连续，在开区间(0,1)内可导，并且f(1)=0，又F(x)=xf(x)\\证明：开区间内至少存在一点使x_0f(x)f^{'}(x)+f^{'}(x)=0
$$
证明：
$$
由题意知:F(x)在[0,1]上连续，在(0,1)内可导，且F^{'}(x)=xf^{'}(x)+f(x)\\
又F(0)=0,F(1)=f(1)=0，即F(0)=F(1)=0\\
根据罗尔定理得至少存在一点\xi∈(0,1)，使F^{'}(\xi)=0，即\xi f^{'}(\xi)+f(\xi)=0
$$

> 拉格朗日中值定理
>
> 如果一个函数①在其闭区间[a,b]上连续，②在开区间(a,b)内可导，其导数在开区间(a,b)内至少有一点的函数值为原函数两端点函数值差除以两端点差

$$
f^{'}(\xi)=\frac{f(b)-f(a)}{b-a}，一般题目让求出\xi，切记代入\frac{f(b)-f(a)}{b-a}求出结果
$$

> 推论1：函数在区间(a,b)内可导且导数恒等于0，则函数在该区间内是一个常数
> $$
> f^{'}(x)=0，x∈(a,b)，则y=f(x)在(a,b)内是一个常数
> $$
> 

> 推论2：两个函数在区间(a,b)内可导且两函数的同一点处的导数恒相等，则两函数在区间内只相差一个常数C
> $$
> 若f^{'}(x)=g^{'}(x),x∈(a,b)，则f(x)=g(x)+C(C为常数)
> $$
> 

## 7，洛必达法则

> 定理3   
>
> 如果两函数满足（也就是零比零型）
>
> ①趋近同一点的极限为0
>
> ②在该点的某去心领域内两函数都可导，且被除函数导数不为0
>
> ③趋近某一点的极限值为一个常数或无穷
> $$
> \lim\limits_{x\to x_0}f(x)=0，\lim\limits_{x\to x_0}g(x)=0\\
> 在x_0的某去心领域内f(x)、g(x)都可导，且g^{'}(x)不为0\\
> \lim\limits_{x\to x_0}\frac{f(x)}{g(x)}=\lim\limits_{x\to x_0}\frac{f^{'}(x)}{g^{'}(x)}=A或∞
> $$
> 则
> $$
> \lim\limits_{x\to x_0}\frac{f(x)}{g(x)}=\lim\limits_{x\to x_0}\frac{f^{'}(x)}{g^{'}(x)}=A或∞
> $$
> 洛必达法则用于求无穷比无穷、零比零型这种**未定式的极限**，**不是未定式不能使用洛必达**
>
> 注意：化简先行，用得越晚越简单，化到最简再用，在化简过程中碰到无穷比无穷、零比零型的时候再用

使用洛必达也可以使用等价无穷小替换、约去零因子等手法，但是**不满足条件**、**不是未定式**等情况不能使用洛必达

> 定理4
>
> 如果两函数满足（也就是无穷比无穷型）
>
> ①趋近同一点的极限为无穷
>
> ②在该点的某去心领域内两函数都可导，且被除函数导数不为0
>
> ③趋近某一点的极限值为一个常数或无穷
> $$
> \lim\limits_{x\to x_0}f(x)=0，\lim\limits_{x\to x_0}g(x)=0\\
> 在x_0的某去心领域内f(x)、g(x)都可导，且g^{'}(x)不为0\\
> \lim\limits_{x\to x_0}\frac{f(x)}{g(x)}=\lim\limits_{x\to x_0}\frac{f^{'}(x)}{g^{'}(x)}=A或∞
> $$
> 则
> $$
> \lim\limits_{x\to x_0}\frac{f(x)}{g(x)}=\lim\limits_{x\to x_0}\frac{f^{'}(x)}{g^{'}(x)}=A或∞
> $$

方法的选择【总之不到最后尽量不用洛必达】
$$
\frac{0}{0}型求极限=
\begin{cases}
①因式分解\\
②有理化\\
③洛必达
 \end{cases}
，
 \frac{∞}{∞}型求极限=
\begin{cases}
①抓大头\\
②同除最高次项\\
③洛必达
 \end{cases}
$$
而且，如果洛完还是未定式，继续洛

**其它类型的未定式**

例如
$$
0*∞，∞-∞，0^0，1^∞，∞^0
$$
全部转换成无穷比无穷和零比零型，对于带指数或幂的，使用**“e抬高”**

## 8，函数的单调性与极值

1. 函数的单调性

   > 定理5  
   >
   > 若函数在闭区间上连续，在开区间内可导
   >
   > 则若导数≥0，且等号仅在有限多个点处成立，则函数`f(x)`在开区间内**单增**
   >
   > 则若导数≤0，且等号仅在有限多个点处成立，则函数`f(x)`在开区间内**单减**

   解题步骤：

   先求定义域，再求导数，找出导数为0的点和导数不存在的点，并用这些点分开若干单调区间

2. 函数的极值
   一个极大值，一个极小值，顾名思义就是区间内最大/最小的那个值

   > 定理6  函数的极值点处，其导数为0或者不存在【也叫**费马引理**】

   

   > 定理7  (极值存在的必要条件)函数在极值点处可导，则
   > $$
   > f^{'}(x_0)=0
   > $$

3. 驻点

   > 函数一阶导为0的地方为**驻点**

   $$
   如果f^{'}(x_0)=0，则称x=x_0为函数的驻点\\
   x=x_0为f(x)的极值点\nrightarrow x=x_0为f(x)的驻点\\
   x=x_0为f(x)的驻点\nrightarrow x=x_0为f(x)的极值点
   $$

   也就是说，**驻点和极值点不能单独互相推论**

   > 极值点可能是驻点、不可导点

   > 定理8  极值存在的第一充分条件
   > $$
   > 一函数在x_0处连续可导\\
   > 若x<x_0时，f^{'}(x)＞0；而当x>x_0时，f^{'}(x)＜0，则f(x_0)为f(x)的极大值\\
   > 若x<x_0时，f^{'}(x)＜0；而当x>x_0时，f^{'}(x)＞0，则f(x_0)为f(x)的极小值\\
   > 若在点x_0的两侧领域内f^{'}(x)不变号，则f(x_0)不是f(x)的极值
   > $$
   > 因为极值的情况下，`f'(x)=0`是一条水平切线，而且**极值点一定在定义域内**

   > 定理9  极值存在的第二充分条件
   > $$
   > 函数在x_0处有二阶导数且f^{'}(x_0)=0，f^{"}(x_0)≠0\\
   > 若二阶导＞0则该点为函数的极小值点\\
   > 若二阶导＜0则该点为函数的极大值点
   > $$
   > **如果是函数驻点且二阶导为0，则使用定理8来判断**
   >
   > 对于驻点二阶导不为0的点都可以用二阶导在该点的政府在判定极值点和极值

## 9，函数的最值

1. 函数在**开区间**内的最值

   > 定理10  
   >
   > 若函数在某个开区间内连续且只有一个极值点，那么
   >
   > 如果它为极大值点，那么它也是最大值点
   >
   > 如果它为极小值点，那么它也是最小值点

2. 函数在**闭区间**上的最值
   连续函数在闭区间上一定存在最大值和最小值，所以解题步骤为：

   > ①求导，找出所有的驻点和不可导点
   >
   > ②求出驻点、不可导点、区间端点的函数值
   >
   > ③比较这些函数值，最大的就是最大值，最小的就是最小值

   > 函数的极大值不一定大于极小值，但是函数的最大值一定不会小于最小值

   > 实际意义：生活中有很多，比如成本最低、用料最省、产品最多等

## 10，曲线的凹凸性及拐点

## 11，曲线的渐近线