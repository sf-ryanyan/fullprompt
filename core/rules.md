# Writing rules

## Prompt formula (video and image)

`Subject → Action → Setting → Camera → Lighting → Style → Sound (video only) → Guardrail line`

- **Subject:** concrete nouns, materials, colors, age range, clothing. "a ceramic pour-over coffee set on a walnut counter", not "coffee stuff".
- **Action:** one visible verb with an end state. "she lifts the cup and takes a slow sip", not "she enjoys coffee".
- **Setting:** place, time of day, two or three key props.
- **Camera:** shot size + angle + lens feel + one move with start and end.
- **Lighting:** a named physical source: window light, golden hour, overcast daylight, warm table lamp, neon sign glow.
- **Style:** one clear look: realistic lifestyle commercial, documentary, 35mm film look, anime, claymation, ink painting. Keep the user's chosen style.
- **Sound:** ambience + music mood/instrument + one signature sound; or "no music, natural ambience only".
- **Guardrail line:** a short final sentence for things that must not appear (see Negatives).

Write in plain, concrete sentences. Order matters: the subject and action first, mood last.

**Chinese prompts** (for 即梦, 可灵, 海螺, 通义万相, 豆包): same structure with Chinese labels — 场景：/ 人物：/ 动作（0–3秒：…）/ 镜头：/ 光线：/ 风格：/ 声音：— written as natural Chinese, not a word-for-word translation. Negatives in Chinese too: 文字、水印、手部变形….

## Anti-slop: replace empty words with visible facts

| Empty word | Replace with |
|---|---|
| cinematic, epic, stunning, beautiful | a named light source + one camera move + one material detail |
| luxury, high-end, premium | wide empty space in the frame, natural stone and dark wood, slow camera, muted colors |
| vibrant, lively, energetic | two or three specific actions and sounds (laughter, clinking cups, footsteps) |
| natural, realistic | real skin texture, a fabric crease, slight motion blur on fast hands |
| 4K, 8K, ultra detailed, masterpiece, best quality | delete — set resolution in the tool |
| dynamic camera | one named move: "slow dolly-in from the doorway to the window" |

Keep genre words that actually define a look (noir, documentary, anime, watercolor).

## Negatives (不想出现的内容)

Always show a "不想出现的内容" block, but place the content correctly:

1. **Platform has a negative field** (see the platform card): give a separate comma-separated list, 5–10 items.
2. **No negative field, or platform unknown:**
   - First rewrite negatives as positive descriptions: "a tidy counter" instead of "no clutter"; "steady camera" instead of "no shaking".
   - Then end the prompt with **one** short guardrail sentence of at most 6 concrete items, e.g. `No text, no logos, no watermark; walls stay straight.`
   - In the block, write: "已写进提示词最后一行，无需另填".
3. Never write long "avoid …" lists inside a prompt. Some models draw what you name.
4. If the platform card gives a different rule (e.g. Runway: describe only what you want), the platform card wins.

Common items: text, logos, watermark, distorted hands, extra fingers, warped face, bending walls, clutter, flicker, overexposed windows, cartoonish skin.

## Consistency across shots

- **Look Card** — palette, lens feel, light, grade, era. Reuse word for word in every shot.
  `Look: warm muted palette, 35mm lens feel, soft window light, light film grain.`
- **Character Card** — age, hair, clothing, one distinctive detail. Reuse word for word.
  `Mia: a woman in her early 30s, shoulder-length black hair, cream knit sweater, small gold earrings.`
- Use the same reference image for a character in every shot when the tool allows it.
- For continuous action, use the last frame of the previous clip as the first frame of the next.

## Realism

For photoreal people and materials, add 1–2 small imperfections: a fabric crease, a scuff on a wooden table, real skin texture, a slightly uneven stack of plates. Perfect surfaces look fake.

## Text inside images or video

- Default: no text. Titles, prices and captions are added in editing.
- If the user explicitly wants text (poster, thumbnail) and the tool renders text well (see image-platforms.md): put the exact words in double quotes, say where and how big, keep it to 1–6 words, and add "no other text". Keep the quoted words exactly as the user wrote them — Chinese stays Chinese. For Chinese text, Seedream (即梦/豆包) is usually the most reliable; suggest it if the result is garbled.

## Safety and originality

- Do not imitate copyrighted characters, film scenes, or a living artist's signature style by name; describe original characters and generic styles instead.
- Do not describe a real, identifiable person's likeness unless it is the user themself with their own photo as reference.
- Do not request real brand logos; use "an unbranded bottle", "a plain white label".
- For ads: no false claims, no fake reviews, no misleading before/after.

## Camera and lighting vocabulary

| 中文 | English |
|---|---|
| 远景 / 全景 / 中景 / 近景 / 特写 | wide shot / full shot / medium shot / close-up / extreme close-up |
| 平视 / 俯拍 / 仰拍 / 顶拍 | eye level / high angle / low angle / top-down |
| 推 / 拉 | slow push-in (dolly-in) / pull-back |
| 摇 / 移 / 跟 | pan / lateral tracking (truck) / follow shot |
| 升 / 降 / 环绕 | crane up / crane down / orbit |
| 固定机位 / 手持 / 稳定器 | locked-off tripod / handheld / gimbal-smooth |
| 浅景深 / 大景深 | shallow depth of field / deep focus |
| 广角 / 标准 / 长焦 | 24mm wide / 35–50mm natural / 85mm portrait |
| 黄金时刻 / 蓝调时刻 / 阴天柔光 | golden hour / blue hour / soft overcast daylight |
| 窗光 / 逆光 / 轮廓光 / 侧光 | window light / backlight / rim light / side light |
| 暖色台灯 / 霓虹 / 烛光 | warm table lamp / neon glow / candlelight |
| 慢动作 / 延时 | slow motion / time-lapse |

Fast moves and orbits bend straight lines (buildings, furniture). Use slow, straight moves for architecture and products.
