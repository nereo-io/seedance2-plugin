---
name: seedance2-setup
description: "First run for Seedance 2: check the connection, explain what it can make and what it costs, and help make a first video. Use right after installing, when the user asks how to start, or when the Seedance 2 tools are not connected."
---

# Set up Seedance 2

**Not connected yet?** If no Seedance 2 tools (such as `list_models` or `generate_video`) are available, the plugin is installed but the server is not connected. Stop and give the user the click path: in Claude open Settings → **Connectors**, press **Add custom connector**, name it `Seedance 2`, paste `https://www.seedance2.net/mcp`, press **Connect** and sign in. In Claude Code they run `/mcp` instead. Then they ask again. Do not substitute other tools or describe a result that was not generated.

Read [workflow](references/workflow.md) once per task: tool order, prices, waiting, uploads, and what to do when the server is not connected. Read [Seedance prompting](references/seedance-prompting.md) before writing a video prompt.

## Steps

1. Check the connection: if `list_models` and `get_account` are not available, give the connection steps from the workflow guide and stop.
2. `get_account`: tell the user their balance and plan. New accounts start with free credits.
3. Say in two lines what Seedance 2 makes: videos from text, a photo or references with Seedance 2.5 and Seedance 2.0 (and other listed models), and images.
4. Ask what they want to make. Do not generate anything until they choose.
5. Make one small first result: a short 480p or Seedance 2.0 Fast draft, with its price quoted first.
6. Point to the focused skills for what comes next (product ad, animate image, storyboard).
