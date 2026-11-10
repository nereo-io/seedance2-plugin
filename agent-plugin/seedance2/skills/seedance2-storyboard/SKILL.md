---
name: seedance2-storyboard
description: "Plan a video before rendering: script, shot list, timing and optional storyboard frames made with Seedance 2 image models. Use when the user wants to plan, storyboard or outline a video, or when a request needs several shots and no plan exists yet."
---

# Storyboard

Read [workflow](references/workflow.md) once per task: tool order, prices, waiting, uploads, and what to do when the server is not connected. Read [Seedance prompting](references/seedance-prompting.md) before writing a video prompt.

## Steps

1. Write the shot list as a table: shot number, length (s), what happens, camera, audio, mode (text, first frame, references).
2. Keep each shot to one action. Total length = the sum of shot lengths.
3. Estimate the cost: price each shot from `list_models` and give the total. Planning spends nothing.
4. Storyboard frames are optional and cost credits: offer one `generate_image` frame per shot at the video's aspect ratio. Approved frames become first frames for image to video.
5. Only render clips when the user approves the plan; then follow `seedance2-generate-video` per shot.
