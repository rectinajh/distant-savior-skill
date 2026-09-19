# 豆豆小说技能包

两个基于豆豆小说《遥远的救世主》的 [Agent Skills](https://github.com/openai/skills)，可以直接被 Codex 加载使用。

## 包含什么

**`doudou-culture-attributes`** —— 全书知识库与应用框架

按 46 章拆分的结构化提炼（核心思想、框架原则、关键概念、心智模型、反面模式、实例还原、要点、关联），外加术语表、可复用技法表与判断速查表。适合用文化属性、强势文化、天道、杀富济贫、得救之道这些概念分析商业与人生问题，也适合按章查阅人物决策与商战过程。

**`ding-yuanying`** —— 以丁元英的口吻与思维方式对话

不是复述剧情，而是扮演这个人：话少、先看条件、只讲规律、不做道德裁判。内含三份参考文件——用词与句法规则、他的原话库（含两首诗词）、以及他在钱、感情、宗教、扶贫、生死等主题上的立场，用来保证回答不跑味。它会按需调用上面的知识库。

## 安装

用 skills CLI：

```bash
npx skills add https://github.com/rectinajh/agent-skills --skill ding-yuanying
npx skills add https://github.com/rectinajh/agent-skills --skill doudou-culture-attributes
```

手动安装（Codex）：

```bash
cp -R ding-yuanying doudou-culture-attributes ~/.codex/skills/
```

装好后新开一轮对话即可使用，例如「用丁元英的角度说说这件事」，或直接点名 `$ding-yuanying`。

## 目录结构

```
.
├── ding-yuanying/
│   ├── SKILL.md              人物扮演规则
│   ├── agents/openai.yaml    UI 元数据
│   └── references/
│       ├── voice.md          用词、句法、禁忌与自检
│       ├── canon.md          原话库（按主题）
│       └── positions.md      各主题上的立场
└── doudou-culture-attributes/
    ├── SKILL.md              核心框架 + 46 章索引 + 主题索引
    ├── chapters/             46 个分章文件
    ├── glossary.md           术语表
    ├── patterns.md           技法与模式
    └── cheatsheet.md         判断规则速查
```

## 使用提示

`ding-yuanying` 是虚构角色的扮演，不代表作者立场，也不构成投资、法律或经营建议。用于真实决策前请自行判断。

## 版权说明

本仓库内容是对《遥远的救世主》（豆豆著）的提炼、重构与引用，不含原文长篇段落，供个人学习与研究使用，不得用于任何商业用途。需要完整内容请购买正版书籍。
