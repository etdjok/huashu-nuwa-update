# 女娲 · Skill 造人术

输入一个名字，蒸馏任何人的思维方式——心智模型、决策启发式、表达 DNA、价值观与诚实边界，生成一套可直接运行的 Agent Skill。

基于开放的 [Agent Skills 协议](https://agentskills.io)，可在 Claude Code、Codex、Cursor、OpenClaw、Hermes 等 50+ 兼容 runtime 中运行。

---

## 快速开始

```bash
npx skills add etdjok/huashu-nuwa
```

或直接安装到指定目录：

```bash
git clone https://github.com/etdjok/huashu-nuwa.git ~/.trae-cn/skills/huashu-nuwa
```

安装后对 AI 说：「蒸馏一个 XXX」「造一个张小龙的视角 Skill」。

---

## 它做什么

女娲不是角色扮演，是**认知框架提取**：

| 层次 | 输出 |
|------|------|
| 心智模型 | 他用什么框架看世界（镜片） |
| 决策启发式 | 他如何做判断（直觉规则） |
| 表达 DNA | 他的语气、节奏、用词偏好 |
| 反模式 | 他绝对不会做的事 |
| 诚实边界 | 这个 Skill 做不到的事 |

---

## 已蒸馏人物（15 个示例 Skill）

| 人物 | 领域 |
|------|------|
| Paul Graham | 创业 / 写作 / 产品 |
| 张一鸣 | 产品 / 组织 / 全球化 |
| Karpathy | AI / 工程 / 教育 |
| Ilya Sutskever | AI 安全 / scaling |
| MrBeast | 内容创造 / YouTube |
| 特朗普 | 谈判 / 传播 / 行为预判 |
| 乔布斯 | 产品 / 设计 / 战略 |
| 马斯克 | 工程 / 成本 / 第一性原理 |
| 芒格 | 投资 / 多元思维 / 逆向思考 |
| 费曼 | 学习 / 教学 / 科学思维 |
| Naval | 财富 / 杠杆 / 人生哲学 |
| 塔勒布 | 风险 / 反脆弱 |
| 张雪峰 | 教育选择 / 职业规划 |
| 孙宇晨 | 营销 / 注意力经济 |
| X 导师 | X/Twitter 运营方法论 |

示例位于 `examples/`，每个都包含完整调研数据，可直接复制到 skills 目录使用。

---

## 工作原理

1. **六路并行采集**——著作、播客/访谈、社交媒体、批评者视角、决策记录、人生时间线，6 个 Agent 同时跑
2. **三重验证提炼**——观点须跨领域复现、有预测力、有排他性，才能成心智模型
3. **构建 Skill**——SKILL.md + references/，含心智模型、启发式、表达 DNA、反模式、诚实边界
4. **FIDELITY 出厂检验**——独立子 Agent 盲测，评分卡见 [references/fidelity-scorecard.md](references/fidelity-scorecard.md)

详细方法论见 [references/extraction-framework.md](references/extraction-framework.md)。

---

## 仓库结构

```
huashu-nuwa/
├── SKILL.md                     # 女娲本体（v1.3.0）
├── references/
│   ├── extraction-framework.md  # 提炼方法论
│   ├── fidelity-scorecard.md    # 出厂检验评分卡
│   └── skill-template.md        # 生成 Skill 模板
├── scripts/
│   ├── quality_check.py         # 质量检查
│   ├── merge_research.py        # 研究数据合并
│   ├── download_subtitles.sh    # 播客字幕下载
│   └── srt_to_transcript.py    # 字幕转文本
└── examples/                    # 15 个示例 Skill（含完整调研数据）
    ├── steve-jobs-perspective/
    ├── munger-perspective/
    └── ...
```

---

## 版本历史

| 版本 | 说明 |
|------|------|
| v1.3.0 | 新增 Phase 0C（URL/长文/本地文档蒸馏路径）、Phase 4.5 FIDELITY 出厂检验、版本回滚机制、渐进式披露分层结构 |
| v1.1.0 | 新增环境自适应探测（`.claude` → `.trae`）、非公众人物强制 checklist、双 Agent 分离检验 |

---

## 许可证

MIT — Copyright (c) 2026 Huashu (花叔)
