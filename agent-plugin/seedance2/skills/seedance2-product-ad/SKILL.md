---
name: seedance2-product-ad
description: "Make a short product video ad from product photos with Seedance 2.5 or Seedance 2.0: hero shots, reveals, packshots and variants for TikTok, Reels, Shorts or web. Use when the user wants an ad or promo for a physical or digital product."
---

# Product video ad

**Not connected yet?** If no Seedance 2 tools (such as `list_models` or `generate_video`) are available, the plugin is installed but the server is not connected. Stop and give the user the click path: in Claude open Settings → **Connectors**, press **Add custom connector**, name it `Seedance 2`, paste `https://www.seedance2.net/mcp`, press **Connect** and sign in. In Claude Code they run `/mcp` instead. Then they ask again. Do not substitute other tools or describe a result that was not generated.

Read [workflow](references/workflow.md) once per task: tool order, prices, waiting, uploads, and what to do when the server is not connected. Read [Seedance prompting](references/seedance-prompting.md) before writing a video prompt.

## Steps

1. Collect: product photo(s), the platform (sets the ratio: 9:16 social, 16:9 web), length (6–10 s is typical), mood, and any text or claim the user wants. On-screen text is better added in editing than generated.
2. Keep the product exact:
   - Opening must match the photo → image to video with the photo as the first frame.
   - Product in a new scene → reference to video with the photo(s) as references; repeat colour, material and logo position in the prompt.
3. Plan 1–3 shots: hero (slow orbit or push-in), use or context, closing packshot. Each is its own clip.
4. Draft one shot cheaply (Seedance 2.0 Fast or 480p), confirm the look with the user, then render the rest at the agreed quality.
5. Quote the total for all shots before starting. Generate, poll, and list the URLs in shot order.

## Prompt pattern

"[Product with fixed details] on [surface/setting]. [One motion]. [Camera move]. [Light]. Premium commercial look, [ratio]. [Audio: ambient sound or none]."
