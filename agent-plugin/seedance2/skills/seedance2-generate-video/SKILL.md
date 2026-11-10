---
name: seedance2-generate-video
description: "Generate one video clip with Seedance 2.5, Seedance 2.0 or another Seedance 2 model, from text, a first frame, or references. Use for a single clip when the user has not asked for an ad, a storyboard or a multi-shot drama."
---

# Generate a video

Read [workflow](references/workflow.md) once per task: tool order, prices, waiting, uploads, and what to do when the server is not connected. Read [Seedance prompting](references/seedance-prompting.md) before writing a video prompt.

## Steps

1. Work out the mode: text only → text to video; a photo that must be the opening frame → image to video; photos, clips or audio that guide identity, style or sound → reference to video.
2. `list_models` and pick the model: Seedance 2.5 by default; Seedance 2.0 when cost matters or the clip is 15 s or less; Seedance 2.0 Fast or 480p for a draft. Use the model the user names.
3. Settle length, aspect ratio, resolution and audio. Ask only what the user has not said and you cannot infer.
4. Write the prompt with the structure in the prompting guide.
5. Quote the price from `list_models`, then `generate_video`.
6. `get_task` with `waitSeconds: 20` until done; show the URL.
7. Offer one specific next step: a longer or higher-resolution render of this take, or a variant.
