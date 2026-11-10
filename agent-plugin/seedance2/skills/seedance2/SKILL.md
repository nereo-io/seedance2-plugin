---
name: seedance2
description: "Route Seedance 2 requests: mixed or unclear video and image work, the user's credit balance and plan, recent generations, or what Seedance 2 can do. Prefer a focused seedance2-* skill when the request has one clear outcome."
---

# Seedance 2

Seedance 2 makes videos and images on the user's Seedance 2 account, paid with their credits. Models include Seedance 2.5, Seedance 2.0, Seedance 2.0 Fast and Seedance 2 Mini, plus other video and image models listed by `list_models`.

Read [workflow](references/workflow.md) once per task: tool order, prices, waiting, uploads, and what to do when the server is not connected. Read [Seedance prompting](references/seedance-prompting.md) before writing a video prompt.

## Route the request

| The user wants | Use |
| --- | --- |
| One video clip from text or a photo | `seedance2-generate-video` |
| A photo brought to life, first frame kept exact | `seedance2-animate-image` |
| A product video ad from product photos | `seedance2-product-ad` |
| A creator-style UGC ad with a presenter | `seedance2-ugc-ad` |
| A script, shot list or storyboard before rendering | `seedance2-storyboard` |
| A multi-shot short drama with recurring characters | `seedance2-short-drama` |
| To connect, get started or take a tour | `seedance2-setup` |
| Balance, plan, or what a past generation cost | `get_account`; `get_task` without `taskId` for recent generations |
| A single image | `list_models` (image models), then `generate_image` |

## Balance and buying

Quote the balance from `get_account`. Plans and credits are bought on https://www.seedance2.net/pricing, not in chat; do not start or recommend a purchase.
