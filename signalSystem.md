## 信号与系统
[toc]
---
### 信号
---
#### 连续信号
- 时域：$x(t)$
- 频域：$X(\mathbf{j}\omega)$
$$f(t)=\frac{1}{2\pi}\int F(\omega)e^{\mathbf{j}\omega t}d\omega$$
- 复频域：$X(s)$
$$f(t)=\frac{1}{2\pi}\int F(s)e^{\mathbf{j}st}ds$$
#### 离散信号
- 时域：$x(n)$
- 频域：$x(e^{\mathbf{j}\omega})$
$$$$
- Z域：$X(z)$
$$x(n)=\frac{1}{2\pi}\int x(z)$$
---

### 系统
---
#### 连续系统
- 时域：微分方程
- 频域：$H(\mathbf{j}\omega)$
- 复频域：$H(s)$
#### 离散系统
- 时域：差分方程
- 频域
- Z域
---

### 信号与系统分析导论
---
#### 信号的描述
#### 信号的自变量变换
#### 基本信号
#### 系统及其数学模型
#### 系统的性质
- 线性：同时满足均匀性与叠加性
- 时不变性：系统输出与时间无关
- 因果性
- 稳定性：输入有界，输出也有界
- 可逆性
#### 信号分类
- 能量信号
- 功率信号
- 信号总能量与平均功率都是$\infin$
#### 信号分解
$$x(t)=x_e(t)+x_0(t)$$
---
### 信号与系统的时域分析
---
#### LTI系统的时域分析---卷积积分和卷积和
#### LTI系统的微分方程和差分方程表示
#### LTI系统的框图表示
#### 奇异函数
---
### 周期信号、非周期信号的傅利叶分析
---
#### 周期信号的频域分析
- 周期信号的傅利叶级数
$$f(t)=\sum^{\infin}_{n=-\infin}C_n\mathbf{e}^{\mathbf{j}n\omega_0t}$$
$$C_n=\frac1{T_0}\int_{T_0}f(t)\mathbf{e}^{-\mathbf{j}n\omega_0t}dt$$
- 周期信号的傅利叶变换
$$X(\mathbf{j}\omega)=2\pi\sum^\infin_{k=-\infin}a_k\delta(\omega-k\omega_0)$$
#### LTI系统的频域分析
1. 连续时间傅利叶变换
---
### 系统的频域特性
#### 傅利叶变换的模和相位
$$Y(\mathbf{j}\omega)$$
#### LTI系统的幅频特性和相频特性，系统的失真
#### 系统的不失真传输条件
#### 理想滤波器的频域、时域特性及其不可实现性
- 理想滤波器：
$$H(\mathbf{j}\omega)$$
- 采样
$$p(t)=\sum^\infin_{n=-\infin}\delta(t-nT)$$
$$P(\mathbf{j}\omega)=\omega_s\sum\delta(\omega-k\omega_s)$$
$$X_p(\mathbf{j}\omega)=\frac1{2\pi}X(\mathbf{j}\omega)*\frac{2\pi}T\sum\delta(\omega-k\omega_s)$$
#### 信号的幅度调制与解调
---
### 拉普拉斯变换
---
### Z变换
---
### Z变换与拉普拉斯变换的关系
$$对x_a(t)采样，
X(z)|_{z=\mathbf{e}^{sT}}=X(s)$$
$$z=|z|\mathbf{e}^{\mathbf{j}\phi}$$

> 考试时间：2019-1-3 第二场
>
> 地点：X4151
>
> 答疑：9120
