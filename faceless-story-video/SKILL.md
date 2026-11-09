---
name: faceless-story-video
description: Turn one topic or idea into a complete 60-90 second faceless story video plan for YouTube Shorts, TikTok and Instagram Reels — moral/emotional story in Urdu or English, scene-by-scene image prompts with a consistent character, Urdu voiceover script, kinetic captions, thumbnail brief, title/description/hashtags and a 9:16 export checklist. Use when the user wants a short story video without showing their face, or asks for a story script, scene prompts, narration, captions or a thumbnail for a Short/Reel.
---

# Faceless Story Video (Lite)

One topic in, one complete video plan out. The plan is ready to produce: the story, the pictures, the voice, the captions, the thumbnail and the upload text. This Lite version makes **one story format: a moral / emotional story, 60-90 seconds, Urdu or English**. (More formats live in the Pro version.)

## Workflow

Follow the steps in order. Do not skip the story before the pictures: every image prompt and every caption line comes from the finished story, never the other way round.

1. **Topic.** Ask for one topic or idea if the user did not give one (for example: "a boy who returns a lost wallet", "a mother's sacrifice"). One topic, one story.
2. **Story.** Write the story first, in the scene JSON format in `references/story-structure.md`. 60-90 seconds, 6-12 scenes, hook in the first 3 seconds, one twist, ending with a clear moral or emotional payoff.
3. **Image prompts.** Write one image prompt per scene from `references/image-prompts.md`. Same character in every scene (same face, hairstyle and costume — repeat the description in every prompt). 3D-cartoon style, 9:16.
4. **Voiceover script.** Write the narration from `references/urdu-narration.md`. Urdu narration is written ONLY in Urdu script. Never Devanagari. One speaker per clip — never write dialogue between two people in one clip; split it into one-speaker clips.
5. **Captions.** One style in Lite: gold word-highlight kinetic captions (the spoken word turns gold as it is said). Produce an SRT file with the exact narration lines and timings.
6. **Thumbnail + SEO.** One thumbnail brief (see below) plus title, description and hashtags for Shorts, TikTok and Reels.
7. **Export checklist.** End with the checklist below so the video ships in the right format.

## Output 1 — Story JSON

Return the story as JSON with exactly these keys: `title`, `language` (`"ur"` or `"en"`), `style` (`"moral"`), `mood` (one word), `scenes` (a list of 6-12 scenes). Each scene has: `duration` (seconds, number), `visual` (one short keyword, e.g. `rainy_street`), `camera` (`push`, `pull`, `pan_left` or `pan_right`), `effect` (`rain`, `dust` or `embers`), `ambience` (`rain` or `empty`), `sfx` (one short sound for the scene, e.g. `rain`, `birds chirping` — or empty if the scene is quiet), `narration` (1-2 spoken sentences, Urdu script for `ur`), `caption` (same as narration, or a shorter on-screen version), `visual_description` (2-3 sentences in English: WHERE the scene happens, WHAT objects are visible, WHAT the character is DOING), `props` (2-4 key objects, in English), `shot` (`close_up`, `medium_shot`, `wide_shot` or `full_body` — vary it, never the same shot twice in a row). Scene durations must add up to 60-90 seconds. See `examples/example-story.json` for a complete example.

## Output 2 — Image prompts

One prompt per scene. Formula: `[style] + [character, repeated exactly] + [place and action from visual_description] + [mood and light] + 9:16 vertical`. Style default: `3D cartoon, Pixar-style, soft light, expressive faces`. Never put text, words or letters inside an image prompt — AI image tools misspell text; all words go in the captions, never in the picture. Full rules in `references/image-prompts.md`.

## Output 3 — Voiceover script

Narration is the story's `narration` fields, in order, one clip per scene. Urdu: natural spoken Urdu, short sentences, warm tone. Never write narration in Roman Urdu when the language is `ur` — Urdu script only. Never mix two speakers in one scene. Full rules in `references/urdu-narration.md`.

## Output 4 — Captions (Lite style: gold word-highlight)

SRT format, one file. Each caption event matches one scene's narration, split into short lines (max 2 lines, max 5-6 words per line). The spoken word is highlighted gold as it is said; the rest stays white. Urdu captions stay in Urdu script, right-to-left, one whole line per event (never split an Urdu line word-by-word — the script breaks). Roman Urdu or English captions may highlight word by word.

## Output 5 — Thumbnail brief + SEO

Thumbnail brief: one 9:16 image idea (the most emotional moment of the story, one character, one big feeling, no text in the image), plus 3 thumbnail title options (max 5 words each, Urdu or English matching the video language). SEO: 1 title (max 70 characters), 1 description (2-3 lines + the moral in one line), 8-10 hashtags (mix of broad: #Shorts #Story, and specific: #UrduStory #MoralStory). Keep every claim honest — never promise the video contains something it does not.

## Output 6 — Export checklist

- 9:16 vertical, 1080x1920, 24-30 fps
- 60-90 seconds total
- Voice on every scene (no silent scene — a scene with no voice gets a warning, not a pass)
- Captions burned in or SRT sidecar, inside the safe zone (away from the TikTok/Reels buttons)
- Thumbnail exported as a still from the most emotional scene

## Hard rules (never break these)

- Urdu narration is ALWAYS Urdu script. Never Devanagari, never Roman Urdu for `ur` stories.
- One speaker per clip. Never two people talking in one scene.
- No faces of real people, no real-person names, no graphic violence, no hate. Clean, family-friendly stories only.
- Never put text inside an image prompt.
- Never invent a fact about the video (views, platform, price) — only what the plan contains.

## What this skill does NOT do

This skill writes everything **except the rendered MP4**. In Claude Code with ffmpeg/Remotion it can drive the render; in the Claude app, assemble the video in CapCut (or any editor) from the script, prompts, voiceover and SRT this skill produces. It does not generate images or audio by itself — it writes the prompts and scripts your tools use.

## References (read when needed)

- `references/story-structure.md` — story arc, scene format, shot list, duration math.
- `references/urdu-narration.md` — Urdu script rules, narration style, pronunciation notes.
- `references/image-prompts.md` — consistent-character prompts, style, negatives.
- `examples/example-story.json` — a complete moral story in the exact JSON format.
- `examples/example-output.md` — what the finished output looks like for that example.
