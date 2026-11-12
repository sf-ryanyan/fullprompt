# Image platform cards

Last checked: 2026-11. If the user's tool behaves differently, follow the tool.

| Platform | Prompt style | Negative field | Text in image | Notes |
|---|---|---|---|---|
| GPT Image (ChatGPT) | Full natural sentences | No — use a guardrail sentence | Good | Great for edits from a reference photo; say exactly what to keep |
| Nano Banana (Gemini image) | Full natural sentences | No — use a guardrail sentence | Good | Strong at keeping a person or product consistent across edits |
| Seedream (即梦 / 豆包) | Natural sentences, English or Chinese | Depends on host | Good, including Chinese text | Good for Chinese posters |
| Midjourney | Short comma phrases + parameters | `--no …` | Weak — add text later | Parameters: `--ar 9:16`, `--style raw` for a more photographic look |
| Stable Diffusion / Flux | Keywords or sentences (Flux prefers sentences) | Yes (SD); limited (Flux) | Flux decent, SD weak | Put negatives in the separate field for SD |

## Syntax examples

**Natural-sentence tools (GPT Image, Nano Banana, Seedream, Flux):**
```
A ceramic pour-over coffee set on a walnut counter in a quiet café, early morning. Medium shot at eye level, set on the right third, top 40% left as a blurred cream wall for a title. Soft side window light, warm muted palette, light film grain. No text, no logos.
```

**Midjourney:**
```
ceramic pour-over coffee set on a walnut counter, quiet café, early morning, soft side window light, medium shot, eye level, negative space at top, warm muted palette, editorial photography --ar 4:5 --style raw --no text, logo, watermark
```

**Stable Diffusion:**
- Prompt: `ceramic pour-over coffee set, walnut counter, quiet cafe, morning window light, editorial photo, shallow depth of field`
- Negative: `text, logo, watermark, blurry, deformed, oversaturated`

## Editing from a reference photo

- Say what must stay: "keep the product shape, label and color exactly the same".
- Say only what changes: "replace the background with a sunlit marble counter".
- One change per edit is more reliable than many.
