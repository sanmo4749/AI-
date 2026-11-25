# 技能

这里存放可安装的撰述技能，与 [personal-archive](../personal-archive/README.md) 里的学术档案分开。档案是曾建华的公开学术记忆；技能是动笔时要遵守的体例，不是档案条目。

## 明清名学史撰述体例

文件：[skills/明清名学史撰述体例/SKILL.md](明清名学史撰述体例/SKILL.md)

撰写、修订或续写《中国诸子学通史·明清卷》名家部，或《明清名学史》的章节时使用。它规定如何依已保存目录落笔，学术史写什么，语言、小传、引文与脚注如何处理，文稿用何种格式，以及交稿前核对什么。文件开头的 YAML 含 `name` 与 `description`，其后是体例全文。

本技能不代替「中国诸子学术通史研究」（调用名 zhuzi-academic-history）。写上述章节时，两份一起加载：先遵循通史研究技能，再执行本体例。本仓库没有收录「中国诸子学术通史研究」，需要另行安装。

## 如何安装与调用

一个技能就是内含 `SKILL.md` 的文件夹。请整夹复制或链接，保留文件夹名「明清名学史撰述体例」，与 frontmatter 里的 `name` 一致。不要改写 `SKILL.md`。

### 直接复制到助手的 skills 目录

在已克隆的仓库根目录执行，把尖括号换成该助手的 skills 目录：

```bash
cp -R "skills/明清名学史撰述体例" "<助手的 skills 目录>/"
```

各助手认的位置如下。个人目录对本机全部项目生效；项目目录只对当前仓库生效。

| 助手 | 个人目录 | 项目目录 |
| --- | --- | --- |
| Cursor | `~/.cursor/skills/` 或 `~/.agents/skills/` | `.cursor/skills/` 或 `.agents/skills/` |
| Claude Code | `~/.claude/skills/` | `.claude/skills/` |
| Codex | `~/.agents/skills/` | `.agents/skills/` |
| Grok Bot | `~/agent-data/workflows/` | `agent-data/workflows/` |

Cursor 同时读取 `.claude/skills/`、`.codex/skills/` 以及个人目录里的 `~/.claude/skills/`、`~/.codex/skills/`。复制后重新打开该助手，在技能列表中确认出现「明清名学史撰述体例」。撰写或修订上述章节时会按 `description` 加载；也可以在对话里点名这个技能。

Grok Bot 若能读写本机技能库，将该文件夹放入 `~/agent-data/workflows/`（项目内则为 `agent-data/workflows/`）。若只能在对话里保存，把 `SKILL.md` 交给该 Bot，请按原文存为同名技能，并在 Connect apps 的 Private skills 中对当前 Bot 启用。

### 克隆后指向本仓库路径

先克隆，再用符号链接把仓库里的这一夹接到助手的 skills 目录。之后在本仓库执行 `git pull`，助手读到的仍是同一份文件。

```bash
git clone https://github.com/sanmo4749/AI-.git
cd AI-
mkdir -p ~/.cursor/skills ~/.claude/skills ~/.agents/skills ~/agent-data/workflows
ln -s "$PWD/skills/明清名学史撰述体例" ~/.cursor/skills/
ln -s "$PWD/skills/明清名学史撰述体例" ~/.claude/skills/
ln -s "$PWD/skills/明清名学史撰述体例" ~/.agents/skills/
ln -s "$PWD/skills/明清名学史撰述体例" ~/agent-data/workflows/
```

只用其中一种助手时，保留对应的一行即可。项目级安装则链到该项目的 `.cursor/skills/`、`.claude/skills/`、`.agents/skills/` 或 `agent-data/workflows/`。

在 Cursor、Claude Code 或 Codex 中打开本仓库，不会自动加载根目录的 `skills/`。助手扫描的是上表那些目录，以及其中「直接包含 `SKILL.md`」的文件夹。Claude Code 的 `--add-dir` 也只扫描所加目录下的 `.claude/skills/`，不扫描本仓库的 `skills/`。因此要么复制，要么把本文件夹链接进上述位置。

### 稳定的 blob 与 raw 链接

合并到默认分支 `main` 之后，路径固定为 `skills/明清名学史撰述体例/SKILL.md`。

- blob：<https://github.com/sanmo4749/AI-/blob/main/skills/明清名学史撰述体例/SKILL.md>
- raw：<https://raw.githubusercontent.com/sanmo4749/AI-/main/skills/明清名学史撰述体例/SKILL.md>

同一文件的百分号编码写法：

- blob：`https://github.com/sanmo4749/AI-/blob/main/skills/%E6%98%8E%E6%B8%85%E5%90%8D%E5%AD%A6%E5%8F%B2%E6%92%B0%E8%BF%B0%E4%BD%93%E4%BE%8B/SKILL.md`
- raw：`https://raw.githubusercontent.com/sanmo4749/AI-/main/skills/%E6%98%8E%E6%B8%85%E5%90%8D%E5%AD%A6%E5%8F%B2%E6%92%B0%E8%BF%B0%E4%BD%93%E4%BE%8B/SKILL.md`

拉取请求尚未并入 `main` 时，把链接中的 `main` 换成该请求的分支名即可预览。合并之后，以上 `main` 链接即为稳定地址。不能克隆时，可让助手读取 raw 链接；这只是临时调用，不能代替把文件夹装进 skills 目录。其他能读取 `SKILL.md` 的助手，同样复制该文件夹，或在对话中给出上述 raw 链接。
