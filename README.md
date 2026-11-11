# 豆豆小说技能包

基于豆豆小说《遥远的救世主》的 [Agent Skills](https://github.com/openai/skills)，可被 Codex / Cursor 等加载使用。

## 包含什么

**`ding-yuanying`** —— 以丁元英的口吻与思维方式对话，并内置全书语料库

不是复述剧情，而是扮演这个人：话少、先看条件、只讲规律、不做道德裁判。口吻侧有用词与句法规则、原话库（含两首诗词）、以及钱、感情、宗教、扶贫、生死等主题立场；语料库侧并入原 `doudou-culture-attributes`：46 章结构化提炼、核心框架、术语表、技法表与判断速查。可角色扮演，也可按章 / 按主题查阅后再用他的口吻作答。

## 安装

用 skills CLI：

```bash
npx skills add https://github.com/rectinajh/distant-savior-skill --skill ding-yuanying
```

手动安装（Codex）：

```bash
cp -R ding-yuanying ~/.codex/skills/
```

装好后新开一轮对话即可使用，例如「用丁元英的角度说说这件事」，或直接点名 `$ding-yuanying`。

> 若本地仍装有旧版独立技能 `doudou-culture-attributes`，可删除；其内容已并入本技能的 `references/`。

## 目录结构

```
.
└── ding-yuanying/
    ├── SKILL.md                 人物扮演规则 + 语料库查阅指引
    ├── manifest.yaml            版本、作者、分类等元数据
    ├── agents/openai.yaml       UI 元数据
    └── references/
        ├── voice.md             用词、句法、禁忌与自检
        ├── canon.md             原话库（按主题）
        ├── positions.md         各主题上的立场
        ├── framework.md         核心框架 + 46 章索引 + 主题索引
        ├── glossary.md          术语表
        ├── patterns.md          技法与模式
        ├── cheatsheet.md        判断规则速查
        └── chapters/            46 个分章文件
```

## 使用提示

`ding-yuanying` 是虚构角色的扮演，不代表作者立场，也不构成投资、法律或经营建议。用于真实决策前请自行判断。

## 版权说明

本仓库内容是对《遥远的救世主》（豆豆著）的提炼、重构与引用，不含原文长篇段落，供个人学习与研究使用，不得用于任何商业用途。需要完整内容请购买正版书籍。
