# Faceless Story Video Skill — Free Lite

Turn one topic into a complete 60-90 second faceless story video plan for YouTube Shorts, TikTok and Instagram Reels: moral/emotional story in **Urdu or English**, scene-by-scene image prompts with a consistent character, Urdu voiceover script, gold word-highlight captions, thumbnail brief, title/description/hashtags and a 9:16 export checklist.

Works with Claude Code, the Claude app, Gemini CLI, Codex, Cursor and any other tool that reads Agent Skills (`SKILL.md`).

## Quick start

1. Install the skill (see `INSTALL.md` — 2 minutes, no code).
2. Tell Claude your topic: *"Make a faceless story video about a boy who returns a lost wallet, in Urdu, 60 seconds."*
3. Claude writes the story, the image prompts, the voiceover, the captions, the thumbnail brief and the upload text.
4. Make the pictures from the prompts, record the voiceover (or use a voice tool), and assemble in CapCut.

See `faceless-story-video/examples/` for a complete example: the story `example-story.json` and its finished output `example-output.md`.

## Free Lite vs Pro

| | Free Lite (this repo) | Pro (coming soon, $12–$19 one-time) |
|---|---|---|
| Story formats | 1 — moral / emotional | 5 — moral, horror, history, Islamic story, motivational |
| Languages | Urdu + English | Urdu + Roman Urdu + English |
| Caption styles | 1 — gold word-highlight | SRT files + more styles |
| Thumbnail | 1 brief | A/B variants |
| Extras | — | 30-day posting calendar |

## Honest limits

- This skill writes everything **except the rendered MP4**. In Claude Code with ffmpeg/Remotion it can drive the render; in the Claude app, assemble the video in CapCut from the script, prompts, voiceover and SRT the skill produces.
- Claude app upload: guides disagree — one says Skills upload needs a Pro plan, another says all plans including Free. Test on a free account before assuming; Claude Code and Gemini CLI have no such limit.
- The skill never promises views, earnings or a platform result — only the plan it writes.

## Why Urdu?

Most free video skills are English-only, and most caption/video tools break Urdu right-to-left text. This skill is built for Urdu first: Urdu-script narration, correct pronunciation notes, and captions that keep Urdu lines whole instead of splitting them word by word.

## Files

- `faceless-story-video/SKILL.md` — the skill itself.
- `faceless-story-video/references/` — story structure, Urdu narration rules, image prompts.
- `faceless-story-video/examples/` — a complete moral story + its finished output.
- `INSTALL.md` — install steps for every platform.
- `CHANGELOG.md` — what changed in each version.

## License

MIT — free to use, share and remix. See `LICENSE`.
