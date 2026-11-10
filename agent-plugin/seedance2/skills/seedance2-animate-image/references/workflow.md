# Seedance 2 workflow

How to run any Seedance 2 job through the `seedance2` MCP server. Read once per task.

## Tools

| Tool | Use | Spends credits |
| --- | --- | --- |
| `get_account` | Balance and plan. Read before proposing paid work; quote the balance from here. | No |
| `list_models` | Models, modes, lengths, resolutions, aspect ratios, accepted inputs and credit prices. Pass `model` for one model's full price table. | No |
| `generate_video` | Text to video, image to video (`images`: first frame, optional last frame), reference to video (`references`). Returns a `taskId`. | Yes |
| `generate_image` | Text to image, or edit / combine images (`images`). Returns a `taskId`. | Yes |
| `get_task` | State (`running`, `done`, `failed`) and output URLs. `waitSeconds` up to 20. Without `taskId`: the latest generations. | No |
| `upload_media` | Upload the user's local image, video or audio files; returns public URLs to pass as frames or references. | No |

## Order of work

1. `get_account`, then `list_models` for the mode you need.
2. Pick the model and settings. Take ids and options from `list_models`; never guess a model id or a parameter.
3. Tell the user what you will make and what it costs, quoting `list_models`.
4. `generate_video` or `generate_image`.
5. `get_task` with `waitSeconds: 20`, repeated while `state` is `running`. Videos take about a minute to several minutes; images 10–60 seconds.
6. Show the output URL(s). Every result is also saved in the user's Seedance 2 Library.

## Spending

- Generate only what the user asked for. Ask before generating again something that already has a result.
- Failed generations are refunded automatically; say so if one fails.
- If a generation is refused for credits, tell the user what it needs against their balance and offer a cheaper setting (shorter, lower resolution, or a cheaper model) when one fits.
- Never submit the same generation twice. If a submit timed out, call `get_task` without a `taskId` and check the latest generations before trying again.

## Decisions that are the user's

Style, aspect ratio, length, and the model when prices differ a lot. Ask with the client's own choice UI when it has one (2–4 options, your recommendation first); otherwise ask in the chat. Do not ask about what the user already said.

## Media

- Frames and references must be public https URLs.
- Local files: call `upload_media` (Claude Code, Codex, Cursor and scripts can send files), PUT or POST the bytes as it says, then use the returned `url`.
- A file that is already at a public https URL needs no upload.

## Not connected?

If the Seedance 2 tools (`list_models`, `generate_video`) are missing, the server is not connected. Tell the user how to connect it and stop:

- Claude: Settings → Connectors → Add custom connector, name `Seedance 2`, URL `https://www.seedance2.net/mcp`, then Connect and sign in.
- Claude Code: `claude mcp add --transport http seedance2 https://www.seedance2.net/mcp`, then `/mcp` and sign in.
- Codex: add `[mcp_servers.seedance2]` with `url = "https://www.seedance2.net/mcp"` to `~/.codex/config.toml`.
- Other clients: https://www.seedance2.net/plugin

Do not describe a video or image as made when no tool produced it.
