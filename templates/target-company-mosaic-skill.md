---
name: mosaic-<ticker-lowercase>
description: >-
  [<Company Name> (<Ticker>)] 数学量化马赛克投研模型 (Quantitative Mosaic Skill)。
  基于第一性原理物理单位（<基础物理单位>）、供需瓶颈方程、固定/可变成本经营杠杆模型及逆向高频数据节点构建。
---

# Quantitative Mosaic Model: <Company Name> (`<Ticker>`)

## Step 1: 物理与商业属性定义 (Physical & Commercial Ontology)

* **核心商业本质**：`<设备 / 耗材 / 算力 / 软件 / 能源>`
* **基础物理产出量纲 ($u_{\text{base}}$)**：`<例如：等效 12 寸晶圆片数 / 测试秒数 / 兆瓦时 / 机架台数>`
* **计价与商业变现物理锚点**：`<例如：按单台设备交付验收 / 按测试时间吞吐量 / 按瓦特容量租赁>`

---

## Step 2: 供给与需求物理方程 ($Q_{\text{actual}} = \min(Q_{\text{supply}}, Q_{\text{demand}})$)

### 2.1 供给侧物理约束方程 (Supply Constraint)

$$Q_{\text{supply}}(t) = \min_{i \in \mathcal{B}} \left( \frac{C_i(t) \cdot \eta_i(t) \cdot Y_i(t)}{\alpha_i} \right)$$

| 变量符号 | 物理定义 | 物理量纲 | 基准校准区间 | 制约机理说明 |
| :--- | :--- | :--- | :--- | :--- |
| $C_1(t)$ | `<核心瓶颈物料/产能配额>` | `<物理单位>` | `<数值>` | `<如：上游单一供应商配额>` |
| $\eta_1(t)$ | `<有效设备稼动率>` | `%` | `<数值>` | `<如：扣除维护与换线耗时>` |
| $Y_1(t)$ | `<综合物理良率>` | `%` | `<数值>` | `<如：封装或测试直通率>` |
| $\alpha_1$ | `<单件产出物理消耗定额>` | `<物理单位/件>` | `<数值>` | `<如：每台系统消耗晶圆面积>` |

### 2.2 需求侧物理驱动方程 (Demand Driver)

$$Q_{\text{demand}}(t) = \sum_{k} \left( \frac{\text{CapEx}_k(t) \cdot \omega_k(t)}{P_{\text{sys}}(t)} \right) \cdot \gamma_{\text{attach}}(t) \cdot m_{\text{replace}}(t)$$

| 变量符号 | 物理定义 | 物理量纲 | 基准校准区间 | 驱动机理说明 |
| :--- | :--- | :--- | :--- | :--- |
| $\text{CapEx}_k(t)$ | `<下游核心客户资本开支>` | `USD / RMB` | `<数值>` | `<具体客户群资本开支预算>` |
| $\omega_k(t)$ | `<目标环节物理价值占比>` | `%` | `<数值>` | `<资本开支分配至本环节比例>` |
| $\gamma_{\text{attach}}(t)$ | `<单系统物理配套乘数>` | `<件/套>` | `<数值>` | `<技术迭代带来的单机用量倍增>` |
| $m_{\text{replace}}(t)$ | `<存量物理替换系数>` | `1/Years` | `<数值>` | `<物理磨损或代际淘汰周期倒数>` |

---

## Step 3: 财务翻译与经营杠杆模型 (Financial Translation)

### 3.1 收入与毛利解析方程
$$\text{Rev}(t) = Q_{\text{actual}}(t) \cdot \text{ASP}(t)$$
$$\text{COGS}(t) = \text{FC}_{\text{mfg}}(t) + Q_{\text{actual}}(t) \cdot \frac{v_{\text{raw}}(t)}{Y(t)}$$
$$\text{GP}(t) = \text{Rev}(t) - \text{COGS}(t)$$

### 3.2 每股收益 (EPS) 与经营杠杆
$$\text{EPS}(t) = \frac{\big(\text{GP}(t) - \text{OpEx}_{\text{fixed}}(t) - \beta_{\text{var}} \cdot \text{Rev}(t) - I_{\text{net}}(t)\big) \cdot (1 - \tau_{\text{tax}})}{S_{\text{diluted}}(t)}$$

---

## Step 4: 逆向工程高频数据节点 (Reverse Engineering Data Nodes)

| 节点类别 | 精确追踪指标 / 编码 | 数据源与抓取路径 | 映射的物理变量 | 领先周期 |
| :--- | :--- | :--- | :--- | :--- |
| **海关 HS 编码** | `HS Code: <8-10位编码>` | `<海关统计局 / 进出口数据库>` | $Q_{\text{supply}}, Q_{\text{actual}}$ | `<如：1-2 个月>` |
| **上下游财报科目** | `<指定供应商/客户名称 + 精确会计科目>` | `<SEC EDGAR 10-Q / 巨潮资讯季报>` | $C_1(t), \text{CapEx}_k(t)$ | `<如：1 个季度>` |
| **行业物理高频指标** | `<电网并网MW / 货运指数 / FSE招聘数>` | `<具体行业网站或监管公示平台>` | $\eta(t), Q_{\text{demand}}(t)$ | `<如：实时 / 周度>` |

---

## Step 5: 强制输出协议 (Mandatory Output Schema)

调用本 Skill 分析 `<Ticker>` 时，必须输出以下三部分：
1. **核心变量提取表**：当前周期各物理参数的实时提取值与数据出处。
2. **瓶颈判定结论**：显式计算 $Q_{\text{supply}}$ vs $Q_{\text{demand}}$，指出当前决定 $Q_{\text{actual}}$ 的单一最紧约束。
3. **敏感性冲击测试**：当核心瓶颈变量或良率 $Y$ 变动 $\pm 5\%$ 时，对 $\text{Rev}$、$\text{GM}\%$、$\text{EPS}$ 的量化弹性矩阵。
