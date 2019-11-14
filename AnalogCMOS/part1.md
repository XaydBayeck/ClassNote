# MOS器件物理基础
[toc]

### MOS的I/V特性

#### 阈值电压
- $V_{TH}=\Phi_{MS}+2\Phi_F+\dfrac{Q_{dep}}{C_{ox}}$

- $\Phi_F=(kT)$

#### I/V特性
- $V_{GS}<V_{TH}:I_D=0$

- $V_{DS}\le V_{GS}-V_{TH}:I_D=\mu_nC_{ox}\dfrac{W}L[(V_{GS}-V_{TH})V_{DS}-\dfrac{1}2V_{DS}^2]$

- $V_{DS}\ge V_{GS}-V_{TH}:I_D=\mu_nC_{OX}\dfrac{W}L(V_{GS}-V_{TH})^2$

- $R_{on}=\dfrac{1}{\mu_nC_{ox}\dfrac{W}L(V_{GS}-V_{TH})}$

- 饱和区： $g_m=\mu_nC_{ox}\dfrac{W}L(V_{GS}-V_{TH})=\sqrt{2\mu_nC_{ox}\dfrac{W}LI_D}=\dfrac{2I_D}{V_{GS}-V_{TH}}$

- 线性区： $g_m=\mu_nC_{ox}\dfrac{W}LV_{DS}$

#### 二级效应
- 体校应/背栅效应
$$V_{TH}=V_{TH0}=\gamma(\sqrt{|2\Phi_F+V_{SB}|}-\sqrt{|2\Phi_F|})$$

- 沟道长度调制效应
$$I_D=\dfrac{1}2\mu_nC_{ox}\dfrac{W}L(V_{GS}-V_{TH})^2(1+\lambda V_{DS})$$

- 亚阈值导电效应
$$I_D=I_0\mathrm{exp}\dfrac{V_{GS}}{\zeta V_{T}},\,\,V_T=\dfrac{kT}q$$

### 单级放大器
#### 共源级别
##### 采用电阻负载的共源级电路
- $A_\upsilon=-g_mR_D$



### 差动放大器
#### 基本差动对
