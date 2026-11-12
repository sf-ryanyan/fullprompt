# Mode D — Editing storyboard (分镜清单)

A shot list that an editor, an auto-edit tool, or the user can follow directly.

## Header

```
片名：… ｜ 总时长：30s ｜ 比例：9:16 ｜ 节奏：前 3 秒钩子，中段平稳，结尾停留 ｜ 音乐：轻快吉他
```

## Table

| 镜号 | 时长 | 画面内容 | 素材关键词 | 景别/运镜 | 字幕/旁白 | 音乐/音效 | 转场 |
|---|---|---|---|---|---|---|---|
| 1 | 0–3s | … | english, short, keywords | 近景/慢推 | 钩子字幕 | 音乐起 | 硬切 |

## Rules

- **Math check:** all shot durations add up exactly to the total length.
- **Hook** in the first 3 seconds; one idea per shot; most shots 2–4 seconds for short video.
- **Material keywords** in short English words that match how footage is named or described (kitchen, window, drone, pour, close-up), so it is easy to search a footage folder.
- **Captions:** ≤ 12 Chinese characters or ≤ 7 English words per line.
- Missing footage → mark `【需补拍/AI生成】`; offer a Mode A prompt for that shot.
- If a voiceover exists, align each line with its shot and check the speaking time (Mode C length math).

## Machine-readable option

If the user's editing tool needs a file, also output the same table as CSV:

```
shot,start,end,description,keywords,camera,caption,audio,transition
1,0,3,"…","kitchen;window;morning","close-up;slow push-in","…","music in","cut"
```

## Example

Input: "30 秒新店开业短视频分镜"

| 镜号 | 时长 | 画面内容 | 素材关键词 | 景别/运镜 | 字幕/旁白 | 音乐/音效 | 转场 |
|---|---|---|---|---|---|---|---|
| 1 | 0–3s | 卷帘门拉起，阳光照进店里 | shutter, door, morning light | 中景/固定 | 今天，我们开门了 | 卷帘门声 + 音乐起 | 硬切 |
| 2 | 3–7s | 咖啡萃取特写 | espresso, pour, close-up | 特写/固定 | 每一杯都现做 | 咖啡机声 | 硬切 |
| 3 | 7–12s | 店员把拿铁递给客人 | barista, latte, handoff | 中景/慢推 | — | 环境人声 | 叠化 |
| 4 | 12–18s | 店内环境全景 | interior, seating, plants | 全景/横移 | 安静的角落给你 | 音乐 | 硬切 |
| 5 | 18–25s | 客人靠窗喝咖啡微笑 | window seat, customer, smile | 中景/固定 | — | 音乐 | 硬切 |
| 6 | 25–30s | 门头外景，结尾停留 | storefront, exterior, signage | 远景/慢拉 | 开业首周第二杯半价 | 音乐收 | 淡出 |

总时长核对：3+4+5+6+7+5 = 30 秒 ✓
