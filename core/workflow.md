# Workflow

## Step 0 — Library check

Look for `prompt-library.md` in a folder on the user's own computer (Claude Code project folder or a connected folder), or in a file the user uploaded to this chat.
- If an entry with similar tags is rated ⭐4 or higher, start from it and say so in one line: "基于提示词库里的 party-01 改写".
- If there is no library, skip silently. Do not search a temporary chat sandbox — files there are not the user's library.

## Step 1 — Pick the mode

| The user wants | Mode | Files |
|---|---|---|
| AI video, a clip, a shot, 短视频镜头 | A Video (default when unclear) | modes/video.md |
| A picture, cover, poster background, first frame | B Image | modes/image.md |
| A talking avatar, 数字人, 口播, voiceover script | C Avatar script | modes/avatar.md |
| A shot list, 分镜, editing script, B-roll plan | D Storyboard | modes/storyboard.md |

Use a scene pack only when the user's **goal** fits it, not just the setting: real estate = promoting a property, listing or agent; e-commerce = selling a product; food = promoting a restaurant or dish; short drama = a story with characters; talking-head = a presenter or knowledge video. A party that happens to be in a house is not real estate. If the goal is unclear, make 用途 one of the questions.

## Step 2 — 8-element check

Check the idea against the 8 elements, plus sound (video) and things to avoid:

| # | Element | Example of "specified" |
|---|---|---|
| 1 | 场景 Scene | "a sunlit open-plan living room with oak floors" |
| 2 | 人物 Characters | "a woman in her 30s in a navy dress" |
| 3 | 动作 Action | "pours tea and hands a cup to her friend" |
| 4 | 镜头 Camera | "medium shot, eye level, slow push-in" |
| 5 | 光线 Lighting | "golden-hour window light" |
| 6 | 风格 Style | "realistic lifestyle commercial" |
| 7 | 时长 Duration | "8 seconds" (video only) |
| 8 | 比例 Ratio | "9:16" |

The 8 elements apply to Modes A and B. For the other modes, check these instead:
- **Mode C (script):** purpose, length, language, tone, 1–3 key points (selling points, facts), call to action.
- **Mode D (storyboard):** total length, ratio, existing footage or AI-generated, voiceover yes/no, the 1–3 key messages.

- **0–2 missing** → fill with defaults, continue, and list them as assumptions.
- **3+ missing, or platform unknown and it matters** → Step 3.
- **User says "直接写 / 不用问 / 快速 / just write it"** → skip questions; fill defaults; put one assumption line at the top of the output.

**Defaults** (when not given):
- Video: 9:16, 8 seconds, realistic style, natural light, eye level, one slow camera move.
- Image: 4:5 for social posts, 16:9 for covers and listings, eye level, natural light.
- Script (Mode C): 30 seconds, user's language, warm and confident, CTA "评论区告诉我". Never invent facts or offers — if key points are missing, ask.
- Storyboard (Mode D): 30 seconds, 9:16, mixed real footage + AI shots, with voiceover.
- Platform: unknown → write a platform-neutral English prompt and put negatives inside the prompt (see core/rules.md).

## Step 3 — Ask (one round, max 3 questions)

Ask only questions whose answers change the result. Priority order:
1. Purpose / platform / ratio
2. Mood / style
3. Subject details (place, people, product)

Format — every question has short A/B/C options; the user can reply with letters:

```
开写前确认 3 件事（回字母就行，比如 "A C A"；不想答就说"直接写"）：
Q1 用在哪里？ A. 抖音/小红书竖屏 9:16 ｜ B. YouTube/横屏 16:9 ｜ C. 方图 1:1
Q2 想要什么感觉？ A. 高级安静 ｜ B. 热闹有活力 ｜ C. 温馨自然
Q3 用什么平台生成？ A. 即梦/可灵/海螺（国内） ｜ B. Veo/Sora/Runway/Kling（海外） ｜ C. 不确定
```

- Write the questions in the user's language.
- **With a scene pack:** the total is still max 3. Take the platform question first (only if needed), then fill the remaining slots with the pack's questions, most important first.
- Platform question: include it when the platform is unknown and the user is producing video; skip it for images unless text-in-image is needed.
- If the user skips a question, use the default and say so.
- Never ask a second round. If something is still unclear, assume and state it.

## Step 4 — Build

1. Read `core/rules.md` and the mode file.
2. Read the platform card for the user's tool (or write platform-neutral).
3. If a scene pack fits, fill its template.
4. For more than one shot, write a **Look Card** and a **Character Card** first and reuse them word for word.

## Step 5 — Pre-flight self-check (must pass)

Fix problems silently, then report one line: "自检：通过" or "自检：动作太多，已拆成 2 段".

| # | Check | Pass rule |
|---|---|---|
| 1 | 8 elements | all present or listed as assumptions |
| 2 | Event density (video) | seconds ÷ action beats ≥ 3; between 2 and 3 → add time or cut a beat; under 2 → split into clips. If the user set the duration, keep it and cut beats instead |
| 3 | One camera move | exactly one move per shot, with a start and an end point |
| 4 | People | at most 2 people interacting in focus; others soft in the background |
| 5 | Hands | no close-ups of fine hand work (typing, shuffling cards, threading) |
| 6 | Text | no words, prices, signs or logos in the visual unless explicitly wanted and supported |
| 7 | Anti-slop | no empty praise words |
| 8 | No conflicts | one time of day, one style, one speed |
| 9 | Sound (video) | a sound line is present |
| 10 | Ending (video) | calm final hold of about 1 second |
| 11 | Realism | 1–2 small natural imperfections for photoreal people or materials |
| 12 | Pack rules | the scene pack's own checks pass (e.g. Fair Housing for real estate, accurate product look for e-commerce) |
| 13 | Length | within the platform limit; aim for 60–180 English words or 100–300 Chinese characters per clip |
| 14 | Safety | no copyrighted characters, no real person's likeness, no real brand logos |

## Step 6 — Output format

Modes A and B use this exact structure. Modes C and D use the output format in their mode file, followed by the same 自检 line and 下一步 line. Headings in the user's language.

~~~
（如有假设）假设：竖屏 9:16 · 8 秒 · 写实 · 平台未定

## ✅ 可直接复制
**提示词**
```
<final prompt only — no notes inside>
```
**不想出现的内容**
```
<negative list, or "已写进提示词最后一行，无需另填">
```
**参数建议**：平台/模型 · 比例 · 时长 · 先低清试一次，满意再出高清

## 🔤 中文对照
<2–4 lines describing the picture>

## ✏️ 改了什么
| 原来 | 改成 | 为什么 |
<3–6 rows>

自检：<one line>

## 💡 下一步
<one sentence, e.g. "建议先用开头画面出一张首帧图，满意后再转视频。效果好就回复"存"。">
~~~

- The translation section translates the prompt into the user's language. Skip it when the user writes in English, or when the prompt itself is already in the user's language (e.g. a Chinese prompt for 即梦/可灵).
- Default: **one stable version**.
- If the user asks for options ("多给几个 / 对比 / variants"), give 2–3 versions labeled A/B/C, each changing **one** variable (camera, light or mood), and say which variable changed.
- For multi-shot work, output the Look Card and Character Card first, then one copy block per shot.
- If the user only wants the prompt ("只要提示词"), output the copy block and the negative block only.

## Step 7 — Save to library (only on request)

Trigger words: 存, 好用, 收藏, save. Read `library/library-format.md`, then:
- Ask for a ⭐1–5 rating if none was given (one short question).
- **Running on the user's computer** (Claude Code, or a connected folder): append the entry to `prompt-library.md` there; create it from the template if missing. Say where it was saved.
- **Web or app chat** (claude.ai): the chat's file sandbox is temporary and is lost after the chat — never say "已保存" for a file written there. Instead:
  - If the user uploaded their `prompt-library.md` in this chat: add the entry and give the updated file back as a download, saying "下载替换你原来的文件".
  - Otherwise: show the entry in a code block and say "复制这段，粘贴到你的提示词库文件里；下次把这个文件拖进对话，我就能直接用".
- Same idea already saved → update that entry with a new version and a note; do not duplicate.

Library search: when the user asks "库里有什么 / 找一下派对的", list matching entries as `标题 · 标签 · ⭐`.

## Step 8 — Fix loop

When the user reports a bad result:
1. If the prompt that produced the result is not in this chat, ask the user to paste it (and describe or attach the result). Then read `core/troubleshooting.md` and name the likely cause in one line.
2. Change **one** variable only.
3. Output the new prompt with "这次只改了：…".
4. If the same problem happens twice: split the shot, remove people, simplify hands, or switch to image-first.
5. If the prompt is in the library, add the cause and fix to its notes.
