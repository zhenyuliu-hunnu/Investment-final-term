CAPM 由两个部分构成：资本市场线（CML）和证券市场线（SML），SML是资本资产定价模型（CAPM）的图形表示。

# CML 推导

• **选择一个有效前沿上的投资组合（市场组合）：** 假设存在一个特殊的投资组合（市场组合），它在与无风险资产组合时能够通过一条直线与有效前沿相切。这条直线就是资本市场线。

• **确定切点（市场组合）：** 通过优化，找到使得从无风险资产点  $(0, R_f)$  到有效前沿上的某点（市场组合）之间的斜率最大化的投资组合。这个切点对应的投资组合就是市场组合，具有最佳的夏普比率。

• **绘制CML：** 资本市场线是从无风险资产点  $(0, R_f)$  开始，经过市场组合点，并延伸到更高风险和收益水平的直线。

假设：
- $R_f$  ：无风险资产的回报率。
- $R_m$  ：市场组合的预期回报率。
- $\sigma_m$  ：市场组合的标准差（风险）。
- $\sigma_p$ ：任意在CML上的投资组合的标准差。
- $R_p$：任意在CML上的投资组合的预期回报率。

投资组合  P  由无风险资产和市场组合组成，设  w  为投资于市场组合的比例，则：
$$R_p = wR_m + (1 - w)R_f$$
由于无风险资产的标准差为零，投资组合  P  的标准差仅由市场组合的风险部分决定：$\sigma_P = w\sigma_m$，即
$$w=\frac{\sigma_{p}}{\sigma_m}$$
将  w  代入预期回报率公式：
$$R_p = \frac{\sigma_p}{\sigma_m}R_m + \left(1 - \frac{\sigma_p}{\sigma_m}\right)R_f$$
化简得：
$$R_p = R_f + \left( \frac{R_m - R_f}{\sigma_m} \right) \sigma_p$$


# SML 推导

持有资产 $i$ 的权重为 $w$，持有市场组合$m$的权重为$1-w$。那么有：
$$R_p=wR_i+(1-w)R_m$$
$$
\sigma^2_{p}=D\left( wi+\left( 1-w \right) m \right) =w^{2}\sigma_{i}^{2} +\left( 1-w \right)^{2} \sigma_{m}^{2} +2w\left( 1-w \right) \sigma_{im}
$$
其中$\text{Cov}(i,m)=\sigma_{im}$。两式对 $w$ 求偏导：
$$\frac{\partial R_{p}}{\partial w} =R_{i}-R_{m}$$
$$\frac{\partial \sigma_{p}}{\partial w} =\frac{w\sigma_{i}^{2} +(w-1)\sigma_{m}^{2} +(1-2w)\sigma_{im}}{\sigma_{p}}$$

$w=0$时，$\sigma_p=\sigma_m$，SML 是可行集的切线，与 CML 重合

$$
\frac{\partial \sigma_{p}}{\partial w}\bigg|_{w=0}=\frac{\sigma_{im}-\sigma^2_m}{\sigma_m}
$$
此时斜率为
$$\frac{\partial R_{p}}{\partial \sigma_{p}}\bigg|_{w=0} =\left(\frac{\partial R_{p}}{\partial w} \div \frac{\partial \sigma_{p}}{\partial w}\right)\bigg|_{w=0}=\frac{(R_i-R_m)\sigma_m}{\sigma_{im}-\sigma^2_m}$$

CML 切线为：
$$\frac{R_m - R_f}{\sigma_m}$$
联立得到 $R_i$
$$
\frac{(R_{i}-R_{m})\sigma_{m}}{\sigma_{im} -\sigma_{m}^2} =\frac{R_{m}-R_{f}}{\sigma_{m}} \Longrightarrow R_{i}=R_{f}+\frac{\sigma_{im}}{\sigma_{m}^{2}} \left( R_{m}-R_{f} \right) =R_{f}+\beta_{i} \left( R_{m}-R_{f} \right)
$$
其中：
$$
\beta_i=\frac{\text{Cov}(i,m)}{\sigma^2_m}
$$
# CAPM 的应用

某项目**未来期望收益**为100万美元，β=0.8。若当时短期国债的平均收益为10%，市场组合的期望收益为20%，则该项目最大可接受的投资成本是多少？


未来期望收益即 未来售价Q - 成本P==（求解目标）== = 100

那么简单收益率为 $R=\frac{Q-P}{P}=\frac{100}{P}$，该值与对应的CAPM收益相等，即：

$$
\frac{100}{P}=R_f+\beta_i(R_m-R_f)=10\%+0.8\times(20\%-10\%)=18\%
$$

解得 $P=\frac{100}{18\%} \approx 555.56$

