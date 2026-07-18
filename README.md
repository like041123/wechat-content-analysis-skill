# WeChat Content Analysis Skill

> 属于 [awesome-trae-skills](https://github.com/topics/awesome-trae-skills) 系列 · [TRAE](https://www.trae.cn/) 自定义 Skill

一个用于**深度分析微信公众号内容**的 TRAE Skill，覆盖内容质量评估、互动数据分析、内容策略诊断与优化建议。适用于运营人员、内容创作者、品牌营销团队及行业研究者。

## 能力概览

| 分析维度 | 核心内容 |
|---------|---------|
| 内容质量 | 标题类型识别与吸引力评分、结构逻辑（开头/正文/CTA）、可读性（句长/段落/图文比）、主题与情感倾向 |
| 互动数据 | 互动率计算、分项互动率（点赞/在看/评论/分享）、行业基准对比、爆款识别 |
| 内容策略 | 发布节奏与黄金时段、内容矩阵（主题/类型分布）、原创比例、爆款规律提取 |
| 账号定位 | 定位清晰度、人设一致性、差异化程度、用户价值评估 |

## 仓库结构

```
wechat-content-analysis-skill/
├── SKILL.md                          # 主技能文件（含 frontmatter 与方法论）
└── references/
    ├── analysis-rubric.md            # 评分标准与行业基准
    └── report-templates.md           # 报告模板与输出规范
```

## 安装

将本仓库克隆到 TRAE 的技能目录：

```bash
# 方式一：克隆到全局技能目录
git clone https://github.com/like041123/wechat-content-analysis-skill.git \
  ~/.trae/skills/wechat-content-analysis

# 方式二：克隆到项目级技能目录
git clone https://github.com/like041123/wechat-content-analysis-skill.git \
  .trae/skills/wechat-content-analysis
```

安装后，TRAE 会在你提出公众号分析相关需求时自动调用本技能。

## 触发场景

- "帮我分析这篇文章 https://mp.weixin.qq.com/s/xxxxx"
- "分析一下『XX财经』这个公众号最近的内容策略"
- "对比这两个教育类公众号的内容表现"
- "基于数据给我公众号内容优化建议"

## 核心特性

- **数据驱动评分**：所有维度采用 1-10 分制，评分必须附证据引用，避免空泛评价
- **行业基准内置**：`references/analysis-rubric.md` 内置互动率、阅读量、发布频率等多行业基准
- **三套报告模板**：单篇分析、账号诊断、多账号对比，覆盖常见场景
- **技能协同**：可与 `html-report`、`xlsx`、`html-deck` 等技能联动

## 使用示例

### 单篇文章分析
粘贴公众号文章链接或正文，技能会：
1. 抓取文章元数据（标题、作者、发布时间）
2. 按四维度（标题/结构/可读性/主题情感）逐项分析
3. 输出评分卡表格 + 3 条优化建议

### 账号诊断
提供账号近期 10-20 篇文章样本，技能会完成内容矩阵分析、识别爆款规律、生成诊断报告。

详见 `SKILL.md` 中的"示例用法"章节。

## 注意事项

- 微信互动数据存在刷量可能，分析时会提示数据可信度
- 不同行业基准数据差异大（如财经类阅读量普遍高于教育类），避免一刀切评判
- 分析建议不涉及诱导分享、刷量等违反微信运营规范的行为

## License

[MIT](./LICENSE)

## 相关仓库

- [agent-builder-skill](https://github.com/like041123/agent-builder-skill) — 智能体搭建技能
- [arch-vision-skill](https://github.com/like041123/arch-vision-skill) — 架构全景生成技能
