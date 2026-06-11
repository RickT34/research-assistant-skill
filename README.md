# Research Assistant Skill

一个面向实验型计算机科研新手的 Codex skill。它把「科研新手做事手册」打包成可调用的研究工作流助理，帮助用户把模糊、焦虑、过大的科研任务压成可观察、可验证、可交付的下一步。

## What It Helps With

- 读论文和整理 related work 坐标系
- 定义具体研究问题和边界
- 复现论文、对齐 benchmark、排查异常指标
- 看数据、读代码、做 sanity check
- 做 error analysis、failure taxonomy、probing set
- 从观察生成假设，并设计最小实验
- 周计划、日报、Go / Pivot / Stop 决策
- 向导师、合作者或同学有效求助

这个 skill 的核心取向是：少一点空转，多一点证据；少一点“大而全计划”，多一点能改变下一步判断的 artifact。

## Repository Layout

```text
.
├── SKILL.md
├── agents/
│   └── openai.yaml
└── references/
    ├── handbook-index.md
    ├── handbook.md
    └── handbook-revision-log.md
```

- `SKILL.md`: skill 的入口说明、触发场景、工作流和回答格式。
- `references/handbook-index.md`: 按用户问题快速路由到手册章节。
- `references/handbook.md`: 完整科研新手手册。
- `references/handbook-revision-log.md`: 手册公开发布后继续迭代时的修订记录。
- `agents/openai.yaml`: 可选的界面显示信息。

## Installation

Clone this repository into your Codex skills directory:

```bash
git clone https://github.com/YOUR-USER/research-assistant-skill.git ~/.codex/skills/research-assistant
```

Then start a new Codex session and invoke it with:

```text
[$research-assistant] 我现在复现论文结果对不上，帮我定位下一步。
```

If you keep the repository elsewhere, copy or symlink the repository folder to:

```text
~/.codex/skills/research-assistant
```

## Usage Examples

```text
我读了很多论文，但没形成判断，帮我整理下一步。
```

```text
这个 benchmark 分数上去了，但我不知道是不是真有意义，帮我设计 error analysis。
```

```text
我想给导师发一段求助信息，说明我复现结果和论文不一致。
```

When handbook guidance materially shapes the answer, the skill is instructed to cite exact sections, for example:

```text
手册依据：§6.2 复现第一周 SOP；§8.2 Overfit One Batch
补充判断：...
```

## Design Principles

- Move from a large unclear problem to a small testable subproblem.
- Separate observed facts from hypotheses.
- Prefer one-variable changes over multi-variable churn.
- Inspect samples and intermediate outputs instead of trusting aggregate metrics alone.
- Create artifacts: briefs, logs, tables, reports, cards, checklists, or decision records.
- Make stop and pivot decisions explicit instead of drifting.

## Language

The skill works best in Chinese or mixed Chinese/English research contexts. The bundled handbook is written in Chinese and focuses on ML / NLP / LLM / recommender systems / AI safety style experimental CS research.

## Contributing

Contributions should keep the skill practical and evidence-oriented. If you change the handbook, also update `references/handbook-revision-log.md` with:

- date
- trigger
- change
- rationale

Small clarifying examples are usually better than broad rewrites.

## License

This project is released under the MIT License. See [LICENSE](LICENSE).
