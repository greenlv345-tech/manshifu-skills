# 满师傅 Skills

为中文新媒体创作者准备的 8 个 AI Agent 技能：公众号结构、朋友圈文案、小红书图文策划、写作诊断与封面创意。

**把真实素材整理成别人愿意读、看得懂、知道下一步怎么做的内容。**

作者：满师傅 · [GitHub](https://github.com/greenlv345-tech) · [MIT License](LICENSE)

These eight Chinese-language Agent Skills cover content planning, writing, editing, and cover design. Each skill is a self-contained `SKILL.md` with no bundled executable scripts.

## 技能清单

| 技能 | 安装名称 | 用途 |
|---|---|---|
| [AI工作流爆款封面](skills/ai-workflow-viral-cover/SKILL.md) | `ai-workflow-viral-cover` | 黑红金高对比、大数字结果、AI协作复盘风格，1秒看到结果 |
| [结论先行写作](skills/conclusion-first-manshifu/SKILL.md) | `conclusion-first-manshifu` | 把文章改成加粗结论开篇、读者一眼抓住核心 |
| [成交型朋友圈写作](skills/deal-moments-writing/SKILL.md) | `deal-moments-writing` | 把素材写成自然有信任感、轻引导咨询的朋友圈文案 |
| [小红书图文策划](skills/rednote-content-planner/SKILL.md) | `rednote-content-planner` | 把内容拆成多页卡片，输出封面钩子、页面文案和发布正文 |
| [Skill推广文章写作](skills/skill-promo-writer/SKILL.md) | `skill-promo-writer` | 讲透价值、保留关键技巧、驱动安装 |
| [文章结构重排](skills/structure-reorder/SKILL.md) | `structure-reorder` | 找战略重心、拆段落功能、按读者理解成本重排、查协同性 |
| [公众号文章结构化写作](skills/wechat-article-structure/SKILL.md) | `wechat-article-structure` | 搭骨架、补说服链、定战略重心，输出可写版本 |
| [写作诊断](skills/writing-diagnosis/SKILL.md) | `writing-diagnosis` | 不只看文笔，追溯到读者价值、视角偏差、经营逻辑、系统性根因 |

## 安装

### 使用 Skills CLI

需要先安装 Node.js（含 npm / npx），并使用支持 Agent Skills 的 AI 工具。

查看可安装技能：

```bash
npx skills add greenlv345-tech/manshifu-skills --list
```

按需安装，例如只安装「结论先行」：

```bash
npx skills add greenlv345-tech/manshifu-skills --skill conclusion-first-manshifu
```

安装时按 CLI 提示选择你的 AI 工具和安装范围。也可以不加 `--skill`，在交互界面选择需要的技能：

```bash
npx skills add greenlv345-tech/manshifu-skills
```

### 手动安装

点击仓库的 **Code → Download ZIP**，解压后，从 `skills/` 中选择需要的完整文件夹，放入你的 AI 工具支持的技能目录。

- 项目级 Agent Skills 目录示例：`你的项目/.agents/skills/技能名/SKILL.md`。
- Claude Code 项目目录示例：`你的项目/.claude/skills/技能名/SKILL.md`。
- 其他工具按各自的技能导入方式操作，不要把 8 个 `SKILL.md` 放在同一层覆盖彼此。

这些文件按 Agent Skills 结构整理；实际加载方式、自动触发和可调用工具由宿主决定。本仓库不承诺已在所有宿主逐项实测。

## 怎么使用

安装后，直接向 AI 描述任务，并附上你的真实素材。例如：

| 你要做什么 | 可以这样说 |
|---|---|
| 让开头更直接 | 使用 conclusion-first-manshifu，把下面这篇文章改成结论先行，保留事实和语气。 |
| 写朋友圈 | 使用 deal-moments-writing，把这段真实项目经历写成一条自然的朋友圈，结尾轻轻引导咨询。 |
| 策划小红书 | 使用 rednote-content-planner，把这篇文章拆成 7 页图文，给出每页标题、文案和配图建议。 |
| 搭公众号大纲 | 使用 wechat-article-structure，面向新媒体从业者，为这个主题搭结构；缺少的案例请标出来。 |
| 诊断文章 | 使用 writing-diagnosis，找出这篇文章在读者价值、主线和论据上的问题。 |
| 重排结构 | 使用 structure-reorder，在保留事实的前提下重排段落，并解释调整理由。 |
| 推广技能 | 使用 skill-promo-writer，根据这份 SKILL.md 写一篇推广文，示例与已验证效果要分清。 |
| 做封面 | 使用 ai-workflow-viral-cover，为这份真实复盘设计黑红金封面；只使用我提供的数据。 |

## 一个内容工作流

1. 用 `wechat-article-structure` 确定主线和大纲。
2. 用 `writing-diagnosis` 找出读者价值、证据和逻辑问题。
3. 根据诊断，用 `structure-reorder` 调整结构，或用 `conclusion-first-manshifu` 改写开头。
4. 将定稿交给 `rednote-content-planner` 拆成图文，或交给 `deal-moments-writing` 改成朋友圈。
5. 需要黑红金视觉时，再用 `ai-workflow-viral-cover` 设计封面。

按任务选择技能，不必每次运行全部流程。

## 能力与边界

- 8 个技能都是文本规则与工作流程，本身不附带运行脚本或收费接口。
- 小红书技能输出图文策划与文案，不自动生成全部卡片，也不自动登录发布。
- 封面技能需要宿主提供生图能力；没有生图工具时只能交付提示词和版式说明。示例数字不是效果承诺。
- 大模型、生图、笔记存储等外部服务可能收费，由使用者自行配置；本仓库不提供 API Key。
- 涉及案例、客户信息、数据、引用和效果数字，请使用真实且允许公开的材料。文案产出不等于已发布，不保证流量、成交或所谓「爆款」。
- 笔记保存功能取决于宿主是否有相应工具，应在用户要求或已有授权的范围内执行。

## 来源与开源协议

本仓库由满师傅提供的技能包整理而来，原创技能编排与说明采用 [MIT License](LICENSE)，允许使用、修改和商业使用，分发时保留许可证及版权声明。

部分写作方法参考小马宋《营销笔记》，技能内保留了来源标注。第三方引用不因本仓库开源而转为 MIT 授权，详见 [来源与引用说明](NOTICE.md)。

## 反馈

欢迎通过 [Issues](https://github.com/greenlv345-tech/manshifu-skills/issues) 提交使用反馈，或通过 Pull Request 改进技能。请说明所用 AI 工具、使用场景和期望结果；不要上传账号密钥、客户隐私或未获授权的材料。
