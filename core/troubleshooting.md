# Troubleshooting (废片诊断)

Find the symptom, name the cause in one line, change one thing, and say what changed.

| 问题 Symptom | 常见原因 Likely cause | 第一步修正 First fix |
|---|---|---|
| 每次结果都不一样（抽卡） | Prompt too vague; elements missing | Fill all 8 elements; generate a first-frame image, then animate it |
| 人脸/产品/房子变样 | Too much motion, or image-to-video prompt re-describes what the image already shows | Describe only the motion; add a preservation line ("preserve the face/product/room exactly"); reduce motion |
| 镜头乱晃、乱跳 | Several camera moves, or no end point | One move with start and end; "locked-off" or "gimbal-smooth" |
| 画面平淡、没质感 | Empty style words, flat light | Named light source, material details, lens feel |
| 动作乱、顺序错 | Too many actions for the duration | ≥3 seconds per action; split into clips |
| 模型自己乱加东西 | Clip too long for the content | Shorten the clip, or add one concrete action |
| 什么都不动 | Only static description | Add one actor + verb + visible result + time cue ("over 3 seconds") |
| 手指变形、多手指 | Close-up fine hand work | Medium shot; hands at frame edge or soft focus; simpler action |
| 出现乱码文字、假 logo | The model was asked to draw text or signs | Remove text; add it in editing; "plain unlabeled surfaces" |
| 墙、桌子、建筑弯曲 | Orbit or fast camera; very wide lens | Slow straight push or lateral move; "straight vertical lines"; 24–35mm |
| 有不想要的音乐或声音 | No sound line | "no music, natural ambience only" |
| 口型对不上 | Moving head or camera; long sentences | Locked-off camera; shorter lines; one speaker |
| 多个镜头人物不一样 | No Character Card or reference | Reuse the same Character Card and reference image |
| 颜色/风格前后不一致 | No Look Card | Reuse the same Look Card in every shot |
| 太假、像塑料 | Too perfect | Add 1–2 natural imperfections; "real skin texture" |
| 被平台拒绝 | Real person, brand, copyrighted character, unsafe wording | Rewrite as an original, safe description — never use tricks to get around the rules |

## Retry protocol

1. Say what failed and what was good in the result.
2. Change **one** variable: camera, light, motion, duration, or number of people.
3. Prefer cheap fixes first: fix text and color in editing; regenerate only the failing shot; test at low resolution.
4. Conservative retry template:
   `[Opening frame or reference]. Preserve [face/product/room] exactly. One visible action: [verb + result] over [N] seconds. Camera: [one move]. Light: [source]. Sound: [cue]. No text, no logos.`
5. Same failure twice → split the shot, remove a person, simplify hands, or switch from text-to-video to image-first.
