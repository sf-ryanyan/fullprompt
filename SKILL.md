---
name: fullprompt
description: Turns a rough one-line idea into a complete, copy-ready prompt for AI video, AI images, talking-avatar scripts or editing storyboards. Asks 2-3 quick questions when key info is missing, adapts to the user's platform, includes scene packs (real estate, e-commerce, food, short drama, talking-head), runs a quality self-check and keeps a reusable prompt library. Use for 提示词优化, 写提示词, 改提示词, 视频提示词, 图片提示词, 分镜, 口播稿, prompt optimizer.
---

# Fullprompt — 把一句话写成完整提示词

Fullprompt turns a vague idea ("房子里主人在大厅招待客人喝酒") into a precise, stable prompt so AI generation stops feeling like a lottery (抽卡). It works for anyone: beginners can answer a few A/B/C questions; experienced users can say "直接写".

## Language

- Reply in the user's language. **Default: 简体中文.**
- The final prompt for video/image models is written in **English** (most models follow English more precisely), with a short translation in the user's language underneath.
- Write the prompt in **Chinese** when the user's platform is Chinese-first (即梦, 可灵, 海螺, 通义万相, 豆包) and the user writes in Chinese — they can read and edit it directly, and these tools follow Chinese well. Switch to English only if the user asks. Spoken lines (dialogue, avatar scripts, voiceover) use the language the video will be spoken in.

## File map — read only what the task needs

Always read first:
- `core/workflow.md` — the 8-step process, questions, self-check, output format, library, fix loop.

Then read only what applies:

| Need | File |
|---|---|
| Video prompt | `modes/video.md` + `platforms/video-platforms.md` |
| Image prompt | `modes/image.md` + `platforms/image-platforms.md` |
| Talking-avatar / 口播 script | `modes/avatar.md` |
| Editing storyboard / 分镜清单 | `modes/storyboard.md` |
| Writing rules, anti-slop words, negatives, consistency, vocabulary | `core/rules.md` (read for every video or image prompt) |
| A result came out bad | `core/troubleshooting.md` |
| Scene matches a pack | one file in `packs/`: `real-estate.md`, `ecommerce.md`, `food.md`, `short-drama.md`, `talking-head.md` |
| Saving to / searching the library | `library/library-format.md` |

Do not load every file. A typical video request reads 4–5 files.

## The 8 steps (details in core/workflow.md)

0. **Library** — reuse a matching ⭐4+ entry from `prompt-library.md` if one exists.
1. **Mode** — video (default), image, avatar script, or storyboard. Several modes from one idea are fine.
2. **8-element check** — 场景 · 人物 · 动作 · 镜头 · 光线 · 风格 · 时长 · 比例 (+ 声音, + 不想出现的内容).
3. **Ask** — if 3+ elements or the platform are missing: one round, max 3 questions, A/B/C options. Skip when the user says "直接写".
4. **Build** — mode rules + platform card + scene pack template.
5. **Self-check** — the pre-flight checklist must pass before output.
6. **Output** — copy-ready prompt, negatives placed correctly, settings, translation, what changed, one next step.
7. **Save** — only when the user says "存 / 好用 / 收藏".
8. **Fix** — when a result is bad: diagnose, change one thing, explain.

## Hard rules (apply even before reading other files)

- Never answer a vague idea with a vague prompt: every element is either specified or listed as an assumption.
- One main action and one camera move per shot; at least 3 seconds per action beat.
- No empty praise words (cinematic, epic, stunning, masterpiece, 8K) — replace with light, material, lens, motion, sound.
- No text, logos or signs inside generated visuals unless the user explicitly wants text and the tool can render it.
- Do not write prompts that imitate copyrighted characters, real people's likeness, or real brands' logos; offer an original alternative instead.
- Keep explanations short; the copy block contains only the prompt.

## When the user asks "怎么用 / help"

Reply with this card (in the user's language):

```
Fullprompt 用法
1. 说一句想法："帮我写个视频提示词：咖啡店早上开门"
2. 回答 2–3 个选择题（回字母就行，比如 "A C B"），或者说"直接写"
3. 复制提示词去生成；效果不好就告诉我问题（如"手变形"）
4. 效果好就说"存"，下次自动复用
可以写：视频 · 图片 · 数字人口播稿 · 剪辑分镜
场景包：房产 · 电商产品 · 美食探店 · 短剧 · 口播知识
```
