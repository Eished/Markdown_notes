# [Typora 使用 Markdown 嵌入 LaTeX 数学公式符号语法](https://www.cnblogs.com/muyisir/p/11440164.html)

> 博客园不支持渲染 LaTeX 数学公式，需要用到什么公式，请复制到您所用的支持 LaTeX 的编辑器中查看实现效果。Typora 可以渲染 LaTeX 数学公式。

## 公式内换行

在网上看了许多关于latex多行公式对齐的教程，大多比较凌乱。在此总结一种最整洁的写法：

```latex
\begin{eqnarray}    \label{eq}
E&=&(a+b)(a-b)+b^2  \nonumber    
~&=&a^2-b^2+b^2 \nonumber    
~&=&a^2
\end{eqnarray}
```


以上公式中， “&=&”代表在“=”处对齐， “nonumber”代表此行不参与自动编号，“”表示换行。“～”输入或不输入对结果没有影响。效果如下

有时候公式太长，用=号对齐很难看(有的公式**左边很长，右边很短**)，此时难免需要进行"**公式左对齐**"。所需要的环境还是"**align**"(或者是align*，不带公式编号)。

```latex
\begin{align*}\label{2}
  & X(0) = x(0)W_{N}^{0\cdot0} + x(1)W_{N}^{0\cdot1} + \cdots + x(N-1)W_{N}^{0\cdot(N-1)}\\
  & X(1) = x(0)W_{N}^{1\cdot0} + x(1)W_{N}^{1\cdot1} + \cdots + x(N-1)W_{N}^{1\cdot(N-1)} \\
  & \cdots \\
  & X(N-1) = x(0)W_{N}^{(N-1)\cdot0} + x(1)W_{N}^{(N-1)\cdot1} + \cdots + x(N-1)W_{N}^{(N-1)\cdot(N-1)} \\
\end{align*}
```

说明1：&符号就是"**对齐的位置**"，放置在最左边就是多行公式左对齐；
说明2：\符号是每一行公式结束后的换行。

## 行内与独行

### 行内公式

将公式插入到本行内

```latex
$公式内容$
\inline
```

例：坐标轴 ![img](https://img2018.cnblogs.com/blog/1410667/201909/1410667-20190901135349117-159501400.png)

```latex
$xOy$
```

### 独行公式

公式单独占用一行

```latex
$$公式内容$$
\displaystyle
```

例：等差数列求和公式：

![img](https://img2018.cnblogs.com/blog/1410667/201909/1410667-20190901135419581-1474916726.png)

```latex
$$S_n = \frac{1}{2}n(a_1 + a_n) = na_1 + \frac{n(n-1)}{2}d, n\in N^*$$
```

------

## 上标、下标与组合

### 上标

```latex
$底数^指数$
$y = x^2$
```

例：![img](https://img2018.cnblogs.com/blog/1410667/201909/1410667-20190901135443547-1237640263.png)

```latex
$y=x^2$
```

### 下标

```latex
$CuSO_4·5H_2O$
```

例：![img](https://img2018.cnblogs.com/blog/1410667/201909/1410667-20190901135457565-1318376892.png)

```latex
$CuSO_4·5H_2O$
```

### 上下标组合

例：等比数列求和公式：

![img](https://img2018.cnblogs.com/blog/1410667/201909/1410667-20190901135516353-147819992.png)

```latex
$$S_n = na_1 (q=1)$$
$$S_n = \frac{a_1 (1 - q^n)}{1-q} (q\neq1)$$
```

------

## 汉字、字体与格式

### 汉字形式

```latex
\mbox{}
```

例：![img](https://img2018.cnblogs.com/blog/1410667/201909/1410667-20190901135530350-1759414323.png)

```latex
$V_{\mbox{升}}$
```

### 字体控制

不加此内容，公式会缩至与文字同高。加此内容，公式会以原大小显示。

```latex
\displaystyle
```

![img](https://img2018.cnblogs.com/blog/1410667/201909/1410667-20190901135816919-1670168488.png)

```latex
$\displaystyle \frac{x+y}{y+z}$
$\frac{x+y}{y+z}$
```

### 下划线符号

```latex
\underline
```

![img](https://img2018.cnblogs.com/blog/1410667/201909/1410667-20190901135847875-7309157.png)

```latex
$\underline{x+y}$
```

### 标签

```latex
\tag{数字}
```

![img](https://img2018.cnblogs.com/blog/1410667/201909/1410667-20190901135901398-1853346454.png)

```latex
$\tag{69}$
```

### 上大括号

```latex
\overbrace{算式}
```

例：![img](https://img2018.cnblogs.com/blog/1410667/201909/1410667-20190901135918421-859338730.png)

```latex
$\overbrace{a+b+c}^{2.0}$
```

### 下大括号

```latex
\underbrace{算式}
```

例：![img](https://img2018.cnblogs.com/blog/1410667/201909/1410667-20190901135933030-1222780150.png)

```latex
$a+\underbrace{b+c}_{1.0}+d$
```

### 上位符号

```latex
\stackrel{上位符号}{基位符号}
```

例：![img](https://img2018.cnblogs.com/blog/1410667/201909/1410667-20190901140010893-18937460.png)

```latex
$\vec{x}\stackrel{\mathrm{def}}{=}{x_1,\dots,x_n}$
```

------

## 占位符

### 两个 quad 空格

```latex
\qquad
```

![img](https://img2018.cnblogs.com/blog/1410667/201909/1410667-20190901140024739-143711231.png)

```latex
$x\qquad y$
```

### quad 空格

```latex
\quad
```

![img](https://img2018.cnblogs.com/blog/1410667/201909/1410667-20190901140037673-967611782.png)

```latex
$x\quad y$
```

### 大空格

```latex
\
```

![img](https://img2018.cnblogs.com/blog/1410667/201909/1410667-20190901140048625-736602768.png)

```latex
$x \ y$
```

### 中空格

```latex
\:
```

![img](https://img2018.cnblogs.com/blog/1410667/201909/1410667-20190901140100578-1879998212.png)

```latex
$x \: y$
```

### 小空格

```latex
\,
```

![img](https://img2018.cnblogs.com/blog/1410667/201909/1410667-20190901140111094-1455447030.png)

```latex
$x \, y$
```

### 贴紧

```latex
\!
```

例：![img](https://img2018.cnblogs.com/blog/1410667/201909/1410667-20190901140120501-995519862.png)

```latex
$x \! y$
```

### 无空格

例：![img](https://img2018.cnblogs.com/blog/1410667/201909/1410667-20190901140133285-1030042921.png)

```latex
$xy$
```

------

## 界定符与组合

### 括号

```latex
\big(算式\big)
```

例：![img](https://img2018.cnblogs.com/blog/1410667/201909/1410667-20190901140149580-2076416409.png)

```latex
$() \big(\big)$
```

### 中括号

```latex
[]
\left[ \right]
```

![img](https://img2018.cnblogs.com/blog/1410667/201909/1410667-20190901140218377-2130810165.png)

```latex
$[x + y]$
$\left[ abc \right]$
```

> 第二种中括号可以跨行，例如矩阵左右两边的中括号

### 大括号

```latex
\{算式\}
```

例：![img](https://img2018.cnblogs.com/blog/1410667/201909/1410667-20190901140229712-954970496.png)

```latex
$\{x + y\}$
```

### 自适应括号

```latex
\left(算式 \right)
```

例：![img](https://img2018.cnblogs.com/blog/1410667/201909/1410667-20190901140239956-647046614.png)

```latex
$\left(xyz\right)$
```

### 组合公式

![img](https://img2018.cnblogs.com/blog/1410667/201909/1410667-20190901140352757-1776094474.png)

```latex
${n+1 \choose k}={n \choose k}+{n \choose k-1}$
$\sum_{k_0,k_1,\ldots>0 \atop k_0+k_1+\cdots=n}A_{k_0}A_{k_1}\cdots$
```



### 左大括号 联立公式


方法一：

```latex
$$ f(x)=\left\{
\begin{aligned}
x & = & \cos(t) \\
y & = & \sin(t) \\
z & = & \frac xy
\end{aligned}
\right.
```


$$
```latex
$$ f(x)=\left\{
\begin{aligned}
x & = & \cos(t) \\
y & = & \sin(t) \\
z & = & \frac xy
\end{aligned}
\right.
$$


方法二：

$$ F^{HLLC}=\left\{
\begin{array}{rcl}
F_L   &   & {0   <   S_L}\\
F^*_L  &   & {S_L \leq 0 < S_M}\\
F^*_R  &   & {S_M \leq 0 < S_R}\\
F_R   &   & {S_R \leq 0}
\end{array} \right. $$

```latex
 F^{HLLC}=\left\{
\begin{array}{rcl}
F_L   &   & {0   <   S_L}\\
F^*_L  &   & {S_L \leq 0 < S_M}\\
F^*_R  &   & {S_M \leq 0 < S_R}\\
F_R   &   & {S_R \leq 0}
\end{array} \right. 
```

方法三:

$$f(x)=
\begin{cases}
0& \text{x=0}\\
1& \text{x!=0}
\end{cases}$$

```latex
f(x)=
\begin{cases}
0& \text{x=0}\\
1& \text{x!=0}
\end{cases}
```



------

## 四则运算

### 加

例：![img](https://img2018.cnblogs.com/blog/1410667/201909/1410667-20190901140412528-800465065.png)

```latex
$x+y=z$
```

### 减

例：![img](https://img2018.cnblogs.com/blog/1410667/201909/1410667-20190901140424310-1508376556.png)

```latex
$x-y=z$
```

### 加减运算

```latex
\pm
```

例：![img](https://img2018.cnblogs.com/blog/1410667/201909/1410667-20190901140438809-331895415.png)

```latex
$x \pm y = z$
```

### 减加运算

```latex
\mp
```

例：![img](https://img2018.cnblogs.com/blog/1410667/201909/1410667-20190901140455069-1121791582.png)

```latex
$x \mp y = z$
```

### 乘

#### 叉乘

```latex
\times
```

例：![img](https://img2018.cnblogs.com/blog/1410667/201909/1410667-20190901140511170-1956862419.png)

```latex
$x \times y = z$
```

#### 点乘

```latex
\cdot
```

例：![img](https://img2018.cnblogs.com/blog/1410667/201909/1410667-20190901140526536-1103737936.png)

```latex
$x \cdot y = z$
```

#### 星乘

```latex
\ast
```

例：![img](https://img2018.cnblogs.com/blog/1410667/201909/1410667-20190901140536712-1621905892.png)

```latex
$x \ast y = z$
```

### 除

#### 除号

```latex
\div
```

例：![img](https://img2018.cnblogs.com/blog/1410667/201909/1410667-20190901140549800-148826746.png)

```latex
$x \div y = z$
```

#### 斜杠除

```latex
x/y
```

例：![img](https://img2018.cnblogs.com/blog/1410667/201909/1410667-20190901140604369-1339939972.png)

```latex
$x / y = z$
```

### 分式

```latex
\frac{分子}{分母}
{分子}\over{分母}
```

![img](https://img2018.cnblogs.com/blog/1410667/201909/1410667-20190901140630648-855106215.png)

```latex
$\frac{x+y}{y+z}$
${x+y}\over{y+z}$
```

### 绝对值

```latex
|算式|
```

例：![img](https://img2018.cnblogs.com/blog/1410667/201909/1410667-20190901140640866-1714213583.png)

```latex
$y = |x|$
```

------

## 高级运算

### 平均数

```latex
\overline{算式}
```

例：![img](https://img2018.cnblogs.com/blog/1410667/201909/1410667-20190901140653506-850526147.png)

```latex
$\overline{xyz}$
```

### 开方

#### 开平方

```latex
\sqrt
```

例：![img](https://img2018.cnblogs.com/blog/1410667/201909/1410667-20190901140705279-623213231.png)

```latex
$\sqrt x$
```

#### 开多次方

```latex
\sqrt[开方数]{被开方数}
```

例：![img](https://img2018.cnblogs.com/blog/1410667/201909/1410667-20190901140714967-655169582.png)

```latex
$\sqrt[3]{x+y}$
```

### 对数

```latex
\log
```

例：![img](https://img2018.cnblogs.com/blog/1410667/201909/1410667-20190901140723988-854431695.png)

```latex
$\log_5{x}$
```

### 极限

```latex
\lim
\displaystyle \lim
```

![img](https://img2018.cnblogs.com/blog/1410667/201909/1410667-20190901140738837-840035544.png)

```latex
$\lim^{x \to \infty}_{y \to 0}{\frac{x}{y}}$
$\displaystyle \lim^{x \to \infty}_{y \to 0}{\frac{x}{y}}$
```

### 求和

```latex
\sum
\displaystyle \sum
```

![img](https://img2018.cnblogs.com/blog/1410667/201909/1410667-20190901140751686-1305894721.png)

```latex
$\sum^{x \to -\infty}_{y \to 0}{\frac{x}{y}}$
$\displaystyle \sum^{x \to -\infty}_{y \to 0}{\frac{x}{y}}$
```

### 积分

```latex
\int
\displaystyle \int
```

![img](https://img2018.cnblogs.com/blog/1410667/201909/1410667-20190901140803500-785716155.png)

```latex
$\int^{\infty}_{0}{xdx}$
$\displaystyle \int^{\infty}_{0}{xdx}$
```

### 微分

```latex
\partial
\displaystyle \partial
```

![img](https://img2018.cnblogs.com/blog/1410667/201909/1410667-20190901140815920-119886306.png)

```latex
$\frac{\partial x}{\partial y}$
$\displaystyle \frac{\partial x}{\partial y}$
```

### 矩阵

```latex
\begin{matrix} \end{matrix}
```

例：

![img](https://img2018.cnblogs.com/blog/1410667/201909/1410667-20190901140831308-1087469718.png)

```latex
$$\left[ \begin{matrix} 1 & 2  & \cdots & 5 & 6 & \cdots & 9 & 10 \\ \vdots & \vdots & \cdots & \vdots & \vdots & \cdots & \cdots & \ddots \\ a & b & \cdots & e & f & \cdots & i & j \end{matrix} \right]$$
```

## 逻辑运算

### 大于、小于和等于

#### 大于

例：![img](https://img2018.cnblogs.com/blog/1410667/201909/1410667-20190901140841564-538862488.png)

```latex
$x+y>z$
```

#### 大于等于

```latex
\geq
```

例：![img](https://img2018.cnblogs.com/blog/1410667/201909/1410667-20190901140850155-763800603.png)

```latex
$x+y \geq z$
```

#### 小于

例：![img](https://img2018.cnblogs.com/blog/1410667/201909/1410667-20190901142230803-603969653.png)

```latex
$x+y<z$
```

#### 小于等于

```latex
\leq
```

例：![img](https://img2018.cnblogs.com/blog/1410667/201909/1410667-20190901142243972-502447123.png)

```latex
$x+y \leq z$
```

#### 等于

例：![img](https://img2018.cnblogs.com/blog/1410667/201909/1410667-20190901142254967-46961445.png)

```latex
$x+y=z$
```

### 不等于

```latex
\neq
```

例：![img](https://img2018.cnblogs.com/blog/1410667/201909/1410667-20190901142310742-977614663.png)

```latex
$x \neq y$
```

### 不大于等于、不小于等于

#### 不大于等于

```latex
\ngeq
\not\geq
```

![img](https://img2018.cnblogs.com/blog/1410667/201909/1410667-20190901142324958-1365488410.png)

```latex
$x \ngeq y$
$x \not\geq y$
```

#### 不小于等于

```latex
\nleq
\not\leq
```

![img](https://img2018.cnblogs.com/blog/1410667/201909/1410667-20190901142339973-542510861.png)

```latex
$x \nleq y$
$x \not\leq y$
```

### 约等于

```latex
\approx
```

![img](https://img2018.cnblogs.com/blog/1410667/201909/1410667-20190901142349103-967468106.png)

```latex
$\frac{1}{3} \approx 0.3$
$\displaystyle \frac{1}{3} \approx 0.3$
```

### 恒等于

```latex
\equiv
```

例：![img](https://img2018.cnblogs.com/blog/1410667/201909/1410667-20190901142357963-1373710766.png)

```latex
$x + y \equiv z$
```

------

## 集合运算

### 属于、不属于

#### 属于

```latex
\in
```

例：![img](https://img2018.cnblogs.com/blog/1410667/201909/1410667-20190901142407835-1518187291.png)

```latex
$x \in A$
```

#### 不属于

```latex
\notin
\not\in
```

例：![img](https://img2018.cnblogs.com/blog/1410667/201909/1410667-20190901142419126-1846710239.png)

```latex
$x \notin A, y \not \in B$
```

### 子集运算

#### 子集

```latex
\subset
\supset
```

![img](https://img2018.cnblogs.com/blog/1410667/201909/1410667-20190901142434265-765198227.png)

```latex
$A \subset B$
$A \supset B$
```

#### 非子集

```latex
\not\subset
\not\supset
```

![img](https://img2018.cnblogs.com/blog/1410667/201909/1410667-20190901142447299-2005279311.png)

```latex
$A \not\subset B$
$A \not\supset B$
```

#### 真子集

```latex
\subseteq
\supseteq
```

![img](https://img2018.cnblogs.com/blog/1410667/201909/1410667-20190901142500585-649833233.png)

```latex
$A \subseteq B$
$A \supseteq B$
```

#### 非真子集

```latex
\subsetneq
\supsetneq
```

![img](https://img2018.cnblogs.com/blog/1410667/201909/1410667-20190901142514311-1272906096.png)

```latex
$A \subsetneq B$
$A \supsetneq B$
```

### 集合布尔运算

#### 交集

```latex
\cap
```

![img](https://img2018.cnblogs.com/blog/1410667/201909/1410667-20190901142525151-430514319.png)

```latex
$A \cap B$
```

#### 并集

```latex
\cup
```

![img](https://img2018.cnblogs.com/blog/1410667/201909/1410667-20190901142535017-984839456.png)

```latex
$A \cup B$
```

#### 差集

```latex
\setminus
```

![img](https://img2018.cnblogs.com/blog/1410667/201909/1410667-20190901142549632-697457057.png)

```latex
$A \setminus B$
```

#### 同或运算

```latex
\bigodot
```

![img](https://img2018.cnblogs.com/blog/1410667/201909/1410667-20190901142558209-227435357.png)

```latex
$A \bigodot B$
```

#### 同与运算

```latex
\bigotimes
```

![img](https://img2018.cnblogs.com/blog/1410667/201909/1410667-20190901142608439-569583212.png)

```latex
$A \bigotimes B$
```

### 常用数集

```latex
\mathbb{数集字母}
```

![img](https://img2018.cnblogs.com/blog/1410667/201909/1410667-20190901142625481-1044182661.png)

### 空集

```latex
\empty
\emptyset
```

![img](https://img2018.cnblogs.com/blog/1410667/201909/1410667-20190901142638011-681171407.png)

------

## 数学符号

### 无穷

```latex
\infty
```

![img](https://img2018.cnblogs.com/blog/1410667/201909/1410667-20190901142720445-974911991.png)

### 虚数

```latex
\imath
\jmath
```

![img](https://img2018.cnblogs.com/blog/1410667/201909/1410667-20190901142734952-18454459.png)

### 向量符号

```latex
\vec{字母}
```

![img](https://img2018.cnblogs.com/blog/1410667/201909/1410667-20190901142749838-1211646163.png)

```latex
$\vec{AC} = \vec{AB} + \vec{BC}$
```

### 导数

#### 一阶导数

```latex
\dot{a}
```

![img](https://img2018.cnblogs.com/blog/1410667/201909/1410667-20190901142759854-515137057.png)

#### 二阶导数

```latex
\ddot{a}
```

![img](https://img2018.cnblogs.com/blog/1410667/201909/1410667-20190901142807520-1042302527.png)

以此类推：

![img](https://img2018.cnblogs.com/blog/1410667/201909/1410667-20190901142821270-127069582.png)

### 箭头

#### 上箭头

![img](https://img2018.cnblogs.com/blog/1410667/201909/1410667-20190901142849630-2085324530.png)

```latex
\uparrow
```

#### 双线上箭头

![img](https://img2018.cnblogs.com/blog/1410667/201909/1410667-20190901142906918-918461504.png)

```latex
\Uparrow
```

#### 下箭头

![img](https://img2018.cnblogs.com/blog/1410667/201909/1410667-20190901142924224-1165099485.png)

```latex
\downarrow
```

#### 双线下箭头

![img](https://img2018.cnblogs.com/blog/1410667/201909/1410667-20190901142937501-858562931.png)

```latex
\Downarrow
```

#### 左箭头

![img](https://img2018.cnblogs.com/blog/1410667/201909/1410667-20190901142952084-1516960913.png)

```latex
\leftarrow
```

#### 双线左箭头

![img](https://img2018.cnblogs.com/blog/1410667/201909/1410667-20190901143003089-1727379883.png)

```latex
\Leftarrow
```

#### 右箭头

![img](https://img2018.cnblogs.com/blog/1410667/201909/1410667-20190901143015710-1480938126.png)

```latex
\rightarrow
```

#### 双线右箭头

![img](https://img2018.cnblogs.com/blog/1410667/201909/1410667-20190901143027159-1307802968.png)

```latex
\Rightarrow
```

#### 箭头上文字

$\stackrel{a}{\longrightarrow}$

示例：

```
$0\stackrel{a}{\longrightarrow}1$
```



#### 更多箭头符号

latex	显示效果

```latex
\uparrow	↑
\downarrow	↓
\Uparrow	⇑
\Downarrow	⇓
\updownarrow	↕
\Updownarrow	⇕
\rightarrow	→
\leftarrow	←
\Rightarrow	⇒
\Leftarrow	⇐
\leftrightarrow	↔
\Leftrightarrow	⇔
\longrightarrow	⟶
\longleftarrow	⟵
\Longrightarrow	⟹
\Longleftarrow	⟸
\longleftrightarrow	⟷
\Longleftrightarrow	⟺

latex	显示效果
\mapsto	↦
\longmapsto	⟼
\hookleftarrow	↩
\hookrightarrow	↪
\leftharpoonup	↼
\rightharpoonup	⇀
\leftharpoondown	↽
\rightharpoondown	⇁
\rightleftharpoons	⇌
\leadsto	⇝
\nearrow	↗
\searrow	↘
\swarrow	↙
\nwarrow	↖
\nleftarrow	↚
\nrightarrow	↛
\nLeftarrow	⇍
\nRightarrow	⇏
\nleftrightarrow	↮
\nLeftrightarrow	⇎
\dashrightarrow	⇢
\dashleftarrow	⇠
\leftleftarrows	⇇
\leftrightarrows	⇆
\Lleftarrow	⇚
\twoheadleftarrow	↞
\leftarrowtail	↢
\looparrowleft	↫
\leftrightharpoons	⇋
\curvearrowleft	↶
\circlearrowleft	↺
\Lsh	↰
\upuparrows	⇈
\upharpoonleft	↿
\downharpoonleft	⇃
\multimap	⊸
\leftrightsquigarrow	↭
\rightrightarrows	⇉
\rightleftarrows	⇄
\rightrightarrows	⇉
\rightleftarrows	⇄
\twoheadrightarrow	↠
\rightarrowtail	↣
\looparrowright	↬
\rightleftharpoons	⇌
\curvearrowright	↷
\circlearrowright	↻
\Rsh	↱
\downdownarrows	⇊
\upharpoonright	↾
\downharpoonright	⇂
\rightsquigarrow	⇝
```



------------------------------------------------


### 省略号

#### 低端对齐

![img](https://img2018.cnblogs.com/blog/1410667/201909/1410667-20190901143050625-1787524583.png)

```latex
\ldots
```

#### 中线对齐

![img](https://img2018.cnblogs.com/blog/1410667/201909/1410667-20190901143106002-1366623163.png)

```latex
\cdots
```

#### 垂直对齐

![img](https://img2018.cnblogs.com/blog/1410667/201909/1410667-20190901143115761-1845936265.png)

```latex
\vdots
```

#### 斜对齐

![img](https://img2018.cnblogs.com/blog/1410667/201909/1410667-20190901143136468-761288732.png)

```latex
\ddots
```

### 其他数学符号 音节符号

#### ā

```latex
$\bar{a}$
```

#### á

```latex
$\acute{a}$
```

#### ǎ

```latex
$\check{a}$
```

#### à

```latex
$\grave{a}$
```

#### â

```latex
$\hat{a}$
```

#### $\breve{a}$

```latex
$\breve{a}$
```

#### ã

```latex
$\tilde{a}$
```

#### å

```latex
$\mathring{x}$
```

## 希腊字母

| 大写字母 |    效果    |    实现    | 小写字母 |    效果    |    实现    |
| :------: | :--------: | :--------: | :------: | :--------: | :--------: |
|    A     |  $\Alpha$  |  `\Alpha`  |    α     |  $\alpha$  |  `\alpha`  |
|    B     |  $\Beta$   |  `\Beta`   |    β     |  $\beta$   |  `\beta`   |
|    Γ     |  $\Gamma$  |  `\Gamma`  |    γ     |  $\gamma$  |  `\gamma`  |
|    Δ     |  $\Delta$  |  `\Delta`  |    δ     |  $\delta$  |  `\delta`  |
|    Ε     | $\Epsilon$ | `\Epsilon` |    ε     | $\epsilon$ | `\epsilon` |
|    Ζ     |  $\Zeta$   |  `\Zeta`   |    ζ     |  $\zeta$   |  `\zeta`   |
|    Η     |   $\Eta$   |   `\Eta`   |    η     |   $\eta$   |   `\eta`   |
|    Θ     |  $\Theta$  |  `\Theta`  |    θ     |  $\theta$  |  `\theta`  |
|    Ι     |  $\Iota$   |  `\Iota`   |    ι     |  $\iota$   |  `\iota`   |
|    Κ     |  $\Kappa$  |  `\Kappa`  |    κ     |  $\kappa$  |  `\kappa`  |
|    Λ     | $\Lambda$  | `\Lambda`  |    λ     | $\lambda$  | `\lambda`  |
|    Μ     |   $\Mu$    |   `\Mu`    |    μ     |   $\mu$    |   `\mu`    |
|    Ν     |   $\Nu$    |   `\Nu`    |    ν     |   $\nu$    |   `\nu`    |
|    Ξ     |   $\Xi$    |   `\Xi`    |    ξ     |   $\xi$    |   `\xi`    |
|    Ο     | $\Omicron$ | `\Omicron` |    ο     | $\omicron$ | `\omicron` |
|    Π     |   $\Pi $   |   `\Pi`    |    π     |   $\pi$    |   `\pi`    |
|    Ρ     |   $\Rho$   |   `\Rho`   |    ρ     |   $\rho$   |   `\rho`   |
|    Σ     |  $\Sigma$  |  `\Sigma`  |    σ     |  $\sigma$  |  `\sigma`  |
|    Τ     |   $\Tau$   |   `\Tau`   |    τ     |   $\tau$   |   `\tau`   |
|    Υ     | $\Upsilon$ | `\Upsilon` |    υ     | $\upsilon$ | `\upsilon` |
|    Φ     |   $\Phi$   |   `\Phi`   |    φ     |   $\phi$   |   `\phi`   |
|    Χ     |   $\Chi$   |   `\Chi`   |    χ     |   $\chi$   |   `\chi`   |
|    Ψ     |   $\Psi$   |   `\Psi`   |    ψ     |   $\psi$   |   `\psi`   |
|    Ω     |  $\Omega$  |  `\Omega`  |    ω     |  $\omega$  |  `\omega`  |

> - 此文参考自 [@Daniel_Gavin 的文章《Markdown数学公式语法》（ 简书 ）](https://www.jianshu.com/p/e74eb43960a1)
> - 推荐网站：[Online LaTeX Equation Editor](http://latex.codecogs.com/eqneditor/editor.php)

分类: [Markdown_LaTeX](https://www.cnblogs.com/muyisir/category/1538277.html)