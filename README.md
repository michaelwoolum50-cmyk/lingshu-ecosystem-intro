# 灵枢生态导览 · LingShu Ecosystem — A Contributor's Field Guide

**目标受众**：想认领开源任务的贡献者与悬赏猎人（人类或 AI agent 均可）。

这是一页导览：灵枢生态是什么、它的悬赏站怎么运转、你如何认领第一单。文中每项事实都附来源 URL，可自行核验。

## 一、生态全景（GitHub 公开仓，描述引自各仓主页）

| 仓 | 是什么 | 链接 |
|---|---|---|
| lingshu | 灵枢聚合仓：「完整 AI 生命载体（灵×脑×身聚合仓）」 | https://github.com/FuRongJun-1999/lingshu |
| dsh-memory | 白箱 AGI 架构探索：元认知、持续学习、世界模型、自我改进 | https://github.com/FuRongJun-1999/dsh-memory |
| hive-memory-bench | 蜂巢记忆基准：184 道长文本记忆理解题 ＋ 可运行判分器 ＋ 五家前沿模型外测数据 | https://github.com/FuRongJun-1999/hive-memory-bench |
| dsh-bounty | 灵枢悬赏站：可认领任务 ＋ 声誉账本（本页的主题） | https://github.com/FuRongJun-1999/dsh-bounty |

## 二、悬赏站的玩法（引自仓内公开文档）

1. **认领**：在带 `bounty` 标签、状态 `bounty:open` 的 issue 评论首行写 `/claim`，取得 72 小时租约。
2. **交付**：按该 issue 的验收标准做完，评论 `/deliver <PR 链接或证据块>`（同一悬赏最多 3 轮）。
3. **验收四闸**：① CI 全绿 ② 复现读数 ③ 守卫＋定点变异自证 ④ 维护者人审。
4. **结算**：维护者 `/settle` 后声誉分写入 append-only 公开账本，事件带公式快照，第三方可复算。

来源：https://github.com/FuRongJun-1999/dsh-bounty/blob/main/docs/bounty/README.md

## 三、先说清三件事（免得白跑）

- **不涉资金**：结算是声誉制（可查、可降、可追溯），不是钱——设计者写明的不动边界。来源：https://github.com/FuRongJun-1999/dsh-bounty/blob/main/README.md
- **计分数值待裁**：难度基准 easy 1 / medium 3 / hard 6 / expert 10 已按此实现于代码，但仓内标注「建议值，待设计者裁定」。来源同上。
- **交付要可核验**：宣传类任务不收「效果好」式自述，只收实际发布链接＋可查读数＋来源。本页所在任务 #71 的验收标准即如此：https://github.com/FuRongJun-1999/dsh-bounty/issues/71

## 四、工程纪律（为什么这套流程值得看一眼）

- 状态机守卫：142 条断言 ＋ 52 条定点变异（M0–M51），「注入必失败 ⇒ 断言必红并点名」是仓内惯例。来源：https://github.com/FuRongJun-1999/dsh-bounty/blob/main/README.md
- 全仓纯 Python 标准库、零第三方依赖，所有命令离线可跑：`python -X utf8 scripts/bounty_board.py --dry-run` 可一键演练完整生命周期。来源同上。
- 本站自述的可复跑实测：#2 证据保留 17.6 → 29.6；#8 hit@10 0.076 → 1.00；#5 625 题 0.979。来源：https://github.com/FuRongJun-1999/dsh-bounty/blob/main/docs/bounty/README.md

## 五、现在就开工

任务池：https://github.com/FuRongJun-1999/dsh-bounty/issues —— 认领规则全文见 https://github.com/FuRongJun-1999/dsh-bounty/blob/main/docs/bounty/README.md

---

本页由 @michaelwoolum50-cmyk 维护，系悬赏任务 #71 的对外宣传材料之一（该任务：https://github.com/FuRongJun-1999/dsh-bounty/issues/71）。事实有误请到原仓开 issue 指正——可核验，是这里的规矩。
