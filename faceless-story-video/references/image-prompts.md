# Image prompts (consistent character, 3D cartoon)

## The formula (every prompt, every scene)

`[style] + [character — repeated EXACTLY in every prompt] + [place and action from visual_description] + [mood and light] + vertical 9:16`

Example: `3D cartoon, Pixar-style, soft light. A kind 10-year-old Pakistani boy, round face, short black hair, green shalwar kameez, standing on a rainy street at dusk, holding a brown leather wallet he just found, surprised and hopeful expression, wet road reflecting warm shop lights, cinematic, vertical 9:16.`

## The character block (write once, repeat everywhere)

Before the first prompt, write one character block: age, face, hair, outfit, one special detail (e.g. a red cap, a torn school bag). Then paste that block word-for-word into every scene prompt. If you change one word of the description, the character's face changes — that is the most common failure in faceless videos.

## Style

- Default: `3D cartoon, Pixar-style, soft light, expressive faces, warm colours`.
- Alternatives only if the user asks: `soft watercolour storybook`, `clay animation style`, `flat vector cartoon`.
- One style per video. Never mix styles between scenes.

## Negatives (put in every prompt or in the tool's negative field)

`no text, no words, no letters, no watermark, no logo, no extra fingers, no distorted face, no blurry background character`.

## Text rule

NEVER put text, words or letters inside an image prompt. Image tools misspell text every time. All words go in the captions, never in the picture. If a scene needs a sign or a letter, describe it as "a blank paper letter" and let the narration say what is written.

## Places and props

- Take the place, objects and action from the scene's `visual_description` and `props` — never invent a new place mid-video.
- One clear place per scene. Two places in one prompt confuse the image.
- Props must be visible and countable: "a brown leather wallet", "three samosas on a plate", "one old letter". Vague props ("some things") produce clutter.

## Common fixes

- Face changed between scenes → the character block was not repeated exactly. Copy it, do not retype it.
- Character looks adult in one scene, child in the next → the age is missing from the block. Always include the age.
- Image is landscape → "vertical 9:16" was missing from the prompt. Always end the prompt with it.
- Text appears in the image → a word slipped into the prompt. Remove it; captions carry all words.
