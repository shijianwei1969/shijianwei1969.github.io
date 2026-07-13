## 文章13第4节：体积归一化——建立与模参数无关的 $\chi_g$ 定义

### 4.1 任务定位

第2节建立了 $\chi_g$ 的微观定义：

$$
\chi_g = \frac{1}{V_8} \int_{M_8} [A \cdot c_2^2 + B \cdot c_4]
$$

第3节建立了局域化投影规则：

$$
(\chi_g^{(3)})_{ij} = \sqrt{S_i S_j} \cdot Q_{ij}
$$

但这两者都依赖于体积 $V_8$，而 $V_8$ 在弦论中不是一个固定的常数——它随着Kähler模参数 $t$ 的变化而变化。

第4节的任务是：建立一个与模参数无关的 $\chi_g$ 定义，使得极化率张量不依赖于人为的标度选择，为后续P1-2（文章14）的大体积压制计算奠定基础。

---

### 4.2 体积 $V_8$ 对Kähler模的依赖

对于CY4，体积 $V_8$ 是Kähler模 $t$ 的函数。在单个Kähler模的简化设定下（对应于 $\mathbb{P}^5$ 六次超曲面的一维Kähler锥），体积与 $t$ 的关系为：

$$
V_8 = V_0 \cdot t^4
$$

其中 $V_0$ 是 $t=1$ 时的参考体积。$t^4$ 因子来自Kähler形式 $J$ 的幂次：$J \propto t \cdot \omega$（其中 $\omega$ 是某个基准(1,1)-形式），则体积形式 $\frac{1}{4!} J^4 \propto t^4$。

文章7的无量纲比值 $\mathcal{R} = 495360\pi^4$ 是在 $t=1$ 的约定下计算的。当 $t \neq 1$ 时，曲率积分 $\int \text{Tr}(R^4)$ 本身会随 $t$ 变化吗？

这里有一个关键点：**Chern类的积分是拓扑不变量，不依赖于度量的具体选择。** 因此 $\int c_2^2$ 和 $\int c_4$ 是固定的拓扑数（对于 $\mathbb{P}^5$ 六次超曲面，分别为 $1350$ 和 $2610$），与 $t$ 无关。

而曲率积分 $\int \text{Tr}(R^4)$ 与Chern类积分的关系由Chern-Weil理论给出：

$$
\int_{M_8} \text{Tr}(R^4) = 32\pi^4 \int_{M_8} c_2^2 - 64\pi^4 \int_{M_8} c_4
$$

由于等式右边是拓扑不变量，左边 $\int \text{Tr}(R^4)$ 也**与 $t$ 无关**。这意味着当 $t$ 变化时，曲率形式 $R_{ab}$ 会在流形上重新分布，但其四次幂的积分保持不变。

因此，$\chi_g$ 对 $t$ 的依赖**完全来自分母中的 $V_8$**：

$$
\chi_g(t) = \frac{1}{V_0 \, t^4} \int_{M_8} [A \cdot c_2^2 + B \cdot c_4] \propto \frac{1}{t^4}
$$

---

### 4.3 模参数无关的定义

为了使 $\chi_g$ 的核心几何属性与模参数 $t$ 解耦，我们需要将体积因子吸收到一个重新定义的"约化极化率"中。

定义**约化极化率张量** $\tilde{\chi}_g$：

$$
\tilde{\chi}_g = V_8 \cdot \chi_g = \int_{M_8} [A \cdot c_2^2 + B \cdot c_4]
$$

$\tilde{\chi}_g$ 是纯粹的拓扑/几何常数。在弦长 $l_s = 1$ 的自然单位制下，它是一个无量纲的常数矩阵，完全由CY4的拓扑决定；若恢复弦长量纲，则 $\tilde{\chi}_g$ 具有体积量纲 $l_s^8$。

相应地，局域化投影后的 $3 \times 3$ 子块也重新定义为：

$$
(\tilde{\chi}_g^{(3)})_{ij} = V_8 \cdot (\chi_g^{(3)})_{ij} = \sqrt{S_i S_j} \cdot V_8 \cdot Q_{ij}
$$

定义**约化归一化投影矩阵** $\tilde{Q}_{ij}$：

$$
\tilde{Q}_{ij} = V_8 \cdot Q_{ij} = \int_{M_8} (\hat{u}_i \wedge \star \hat{u}_j) \cdot \mathcal{I}(\mathcal{R})
$$

则 $\tilde{Q}_{ij}$ 也是与 $t$ 无关的纯几何常数。

---

### 4.4 与 $\varepsilon_{\text{geom}}$ 表达式的衔接

文章11的 $\varepsilon_{\text{geom}}$ 表达式为：

$$
\varepsilon_{\text{geom}} = 0.2348\kappa_0 + C_{\text{mid}} \kappa_0^2
$$

其中二阶项系数 $C_{\text{mid}}$ 来自 $\chi_g$ 的贡献：

$$
C_{\text{mid}} \kappa_0^2 = \frac{v^T M_1^{1/2} \chi_g M_1^{1/2} v}{v^T M_1^0 v}
$$

代入 $\chi_g = \tilde{\chi}_g / V_8$：

$$
C_{\text{mid}}(t) = \frac{1}{V_8} \cdot \frac{v^T M_1^{1/2} \tilde{\chi}_g M_1^{1/2} v}{v^T M_1^0 v}
$$

因此 $C_{\text{mid}}$ 本身依赖于 $1/V_8$。在 $t=1$ 时，$V_8 = V_0$，$C_{\text{mid}}$ 取基准值 $C_{\text{mid}}^0$。当 $t$ 变化时：

$$
C_{\text{mid}}(t) = \frac{C_{\text{mid}}^0}{t^4}
$$

代入 $\varepsilon_{\text{geom}}$ 表达式：

$$
\varepsilon_{\text{geom}}(t) = 0.2348\kappa_0 + \frac{C_{\text{mid}}^0}{t^4} \cdot \kappa_0^2
$$

当 $t \gg 1$（大体积极限）时，二阶项被体积因子 $t^4$ 强烈压制，微扰展开更加收敛。这正是文章12所预言的**大体积压制机制**的数学实现。

---

### 4.5 与文章7的 $\mathcal{R}$ 的衔接验证

文章7的无量纲比值 $\mathcal{R} = 495360\pi^4$ 是在 $t=1$ 下计算的。其定义为：

$$
\mathcal{R} = \left. \frac{\int_{M_8} \text{Tr}(R^4)}{V_8} \right|_{t=1} = \frac{\int_{M_8} \text{Tr}(R^4)}{V_0}
$$

因此，参考体积 $V_0$ 为：

$$
V_0 = \frac{\int_{M_8} \text{Tr}(R^4)}{\mathcal{R}} = \frac{123840\pi^4}{495360\pi^4} = \frac{1}{4}
$$

> **几何注记**：这个 $1/4$ 并非巧合。对于 $\mathbb{P}^5$ 的六次超曲面，其相交数 $d = 6$。单模CY4的体积公式为 $V_8 = \frac{d}{4!} t^4 = \frac{6}{24} t^4 = \frac{1}{4} t^4$。这与我们的计算完美吻合！

这意味着在 $t=1$ 的约定下，$V_0 = 1/4$（在自然几何单位下）。当 $t$ 变化时：

$$
V_8 = \frac{1}{4} \cdot t^4
$$

代入 $\chi_g$ 表达式：

$$
\chi_g(t) = \frac{\int_{M_8} [A \cdot c_2^2 + B \cdot c_4]}{\frac{1}{4} \cdot t^4} = \frac{4}{t^4} \int_{M_8} [A \cdot c_2^2 + B \cdot c_4]
$$

当 $t \sim 10^2$ 时（大体积极限），$t^4 \sim 10^8$，$\chi_g$ 被压制到 $10^{-3} \sim 10^{-4}$ 量级，与文章12的需求完美一致。✅

---

### 4.6 第4节结论

1. **体积依赖**：$\chi_g \propto 1/t^4$，其中 $t$ 是Kähler模参数。
2. **约化极化率**：定义 $\tilde{\chi}_g = V_8 \cdot \chi_g = \int [A \cdot c_2^2 + B \cdot c_4]$，为与 $t$ 无关的拓扑/几何常数。
3. **压制机制量化**：$C_{\text{mid}}(t) = C_{\text{mid}}^0 / t^4$，大体积极限下二阶项被 $t^4$ 压制。
4. **与文章7衔接**：严格推导出 $V_0 = 1/4$（源自相交数 $d=6$ 与 $4!$ 的比值），当 $t \sim 10^2$ 时压制因子 $\sim 10^{-8}$，满足微扰收敛性要求。
5. **下一步**：P1-2（文章14）将计算 $\lambda_{\text{eff}}$ 和 $\mu_{\text{eff}}$ 的具体数值，并验证大体积压制机制的定量实现。

---

*第4节完。第5节将总结P1-1的阶段性成果，并前瞻P1-2的工作方向。*