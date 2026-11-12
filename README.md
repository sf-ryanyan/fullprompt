<div align="center">

# ✨ Fullprompt

**把一句话，写成完整的 AI 提示词**

视频 · 图片 · 数字人口播 · 剪辑分镜 —— 一个 Claude Skill 全搞定

![version](https://img.shields.io/badge/version-1.0.0--beta-blue) ![license](https://img.shields.io/badge/license-MIT-green) ![Claude Skill](https://img.shields.io/badge/Claude-Skill-orange) ![语言](https://img.shields.io/badge/语言-中文优先-red)

</div>

---

## 😩 你是不是也遇到过这些问题？

- 写了一句"房子里主人招待客人喝酒"，生成出来的画面**每次都不一样**，像抽卡
- AI **看不懂你的意思**：人物乱加、镜头乱晃、手指变形、画面里冒出乱码文字
- 不知道镜头、光线、比例、负面提示该怎么写
- 好不容易写出一条好用的提示词，**下次又找不到了**

## 💡 Fullprompt 怎么解决

| 问题 | Fullprompt 的做法 |
|---|---|
| 提示词太笼统 | 按 **8 要素** 补齐：场景 · 人物 · 动作 · 镜头 · 光线 · 风格 · 时长 · 比例，外加声音和不想出现的内容 |
| 不知道该补什么 | 信息不够时，先问你 **2–3 个选择题**，回字母就行 |
| 结果不稳定 | 输出前做 **14 项自检**：动作是否太多、镜头是否只有一个、人物是否太多、有没有空话…… |
| 平台规则不同 | 内置主流平台说明：即梦 / 可灵 / 海螺 / 通义万相 / Seedance / Veo / Sora / Runway / GPT Image / Midjourney 等 |
| 出了废片不知道改哪里 | **废片诊断表**：说出问题，它每次只改一处，帮你找到原因 |
| 好提示词找不到 | **提示词库**：说"存"就保存，下次自动复用 |

## 🚀 功能一览

- 🎬 **视频提示词**：按秒分段、单一运镜、首帧图转视频、多镜头角色一致
- 🖼️ **图片提示词**：构图、焦段、比例、留白；需要文字时教你怎么写
- 🧑‍💼 **数字人口播稿**：自动按时长算字数，标好停顿，适合对口型
- ✂️ **剪辑分镜清单**：镜号、时长、素材关键词、字幕，时长自动核对，可导出 CSV
- 🧩 **5 个场景包**：🏠 房产 · 🛍️ 电商产品 · 🍜 美食探店 · 🎭 短剧 · 🎙️ 口播知识
- 📚 **提示词库**：评分、标签、踩坑记录，越用越好用
- 🌐 **中文优先**：用中文问就用中文答；海外平台的提示词默认英文（模型更听话）并附中文对照，即梦/可灵/海螺等国内平台直接写中文

## 📦 安装

### 方式一：Claude 网页版 / 电脑客户端

1. 到 [Releases](https://github.com/sf-ryanyan/fullprompt/releases) 下载 `fullprompt.zip`（**不用解压**）
2. 打开 Claude → **Settings（设置）→ Capabilities**，确认 **Code execution and file creation** 已打开
3. 进入 **Customize → Skills**，点 **"+"** → **"+ Create skill"** → **"Upload a skill"**，上传 ZIP
   （旧版界面：**Settings → Capabilities → Skills → Upload skill**）
4. 确认 **fullprompt** 开关已打开

### 方式二：Claude Code

在终端运行：

```
git clone https://github.com/sf-ryanyan/fullprompt ~/.claude/skills/fullprompt
```

重启 Claude Code 即可。也可以手动下载本仓库，把所有文件放进 `~/.claude/skills/fullprompt/` 文件夹。

## 🎯 怎么用

**第 1 步：说一句想法**

```
帮我写个视频提示词：房子里主人在大厅招待客人喝酒玩耍
```

**第 2 步：回答选择题（回字母就行）**

```
开写前确认 3 件事（回字母就行，比如 "A C A"；不想答就说"直接写"）：
Q1 用在哪里？ A. 抖音/小红书竖屏 9:16 ｜ B. YouTube/横屏 16:9 ｜ C. 方图 1:1
Q2 想要什么感觉？ A. 高级安静 ｜ B. 热闹有活力 ｜ C. 温馨自然
Q3 用什么平台生成？ A. 即梦/可灵/海螺（国内） ｜ B. Veo/Sora/Runway/Kling（海外） ｜ C. 不确定
```

**第 3 步：复制提示词去生成**

你会拿到：✅ 可直接复制的提示词 · 🚫 不想出现的内容 · ⚙️ 参数建议 · 🔤 中文对照 · ✏️ 改了什么 · 💡 下一步

### 改写前后对比

**改写前**
> 房子里主人在大厅招待客人喝酒玩耍

**改写后**（节选）
```
A modern open-plan living room at early evening: floor-to-ceiling windows with a soft sunset over green hills, light oak floors, a white marble kitchen island.
Foreground: the host, a man in his late 30s in a white linen shirt, and his friend, a woman in her 30s in a navy dress. Background: three guests chat softly, slightly out of focus.
0–4s: The host pours red wine into two glasses and hands one to his friend.
4–7s: They turn toward the window, laughing.
7–10s: They raise their glasses by the window; the final frame holds for one second.
Camera: one slow dolly-in from the entrance toward the window, eye level, 35mm lens feel.
Light: warm golden-hour sunlight, soft pendant lights.
Sound: quiet acoustic guitar, soft laughter, no dialogue.
No text, no logos, no watermark; walls stay straight.
```

| 原来 | 改成 | 为什么 |
|---|---|---|
| "房子里" | 开放式客厅 + 落地窗 + 大理石岛台 | AI 才知道画什么样的房子 |
| "主人、客人" | 前景 2 人，其余背景虚化 | 人太多容易乱、容易变形 |
| "喝酒玩耍" | 拆成 3 段，每段 ≥3 秒 | 动作有顺序，时长够用 |
| 没写镜头和光线 | 一个慢推镜头 + 黄昏暖光 | 镜头稳、画面有质感 |

### 常用说法

| 你说 | 它会 |
|---|---|
| `直接写` | 不提问，用默认设置直接出 |
| `多给几个版本` | 给 A/B/C 三版，每版只改一个变量 |
| `手变形了` / `镜头晃` | 诊断原因，只改一处 |
| `存` / `好用，5 星` | 保存到提示词库 |
| `库里有派对的吗` | 搜索提示词库 |
| `怎么用` | 显示使用说明卡 |

## 📚 提示词库

- **Claude Code / 连接了电脑文件夹**：自动保存到你电脑上的 `prompt-library.md`
- **网页版 / App 聊天**：它会把条目显示出来，你复制保存到自己的 `prompt-library.md`；下次把这个文件拖进对话，它就能直接复用，并把更新后的文件给你下载
- 只有你说"存"才保存，保证库里都是好用的

## 🙏 致谢

Fullprompt 借鉴了以下优秀开源项目的**思路和方法**，所有文字均为重新编写，未复制其代码或原文：

| 项目 | 借鉴的思路 | 许可证 |
|---|---|---|
| [linshenkx/prompt-optimizer](https://github.com/linshenkx/prompt-optimizer) | 改写前后对比、多轮迭代优化 | AGPL-3.0 |
| [jnMetaCode/ai-shortfilm-prompts](https://github.com/jnMetaCode/ai-shortfilm-prompts) | 分段式提示词结构、类型模板、输出前自检、负面提示按平台处理 | MIT |
| [smixs/visual-skills](https://github.com/smixs/visual-skills) | 空话禁用清单、主文件只做分流的结构、英文最终提示词 | CC BY 4.0 |

感谢这些作者的分享。

## ⚠️ 免责声明

- AI 生成结果有随机性，Fullprompt 能大幅提高稳定性，但不能保证每次都完美
- 各平台的时长、比例、功能会更新，请以平台当前界面为准（平台说明最后核对：2026 年 11 月）
- 请遵守各生成平台的使用规则；不要用于生成侵权、冒充他人或误导性的内容
- 房产、电商等商业用途请自行确认广告合规

## 📄 版权与许可

© 2026 Ryan Yan · 基于 [MIT License](LICENSE) 开源，欢迎使用、修改和分享，请保留版权声明。

## 👤 关于作者

Ryan Yan，一名数据分析师。

---

<div align="center">

如果 Fullprompt 对你有帮助，欢迎点个 ⭐ Star

</div>
