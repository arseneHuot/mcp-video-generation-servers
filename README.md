# MCP servers for AI video generation: transport, auth, scopes and cost before a run

A maintained dataset of **mcp server for ai video generation** options: what each one connects to, where it stops, how to run it, and a link to the vendor's own pricing page rather than a price that will be wrong by the time you read it.

1. **[Wireflow](https://www.wireflow.ai/blog/best-mcp-server-for-video-editing-tools-in-2026)**
2. **[Flora](https://flora.ai)**
3. **[Krea](https://www.krea.ai)**
4. **[fal](https://fal.ai)**
5. **[Comfy Cloud](https://comfy.org/cloud)**
6. **[HeyGen](https://www.heygen.com/model-context-protocol)**
7. **[Magnific](https://www.magnific.com/spaces)**
8. **[Replicate](https://mcp.replicate.com)**
9. **[Runway](https://github.com/runwayml/runway-api-mcp-server)**
10. **[MiniMax](https://github.com/MiniMax-AI/MiniMax-MCP)**
11. **[pitchboom](https://pitchboom.io)**

The tables below are generated from [`data/tools.json`](data/tools.json). Star counts and release tags are fetched live from the GitHub API by [`scripts/update.js`](scripts/update.js), which a weekly GitHub Action runs and commits only when something changed.

<!-- LAST-CHECKED:START -->
Live repository data last checked **2026-10-19** by [`scripts/update.js`](scripts/update.js), which runs weekly via GitHub Actions.
<!-- LAST-CHECKED:END -->

Maintained by [a1adams](https://github.com/a1adams). Corrections are welcome, see [CONTRIBUTING.md](CONTRIBUTING.md).

## Contents

- [The data](#the-data)
- [Capability scores](#capability-scores)
- [The tools](#the-tools)
  - [Wireflow](#1-wireflow)
  - [Flora](#2-flora)
  - [Krea](#3-krea)
  - [fal](#4-fal)
  - [Comfy Cloud](#5-comfy-cloud)
  - [HeyGen](#6-heygen)
  - [Magnific](#7-magnific)
  - [Replicate](#8-replicate)
  - [Runway](#9-runway)
  - [MiniMax](#10-minimax)
  - [pitchboom](#11-pitchboom)
- [Decision this list supports](#decision-this-list-supports)
- [Scope and evidence](#scope-and-evidence)
- [What each column means](#what-each-column-means)
- [Server details](#server-details)
- [Selection notes](#selection-notes)
- [Acceptance recipe](#acceptance-recipe)
- [Evaluation record](#evaluation-record)
- [How this list is maintained](#how-this-list-is-maintained)
- [Contributing](#contributing)
- [License](#license)

## The data

One row per tool, one column per thing people actually check before committing. Columns with nothing verified behind them are dropped rather than filled with guesses.

<!-- DATA-TABLE:START -->
| Tool | Claude connection | Free tier | Model support | Pricing | Open-source SDK / MCP |
|---|---|---|---|---|---|
| **[Wireflow](#1-wireflow)** | Streamable HTTP, OAuth 2.1 with PKCE | [check](https://www.wireflow.ai/pricing) | Image, video and audio models; list_models shows prices | [pricing](https://www.wireflow.ai/pricing) | n/a |
| **[Flora](#2-flora)** | Streamable HTTP, OAuth 2.1 with PKCE | [check](https://flora.ai/pricing) | Video, image and audio generations and saved Techniques | [pricing](https://flora.ai/pricing) | n/a |
| **[Krea](#3-krea)** | Streamable HTTP, OAuth or API token | n/a | Krea image and video models, for example video/google/veo-3.1 | n/a | n/a |
| **[fal](#4-fal)** | Streamable HTTP, API key header or OAuth connector | [check](https://fal.ai/pricing) | Over 1,000 models including image-to-video and text-to-video | [pricing](https://fal.ai/pricing) | n/a |
| **[Comfy Cloud](#5-comfy-cloud)** | Streamable HTTP (public beta), OAuth or API key | [check](https://comfy.org/pricing) | ComfyUI video templates plus partner models such as Seedance | [pricing](https://comfy.org/pricing) | n/a |
| **[HeyGen](#6-heygen)** | Remote server, OAuth | [check](https://www.heygen.com/pricing) | Avatar III, IV and V engines, Video Agent and video translation | [pricing](https://www.heygen.com/pricing) | n/a |
| **[Magnific](#7-magnific)** | Streamable HTTP, OAuth 2.0 | [check](https://docs.magnific.com/pricing) | video_generate with the catalog from video_models_list | [pricing](https://docs.magnific.com/pricing) | n/a |
| **[Replicate](#8-replicate)** | Hosted SSE endpoint or local npm package, API token | [check](https://replicate.com/pricing) | Any Replicate model, including the text-to-video collection | [pricing](https://replicate.com/pricing) | n/a |
| **[Runway](#9-runway)** | Self-run: stdio or a self-deployed HTTP server, API key | [check](https://docs.dev.runwayml.com/guides/pricing/) | Runway API models; Seedance for video and Aleph for video editing by default | [pricing](https://docs.dev.runwayml.com/guides/pricing/) | [runwayml/runway-api-mcp-server](https://github.com/runwayml/runway-api-mcp-server), 23 ★, pushed 2026-09-30 |
| **[MiniMax](#10-minimax)** | Self-run: stdio or SSE, API key | n/a | MiniMax-Hailuo-02 video, plus speech and image | n/a | [MiniMax-AI/MiniMax-MCP](https://github.com/MiniMax-AI/MiniMax-MCP), 1,591 ★, pushed 2026-08-20 |
| **[pitchboom](#11-pitchboom)** | Streamable HTTP, personal API key in a Bearer header | No | Its own motion-design engine; MP4 in 1080p, 4K on Pro and Premium | [pricing](https://pitchboom.io/pricing) | n/a |
<!-- DATA-TABLE:END -->

## Capability scores

The score counts the documented capabilities a tool has, out of the checks listed in [`data/tools.json`](data/tools.json) under `capabilityChecks`. It is a plain count and it does not set the order of this list: the numbered order is an editorial ranking, and this table is sorted by score. The checks and every answer are in the file, so each cell can be checked. Disagree with a cell? Open an issue naming the tool, the check and the evidence.

<!-- CAPABILITY-SCORES:START -->
| Tool | Vendor-hosted endpoint | OAuth sign-in | Read/run/write scope split | Cost shown before a run | Timeline or scene editing | First-party server | Score |
|------|---|---|---|---|---|---|-------|
| **[Wireflow](#1-wireflow)** | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | **6/6** |
| **[Flora](#2-flora)** | ✅ | ✅ | n/a | ✅ | ✅ | ✅ | **5/6** |
| **[pitchboom](#11-pitchboom)** | ✅ | ❌ | ✅ | ✅ | ✅ | ✅ | **5/6** |
| **[fal](#4-fal)** | ✅ | ✅ | n/a | ✅ | n/a | ✅ | **4/6** |
| **[HeyGen](#6-heygen)** | ✅ | ✅ | n/a | n/a | ✅ | ✅ | **4/6** |
| **[Krea](#3-krea)** | ✅ | ✅ | n/a | n/a | n/a | ✅ | **3/6** |
| **[Comfy Cloud](#5-comfy-cloud)** | ✅ | ✅ | n/a | n/a | n/a | ✅ | **3/6** |
| **[Magnific](#7-magnific)** | ✅ | ✅ | n/a | n/a | n/a | ✅ | **3/6** |
| **[Replicate](#8-replicate)** | ✅ | n/a | n/a | n/a | n/a | ✅ | **2/6** |
| **[Runway](#9-runway)** | n/a | ❌ | n/a | n/a | n/a | ✅ | **1/6** |
| **[MiniMax](#10-minimax)** | n/a | n/a | n/a | n/a | n/a | ✅ | **1/6** |
<!-- CAPABILITY-SCORES:END -->

## The tools

### 1. Wireflow

![Wireflow screenshot](https://assets.wireflow.ai/competitors/wireflow-70f47ccd9660.png?v=r5)

- **What it is:** A hosted MCP connector for a node canvas with image, video and audio models. Agents list and run workflows, read prices from list_models, and read or replace a video node's cut with get_video_timeline and edit_video_timeline.
- **Limits:** Generation happens through saved workflows, and only run_workflow spends credits. Custom video block authoring is not open to outside agents yet.
- **Note:** Documentation review 2026-09-28; product and account behaviour were not tested.
- **Links:**
  - [Homepage](https://www.wireflow.ai)
  - [Wireflow best MCP server for video editing tools in 2026 page](https://www.wireflow.ai/blog/best-mcp-server-for-video-editing-tools-in-2026)
  - [Docs](https://www.wireflow.ai/docs/mcp)
  - [Pricing](https://www.wireflow.ai/pricing)

Streamable HTTP endpoint from the official connector docs. Add it as a custom connector, then approve the OAuth consent screen:
```text
https://www.wireflow.ai/api/mcp
```

### 2. Flora

![Flora screenshot](https://assets.wireflow.ai/competitors/flora-2cd907d1b38c.png?v=r5)

- **What it is:** FLORA MCP, a hosted server for Flora's node canvas. Agents run saved Techniques, start image, video and audio generations, and edit canvas nodes, including timeline documents.
- **Limits:** The server gets the same permissions as the signed-in user in the connected workspace. Inside the execute tool, each HTTP request times out after 30 seconds and a whole call after about 5 minutes.
- **Note:** Documentation review 2026-09-28; product and account behaviour were not tested.
- **Links:**
  - [Homepage](https://flora.ai)
  - [Docs](https://developer.flora.ai/mcp/)
  - [Pricing](https://flora.ai/pricing)
  - [Official source 2](https://developer.flora.ai/mcp/tools/)
  - [Official source 3](https://developer.flora.ai/mcp/authentication/)
  - [Official source 4](https://developer.flora.ai/mcp/install/other-clients/)

Server URL from the official Other clients page (transport http, OAuth 2.1 with PKCE):
```text
https://agents.flora.ai/mcp
```

### 3. Krea

![Krea screenshot](https://assets.wireflow.ai/competitors/krea-ai-bfc62405e654.png?v=r5)

- **What it is:** Krea's hosted MCP server. Its tools map to the public API: list models, inspect a schema, generate images or video, run a node app, and poll or cancel jobs.
- **Limits:** OAuth sessions bill compute units on the workspace chosen at consent; API-token sessions bill the separate API balance. The docs list no pre-run price tool.
- **Note:** Documentation review 2026-09-28; product and account behaviour were not tested.
- **Links:**
  - [Homepage](https://www.krea.ai)
  - [Docs](https://www.krea.ai/docs/developers/mcp)
  - [Official source 2](https://www.krea.ai/docs/developers/api-keys-and-billing)

Claude Code command copied from the official MCP page:
```bash
claude mcp add --transport http krea-ai https://api.krea.ai/mcp
```

### 4. fal

![fal screenshot](https://assets.wireflow.ai/competitors/fal-ai-0ec799965278.png?v=r5)

- **What it is:** fal's hosted MCP server for its model catalog. Eleven tools cover model search, schemas, pricing, runs, the job queue and uploads.
- **Limits:** It generates clips through individual models and has no editing or timeline tool. Account operations sit on a separate Platform MCP server.
- **Note:** Documentation review 2026-09-28; product and account behaviour were not tested.
- **Links:**
  - [Homepage](https://fal.ai)
  - [Docs](https://fal.ai/docs/documentation/setting-up/mcp)
  - [Pricing](https://fal.ai/pricing)

Claude Code command copied from the official Run MCP page. Replace YOUR_FAL_KEY with your fal API key:
```bash
claude mcp add --transport http fal-ai \
  https://mcp.fal.ai/mcp \
  --header "Authorization: Bearer YOUR_FAL_KEY"
```

### 5. Comfy Cloud

![Comfy Cloud screenshot](https://assets.wireflow.ai/competitors/comfy-cloud-ac7894e48d8d.png?v=r5)

- **What it is:** Comfy's hosted MCP connection, in public beta. Agents search templates, models and nodes, run templates or saved workflows on Comfy Cloud GPUs, and call partner models.
- **Limits:** Running generations needs an active Comfy Cloud subscription. A separate first-party server, comfy-mcp, drives a local ComfyUI install over stdio.
- **Note:** Documentation review 2026-09-28; product and account behaviour were not tested.
- **Links:**
  - [Homepage](https://comfy.org/cloud)
  - [Docs](https://docs.comfy.org/agent-tools/mcp)
  - [Pricing](https://comfy.org/pricing)

Claude Code command copied from the official Comfy MCP page, then run /mcp to authenticate:
```bash
claude mcp add --transport http comfy-cloud https://cloud.comfy.org/mcp
```

### 6. HeyGen

![HeyGen screenshot](https://assets.wireflow.ai/competitors/heygen-93660b160799.png?v=r5)

- **What it is:** HeyGen's hosted MCP server for avatar video. Tools cover Video Agent sessions, avatar videos, templates, voices, audio search and video translation.
- **Limits:** Usage draws on the credits in your HeyGen plan, and the docs list no pre-run price tool. The tools center on avatar and presenter video rather than a general model catalog.
- **Note:** Documentation review 2026-09-28; product and account behaviour were not tested.
- **Links:**
  - [Homepage](https://www.heygen.com/model-context-protocol)
  - [Docs](https://developers.heygen.com/mcp/overview)
  - [Pricing](https://www.heygen.com/pricing)

Remote MCP server URL from the official overview. Add it as a custom connector and sign in with OAuth:
```text
https://mcp.heygen.com/mcp/v1/
```

### 7. Magnific

![Magnific screenshot](https://assets.wireflow.ai/competitors/magnific-691d474c9ed5.png?v=r5)

- **What it is:** Magnific MCP, from the company formerly branded Freepik. A hosted server with tools for image, video, audio and 3D generation, generation history and Spaces.
- **Limits:** Spaces can be listed and inspected but not run through the listed tools. Generations spend the same credit balance as the app.
- **Note:** Documentation review 2026-09-28; product and account behaviour were not tested.
- **Links:**
  - [Homepage](https://www.magnific.com/spaces)
  - [Docs](https://docs.magnific.com/modelcontextprotocol)
  - [Pricing](https://docs.magnific.com/pricing)

Claude Code command copied from the official Magnific MCP page:
```bash
claude mcp add --transport http magnific https://mcp.magnific.com
```

### 8. Replicate

![Replicate screenshot](https://assets.wireflow.ai/competitors/replicate-dc84c666a83f.png?v=r5)

- **What it is:** Replicate's official MCP server. It exposes the operations of Replicate's HTTP API, so an agent can search models and run predictions on any model, including video models.
- **Limits:** There is no video-specific or editing tool; video runs are ordinary predictions. The hosted connection asks for a Replicate API token during sign-in.
- **Note:** Documentation review 2026-09-28; product and account behaviour were not tested.
- **Links:**
  - [Homepage](https://mcp.replicate.com)
  - [Docs](https://replicate.com/docs/reference/mcp)
  - [Pricing](https://replicate.com/pricing)
  - [Official source 3](https://replicate.com/collections/text-to-video)

Claude Code command copied from mcp.replicate.com, then run /mcp to authenticate:
```bash
claude mcp add replicate https://mcp.replicate.com/sse --transport sse --scope user
```

### 9. Runway

![Runway screenshot](https://assets.wireflow.ai/competitors/runway-2c1b2d181c30.png?v=r5)

- **What it is:** The Runway API MCP server, published in Runway's GitHub organisation. Tools generate video from an image and prompt, edit or upscale video, generate images and speech, and poll or cancel tasks.
- **Limits:** You run it yourself, locally or as an HTTP server you deploy, with a Runway API key. It needs a Runway API developer account with billing set up.
- **Note:** Documentation review 2026-09-28; product and account behaviour were not tested.
- **Links:**
  - [Homepage](https://runway.com)
  - [Docs](https://github.com/runwayml/runway-api-mcp-server)
  - [Pricing](https://docs.dev.runwayml.com/guides/pricing/)

Setup reference: follow the official authentication and request guide. This is a documentation URL, not an executed API example.
```text
https://github.com/runwayml/runway-api-mcp-server
```

### 10. MiniMax

![MiniMax screenshot](https://assets.wireflow.ai/competitors/minimax-fa232c22441c.png?v=r5)

- **What it is:** MiniMax's official MCP server for its speech, image and video APIs, including generate_video and query_video_generation.
- **Limits:** It runs locally with an API key. The README now recommends the MiniMax CLI for the latest models, and warns that using the tools may incur costs.
- **Note:** Documentation review 2026-09-28; product and account behaviour were not tested.
- **Links:**
  - [Homepage](https://www.minimax.io)
  - [Docs](https://github.com/MiniMax-AI/MiniMax-MCP)

Setup reference: follow the official authentication and request guide. This is a documentation URL, not an executed API example.
```text
https://github.com/MiniMax-AI/MiniMax-MCP
```

### 11. pitchboom

- **What it is:** pitchboom's hosted MCP server for its AI motion-design studio for video ads. From a product URL or a short brief it writes the script, builds a storyboard the user edits and approves, adds voice-over in 34 languages and music, and renders an MP4 in 16:9, 9:16, 1:1, 4:5 or 3:4.
- **Limits:** Motion design only: no AI avatars, no live-action or stock footage and no text-to-video generative footage, and it does not publish ads to ad accounts. MCP access needs the Pro or Premium plan (free signup credits are for the web app only), sign-in is by API key with no OAuth yet, and the server code is closed source.
- **Note:** Entry added by the maker of pitchboom on 2026-10-25, from the official MCP docs.
- **Links:**
  - [Homepage](https://pitchboom.io)
  - [Docs](https://pitchboom.io/docs/mcp)
  - [Pricing](https://pitchboom.io/pricing)
  - [GitHub: client config, plugins and an agent skill](https://github.com/arseneHuot/pitchboom)

Claude Code command copied from the official MCP page. Replace pb_live_YOUR_KEY with a personal API key from Settings > API & MCP:
```bash
claude mcp add --transport http pitchboom https://pitchboom.io/api/mcp --header "Authorization: Bearer pb_live_YOUR_KEY"
```

## Decision this list supports

You want an agent in Claude, Cursor, Codex or another MCP client to generate or edit video. This list compares the MCP servers that do it on the details that decide setup and risk: where the server runs, how it signs in, whether permissions are split, whether you see a price before you spend, and whether the agent can edit a cut rather than only generate clips.

## Scope and evidence

Documentation reviewed on 2026-09-28. This is a Wireflow-maintained resource dataset. Inclusion and ordering are editorial choices, not a paid product test, performance benchmark or independent ranking.

Every server here is published by the company that runs the video models or the product behind it. Community wrappers are left out because their setup and upkeep vary. Every cell comes from the vendor's own documentation or repository, and the Server details section links the page for each one. A check means the docs document it. A cross means the docs say it works another way. A dash means not published: the docs reviewed do not document it, which is not proof that it is absent.

The weekly repository job refreshes GitHub metadata. It does not re-check vendor features, prices or plan limits. Follow the official links for current terms.

## What each column means

- **Vendor-hosted endpoint:** the vendor runs a remote MCP URL, so there is nothing to install. The transport is in the Claude connection column of the data table.
- **OAuth sign-in:** the client connects through an OAuth sign-in instead of a pasted API key.
- **Read/run/write scope split:** the grant separates reading, running (which spends money) and changing things, so an agent can get less than full access.
- **Cost shown before a run:** a tool or response shows the price of a generation before it is spent.
- **Timeline or scene editing:** the agent can read and change the cut of a video (tracks, clips or scenes), not only generate new clips.
- **First-party server:** the vendor publishes the server itself.
- Video models covered and the docs link are in the data table and the tool entries.

## Server details

**Wireflow**

- Transport: Streamable HTTP at https://www.wireflow.ai/api/mcp. [Claude Connector (MCP)](https://www.wireflow.ai/docs/mcp)
- Auth: OAuth 2.1 authorization code flow with PKCE and dynamic client registration; no manual API key. [Claude Connector (MCP)](https://www.wireflow.ai/docs/mcp)
- Scope split: yes. Read and run scopes by default; workflows:write, automations:write and teams:invite are opt-in. [Claude Connector (MCP)](https://www.wireflow.ai/docs/mcp)
- Video models: image, video and audio models across more than 100 models; the docs name Seedance and video upscalers such as Topaz. [Claude Connector (MCP)](https://www.wireflow.ai/docs/mcp)
- Cost before a run: yes. list_models returns models with real prices, and preview_video_frames shows still frames without spending credits. [Claude Connector (MCP)](https://www.wireflow.ai/docs/mcp)
- Timeline editing: yes. get_video_timeline reads every scene and clip, and edit_video_timeline replaces the cut through a version-checked writer. [Claude Connector (MCP)](https://www.wireflow.ai/docs/mcp)
- Docs: [wireflow.ai/docs/mcp](https://www.wireflow.ai/docs/mcp)
- First-party or community: first-party. [Claude Connector (MCP)](https://www.wireflow.ai/docs/mcp)

**Flora**

- Transport: streamable HTTP at https://agents.flora.ai/mcp. [Other clients](https://developer.flora.ai/mcp/install/other-clients/)
- Auth: OAuth 2.1 with PKCE; the REST API uses separate API keys. [Authentication](https://developer.flora.ai/mcp/authentication/)
- Scope split: not published. The server receives the same permissions as the user in the connected workspace; read-only tools carry readOnlyHint and three tools carry destructiveHint. [Tools reference](https://developer.flora.ai/mcp/tools/)
- Video models: flora_create_generations starts video generations, and flora_list_models lists the models available to the account. [Tools reference](https://developer.flora.ai/mcp/tools/)
- Cost before a run: yes. flora_list_techniques returns saved Techniques with their run cost. [Tools reference](https://developer.flora.ai/mcp/tools/)
- Timeline editing: yes. flora_get_canvas_node_document reads a timeline's tracks and items, and flora_update_canvas_node_document replaces a timeline document, guarded by base_revision. [Tools reference](https://developer.flora.ai/mcp/tools/)
- Docs: [developer.flora.ai/mcp](https://developer.flora.ai/mcp/)
- First-party or community: first-party. [FLORA MCP](https://developer.flora.ai/mcp/)

**Krea**

- Transport: Streamable HTTP at https://api.krea.ai/mcp. [MCP server](https://www.krea.ai/docs/developers/mcp)
- Auth: OAuth, or an API token in an Authorization header for clients without OAuth. [MCP server](https://www.krea.ai/docs/developers/mcp)
- Scope split: not published. The consent screen binds one workspace for billing and uploads. [MCP server](https://www.krea.ai/docs/developers/mcp)
- Video models: Krea image and video models by API path, for example video/google/veo-3.1. [MCP server](https://www.krea.ai/docs/developers/mcp)
- Cost before a run: not published. [API keys and billing](https://www.krea.ai/docs/developers/api-keys-and-billing)
- Timeline editing: not published. [MCP server](https://www.krea.ai/docs/developers/mcp)
- Docs: [krea.ai/docs/developers/mcp](https://www.krea.ai/docs/developers/mcp)
- First-party or community: first-party. [MCP server](https://www.krea.ai/docs/developers/mcp)

**fal**

- Transport: Streamable HTTP at https://mcp.fal.ai/mcp. [Run MCP](https://fal.ai/docs/documentation/setting-up/mcp)
- Auth: API key in an Authorization header, or an OAuth connector sign-in. [Run MCP](https://fal.ai/docs/documentation/setting-up/mcp)
- Scope split: not published. The server uses the connected account's permissions. [Run MCP](https://fal.ai/docs/documentation/setting-up/mcp)
- Video models: over 1,000 models including image-to-video and text-to-video; the docs use Kling 3.0 in their pricing example. [Run MCP](https://fal.ai/docs/documentation/setting-up/mcp)
- Cost before a run: yes. get_pricing checks the cost of running a model before you use it. [Run MCP](https://fal.ai/docs/documentation/setting-up/mcp)
- Timeline editing: not published. [Run MCP](https://fal.ai/docs/documentation/setting-up/mcp)
- Docs: [fal.ai/docs/documentation/setting-up/mcp](https://fal.ai/docs/documentation/setting-up/mcp)
- First-party or community: first-party. [Run MCP](https://fal.ai/docs/documentation/setting-up/mcp)

**Comfy Cloud**

- Transport: Streamable HTTP at https://cloud.comfy.org/mcp, in public beta. [Comfy MCP](https://docs.comfy.org/agent-tools/mcp)
- Auth: OAuth sign-in with a Comfy account, or a Comfy Cloud API key in an X-API-Key header. [Comfy MCP](https://docs.comfy.org/agent-tools/mcp)
- Scope split: not published. [Comfy MCP](https://docs.comfy.org/agent-tools/mcp)
- Video models: ComfyUI templates and workflows, such as Wan 2.2 video templates, plus partner models such as Seedance through partner_generate. [Comfy MCP](https://docs.comfy.org/agent-tools/mcp)
- Cost before a run: not published. get_billing_status reports the credit balance and tier. [Comfy MCP](https://docs.comfy.org/agent-tools/mcp)
- Timeline editing: not published. [Comfy MCP](https://docs.comfy.org/agent-tools/mcp)
- Docs: [docs.comfy.org/agent-tools/mcp](https://docs.comfy.org/agent-tools/mcp)
- First-party or community: first-party. [Comfy MCP](https://docs.comfy.org/agent-tools/mcp)

**HeyGen**

- Transport: remote server at https://mcp.heygen.com/mcp/v1/; the docs do not name the transport type. [Overview](https://developers.heygen.com/mcp/overview)
- Auth: OAuth sign-in, no API key. [Overview](https://developers.heygen.com/mcp/overview)
- Scope split: not published. [Overview](https://developers.heygen.com/mcp/overview)
- Video models: avatar videos on the Avatar III, IV and V engines, Video Agent, templates and video translation with lip-sync. [Overview](https://developers.heygen.com/mcp/overview)
- Cost before a run: not published. Generation uses the credits in your plan. [Overview](https://developers.heygen.com/mcp/overview)
- Timeline editing: yes, at scene level. get_video_scenes returns a video's scenes, and send_video_agent_message accepts scene-scoped edit_plan changes. [Overview](https://developers.heygen.com/mcp/overview)
- Docs: [developers.heygen.com/mcp/overview](https://developers.heygen.com/mcp/overview)
- First-party or community: first-party. [Overview](https://developers.heygen.com/mcp/overview)

**Magnific**

- Transport: streamable HTTP at https://mcp.magnific.com. [Magnific MCP](https://docs.magnific.com/modelcontextprotocol)
- Auth: OAuth 2.0 with a Magnific account, no API key. [Magnific MCP](https://docs.magnific.com/modelcontextprotocol)
- Scope split: not published. [Magnific MCP](https://docs.magnific.com/modelcontextprotocol)
- Video models: video_generate, with the catalog from video_models_list and video_models_show. [Magnific MCP](https://docs.magnific.com/modelcontextprotocol)
- Cost before a run: not published. Generations cost credits by model and resolution, listed on the pricing page. [Pricing](https://docs.magnific.com/pricing)
- Timeline editing: not published. [Magnific MCP](https://docs.magnific.com/modelcontextprotocol)
- Docs: [docs.magnific.com/modelcontextprotocol](https://docs.magnific.com/modelcontextprotocol)
- First-party or community: first-party. [Magnific MCP](https://docs.magnific.com/modelcontextprotocol)

**Replicate**

- Transport: hosted server at https://mcp.replicate.com/sse over SSE, or the replicate-mcp npm package run locally. [Replicate MCP](https://mcp.replicate.com)
- Auth: the hosted connection asks you to paste a Replicate API token and approve; the local package reads REPLICATE_API_TOKEN. [Replicate MCP](https://mcp.replicate.com)
- Scope split: not published. [MCP server docs](https://replicate.com/docs/reference/mcp)
- Video models: any Replicate model through predictions, including the text-to-video collection. [Text to video collection](https://replicate.com/collections/text-to-video)
- Cost before a run: not published. [MCP server docs](https://replicate.com/docs/reference/mcp)
- Timeline editing: not published. [MCP server docs](https://replicate.com/docs/reference/mcp)
- Docs: [replicate.com/docs/reference/mcp](https://replicate.com/docs/reference/mcp)
- First-party or community: first-party, described as the official hosted MCP server for Replicate. [Replicate MCP](https://mcp.replicate.com)

**Runway**

- Transport: runs locally as a Claude Desktop extension or a stdio config entry, or as an HTTP server you deploy yourself. [README](https://github.com/runwayml/runway-api-mcp-server)
- Auth: a Runway API key, as RUNWAYML_API_SECRET locally or a Bearer header when deployed; the README says to leave OAuth fields blank. [README](https://github.com/runwayml/runway-api-mcp-server)
- Scope split: not published. [README](https://github.com/runwayml/runway-api-mcp-server)
- Video models: runway_listModels lists them; the README recommends Seedance (seedance2) for video and Aleph (aleph2) for video editing. [README](https://github.com/runwayml/runway-api-mcp-server)
- Cost before a run: not published. [README](https://github.com/runwayml/runway-api-mcp-server)
- Timeline editing: not published. runway_editVideo applies a prompt-driven edit to a whole video. [README](https://github.com/runwayml/runway-api-mcp-server)
- Docs: [github.com/runwayml/runway-api-mcp-server](https://github.com/runwayml/runway-api-mcp-server)
- First-party or community: first-party, published in the runwayml GitHub organisation. [Repository](https://github.com/runwayml/runway-api-mcp-server)

**MiniMax**

- Transport: runs locally over stdio or SSE. [README](https://github.com/MiniMax-AI/MiniMax-MCP)
- Auth: a MiniMax API key in MINIMAX_API_KEY. [README](https://github.com/MiniMax-AI/MiniMax-MCP)
- Scope split: not published. [README](https://github.com/MiniMax-AI/MiniMax-MCP)
- Video models: generate_video with MiniMax-Hailuo-02, and query_video_generation for async results. [README](https://github.com/MiniMax-AI/MiniMax-MCP)
- Cost before a run: not published. The README warns that using the tools may incur costs. [README](https://github.com/MiniMax-AI/MiniMax-MCP)
- Timeline editing: not published. [README](https://github.com/MiniMax-AI/MiniMax-MCP)
- Docs: [github.com/MiniMax-AI/MiniMax-MCP](https://github.com/MiniMax-AI/MiniMax-MCP)
- First-party or community: first-party, described as the official MiniMax MCP server. [README](https://github.com/MiniMax-AI/MiniMax-MCP)

**pitchboom**

- Transport: Streamable HTTP at https://pitchboom.io/api/mcp, stateless; initialize and tools/list answer without a key. [pitchboom MCP server](https://pitchboom.io/docs/mcp)
- Auth: a personal API key (pb_live_...) in an Authorization: Bearer header, created at Settings > API & MCP; no OAuth sign-in yet. [pitchboom MCP server](https://pitchboom.io/docs/mcp)
- Scope split: yes. Keys carry Read, Prepare & edit and Spend credits scopes, offered as Full access, No spending and Read only presets. [pitchboom MCP server](https://pitchboom.io/docs/mcp)
- Video models: no model catalog; pitchboom's own motion-design pipeline writes the script and storyboard, adds voice-over and music, and renders MP4 in 1080p, or 4K on Pro and Premium. [pitchboom MCP server](https://pitchboom.io/docs/mcp)
- Cost before a run: yes. create_project, get_estimate, request_variant and paid edits only return a quote; nothing is charged until confirm_operation or approve_storyboard after the user approves the exact amount. [pitchboom MCP server](https://pitchboom.io/docs/mcp)
- Timeline editing: yes, at scene level. get_storyboard reads the scenes, voice-over and on-screen texts, update_storyboard changes texts, order, timing and scenes before approval, and edit_video edits a rendered video. [pitchboom MCP server](https://pitchboom.io/docs/mcp)
- Docs: [pitchboom.io/docs/mcp](https://pitchboom.io/docs/mcp)
- First-party or community: first-party, published by pitchboom. [pitchboom MCP server](https://pitchboom.io/docs/mcp)

## Selection notes

For an agent that should only generate clips, any of the vendor-hosted servers works without a local install, and fal, Flora and Wireflow also show a price before the run. For an agent that assembles or revises a cut, only Wireflow, Flora and HeyGen document tools that read and change the structure of a video. Wireflow is the only server here that documents separate read, run and write scopes. Runway and MiniMax publish servers you run yourself with an API key, which suits a controlled machine more than a shared chat client.

## Acceptance recipe

1. Connect the server in the client your team uses and confirm which account and workspace it acts as.
2. List the tools and note which ones spend money before calling any of them.
3. Ask for the price of one short clip, where the server can show it, and compare it with the pricing page.
4. Generate one short clip, then poll or wait for it and download the output before any link expires.
5. If you need edits, change one scene or clip in an existing cut and confirm the change reads back.
6. Revoke the connection and confirm the agent can no longer run anything.

## Evaluation record

Record the server, client, account or workspace, model, prompt, job ID, price shown before the run, credits or money actually spent, output location and reviewer decision. Keep failed jobs next to successful ones so that a retry does not hide the original result.

## How this list is maintained

- [`data/tools.json`](data/tools.json) is the source of truth. The tables in this README are generated from it and are overwritten on every run, so edit the JSON, not the tables.
- [`scripts/update.js`](scripts/update.js) fetches star counts and latest release tags from the GitHub API for the tools that publish an official repo, stamps the check date, and regenerates the tables. `--offline` regenerates without the network; `--check` exits non-zero if the README has drifted from the data.
- [`.github/workflows/refresh.yml`](.github/workflows/refresh.yml) runs it weekly and on manual dispatch, and commits only when the data actually changed.
- Prices are deliberately not stored as numbers. A stale price in a comparison table is worse than no price, so the table links to each vendor's own pricing page.

## Contributing

Corrections and additions are welcome, including corrections to the entry for the tool that maintains this list. Open an issue with the tool name, a working link, one line on what it does that the tools already listed do not, and one line on where it stops. Entries are judged on whether they are usable today, not on popularity. Full rules in [CONTRIBUTING.md](CONTRIBUTING.md).

## License

[CC0 1.0 Universal](LICENSE), public domain. Take the data, fork the list, no attribution required.

---

Maintained by [a1adams](https://github.com/a1adams).
