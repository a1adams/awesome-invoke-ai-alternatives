# InvokeAI alternatives for local editing and hosted production

A maintained dataset of **invoke ai alternatives** options: what each one connects to, where it stops, how to run it, and a link to the vendor's own pricing page rather than a price that will be wrong by the time you read it.

1. **[InvokeAI](https://invoke.ai)**
2. **[ComfyUI](https://www.comfy.org)**
3. **[Wireflow](https://www.wireflow.ai)**
4. **[Krea AI](https://www.krea.ai)**
5. **[Flora AI](https://flora.ai)**
6. **[fal](https://fal.ai)**

The tables below are generated from [`data/tools.json`](data/tools.json). Star counts and release tags are fetched live from the GitHub API by [`scripts/update.js`](scripts/update.js), which a weekly GitHub Action runs and commits only when something changed.

<!-- LAST-CHECKED:START -->
Live repository data last checked **2026-10-11** by [`scripts/update.js`](scripts/update.js), which runs weekly via GitHub Actions.
<!-- LAST-CHECKED:END -->

Maintained by [a1adams](https://github.com/a1adams). Corrections are welcome, see [CONTRIBUTING.md](CONTRIBUTING.md).

## Contents

- [The data](#the-data)
- [Capability scores](#capability-scores)
- [The tools](#the-tools)
  - [InvokeAI](#1-invokeai)
  - [ComfyUI](#2-comfyui)
  - [Wireflow](#3-wireflow)
  - [Krea AI](#4-krea-ai)
  - [Flora AI](#5-flora-ai)
  - [fal](#6-fal)
- [Decision this list supports](#decision-this-list-supports)
- [Scope and evidence](#scope-and-evidence)
- [Selection notes](#selection-notes)
- [Acceptance recipe](#acceptance-recipe)
- [Evaluation record](#evaluation-record)
- [How this list is maintained](#how-this-list-is-maintained)
- [Contributing](#contributing)
- [License](#license)

## The data

One row per tool, one column per thing people actually check before committing. Columns with nothing verified behind them are dropped rather than filled with guesses.

<!-- DATA-TABLE:START -->
| Tool | Claude connection | REST API | Free tier | Model support | Pricing | Open-source SDK / MCP |
|---|---|---|---|---|---|---|
| **[InvokeAI](#1-invokeai)** | n/a | n/a | n/a | Image operations; see documented model and format support | n/a | [invoke-ai/InvokeAI](https://github.com/invoke-ai/InvokeAI), 28,547 ★, v6.14.2 |
| **[ComfyUI](#2-comfyui)** | n/a | Yes | n/a | Image and video operations; model coverage varies | n/a | [Comfy-Org/ComfyUI](https://github.com/Comfy-Org/ComfyUI), 136,818 ★, v0.39.0 |
| **[Wireflow](#3-wireflow)** | Hosted MCP; see official connector setup | Yes | [check](https://www.wireflow.ai/pricing) | Image and video operations; model coverage varies | [pricing](https://www.wireflow.ai/pricing) | n/a |
| **[Krea AI](#4-krea-ai)** | n/a | Yes | n/a | Image and video operations; model coverage varies | n/a | n/a |
| **[Flora AI](#5-flora-ai)** | Hosted MCP with OAuth | Yes | n/a | Image and video operations; model coverage varies | n/a | n/a |
| **[fal](#6-fal)** | n/a | Yes | n/a | Image and video operations; model coverage varies | n/a | n/a |
<!-- DATA-TABLE:END -->

## Capability scores

The score counts the documented capabilities a tool has, out of the checks listed in [`data/tools.json`](data/tools.json) under `capabilityChecks`. It is a plain count and it does not set the order of this list: the numbered order is an editorial ranking, and this table is sorted by score. The checks and every answer are in the file, so each cell can be checked. Disagree with a cell? Open an issue naming the tool, the check and the evidence.

<!-- CAPABILITY-SCORES:START -->
| Tool | Self-hosted runtime | Visual graph | REST API | Image tools | Score |
|------|---|---|---|---|-------|
| **[ComfyUI](#2-comfyui)** | ✅ | ✅ | ✅ | ✅ | **4/4** |
| **[InvokeAI](#1-invokeai)** | ✅ | ✅ | n/a | ✅ | **3/4** |
| **[Wireflow](#3-wireflow)** | n/a | ✅ | ✅ | ✅ | **3/4** |
| **[Krea AI](#4-krea-ai)** | n/a | ✅ | ✅ | ✅ | **3/4** |
| **[Flora AI](#5-flora-ai)** | n/a | ✅ | ✅ | ✅ | **3/4** |
| **[fal](#6-fal)** | n/a | n/a | ✅ | ✅ | **2/4** |
<!-- CAPABILITY-SCORES:END -->

## The tools

### 1. InvokeAI

![InvokeAI screenshot](https://assets.wireflow.ai/competitors/invokeai-652425592f46.png?v=r5)

- **What it is:** A downloadable visual image-creation environment with canvas and workflow tools.
- **Limits:** Installation, model compatibility and hardware are part of the operating work.
- **Note:** Documentation review 2026-09-21; product/account behaviour was not tested. The local edition is distinct from commercial hosted offerings. Review the project licence and model licences for your use.
- **Links:**
  - [Homepage](https://invoke.ai)
  - [Docs](https://github.com/invoke-ai/InvokeAI)

Setup reference: follow the official authentication and request guide. This is a documentation URL, not an executed API example.
```text
https://github.com/invoke-ai/InvokeAI
```

### 2. ComfyUI

![ComfyUI screenshot](https://assets.wireflow.ai/competitors/comfyui-95a2ddf92942.png?v=r5)

- **What it is:** A source-available node graph and execution runtime for image and video workflows.
- **Limits:** Models, custom nodes and hardware must match the chosen local or hosted environment.
- **Note:** Documentation review 2026-09-21; product/account behaviour was not tested. ComfyUI has both local and hosted routes. Downloadable software does not make GPU use, hosted services or every model licence free.
- **Links:**
  - [Homepage](https://www.comfy.org)
  - [Docs](https://docs.comfy.org)
  - [Comfy-Org/ComfyUI](https://github.com/Comfy-Org/ComfyUI)
  - [Official source 2](https://github.com/Comfy-Org/docs/blob/main/openapi-v2.yaml)

Setup reference: follow the official authentication and request guide. This is a documentation URL, not an executed API example.
```text
https://docs.comfy.org
```

### 3. Wireflow

![Wireflow screenshot](https://assets.wireflow.ai/competitors/wireflow-70f47ccd9660.png?v=r5)

- **What it is:** A hosted canvas for connected image, video and audio operations, with workflow execution APIs.
- **Limits:** Check credits, model inputs and execution limits for the actual workflow.
- **Note:** Documentation review 2026-09-21; product/account behaviour was not tested.
- **Links:**
  - [Homepage](https://www.wireflow.ai)
  - [Wireflow best node based AI workflow platform page](https://www.wireflow.ai/features/best-node-based-ai-workflow-platform)
  - [Docs](https://www.wireflow.ai/docs)
  - [Pricing](https://www.wireflow.ai/pricing)
  - [Official source 1](https://www.wireflow.ai/docs/creating-workflows)
  - [Official source 2](https://www.wireflow.ai/docs/api/run)
  - [Official source 3](https://www.wireflow.ai/docs/mcp)
  - [Official source 4](https://www.wireflow.ai/docs/batch-image-generation)

Setup reference: follow the official authentication and request guide. This is a documentation URL, not an executed API example.
```text
https://www.wireflow.ai/docs
```

### 4. Krea AI

![Krea AI screenshot](https://assets.wireflow.ai/competitors/krea-ai-bfc62405e654.png?v=r5)

- **What it is:** Creative model APIs alongside a Nodes canvas for image, video and audio workflows.
- **Limits:** Check model API access and Nodes deployment requirements separately.
- **Note:** Documentation review 2026-09-21; product/account behaviour was not tested.
- **Links:**
  - [Homepage](https://www.krea.ai)
  - [Docs](https://www.krea.ai/docs/developers/introduction)
  - [Official source 2](https://www.krea.ai/docs/user-guide/features/nodes)
  - [Official source 3](https://www.krea.ai/docs/api-reference/node-apps/execute-a-node-app)
  - [Official source 4](https://www.krea.ai/docs/api-reference/image-enhance/krea-enhance)

Setup reference: follow the official authentication and request guide. This is a documentation URL, not an executed API example.
```text
https://www.krea.ai/docs/developers/introduction
```

### 5. Flora AI

![Flora AI screenshot](https://assets.wireflow.ai/competitors/flora-2cd907d1b38c.png?v=r5)

- **What it is:** A creative canvas with reusable Techniques, API access and a hosted MCP interface.
- **Limits:** A saved Technique must expose suitable inputs; check billing and account access before running it.
- **Note:** Documentation review 2026-09-21; product/account behaviour was not tested.
- **Links:**
  - [Homepage](https://flora.ai)
  - [Docs](https://developer.flora.ai/api/)
  - [Official source 2](https://developer.flora.ai/mcp/)
  - [Official source 3](https://developer.flora.ai/quickstarts/cli/)

Official CLI installation; this installs software but submits no generation:
```bash
go install github.com/florafauna-ai/flora-cli/cmd/flora@latest
```

### 6. fal

![fal screenshot](https://assets.wireflow.ai/competitors/fal-ai-0ec799965278.png?v=r5)

- **What it is:** Model APIs and deployment tools for generated media.
- **Limits:** Each endpoint has its own input schema, pricing and concurrency behaviour.
- **Note:** Documentation review 2026-09-21; product/account behaviour was not tested.
- **Links:**
  - [Homepage](https://fal.ai)
  - [Docs](https://fal.ai/docs/documentation)
  - [Official source 2](https://fal.ai/docs/documentation/quickstart)

Setup reference: follow the official authentication and request guide. This is a documentation URL, not an executed API example.
```text
https://fal.ai/docs/documentation
```

## Decision this list supports

An InvokeAI migration changes more than the image model. Decide how much local control, canvas editing and infrastructure ownership the next system must preserve.

## Scope and evidence

Documentation reviewed on 2026-09-21. This is a Wireflow-maintained resource dataset. Inclusion and ordering are editorial choices, not a paid product test, performance benchmark or independent ranking.

The capability score counts positively documented checks. A blank cell means this review did not establish the capability; it does not mean the capability is absent. Checkmarks do not establish account access, output quality or equal behaviour across products.

The weekly repository job refreshes GitHub metadata. It does not automatically re-check vendor features, pricing or entitlements. Follow the official links for current terms.

## Selection notes

ComfyUI is relevant for another local graph; hosted canvases change the maintenance tradeoff. fal is an API building block when the surrounding application supplies the editor and process.

## Acceptance recipe

1. Record the current model, references, masks and any custom workflow dependencies.
2. Separate non-negotiable local processing from preferences about the interface.
3. Recreate a regional edit and compare untouched areas at the output resolution.
4. Measure installation or hosting work alongside generation time.
5. Export the final file and verify its dimensions, colour and naming requirements.
6. Keep the original local project until the replacement handles a second real input.

## Evaluation record

Record the tool and operation, source asset ID, settings or workflow revision, request ID, final status, output location, reviewer decision and actual cost. Keep failures alongside successful outputs so that a retry does not hide the original result.

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
