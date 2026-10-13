---
name: quantitative-mosaic-generator
description: >-
  生成任意指定标的的数学量化马赛克投研框架 (Supply/Demand/Financial Model & Scraping Nodes) 的元技能 (system:quantitative-mosaic-generator)。
  当用户输入任意一家公司（Ticker）及其核心业务，或要求“生成关于 [Company X] 的 Quantitative Mosaic Skill”、“构建 [Ticker] 的量化马赛克模型”、“逆向物理量纲投研框架”时立即激活。
  严禁使用“市盈率相对估值法”等空洞语言，强制深入到物理单位（瓦特、秒、件、晶圆片数、良率）与精确的供需瓶颈方程。
---

# Meta-Skill: Quantitative Mosaic Generator (`system:quantitative-mosaic-generator`)

## 目标与作用
当用户输入任意一家公司（Ticker）及其核心业务时，系统需自动生成一套包含**精确数学方程**、**核心变量物理约束**和**逆向工程高频数据源**的投研配置档案（`SKILL.md`）。

> **核心铁律**：严禁使用“市盈率相对估值法”、“行业景气度高”、“龙头壁垒深厚”等空洞定性语言；所有推演必须还原并锚定至**第一性原理的物理单位**（如：瓦特 $\text{W}$、测试秒数 $\text{s}$、物理件数 $\text{Units}$、晶圆片数 $\text{Wafers}$、机架数 $\text{Racks}$、百分比良率 $Y\%$）。

---

## 框架生成法则 (Generation Rules)

在为目标公司生成专属 Quantitative Mosaic `SKILL.md` 时，必须严格执行以下 5 个步骤：

### Step 1: 定义物理与商业属性 (Physical & Commercial Ontology)
1. **产业链物理定性**：确认目标公司的核心产品在产业链中的物理性质（资本品设备 / 一次性耗材 / 算力基础设施 / 工业软件授权 / 能源介质）。
2. **基础物理量纲 ($u_{\text{base}}$)**：定义其产出的最基础物理单位及时间维度（例如：$\text{GPU-Hours}$、晶圆测试秒数 $\text{Test-Seconds}$、等效 12 寸晶圆片数 $\text{Wafers/Month}$、液冷机架交付数 $\text{Racks/Quarter}$、有效兆瓦数 $\text{MW}$）。
3. **价值计价锚点**：明确客户付费对应的物理消耗机制（按吞吐量、按装机保有量、按工时或按良率分成）。

---

### Step 2: 建立供给与需求方程 ($Q_{\text{actual}} = \min(Q_{\text{supply}}, Q_{\text{demand}})$)

#### 1. 供给侧方程 (Supply Constraint)
构建显式数学公式，找出制约目标公司有效产出的最关键上游物料、洁净室面积、设备交期或物理瓶颈（如：变压器容量/用电配额、单一垄断供应商配额、工艺良率爬坡曲线）：

$$Q_{\text{supply}}(t) = \min_{i \in \mathcal{B}} \left( \frac{C_i(t) \cdot \eta_i(t) \cdot Y_i(t)}{\alpha_i} \right)$$

* **$C_i(t)$**：第 $i$ 项核心瓶颈资源在周期 $t$ 的名义物理配额或额定产能（如：CoWoS 晶圆分配片数、核心腔体交付量、变电站批复兆瓦数）。
* **$\eta_i(t)$**：设备稼动率或有效运行时间占比（Utilization Rate $\in [0, 1]$）。
* **$Y_i(t)$**：综合良品率（Composite Yield Rate $\in [0, 1]$）。
* **$\alpha_i$**：单位终端产品消耗的第 $i$ 项上游物理资源系数（Unit Consumption Coefficient）。
* **要求**：必须逐一列出所有变量的数学符号、物理量纲、当前基准值区间及物理意义。

#### 2. 需求侧方程 (Demand Driver)
**严禁使用宏观 GDP 或笼统的 CAGR 增速**。必须将需求拆解为**下游资本开支的函数**或**物理替代乘数**（如：技术渗透率 $\times$ 存量设备替换周期 $\times$ 单机物理价值量倍增系数）：

$$Q_{\text{demand}}(t) = \sum_{k \in \mathcal{C}} \left( \frac{\text{CapEx}_k(t) \cdot \omega_k(t)}{P_{\text{system}, k}(t)} \right) \cdot \gamma_{\text{attach}}(t) \cdot m_{\text{replace}}(t)$$

或基于物理吞吐量驱动：

$$Q_{\text{demand}}(t) = N_{\text{installed}}(t) \cdot \rho_{\text{penetration}}(t) \cdot \frac{\tau_{\text{unit}}(t)}{T_{\text{cycle}}}$$

* **$\text{CapEx}_k(t)$**：下游核心客户 $k$ 在周期 $t$ 的特定领域资本开支。
* **$\omega_k(t)$**：该项资本开支中流向目标物理环节的配比权重。
* **$\gamma_{\text{attach}}(t)$**：单套系统配套搭载率（Attach Rate）或物理通道数乘数。
* **$\tau_{\text{unit}}(t)$**：单颗芯片/单件产品的物理处理耗时或消耗定额（如：单颗芯片 ATE 测试秒数）。

#### 3. 实际出货/结算量方程 (Actual Volume Determination)
$$Q_{\text{actual}}(t) = \min\Big(Q_{\text{supply}}(t),\; Q_{\text{demand}}(t)\Big)$$

---

### Step 3: 建立财务翻译模型 (Financial Translation)

建立严格闭环的解析方程，将物理出货量 ($Q_{\text{actual}}$) 和平均物理单价 ($\text{ASP}$) 转换为营业收入 ($\text{Rev}$)、毛利润 ($\text{GP}$)、营业利润 ($\text{EBIT}$) 及每股收益 ($\text{EPS}$)，并显式刻画固定成本摊薄与经营杠杆效应：

1. **收入方程 (Revenue)**：
   $$\text{Rev}(t) = \sum_{j} Q_{\text{actual}, j}(t) \cdot \text{ASP}_j(t)$$
   其中 $\text{ASP}_j(t) = \text{ASP}_{j,0} \cdot (1 + \Delta_{\text{mix}}(t)) \cdot (1 - \delta_{\text{erosion}}(t))$，拆解产品结构升级（Mix Shift）与年降系数。

2. **成本与毛利方程 (Cost of Goods Sold & Gross Profit)**：
   $$\text{COGS}(t) = \text{FC}_{\text{mfg}}(t) + \sum_{j} Q_{\text{actual}, j}(t) \cdot \frac{v_{\text{raw}, j}(t)}{Y_j(t)}$$
   $$\text{GP}(t) = \text{Rev}(t) - \text{COGS}(t), \quad \text{GM}\%(t) = 1 - \frac{\text{FC}_{\text{mfg}}(t)}{\text{Rev}(t)} - \frac{\overline{v_{\text{raw}}}(t)}{\overline{Y}(t) \cdot \overline{\text{ASP}}(t)}$$
   * **$\text{FC}_{\text{mfg}}(t)$**：制造端固定折旧与刚性人工摊销（体现产能利用率带来的经营杠杆）。
   * **$v_{\text{raw}, j}(t)$**：合格品前的单位可变物理物料与能耗成本；除以良率 $Y_j(t)$ 体现良率波动对毛利率的非线性冲击。

3. **每股收益方程 (EPS Translation)**：
   $$\text{EPS}(t) = \frac{\big(\text{GP}(t) - \text{OpEx}_{\text{fixed}}(t) - \beta_{\text{var}} \cdot \text{Rev}(t) - I_{\text{net}}(t)\big) \cdot (1 - \tau_{\text{tax}})}{S_{\text{diluted}}(t)}$$

4. **经营杠杆弹性系数 (Degree of Operating Leverage, DOL)**：
   $$\frac{\partial \ln(\text{EPS})}{\partial \ln(Q_{\text{actual}})} = \frac{Q_{\text{actual}} \cdot \big(\text{ASP} - v_{\text{raw}}/Y - \beta_{\text{var}}\cdot \text{ASP}\big)}{\text{GP} - \text{OpEx}_{\text{fixed}} - \beta_{\text{var}} \cdot \text{Rev} - I_{\text{net}}}$$

---

### Step 4: 设定逆向数据源 (Reverse Engineering Data Nodes)

* **严禁空泛建议**（如“查看公司财报”、“关注行业新闻”、“调研上下游”）。
* **必须具体到可抓取、可验证的指标与字段级别**：
  1. **海关与贸易物理追踪**：指定精确的 6–10 位海关 **HS 编码 (Harmonized System Code)**、特定出口港/州/省代码、计量单位（千克/台）以反推物理出货吨位或台数。
  2. **上下游交叉财报科目**：指定特定单一供应商或核心客户的季报精确会计科目（如：“合同负债 / Contract Liabilities”、“购买商品及劳务支付的现金”、“在建工程转固节奏”、“存货中的原材料与在产品比例”）。
  3. **物理与工程高频另类数据**：如特定机场航空货运指数（如桃园/仁川电子空运吨位）、区域电网并网队列申请（ISO Interconnection Queue MW）、洁净室特种气体消耗量、特定工种招聘数量（如 Field Service Engineer / 驻厂装机工程师岗位数）、晶圆厂设备 Move-in 招标公示。

---

### Step 5: 强制输出协议 (Output Schema)

生成的目标公司 `SKILL.md` 必须包含一段强制约束指令，要求任何最终调用该专属 Skill 的 Agent 严格按照以下结构输出投研报告：

1. **核心物理变量提取表 (Parameter Extraction Table)**：
   列出当前时点所有供给与需求方程变量的最新校准值、物理单位、数据来源与置信度。
2. **瓶颈点精确识别 (Bottleneck Identification)**：
   定量对比 $Q_{\text{supply}}(t)$ 与 $Q_{\text{demand}}(t)$，明确判定当前周期受制于供给侧（指出具体卡点变量 $C_i$ 或 $Y_i$）还是需求侧（指出具体下游变数）。
3. **财务预测与局部导数敏感性矩阵 (Financial Forecast & Sensitivity Matrix)**：
   计算核心物理变量（如良率 $Y$、瓶颈配额 $C_i$、测试耗时 $\tau$、$\text{ASP}$）各自变动 $\pm 5\%$ 时，对 $\text{Rev}$、$\text{GM}\%$ 和 $\text{EPS}$ 的绝对值与百分比冲击。

---

## 执行指令 (Execution Protocol)

当用户发出如下指令时：
- “生成关于 `[Company X / Ticker]` 的 Quantitative Mosaic Skill”
- “用 `quantitative-mosaic-generator` 为 `[Company X]` 建模”
- “生成 `[Company X]` 的数学量化马赛克投研框架”

你必须：
1. 严格遵循上述 **Step 1 至 Step 5** 的逻辑架构。
2. 参考 `./templates/target-company-mosaic-skill.md` 的标准结构。
3. 输出一份完整的、包含标准 YAML Frontmatter、严谨 LaTeX 数学公式和精确逆向数据节点的 Markdown 文档（可直接保存为对应公司的 `SKILL.md`）。
