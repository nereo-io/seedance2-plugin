---
name: seedance2-animate-image
description: "Animate a photo or illustration into a video with Seedance 2.5 or Seedance 2.0, keeping it as the exact first frame, optionally ending on a given last frame. Use when the user shares an image and wants it to move."
---

# Animate an image

Read [workflow](references/workflow.md) once per task: tool order, prices, waiting, uploads, and what to do when the server is not connected. Read [Seedance prompting](references/seedance-prompting.md) before writing a video prompt.

## Steps

1. Get the image as a public https URL (`upload_media` for local files).
2. Choose image to video: the photo is `images[0]`, the first frame. A second image becomes the last frame.
3. Match the aspect ratio to the photo.
4. Prompt for motion only — what moves, what stays fixed, and the camera. Do not re-describe the whole picture; the frame already shows it.
5. Pick the model (Seedance 2.5 by default; Seedance 2.0 for clips of 15 s or less at lower cost), quote the price, `generate_video`, poll `get_task`.

## Good motion prompts

- "Wind lifts her hair; she blinks and looks into the lens. Slow push-in. Everything else still."
- "Steam rises from the cup; light shifts slowly across the table. Static camera."
- "The dragon raises its head and exhales smoke; embers drift up. Slight handheld."
