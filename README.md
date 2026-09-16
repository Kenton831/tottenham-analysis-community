# Tottenham Analysis (Community Edition)

一个用于热刺比赛分析的 Codex skill 公开版本：赛前前瞻与赛后复盘共用一套证据规则，输出自媒体文章与比赛图表。

## 安装

把整个 `tottenham-analysis-community` 文件夹复制到你的 skills 目录：

```text
<CODEX_HOME>/skills/tottenham-analysis-community/
Windows 默认位置: C:\Users\<you>\.codex\skills\tottenham-analysis-community\
```

重启 Codex 后即可用 `$tottenham-analysis-community` 调用。

## 包含什么

| 文件 | 内容 |
|---|---|
| `SKILL.md` | 三档置信度（已确认 / 已报道 / 预测）、来源优先级、模式选择、质量门槛 |
| `references/analysis-workflow.md` | 赛前 10 步、赛后 11 步的步骤清单，每步一句话说明要回答什么 |
| `references/chart-principles.md` | 图表原则：一图一个结论、真实坐标几何、成套一致性、交付前 QA |
| `references/output-and-media.md` | 文章写作的结构与语气 |
| `references/efficiency-and-delegation.md` | 长会话的 token 控制、阶段检查点、子智能体委派边界、图表产线提效 |

## 这个版本精简掉了什么

公开版按「可迁移的最小集」整理：判断框架完整保留，凡是绑定作者本机环境的参数与实现都不随版本分发。具体是四类：

- **图表参数**——只给原则，不给排版、配色、间距的具体数值，也不含图表代码库，视觉层请按自己的环境实现。
- **工作流展开**——只给步骤清单和每步要回答的问题。
- **交付形态**——只保留文章一种。
- **验收细则**——只给质量标准。

去掉的部分多与作者的项目结构、字体和数据管道绑定得比较紧，直接套用别人的参数通常不如照着自己环境补一套。

## 许可

见 [LICENSE](LICENSE)：可免费用于个人非商业用途并需注明来源；禁止二次分发、禁止商用、禁止去除署名。需要其他授权请联系作者。

## 版本

1.0.0
