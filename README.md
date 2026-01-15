# AI-Powered-Recruitment-Platform

基于 Claude Code Agent 的智能简历筛选系统

---

## 项目简介

这是一套完整的、本地化运行的AI简历筛选解决方案，确保招聘过程**公平、公正、透明、可追溯**。

### 核心特点

- **标准先行**：筛选前必须完成备案，锁定后不可修改
- **过程透明**：使用什么模型、什么提示词，全部记录在案
- **结果公示**：筛选标准对外公开，个人结果可查询
- **全程可追溯**：每个评分都有依据，支持审计和申诉
- **宁缺勿滥**：全网核实只采用100%确定的信息

---

## 快速开始

```bash
# 进入系统目录
cd resume-screening-system

# 查看详细说明
cat README.md
```

**详细使用指南请参考**：[resume-screening-system/README.md](resume-screening-system/README.md)

---

## 系统架构

```
第一阶段【备案】 → 第二阶段【执行】 → 第三阶段【公示】 → 第四阶段【归档】
      ↓                  ↓                  ↓                  ↓
  制定标准           启动Claude          公示标准          永久存档
  设计提示词         逐份评估            开放查询          审计日志
  审批签字           全网核实            处理申诉
```

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
    │   ├── 提示词库/                  # 各岗位提示词
    │   └── 输出模板/                  # 输出文件模板
    ├── examples/                      # 示例文件
    ├── docs/                          # 详细文档
    └── workspace/                     # 工作区
```

---

## 适用岗位

系统已提供以下岗位的提示词模板：

| 部门 | 岗位 |
|------|------|
| HR部门 | HR专员、HRBP |
| 技术部门 | Java工程师、前端工程师、产品经理 |
| 财务部门 | 财务专员 |
| 市场部门 | 市场专员 |

> 其他岗位可基于通用模板进行定制

---

## 文档索引

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

## 许可证

本项目仅供学习和内部使用。

---

## 联系方式

如有问题或建议，请提交 Issue。
