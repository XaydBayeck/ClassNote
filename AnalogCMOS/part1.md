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
$$g_{mb}=\dfrac{\partial I_D}{\partial V_{BS}}=g_m\dfrac{\gamma}{2\sqrt{2\Phi_F+V_{SB}}}\quad \eta=\dfrac{g_{mb}}{g_m}$$

- 沟道长度调制效应
$$I_D=\dfrac{1}2\mu_nC_{ox}\dfrac{W}L(V_{GS}-V_{TH})^2(1+\lambda V_{DS})$$
$$r_O=\dfrac1{\lambda I_D}$$

- 亚阈值导电效应
$$I_D=I_0\mathrm{exp}\dfrac{V_{GS}}{\zeta V_{T}},\,\,V_T=\dfrac{kT}q$$

### 单级放大器
#### 放大器分类
|共源级|源跟随器|共栅级|共源共栅级|
|:-|:-|:-|:-|
|电阻负载|电阻偏置|电阻负载|套筒结构|
|二极管连接方式的负载|电流源偏置|电流源负载|折叠式|
|电流源负载|
|有源负载|
|源极负反馈|
#### 共源级
##### 采用电阻负载的共源级电路
- $A_\upsilon=-g_mR_D$
- 考虑沟道长度调制效应：$A_\upsilon=-g_m\dfrac{r_OR_D}{r_O+R_D}$
- 摆幅：$V_{in}-V_{TH1} < V_{out} < V_{DD}$

##### 采用二极管连接型器件作负载的共源级电路
- $A_\upsilon=-g_{m1}\dfrac1{g_{m2}+g_{mb2}}=-\dfrac{g_{m1}}{g_{m2}}\dfrac1{1+\eta}=-\sqrt{\dfrac{\mu(W/L)_1}{\mu(W/L)_2}}\dfrac1{1+\eta}\quad (\eta=\dfrac{g_{mb2}}{g_{m2}})$

- 考虑沟道长度调制效应：$A_\upsilon=-g_{m1}(\dfrac1{g_{m2}}||r_{o1}||r_{o2})$

##### 采用电流源作负载的共源级
- $A_\upsilon=-g_{m1}(r_{o1}||r_{o2})$
- 摆幅：$V_{in}-V_{TH1} < V_{out} < V_{DD}-|V_{GS2}=V_{TH2}|$

##### 有源负载共源级(反向器MOS管实现)
- $A_\upsilon=-(g_{m1}+g_{m2})(r_{o1}||r_{o2})$

##### 带源极负反馈的共源级
- $G_m=\dfrac{g_m}{1+g_mR_S}$

- $A_\upsilon=-G_mR_D$
- 考虑沟道长度调制效应和体校应：$G_m=\dfrac{g_mr_O}{R_S+r_O+(g_m+g_{mb})R_Sr_O}$
- 输出阻抗：$R_{out}=r_O+(g_m+g_{mb})R_Sr_O+R_S$

#### 源跟随器（共漏级）
- $A_\upsilon=\dfrac{g_mR_S}{1+(g_m+g_{mb})R_S}$

- 输出阻抗：$R_{out}=\dfrac1{g_m+g_{mb}}$

#### 共栅级
##### 采用电阻负载的共栅级
- $A_\upsilon=g_m(1+\eta)R_D$
- 输入阻抗：$R_{in}=\dfrac1{\dfrac1{r_O}+g_m+g_{mb}}$
- 考虑输出阻抗和信号源阻抗的情况：
$$A_\upsilon=\dfrac{(g_m+g_{mb})r_O+1}{r_O+(g_m+g_{mb})r_OR_S+R_S+R_D}R_D$$

### 差动放大器
#### 基本差动对
- 共模输入范围：$\sqrt{\dfrac{I_{SS}}{\beta_{1,(2)}}}-V_b\le V_{in,CM}\le V_{DD}-\dfrac{I_{SS}}{2}R_D+V_{TN}$

- 差摸输入范围：$\Delta V_{in}=\pm \sqrt{\dfrac{2I_{SS}}{\beta}}$

- $G_m=\dfrac{2I_{SS}-\beta\Delta V_{in}^2}{\sqrt{\dfrac{4I_{SS}}{\beta}-\Delta V_{in}^2}}$

- $|A_{\upsilon ,DM}|=G_mR_D$

- $A_{\upsilon ,CM}=-\dfrac{R_D/2}{1/(2g_m)+R_{SS}}$

- $A_{CM-DM}=\dfrac{\Delta g_mR_D}{1+(g_{m1}+g_{m2}R_{SS})}$

#### MOS为负载的差动对
- $A_{\upsilon,DM}=-g_{mN}(r_{ON}||r_{OP})$

### 电流镜
#### 基本电流镜误差的产生
- 事实上，VDS1通常是不变的，而VDS2与Iout连接的节点电压有关，一般而言，这个节点的电压是随输入信号变化而变化的，0时， Iout不可能是IREF的“精确”复制。

#### 基本共源共栅电流镜
-

#### 低压共源共栅电流镜

#### 运算放大器的参数
1. 差模开环增益Ad：运放工作于放大区时，其输出电压与差模输入电压之比，常用分贝dB表示。

2. 开环带宽BW（小信号带宽）：开环增益下降3dB（或直流增益的0.707倍）时所对应的信号频率。也称f-3dB带宽。

3. 输出峰-峰电压Vopp(输出摆幅) ：指在特定负载条件下, 运放能输出的最大电压幅度, 即输出摆幅。

4.   线性：运放开环有很大的非线性，负反馈可以减小非线性，开环增益越大，负反馈后带来的非线性就越小。

5. 等效输入噪声电压：屏蔽良好、无信号输入的集成运放，在其输出端产生的任何交流无规则的干扰电压。普通运放该值约为10～20uV

6. 输入失调电压Vos：在运放零输入时为使输出为零需在输入端所加的直流电压。通常以BJT作为差分输入级的运放Vos较小，约几毫伏，MOSFET输入级的运放（常规结构）Vos相对较大。

7. 电源电压抑制比PSRR：运放工作于放大区时，输入失调电压随电源电压改变的变化率，即：


