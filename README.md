# AI-Powered-Recruitment-Platform

**基于 Claude Code Agent 的智能简历筛选系统 | AI Resume Screening System**

> 一套完整的、本地化运行的AI简历筛选解决方案，确保招聘过程公平、公正、透明、可追溯

[![License](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Claude](https://img.shields.io/badge/Powered%20by-Claude-orange.svg)](https://www.anthropic.com/)

---

## 作者

**魏小冲** | 中国人民大学博士生

---

## 项目简介

这是一套基于 **Claude Code Agent** 本地化运行的AI智能简历筛选系统，专为企业HR和招聘团队设计。

### 解决什么问题？

- 传统简历筛选**主观性强**、**标准不统一**
- AI筛选简历缺乏**透明度**和**可追溯性**
- 候选人无法知道**为什么被淘汰**
- 筛选过程缺乏**规范化流程**

### 核心特点

| 特点 | 说明 |
|------|------|
| **标准先行** | 筛选前必须完成备案，Skills、权重锁定后不可修改 |
| **过程透明** | 使用什么模型、什么 Skills，全部记录在案 |
| **结果公示** | 筛选标准对外公开，个人结果可查询 |
| **全程可追溯** | 每个评分都有依据，支持审计和申诉 |
| **宁缺勿滥** | 全网核实只采用100%确定的信息，搜不到不等于造假 |

---

## Skills 框架：系统的核心

> **重要**：Skills 的设计是整个系统成功的关键。每个企业都应该根据自身特点定制 Skills，而不是直接使用通用模板。

### Skills 和 Prompts 的区别

| 概念 | 本质 | 类比 |
|------|------|------|
| **Skills** | 封装好的能力模块 | 员工的专业技能证书 |
| **Prompts** | 单次执行的指令 | "请帮我做XX"这句话 |

**Prompts 是"指令"，Skills 是"能力"**。一个好的 Skills 定义包含：
- 筛选标准（评什么）
- 评分规则（怎么打分）
- 评估流程（怎么做）
- 输出规范（输出什么格式）

### 为什么 Skills 设计如此重要？

1. **同一岗位，不同公司需求完全不同**
   - 互联网大厂的 Java 工程师需要高并发、分布式经验
   - 金融公司的 Java 工程师需要安全合规、事务处理能力
   - AI 创业公司需要 AI 工具使用、快速学习能力

2. **Skills 决定筛选质量的上限**
   - 再好的 AI 模型，Skills 设计不当也无法产出好结果
   - 权重分配体现公司价值观
   - 评分标准决定结果一致性

3. **必须根据公司特点定制**
   - 照搬通用模板会导致筛选效果大打折扣
   - 请阅读 [Skills 设计指南](resume-screening-system/docs/Skills设计指南.md)

---

## 系统架构

```
第一阶段【备案】 → 第二阶段【执行】 → 第三阶段【公示】 → 第四阶段【归档】
      ↓                  ↓                  ↓                  ↓
  制定标准           启动Claude          公示标准          永久存档
  设计Skills          逐份评估            开放查询          审计日志
  审批签字           全网核实            处理申诉
```

---

## 快速开始

```bash
# 1. 克隆仓库
git clone https://github.com/your-username/AI-Powered-Recruitment-Platform.git

# 2. 进入系统目录
cd AI-Powered-Recruitment-Platform/resume-screening-system

# 3. 查看详细说明
cat README.md
```

**重要**：在开始使用前，请务必阅读：
1. [Skills 框架说明](resume-screening-system/docs/Skills框架说明.md) - 理解核心概念
2. [Skills 设计指南](resume-screening-system/docs/Skills设计指南.md) - 如何定制 Skills

**详细使用指南**：[resume-screening-system/README.md](resume-screening-system/README.md)

---

## 目录结构

```
AI-Powered-Recruitment-Platform/
│
├── README.md                          # 本文件
│
└── resume-screening-system/           # 简历筛选系统
    ├── README.md                      # 详细使用指南
    ├── templates/                     # 模板文件
    │   ├── 备案文件/                  # 备案表模板
    │   ├── Skills库/                  # 各岗位 Skills 定义
    │   └── 输出模板/                  # 输出文件模板
    ├── examples/                      # 示例文件
    ├── docs/                          # 详细文档
    └── workspace/                     # 工作区
```

---

## Skills 库

系统提供以下岗位的 Skills 模板作为参考（请根据公司特点定制）：

| 部门 | 岗位 | Skills 文件 |
|------|------|------------|
| HR部门 | HR专员、HRBP | `Skills库/HR部门/` |
| 技术部门 | Java工程师、前端工程师、产品经理 | `Skills库/技术部门/` |
| 财务部门 | 财务专员 | `Skills库/财务部门/` |
| 市场部门 | 市场专员 | `Skills库/市场部门/` |
| 通用 | 基础模板 | `Skills库/通用/` |

> **警告**：这些 Skills 是示例模板，每个公司应该根据自身的公司特点、行业属性和岗位需求进行定制。

---

## 文档索引

### 核心概念文档

| 文档 | 说明 |
|------|------|
| [Skills 框架说明](resume-screening-system/docs/Skills框架说明.md) | 理解 Skills 与 Prompts 的区别 |
| [Skills 设计指南](resume-screening-system/docs/Skills设计指南.md) | 如何根据公司特点设计 Skills |

### 流程文档

| 文档 | 说明 |
|------|------|
| [系统总览](resume-screening-system/README.md) | 完整使用指南 |
| [第一阶段指南](resume-screening-system/docs/第一阶段_备案指南.md) | 如何完成备案 |
| [第二阶段指南](resume-screening-system/docs/第二阶段_执行指南.md) | 如何执行筛选 |
| [第三阶段指南](resume-screening-system/docs/第三阶段_公示指南.md) | 如何公示结果 |
| [第四阶段指南](resume-screening-system/docs/第四阶段_归档指南.md) | 如何归档存储 |
| [全网核实规则](resume-screening-system/docs/全网核实规则.md) | 核实原则和方法 |
| [常见问题FAQ](resume-screening-system/docs/常见问题FAQ.md) | 常见问题解答 |

---

## 前置要求

- [Claude Code CLI](https://docs.anthropic.com/claude-code)
- 有效的 Claude API 访问权限

---

## 关键词 | Keywords

`AI简历筛选` `智能招聘` `Claude` `人工智能招聘` `简历评估` `HR科技` `招聘自动化` `人才筛选` `Skills框架`

`AI Resume Screening` `Intelligent Recruitment` `Claude Code Agent` `HR Tech` `Automated Hiring` `Talent Acquisition` `Resume Evaluation` `Fair Recruitment` `Skills Framework`

---

## Star History

如果这个项目对你有帮助，请给一个 Star 支持一下！

---

## 许可证

本项目采用 MIT 许可证，仅供学习和内部使用。

---

## 联系方式

- **作者**：魏小冲（中国人民大学博士生）
- **问题反馈**：请提交 Issue

---

*让AI招聘更公平、更透明、更可追溯 - Skills 设计是关键*
