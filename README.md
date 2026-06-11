# Research Assistant Skill

一个面向计算机科研新手的 Skill，适合在研究任务卡住、边界不清、实验结果解释不动时使用。

基于[Research-Handbook](https://github.com/ICT-STAR/Research-Handbook)制作。

## 使用场景

- 读论文很多，但没有形成判断或 related work 坐标系。
- 想把一个大方向压成具体、可验证的研究问题。
- 复现论文、对齐 benchmark 或排查和论文结果不一致的问题。
- 看数据、读代码、做 sanity check，不想只盯着总体分数。
- 分析错误样本，整理 failure taxonomy、slice analysis 或 probing set。
- 从观察生成假设，并设计最小实验验证。
- 做周计划、日报、阶段性 Go / Pivot / Stop 决策。
- 给导师、合作者或同学写更清楚的求助信息。

## 安装方法

最简单的方法：把这个 GitHub 仓库链接发给你的 Agent，让它帮你安装。

可以这样说：

```text
请从这个仓库安装 research-assistant skill：
https://github.com/YOUR-USER/research-assistant-skill
```

如果你想手动安装，把仓库克隆到 Codex skills 目录：

```bash
git clone https://github.com/RickT34/research-assistant-skill.git ~/.codex/skills/research-assistant
```

然后在新会话中调用：

```text
我现在复现论文结果对不上，帮我定位下一步。
```
