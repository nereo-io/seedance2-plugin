# Prompting Seedance 2.5 and Seedance 2.0

Read before writing a video prompt. Limits and prices change: confirm them with `list_models`.

## Choosing a model

| Need | Model |
| --- | --- |
| Best quality, longer clips (Seedance 2.5 runs up to 30 s), rich references | Seedance 2.5 |
| Strong quality at lower cost, up to 15 s | Seedance 2.0 |
| Cheap draft to check motion and framing | Seedance 2.0 Fast, Seedance 2 Mini, or 480p |
| The user named another model on the site (Veo 3.1, Kling, Wan, MiniMax, Gemini Omni) | That model |

Draft cheap, then render the take the user likes at full quality. Honour a model the user names.

## Modes

- **Text to video**: everything comes from the prompt.
- **Image to video**: `images[0]` is the first frame and the clip starts on it exactly; an optional second image is the last frame. Use when the opening must match a photo (a product, a face, a scene).
- **Reference to video**: `references` carry images, videos and audio that guide identity, product, style, motion or sound without fixing the first frame. Use for a product or character placed in a new scene, or to borrow a motion or a voice. Reference videos add their length to the billed seconds.

## Prompt structure

Write one clear paragraph in this order:

1. **Subject**: who or what, with the details that must stay fixed (face, outfit, product colour, logo).
2. **Action**: what happens, in time order. One main action per short clip.
3. **Camera**: shot size and movement — wide, medium, close-up; static, slow push-in, pull-back, orbit, tracking, tilt up, handheld, rack focus, POV.
4. **Setting and light**: place, time of day, light quality (soft studio light, golden hour, neon, overcast).
5. **Style**: photoreal, commercial, documentary, anime, claymation; colour grade.
6. **Audio** (when audio is on): ambience, sound effects, music mood, or dialogue in quotes with who says it.

Keep it concrete: "a matte black bottle on wet slate, droplets on the cap" beats "a premium product".

## Lengths and pacing

- 4–6 s: one action, one camera move. Best for ads, loops and drafts.
- 8–15 s: one or two beats, or a described cut ("cut to a close-up of…").
- Seedance 2.5 up to 30 s: a short sequence; describe beats in order.

Shorter clips cost less and stay more coherent. Prefer several short clips the user can cut together over one long one when the story has many beats.

## Aspect ratio

9:16 for Reels, TikTok, Shorts · 16:9 for YouTube, web, presentations · 1:1 or 4:5 for feeds. With image to video, match the photo's ratio.

## Keeping things consistent across clips

- Reuse the same reference images for a character or product in every clip.
- Repeat the fixed details in the same words in every prompt.
- For a sequence, use the last frame of one clip (or a still from it) as the first frame of the next.

## Common fixes

| Problem | Fix |
| --- | --- |
| Product shape or label drifts | Image to video with the product photo as the first frame; fewer moving parts; slower camera |
| Face changes | Reference images of the face from 2–3 angles; avoid fast head turns |
| Too much happening | Fewer actions; shorter length |
| Camera ignored | Put the camera move in its own sentence, early |
| Unwanted music | With audio on, ask for "ambient sound only, no music" |
