债券的持有期限、利息、本金和市场利率决定了债券的内在价值。

假设市场上存在一种普通债券，当前价格为$P$，当前==市场利率==为$y$，期限$T$年，每年付息$C$，最后一年归还面值$F$。由于货币存在时间价值，因此有式一：
$$
P=\sum_{i=1}^{T}\frac{\mathrm{C}}{(1+y)^{i}}+\frac{F}{(1+y)^{T}}
$$
此时对第一项进行等比级数求和得：
$$
P=\frac{\mathrm{C}}{y}\left[1-\frac{1}{(1+y)^{T}}\right]+\frac{F}{(1+y)^{T}}
$$

## 定理一：债券价格和债券收益率反向变动

P 对收益率 y 求偏导：
$$
\frac{\partial P}{\partial y}=\frac{C\,\left(\frac{1}{{\left(y+1\right)}^T}-1\right)}{y^2}-\frac{F\,T}{{\left(y+1\right)}^{T+1}}+\frac{C\,T}{y\,{\left(y+1\right)}^{T+1}}=\frac{C}{y^{2}} \left[ \frac{1}{\left( 1+y \right)^{T}} -1 \right] +\left( \frac{C}{y} -F \right) \frac{T}{\left( 1+y \right)^{T+1}}<0
$$

## 定理二：若利率不变，债券的到期时间与债券价格波动幅度呈正相关关系

P 对期限 T 求偏导得：
$$
\frac{\partial P}{\partial T} =\frac{C\, \ln \left( y+1 \right)}{y\, {\left( y+1 \right)}^{T}} -\frac{F\, \ln \left( y+1 \right)}{{\left( y+1 \right)}^{T}}
$$
又$C=F \cdot y^{\ast}$ （每期付息等于面值乘息票率，$y^{\ast}$ 为==票面的息票率==），可整理为：
$$
\frac{\partial P}{\partial T} =(\frac{Fy^{\ast}}{y} -F)\left( 1+y \right)^{-T} \ln (1+y)=\left[ \frac{F\left( y^{\ast}-y \right)}{y} \right] \left( 1+y \right)^{-T} \ln \left( 1+y \right)
$$
所以：
- $y > y^{\ast}$时，债券**折价**发行，同时上式小于零，因此时期越长，价格越低
- $y < y^{\ast}$ 时，债券**溢价**发行，同时上式大于零，因此时期越长，价格越高


## 定理三：延长到期时间对债券价格波动的影响是递减的

价格P对时间 T 求二阶偏导：
$$
\frac{\partial^{2} P}{\partial T^{2}} =\frac{F\, {\ln \left( y+1 \right)}^{2}}{{\left( y+1 \right)}^{T}} -\frac{C\, {\ln \left( y+1 \right)}^{2}}{y\, {\left( y+1 \right)}^{T}}
$$
整理得：

$$
\frac{\partial^{2} P}{\partial T^{2}} =-\left[ \frac{F\left( y^{\ast}-y \right)}{y} \right] \left( 1+y \right)^{-T} (\ln \left( 1+y \right) )^{2}
$$

所以：
- $y > y^{\ast}$时，债券**折价**发行，同时上式大于零，因此时期越长，价格越低，而价格降低的速度减慢
- $y < y^{\ast}$ 时，债券**溢价**发行，同时上式小于零，因此时期越长，价格越高，而价格升高的速度减慢

## 定理四：债券价格对收益率下降的反应比对同等幅度的收益率上升更敏感

P 对收益率 y 求二阶偏导：

$$
\frac{\partial^{2} P}{\partial y^{2}} =\frac{F\,T\,\left(T+1\right)}{{\left(y+1\right)}^{T+2}}-\frac{2\,C\,T}{y^2\,{\left(y+1\right)}^{T+1}}-\frac{2\,C\,\left(\frac{1}{{\left(y+1\right)}^T}-1\right)}{y^3}-\frac{C\,T\,\left(T+1\right)}{y\,{\left(y+1\right)}^{T+2}} > 0
$$
（不求和，更简单的形式）
$$
\frac{\partial^{2}P}{\partial y^{2}}=\frac{1}{\left(1+y\right)^{2}}\sum_{i=1}^{T}t\frac{(t+1)C(t)}{\left(1+y\right)^{i}}>0
$$
因为一阶导小于零，二阶导大于零，函数凸向原点，因此收益率上升所带来的损失要小于收益率下降所带来的收益。

## 定理五：对于给定的收益率变动幅度，债券的息票率与债券价格的波动幅度成反向变动关系

债券的波动率对 C 求导：
$$\partial\frac{\left(\frac{\partial P}{\partial y}\frac{y}{p}\right)}{\partial\mathrm{C}}=\frac{Fy}{\left(1+y\right)\left(\mathrm{C}\left(1+y\right)^{T}-\mathrm{C}+Fy\right)^{2}}\left(1+y+\left(1+y\right)^{T}\left(Ty-1-y\right)\right)$$
记括号内式子为S(T)，T=1时，即对一年期债券来说，上式为0，而T趋于无穷时，上式取极限值为0，即对无穷期债券来说，也为0。仅当T>1时有：$\mathrm{S}(T+1)-\mathrm{S}(T)=Ty^{2}(1+y)^{T}>0$

因为债券波动为负，因此当T>1时，波动随着息票率的增大而减小，对一年期和无穷期债券不适合。