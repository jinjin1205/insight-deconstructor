# INSIGHT-DECONSTRUCTOR（洞察剥离器）

一个面向 Codex 的严格四步分析 Skill：把复杂项目或问题剥离为可量化、可证伪的硬约束交点，并删除依赖情绪、立场和面子的软约束。

## 能做什么

1. 将输入因素强制归入正反馈、负反馈或无关噪音。
2. 定位最多 3 个导致系统状态跳变的关键开关。
3. 分离硬约束与软约束，并为硬约束建立量化证伪标准。
4. 通过倒置验证筛除无法导出 3 个物质性结果的伪洞察。
5. 输出带成本、责任人和时限的行动建议。

## 安装

```bash
git clone https://github.com/jinjin1205/insight-deconstructor.git ~/.codex/skills/insight-deconstructor
```

重启 Codex 后，可直接输入：

```text
启动洞察剥离器，分析一下这个项目：
【项目名称】……
【当前状态描述】……
【希望达成的目标】……
```

也可以显式调用 `$insight-deconstructor`。

## 设计边界

- 输入不足 50 个字符时，Skill 会要求补充原始数据。
- 缺少至少 2 条可证伪硬约束时，不生成洞察结论。
- 倒置验证无法产出至少 3 个量化结果时，必须返回重新拆解。
- Skill 不会编造金额、时间、数量、法律条文或物理极限。

## 目录

```text
insight-deconstructor/
├── SKILL.md
├── agents/
│   └── openai.yaml
├── LICENSE
└── README.md
```

## License

MIT
