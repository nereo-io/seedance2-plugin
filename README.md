# Seedance 2 plugin for Claude, Claude Code, Codex and Cursor

Make **Seedance 2.5** and **Seedance 2.0** videos, and AI images, from inside your AI assistant. The plugin connects your assistant to the [Seedance 2](https://www.seedance2.net) MCP server and adds skills that know how to prompt Seedance, quote credit prices and deliver the finished clip in the chat.

- Text to video, image to video (first and last frame) and reference to video (images, video, audio)
- Seedance 2.5 clips up to 30 s, Seedance 2.0 up to 15 s, up to 1080p, optional generated audio
- Other models on the same credit balance: Veo 3.1, Kling, Wan, MiniMax, Gemini Omni, Nano Banana, GPT Image, Seedream
- No API key: sign in with a Seedance 2 account (new accounts get free credits)

## Install

**Claude Code**

```
/plugin marketplace add nereo-io/seedance2-plugin
/plugin install seedance2@seedance2-marketplace
/mcp
```

Pick `seedance2` in `/mcp` and sign in.

**Codex**

```
codex plugin marketplace add nereo-io/seedance2-plugin
codex plugin add seedance2@seedance2-marketplace
```

**Claude (web, desktop, mobile)**: Settings → Connectors → Add custom connector, name `Seedance 2`, URL `https://www.seedance2.net/mcp`, then Connect and sign in. Optional: upload [seedance2-skill.zip](https://www.seedance2.net/seedance2-skill.zip) under Settings → Capabilities → Skills.

**Any other MCP client** (ChatGPT, Cursor, Gemini, Grok, OpenClaw, Hermes): add the remote MCP server `https://www.seedance2.net/mcp` (Streamable HTTP, OAuth). Setup screens: https://www.seedance2.net/plugin

## Skills

| Skill | For |
| --- | --- |
| `seedance2` | Mixed requests, balance and plan, recent generations |
| `seedance2-generate-video` | One clip from text, a photo or references |
| `seedance2-animate-image` | Bring a photo to life, first frame kept exact |
| `seedance2-product-ad` | Product photo to short video ad |
| `seedance2-ugc-ad` | Creator-style talking-head or testimonial ad |
| `seedance2-storyboard` | Script, shot list and cost before rendering |
| `seedance2-short-drama` | Multi-shot story with recurring characters |
| `seedance2-setup` | Connect and make a first video |

## MCP tools

`list_models` (models, options, credit prices) · `generate_video` · `generate_image` · `get_task` · `upload_media` · `get_account`. Only `generate_video` and `generate_image` spend credits; failed generations are refunded automatically. Prices: https://www.seedance2.net/pricing

## Example prompts

- "Make a 5-second Seedance 2.5 clip of a matte black bottle on wet slate, slow push-in, soft studio light, 9:16."
- "Animate this photo with Seedance 2.0: wind in her hair, she looks at the camera, 6 seconds."
- "Plan a 30-second product video in four shots, tell me the cost, then render the first shot."

## Support

support@seedance.tv · https://www.seedance2.net/contact

Seedance models are developed by ByteDance. Seedance 2 (seedance2.net) is a separate service that runs them.
