---
name: seedance2-short-drama
description: "Produce a multi-shot short drama or story with recurring characters using Seedance 2.5 or Seedance 2.0: consistent faces and outfits across shots, dialogue and scene cuts. Use for short dramas, story episodes, or narrative series."
---

# Short drama

Read [workflow](references/workflow.md) once per task: tool order, prices, waiting, uploads, and what to do when the server is not connected. Read [Seedance prompting](references/seedance-prompting.md) before writing a video prompt.

## Steps

1. Plan with `seedance2-storyboard`: scenes, shots, dialogue, and the cast.
2. Lock each character: one clean reference image per character (make it with `generate_image` if the user has none, and get approval). Write a one-line description of each and reuse it word for word.
3. Render shot by shot with reference to video, passing that shot's character references. For a continuous scene, use a still from the end of the previous shot as the next first frame.
4. Dialogue: quotes with the speaker named, audio on, lines short enough for the shot length.
5. Quote the total before rendering; render one shot first and confirm the look.
6. Deliver the clip URLs in order with their shot numbers so the user can cut them together.
