---
name: seedance2-storyboard
description: "Plan a video before rendering: script, shot list, timing and optional storyboard frames made with Seedance 2 image models. Use when the user wants to plan, storyboard or outline a video, or when a request needs several shots and no plan exists yet."
---

# Storyboard

**Not connected yet?** If no Seedance 2 tools (such as `list_models` or `generate_video`) are available, the plugin is installed but the server is not connected. Stop and give the user the click path: in Claude open Settings → **Connectors**, press **Add custom connector**, name it `Seedance 2`, paste `https://www.seedance2.net/mcp`, press **Connect** and sign in. In Claude Code they run `/mcp` instead. Then they ask again. Do not substitute other tools or describe a result that was not generated.

Read [workflow](references/workflow.md) once per task: tool order, prices, waiting, uploads, and what to do when the server is not connected. Read [Seedance prompting](references/seedance-prompting.md) before writing a video prompt.

## Steps

1. Write the shot list as a table: shot number, length (s), what happens, camera, audio, mode (text, first frame, references).
2. Keep each shot to one action. Total length = the sum of shot lengths.
3. Estimate the cost: price each shot from `list_models` and give the total. Planning spends nothing.
4. Storyboard frames are optional and cost credits: offer one `generate_image` frame per shot at the video's aspect ratio. Approved frames become first frames for image to video.
5. Only render clips when the user approves the plan; then follow `seedance2-generate-video` per shot.
