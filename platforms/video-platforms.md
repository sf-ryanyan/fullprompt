# Video platform cards

Last checked: 2026-11. Models change fast — if the user's tool shows different limits, follow the tool.
If the platform is unknown, write a platform-neutral English prompt with the guardrail line inside the prompt.

## Quick table

| Platform | Prompt language | Separate negative field | Generates sound | Best at |
|---|---|---|---|---|
| Seedance (即梦, 豆包, ListenHub and other hosts) | English or Chinese | Partial / depends on host | Yes on newer versions | Multi-shot stories, characters, reference images |
| Kling 可灵 | English or Chinese | Yes | Yes on newer versions | Character motion, physics, multi-person dialogue |
| Veo (Google) | English | Yes (API / some UIs) | Yes, native dialogue and sound | Polished commercials, dialogue, synced sound effects |
| Sora (OpenAI) | English | No | Yes | Complex scenes, motion coherence |
| Runway | English | No — describe only what you want | Depends on model | Image-to-video, controlled camera |
| Hailuo 海螺 (MiniMax) | English or Chinese | Yes | Depends on model | Expressive motion, short dramatic clips |
| Wan 通义万相 | English or Chinese | Yes | Depends on model | Open-source option, stylized looks |
| PixVerse | English | Depends on host | Yes | Effects, lip sync, quick social clips |

## Card notes

### Seedance (incl. 即梦 / ListenHub)
- Strong with time-sliced, multi-beat prompts and multiple reference images.
- Give each reference image one clear job: "Image 1 is the opening frame; Image 2 is the character".
- Negatives: put the guardrail line at the end of the prompt.
- Test at low resolution (draft) first, then render the approved version at full resolution.
- On ListenHub: Seedance 2.5 handles 4–30 s; Seedance 2.0 Pro supports start + end frame transitions.

### Kling 可灵
- Use the negative field for: text, watermark, distorted hands, warped face, flicker.
- Good choice for scenes with two people talking; keep lines short.
- Chinese prompts work well in the Chinese app.

### Veo
- Write dialogue as: `The woman says, warmly: "Welcome home."`
- Always add a sound line — Veo generates audio by default.
- Use the negative field when available; keep it to concrete items.

### Sora
- No negative field: write positive descriptions and one short guardrail sentence.
- Describe the shot like a director's note: subject, action, camera, light, sound.

### Runway
- Best with a first-frame image; the prompt should describe motion and camera only.
- Do not write "avoid / no …" lists — describe the desired result instead; keep at most "no text".

### Hailuo 海螺 / Wan 通义万相
- Use the negative field.
- Keep one clear action per clip; short clips are more stable.

### PixVerse
- Good for quick social clips and effects; keep prompts short and concrete.

## Length guide

- Most clips: 5–10 seconds. Longer clips need time slices and more beats.
- For anything longer than the tool's maximum, plan several clips with Mode D and join them in editing.
