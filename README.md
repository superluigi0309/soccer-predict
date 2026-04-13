# Football Betting Prediction Skill

## English Description

An AI-powered football (soccer) match prediction and betting analysis system designed for OpenClaw.

### Features

- **Automated Data Collection**: Scrapes pre-match data from titan007.com, including Asian handicap, over/under, European odds, team fundamentals, lineups, corner kicks, and half-time goals
- **5-Step Quantitative Analysis Framework**:
  1. Data organization and validation
  2. Fundamental analysis (handicap rationality, line movement, bookmaker intent)
  3. Odds probability calculation (true implied probability adjusted for margin)
  4. Logistic regression models for Asian handicap and over/under predictions
  5. EV calculation and betting recommendations
- **Dual Output Modes**: Choose between concise (quick results) or visual/detailed (full HTML reports)
- **Post-Match Review & Learning**: Automated deviation analysis, framework optimization, and accuracy tracking with auto-adjusted weights
- **Enhanced Over/Under Model**: Incorporates half-time goal patterns, corner kick data, league-specific factors, and environmental variables

### Installation

#### Option 1: Using Skills CLI (Recommended)

```bash
npx skills add superluigi0309/soccer-predict
```

#### Option 2: Manual Installation

1. Download the .skill file from GitHub releases
2. Extract to `~/.claude/skills/`

```bash
# Example
mkdir -p ~/.claude/skills
cd ~/.claude/skills
unzip football-betting-prediction.skill
```

#### Option 3: Git Submodule

```bash
# Add as submodule to your project
git submodule add https://github.com/superluigi0309/soccer-predict.git skills/football-betting-prediction
```

### Usage

#### How to Get Match ID

You can get the match ID from titan007.com:

1. Visit [ titan007.com](https://zq.titan007.com/)
2. Find your desired match (e.g., MLS, Premier League, etc.)
3. Click on "数据分析" (Data Analysis) for the match
4. The match ID is the number in the URL: `https://zq.titan007.com/analysis/{match_id}cn.htm`

Alternatively, you can provide a match description instead:
- Format: `Date Time League HomeTeam vs AwayTeam`
- Example: `2026.3.15 09:30 MLS Real Salt Lake vs Austin FC`

#### Start Prediction

Provide a match ID or description to start prediction:

```
Match ID: 2908467
Match description: 2026.3.15 MLS Real Salt Lake vs Austin FC
```

After prediction, provide the match result for post-match review:

```
Score: 2-1
```

### Output Modes

- **Concise Mode**: Quick results — best pick, probability, EV, predicted score
- **Visual Mode**: Full HTML report with data tables, probability bars, and formulas

### Target

Achieve 70%+ accuracy for both Asian handicap and over/under predictions through iterative learning.

---

## 中文描述

专为 OpenClaw 打造的足球比赛博彩预测与分析系统。

### 功能特点

- **自动化数据采集**：从 titan007.com 抓取赛前数据，涵盖亚盘、大小球、欧赔、球队基本面、首发阵容、角球及半场进球等
- **五步量化分析框架**：
  1. 数据整理与验证
  2. 基本面分析（盘口合理性、走势研判、机构意图）
  3. 盘口概率计算（剔除抽水后的真实隐含概率）
  4. 逻辑回归模型（亚盘与大小球双预测）
  5. EV 计算与投注建议
- **双输出模式**：简洁模式（快速获取结果）或可视化模式（完整 HTML 报告）
- **赛后复盘与学习**：自动偏差分析、框架迭代优化、准确率追踪，支持权重动态调整
- **大小球增强模型**：融合半场进球规律、角球数据、联赛特性及环境因素

### 安装

#### 方式一：使用 Skills CLI（推荐）

```bash
npx skills add superluigi0309/soccer-predict
```

#### 方式二：手动安装

1. 从 GitHub releases 下载 .skill 文件
2. 解压至 `~/.claude/skills/`

```bash
# 示例
mkdir -p ~/.claude/skills
cd ~/.claude/skills
unzip football-betting-prediction.skill
```

#### 方式三：Git Submodule

```bash
# 添加为子模块
git submodule add https://github.com/superluigi0309/soccer-predict.git skills/football-betting-prediction
```

### 使用方法

#### 如何获取比赛 ID

你可以从 titan007.com 获取比赛 ID：

1. 访问 [titan007.com](https://zq.titan007.com/)
2. 找到你需要的比赛（如美职业、英超等）
3. 点击比赛的"数据分析"
4. 比赛 ID 即为 URL 中的数字：`https://zq.titan007.com/analysis/{match_id}cn.htm`

或者，你也可以直接提供比赛描述：
- 格式：`日期 时间 联赛 主队 vs 客队`
- 示例：`2026.3.15 09:30 美职业 皇家盐湖城 vs 奥斯汀`

#### 开始预测

提供比赛 ID 或描述开始预测：

```
比赛ID: 2908467
比赛描述: 2026.3.15 美职业 皇家盐湖城 vs 奥斯汀
```

预测完成后，提供赛果进行复盘：

```
比分: 2-1
```

### 输出模式

- **简洁模式**：快速输出最佳推荐、胜率、EV 值及预测比分
- **可视化模式**：完整 HTML 报告，含数据表格、概率进度条及计算公式

### 目标

通过持续迭代学习，实现亚盘与大小球双维度 70%+ 预测准确率。

---

## Repository Structure

```
football-betting-prediction/
├── SKILL.md                          # Main skill definition
├── README.md                         # This file
├── LICENSE                           # License
└── references/
    ├── data-collection.md            # Data scraping guide
    ├── prediction-framework.md       # Analysis framework
    └── review-framework.md           # Post-match review & learning
```

## License

MIT License
