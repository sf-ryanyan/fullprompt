# Prompt library format

The library file is `prompt-library.md` in the user's working folder. Create it with this header if it does not exist:

```
# Prompt Library

Saved by Fullprompt. Entries are added only when you say "存 / 好用 / 收藏".
```

## Entry format

````
## {pack-or-mode}-{nn} ｜ {short title}
- 模式 Mode: 视频 · {platform} · 9:16 · 10s
- 标签 Tags: {3–5 tags, e.g. party, interior, evening, warm}
- 评分 Rating: ⭐⭐⭐⭐
- 原始想法 Idea: {the user's original sentence}
- 备注 Notes: {what worked, what failed and how it was fixed}
- 版本 Version: v1 · {date}

Prompt:
~~~
{full prompt}
~~~
不想出现 Negatives: {list, or "inside prompt"}
````

## Rules

- Number entries per pack or mode: `real-estate-01`, `video-03`.
- Same idea saved again → update the existing entry: bump the version, keep the best prompt, add a note.
- Keep notes short and practical: "hands warped → changed to medium shot".
- Search by tags and title; list results as `标题 · 标签 · ⭐`.
- Never store personal data (phone numbers, addresses, ID numbers) in the library.
