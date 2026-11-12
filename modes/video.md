# Mode A — Video

## Structure of one clip

```
[Scene: place, time of day, 2–3 key details]
[Characters: Character Card, or "no people"]
[Action: one beat for clips under 6 s; time slices for 6 s or longer]
Camera: [shot size, angle, lens feel, ONE move with start and end]
Light: [named source]
Style: [one look]
Sound: [ambience + music mood + signature sound, or "no music, natural ambience only"]
[Guardrail line]
```

## Timing rules

- **≥ 3 seconds per action beat.** A small reaction (a smile, a glance) counts as half a beat.
- **6 seconds or longer → time slices**, one beat per slice: `0–3s: … / 3–6s: … / 6–9s: …`
- End with a calm hold: "the final frame holds for one second".
- Longer stories: several short clips are more stable than one long clip. Plan them with Mode D.

## Camera rules

- Exactly one move per shot, with a start and an end: "slow push-in from the doorway to the window".
- Never combine contradicting moves ("static" + "orbit").
- People and drama: eye level, 35–50mm feel, slow push-in or gentle follow.
- Products and architecture: slow straight moves; avoid fast orbits.

## Image-first (best fix for 抽卡)

For key shots, recommend this order:
1. Write a Mode B prompt for the **opening frame**.
2. The user generates the image and approves it.
3. Animate it with an image-to-video prompt.

### Image-to-video prompt

Describe only what the image cannot show — the motion. Re-describing the image causes drift.

```
The reference image is the opening frame; preserve [face / outfit / product / room layout] exactly.
Only [motion] changes over [N] seconds.
Camera: [one move with an end point].
Light: [source or change].
Sound: [cue].
Nothing else moves; no new objects appear.
```

- **Hold mode** (places, products, scenery): 2–4 small motions (steam, curtains, sunlight moving on the floor, leaves, water shimmer); camera locked-off or one slow push-in.
- **React mode** (people): split one emotion into small steps over ≥ 2 seconds: "she hears the knock, her eyes lift, her shoulders tense".

## Dialogue in video

- ≤ 2.5 English words or ≤ 4 Chinese characters per second.
- One speaker per line, written as: `She says, in a calm voice: "…"`
- Head mostly still, camera locked-off for close-ups with speech.
- Only use spoken dialogue on platforms that generate audio (see video-platforms.md); otherwise put lines in the voiceover plan (Mode C/D).

## Multi-shot sequences

1. Write the Look Card and Character Card first.
2. One copy block per shot, each repeating the cards word for word.
3. Note continuity: "Shot 2 starts from the last frame of Shot 1".

## Worked example

Input: "房子里主人在大厅招待客人喝酒玩耍" → user answers: 9:16, 温馨, modern home, platform unknown.

Self-check catches: 6 people interacting → 2 in focus, others in soft background; 3 beats in 8 s → 10 s; close-up clinking glasses (hands) → medium shot, glasses raised.

```
A modern open-plan living room at early evening: floor-to-ceiling windows with a soft sunset over green hills, light oak floors, a low cream sofa, a white marble kitchen island.
Foreground: the host, a man in his late 30s in a white linen shirt, and his friend, a woman in her 30s in a navy dress. Background: three guests of mixed ages and backgrounds chat and laugh softly by the sofa, slightly out of focus.
0–4s: The host pours red wine into two glasses at the island and hands one to his friend.
4–7s: They turn toward the window, laughing, glasses in hand.
7–10s: They raise their glasses at chest height by the window; the final frame holds for one second.
Camera: one slow dolly-in from the room entrance toward the window, eye level, 35mm lens feel, shallow depth of field.
Light: warm golden-hour sunlight through the windows, soft pendant lights over the island.
Style: realistic lifestyle commercial, natural skin texture, a light crease in the linen shirt, warm muted palette.
Sound: quiet acoustic guitar, soft laughter, light glass clinks, no dialogue.
No text, no logos, no watermark; walls stay straight.
```
