# Quantitative Mosaic Generator (`system:quantitative-mosaic-generator`)

**简体中文** | [English](./README_EN.md)

> **生成任意指定标的的数学量化马赛克投研框架 (Supply/Demand/Financial Model & Scraping Nodes) 的元技能 (Meta-Skill)**

## 简介

`quantitative-mosaic-generator` 是一个专为 AI 投研 Agent（如 Google Antigravity、Claude Code、Codex）设计的 **元技能（Meta-Skill）**，用于向模型注入专业性。

当用户输入任意一家上市公司（Ticker）及其核心业务时，该技能会强制摒弃“市盈率相对估值法”、“行业景气度高”等空洞定性套话，从**第一性原理的物理单位**（瓦特、测试秒数、晶圆片数、机架台数、良率）出发，自动生成一套包含：
1. **物理与商业属性定义**（基础物理单位与变现锚点）
2. **供给与需求约束方程**（$Q_{\text{actual}} = \min(Q_{\text{supply}}, Q_{\text{demand}})$）
3. **财务翻译与经营杠杆模型**（良率损耗、固定折旧摊薄与 EPS 弹性）
4. **逆向工程高频数据源节点**（精确到 8-10 位海关 HS 编码、竞争对手/上下游特定季报科目、行业高频物理指标）
5. **强制量化输出协议**（参数提取、瓶颈识别、$\pm 5\%$ 敏感性矩阵）

---

## 目录结构

```text
quantitative-mosaic-generator/
├── SKILL.md                                    # 核心元技能指令文件（默认中文，零上下文冗余）
├── SKILL_EN.md                                 # 英文版元技能规范（按需懒加载，平时 0 Token 占用）
├── templates/
│   ├── target-company-mosaic-skill.md          # 目标公司专属 Mosaic Skill 标准中文模板
│   └── target-company-mosaic-skill-en.md       # 目标公司专属 Mosaic Skill 标准英文模板
├── README.md                                   # 中文仓库说明文档
├── README_EN.md                                # 英文仓库说明文档
└── .gitignore                                  # Git 忽略规则
```

---

## 安装方式

### 1. Google Antigravity
将本仓库克隆至全局技能目录：
```bash
git clone https://github.com/akdunwu/quantitative-mosaic-generator.git ~/.gemini/config/skills/quantitative-mosaic-generator
```

### 2. OpenAI Codex / Claude Code
```bash
git clone https://github.com/akdunwu/quantitative-mosaic-generator.git ~/.codex/skills/quantitative-mosaic-generator
```

---

## 调用方式

在对话中直接输入：
- `生成关于 [NVDA / 英伟达] 的 Quantitative Mosaic Skill`
- `生成关于 [Teradyne / TER] 的 Quantitative Mosaic Skill`
- `使用 quantitative-mosaic-generator 为 [中际旭创 / 300308] 构建物理量纲投研模型`
