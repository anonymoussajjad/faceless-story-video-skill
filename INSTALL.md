# Install — Faceless Story Video Skill (Free Lite)

No code, no key, no payment. 2 minutes.

## Claude Code

```bash
# From this repo's folder:
mkdir -p ~/.claude/skills
cp -r faceless-story-video ~/.claude/skills/
```

Restart Claude Code (or run `/skills` to reload). Then say: *"Make a faceless story video about [your topic], in Urdu, 60 seconds."*

## Claude app (claude.ai)

1. Zip the `faceless-story-video` folder.
2. In the Claude app: **Customize → Skills → Upload skill** → choose the ZIP.
3. Start a chat and ask for your story video the same way.

Note: guides disagree on whether Skills upload needs a Pro plan or works on all plans including Free. If the upload button is missing on a free account, use Claude Code (free) instead.

## Gemini CLI / Codex / Cursor

These tools read the same `SKILL.md` format:

- **Gemini CLI:** copy `faceless-story-video` into your skills directory (see your tool's docs for the exact path — usually `~/.gemini/skills/`), then ask for a story video.
- **Codex:** copy the folder into your skills directory and reference it in your prompt.
- **Cursor:** place the folder under your project's `.cursor/skills/` (or the global skills folder) and ask for a story video.

## Check it worked

Ask: *"Make a faceless story video about a boy who returns a lost wallet, in Urdu, 60 seconds."*

You should get back: a story in JSON (6-12 scenes), one image prompt per scene, the Urdu voiceover script, captions, a thumbnail brief, title/description/hashtags and an export checklist. If you only get a plain story with no scenes or prompts, the skill did not load — re-check the folder path and reload.

## Update

New versions replace the `faceless-story-video` folder. Delete the old folder first, then copy the new one — never mix two versions in one folder.
