# PN结
[toc]
## PN结的平衡状态
#### 电流密度方程
$$
J_n=q\mu_nnE+qD_n\dfrac{\mathrm{d}n}{\mathrm{d}x},\quad
J_p=q\mu_ppE+qD_p\dfrac{\mathrm{d}n}{\mathrm{d}x}
$$
$$
\dfrac{\partial n}{\partial t}=D_p\dfrac{\partial^2n}{\partial x^2}-\dfrac{\Delta n}{\tau_p}
$$
$$
\dfrac{\partial p}{\partial t}=D_p\dfrac{\partial^2p}{\partial x^2}-\dfrac{\Delta p}{\tau_p}
$$

#### PN结分类
- 线性缓变结:$\qquad N_D-N_A=ax$

- 突变结:
$
\qquad N_D-N_A=
\begin{cases}
N_D & x>0,\\
-N_A & x<0.
\end{cases}
$

#### 内建电场
- 突变结
$$
E(x)=\dfrac{q}{\epsilon_s}(x-x_n)N_D\,(0\le x\le x_n),\quad
E(x)=\dfrac{q}{\epsilon_s}(x-x_p)N_A\,(-x_p\le x\le 0)
$$
$$
|E_{max}|=\sqrt{\dfrac{2qN_0}{\epsilon_s}V_{bi}}
$$
$$
P^+N单边突变结:N_A\gg N_D,N_0\approx N_D,x_n\approx x_d\\
|E_{max}|=\sqrt{\dfrac{2qN_D}{\epsilon_s}V_{bi}}
$$
$$
pN^+单边突变结:N_D\gg N_A,N_0\approx N_A,x_p\approx x_d\\
|E_{max}|=\sqrt{\dfrac{2qN_A}{\epsilon_s}V_{bi}}
$$
- 缓变结
$$
|E(x)|=|E_{max}|\cdot[1-(\dfrac{2x}{x_d})^2],\quad |E_{max}|=\dfrac{aqx_d^2}{8\epsilon_s}
$$

#### 耗尽区宽度
- 突变结
$$
|E(0)|=|E_{max}|=\dfrac{q}{\epsilon_s}N_Dx_x=\dfrac{q}{\epsilon_s}N_Ax_p
$$
$$
x_n=\dfrac{\epsilon_s}{qN_D}|E_{max}|=[\dfrac{2\epsilon_s}{q}\dfrac{N_D}{N_A(N_A+N_D)}V_{bi}]^{\frac12}
$$
$$
x_p=\dfrac{\epsilon_s}{qN_A}|E_{max}|=[\dfrac{2\epsilon_s}{q}\dfrac{N_A}{N_D(N_A+N_D)}V_{bi}]^{\frac12}
$$
$$
耗尽区总宽度:x_d=x_n+x_p=\dfrac{\epsilon_s}{q}\cdot\dfrac{N_A+N_D}{N_AN_D}|E_{max}|=\dfrac{\epsilon_s}{qN_0}|E_{max}|
$$
$$
=\dfrac{2V_{bi}}{|E_{max}|}=\sqrt{\dfrac{2qN_0}{\epsilon_s}V_{bi}}
$$
$$
约化浓度:N_0=\dfrac{N_AN_D}{N_A+N_D}
$$
- 缓变结
$$x_d=\sqrt[3]{\dfrac{12\epsilon_s(V_{bi}-V)}{aq}}$$

#### 内建电势
$$
内建电势:V_{bi}=-\int_{-x_p}^{x_n}E(x)\mathrm{d}x=\dfrac{\epsilon_s}{2qN_0}|E_{max}|^2
$$
$$
|E_{max}|=\sqrt{\dfrac{2qN_0}{\epsilon_s}V_{bi}}
$$
$$
E(x)=\dfrac{kT}{q}\cdot\dfrac{d(lnp)}{dx}
$$
- 突变结
$$
V_{bi}=\dfrac{kT}{q}\mathrm{ln}(\dfrac{N_AN_D}{n_i^2})
$$
- 缓变结
$$
V_{bi}=\int_{-\frac{x_d}2}^{\frac{x_d}2}|E(x)|\mathrm{d}x=\frac23|E_{max}|x_d
$$
$$
V_{bi}=\frac{kT}q\mathrm{ln}(\dfrac{ax_d}{2n_i})^2
$$

#### 载流子浓度分布
$$
n=n_i\mathrm{exp}(-\dfrac{E_i-E_F}{kT}),\quad p=p_i\mathrm{exp}(-\dfrac{E_F-E_i}{kT}),\quad E_i(x)=E_i(x_n)-q\Psi(x)
$$
$$
n(x)=n_{n0}\mathrm{exp}[\dfrac{q\Psi(x)}{kT}],\quad p(x)=p_{p0}\mathrm{exp}[-\dfrac{qV_{bi}+q\Psi(x)}{kT}]
$$
$$
n_{p0}=n_{n0}\mathrm{exp}\lgroup-\dfrac{qV_{bi}}{kT}\rgroup,\quad
n_{p0}=p_{p0}\mathrm{exp}\lgroup-\dfrac{qV_{bi}}{kT}\rgroup
$$

#### 外加电流方向
>当电压正极接 P 区引出端、负级接 N 引出端时，V > 0，称为正偏;
>反之，V < 0，称为反偏。
>
>外加电压的情况下使用$(V_{bi}-V)$替换$V_{bi}$

## PN结的直流电电流电压方程

#### 大注入与小注入
- 小注入：
$
\begin{cases}
\Delta n_p\ll p_{p0} & (对于P区),\\
\Delta p_n\ll n_{n0} & (对于N区).
\end{cases}
\Longrightarrow
\begin{cases}
p_p=p_{p0} & (对于P区),\\
n_n=n_{n0} & (对于N区).
\end{cases}
$

- 大注入：
$
\begin{cases}
\Delta n_p\gg p_{p0} & (对于P区),\\
\Delta p_n\gg n_{n0} & (对于N区).
\end{cases}
\Longrightarrow
\begin{cases}
p_p=\Delta n_p & (对于P区),\\
n_n=\Delta p_n & (对于N区).
\end{cases}
$

#### 势垒区两旁载流子浓度的波耳兹曼分布
$$
\dfrac{p_n}{p_p}=\mathrm{exp}[-\dfrac{q(V{bi}-V)}{kT}]
$$
$$(小注入条件)\qquad
p_n=p_{n0}\mathrm{exp}(\dfrac{qV}{kT}),(x=x_n)\qquad n_p=n_{p0}\mathrm{exp}(\dfrac{qV}{kT}),(x=-x_p)
$$

#### 扩散电流
- 少子浓度边界条件:
  - 少子浓度边界条件
  $
  \begin{cases}
  p_n(x_n)=p_{n0}\mathrm{exp}(\dfrac{qV}{kT}), & p_n|_{x\rightarrow\infty}=p_{n0}\\
  n_p(-x_p)=n_{p0}\mathrm{exp}(\dfrac{qV}{kT}), & n_p|_{x\rightarrow-\infty}=n_{p0}
  \end{cases}
  $

  - 非平衡少子
  $
  \begin{cases}
  p_n(x_n)=p_{n0}[\mathrm{exp}(\dfrac{qV}{kT})-1], & p_n|_{x\rightarrow\infty}=p_{n0}\\
  n_p(-x_p)=n_{p0}[\mathrm{exp}(\dfrac{qV}{kT})-1], & n_p|_{x\rightarrow-\infty}=n_{p0}
  \end{cases}
  $

  - 中性区内的非平衡少子
  $$
  \dfrac{d^2\Delta p_n}{dx^2}=\dfrac{\Delta p_n}{L_p^2},\,L_p=\sqrt{D_p\tau_p}\Longrightarrow \Delta p_n(x)=p_{n0}[\mathrm{exp}(\dfrac{qV}{kT}-1)]\mathrm{exp}(-\dfrac{x-x_n}{L_p})
  $$
  >同理可得
  $$
  \Delta n_p(x)=n_{p0}[\mathrm{exp}(\dfrac{qV}{kT}-1)]\mathrm{exp}(\dfrac{x+x_p}{L_n})
  $$

- 扩散电流
$$
\begin{cases}
J_{dp}=-qD_p(\dfrac{\mathrm{d}\Delta p_n}{\mathrm{d}x})|_{x=x_n}=\dfrac{qD_pp_{n0}}{L_p}[\mathrm{exp}(\dfrac{qV}{kT})-1] & N区\\
J_{dn}=\dfrac{qD_nn_{p0}}{L_n}[\mathrm{exp}(\dfrac{qV}{kT})-1] & P区
\end{cases}
$$
>扩散电流：
$$
J_d=J_0[\mathrm{exp}(\dfrac{qV}{kT})-1],\,J_0=q(\dfrac{D_p}{L_p}p_{n0}+\dfrac{D_n}{L_n}n_{p0})
$$
>近似：
$$
J_d=
\begin{cases}
0 & V=0,\\
J_0\mathrm{exp}(\dfrac{qV}{kT}) & V\gg \dfrac{kT}q,\\
-J_0 & V\ll -\dfrac{kT}q.
\end{cases}
$$

- 反向饱和电流
$
\qquad I_d=AJ_0,\quad A为PN结的结面积.
$

#### PN结的击穿
##### 雪崩击穿
- 碰撞电离率：$\alpha_{i(n/p)}=AE\mathrm{exp}[-(\dfrac BE)^m]\quad A、E、m$为经验常数
- 雪崩倍增因子：$M=\dfrac1{1-\int_0^{x_d}\alpha_i\mathrm{d}x}$
- 雪崩击穿条件：$\int_0^{x_d}\alpha_i\mathrm{d}x\rightarrow1$
- 雪崩击穿电压：
  - 突变结：$V_B=\dfrac{\epsilon_s}{2qN_0}E^2_c=5.2\times10^{13}E_G^{\frac32}N_0^{-\frac34}$
  - 线性缓变结：$V_B=\sqrt{\dfrac{32\epsilon_s}{9aq}}E_c^{\frac32}=10^{10}E_G^{\frac65}a^{\frac25}$
#### 齐纳击穿(隧道击穿)
- 齐纳击穿条件：$d=\dfrac{E_G}{q|E_{max}|}$足够小
#### 热击穿

#### 势垒电容
- 单位结电容：$\dfrac{C_T}{A}=\dfrac{\epsilon_s}{x_d}$
- 突变结电容：$C_T=A\sqrt{\dfrac{\epsilon_s qN_0}{2(V_{bi}-V)}}$
- 线性缓变结电容：$C_T=A\sqrt[3]{\dfrac{aq\epsilon_s}{12(V_{bi}-V)}}$


# MOSFET
### 阈值电压
- 阈值电压的一般表达式
$$
V_T=\Phi_{MS}-\dfrac{Q_{OX}}{C_{OX}}+K(2\Phi_{FP})^{\frac12}+2\Phi_{FP}
$$

- 影响阈值电压的因素
1. 栅氧化层厚度$T_{OX}$
2. 衬底费米势$\Phi_{FB}$
3. 功函数差$\Phi_{MS}$
4. 耗尽区高电离杂质电荷面密度$Q_{AD}$
5. 栅氧化层中的电荷面密度$Q_{OX}$

- 离子注入后的阈值电压
$$V'_T=\Phi_{MS}-\dfrac{Q_{OX}}{C_{OX}}-\frac{Q_T}{C_{OX}}-\frac{Q_A}{C_{OX}}(1-\dfrac{qN_IR^2}{4\epsilon_s\Phi_{FP}})^{\frac12}+2\Phi_{FP}$$
$$\Delta V_T=-\frac{Q_I}{C_{OX}}-\frac{Q_A}{C_{OX}}[(1-\dfrac{qN_IR^2}{4\epsilon_s\Phi_{FP}})^{\frac12}-1]$$
$$N_I=\Delta N\quad Q_I=-qN_IR$$

### MOSFET直流电亚方程
##### 非饱和区
1. 沟道电流只由漂移电流构成，忽略扩散电流
2. 采用缓变沟道近似
3. 沟道内的载流子(电子)迁移率为常数
4. 采用强反型近似，即认为当表面少子浓度达到体内平衡多子浓度($\Phi_S=\Phi_{s,inv}$)时沟道开始导电
5. $Q_{OX}为常数$
- 漏级电流一般表达式
$$I_D=-Z\mu_nQ_n\frac{\mathrm{d}V}{\mathrm{d}y} \quad Q_n=\int_0^bqn\mathrm{d}x \\
I_D=\frac ZL\mu_n\int^{V_D}_{V_S}(-Q_n)\mathrm{d}V$$
- 沟道电子电荷面密度$Q_b$
$$V_G>V_T\qquad Q_n=-C_{OX}(V_G-V_B-V_{FB}-\Phi{S,inv})-Q_A$$
$$V_D>V_S\qquad \Phi_{S,inv}(y)=2\Phi_{FP}-V_B+V(y) \\
x_d(y)=\sqrt{\frac{2\epsilon_s}{qN_A}[2\Phi_{FP}-V_B+V(y)]} \\
Q_A(y)=-qN_Ax_d$$
- 漏级电流精确表达式
$$I_D=\frac ZL\mu_nC_{OX}[(V_{GS}-V_T)V_{DS}-\frac12V_{DS}^2]$$

