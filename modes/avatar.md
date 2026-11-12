# Mode C — Talking-avatar / 口播 script

Write a script that a digital human, a voiceover tool, or a real person can read naturally.

## Length math

| Language | Speaking speed | 15 s | 30 s | 60 s |
|---|---|---|---|---|
| English | ≈ 2.5 words/s | ~38 words | ~75 words | ~150 words |
| 中文 | ≈ 4 字/秒 | ~60 字 | ~120 字 | ~240 字 |

Count characters/words without punctuation; pauses add roughly 10% time. Always state the result: `约 30 秒 · 110 字`.

## Structure

1. **Hook (first 3 s):** one sharp line — a question, a surprising fact, or a pain point.
2. **Body:** 1–3 points, one idea per sentence.
3. **Call to action:** one clear next step ("关注我", "评论区留言", "点主页链接").

## Writing rules

- Short sentences; everyday words; no tongue twisters.
- Numbers written as spoken: "一百二十万", "one point two million".
- Mark pauses: `/` short, `//` long. Use **bold** for stress, at most once per sentence.
- No unverifiable claims, fake statistics or guaranteed results.

## Lip-sync safety (for digital humans)

- Minimal gestures; head mostly still; no big smile in the middle of a sentence.
- Add a line: `表情动作：自然平视，轻微点头，开头和结尾微笑`.
- Long scripts: split into segments of ≤ 20 seconds.

## Output

```
## 🎙️ 口播稿（约 30 秒 · 110 字）
<script with / and // pause marks>

**表情动作**：…
**语气语速**：温和自信 · 正常语速
**画面建议**（可选）：哪几句配 B-roll
```

Offer an English or Chinese version only if the user needs both languages.

## Example

Input: "数字人口播，介绍我的咖啡店新品，30 秒"

```
早上起不来，/ 可能只是因为，/ 你还没喝到对的那杯咖啡。//
我们这周上新了燕麦拿铁。/ 咖啡豆是浅烘的，/ 喝起来酸甜干净，/ 一点都不苦。//
燕麦奶每天现打，/ 口感顺滑，/ 喝完也不腻。//
冰的热的都好喝，/ 上班路上一杯，/ 刚刚好。//
这周到店，/ 第二杯半价。//
你最喜欢什么口味？/ 评论区告诉我。
```
约 30 秒 · 107 字（不含标点，按每秒 4 字计约 27 秒，加上停顿约 30 秒）
