# Design & Dev Tools for Claude Code

The five tools below are installed in this repo. Open the project in Claude Code and they load on their own.

| # | Tool | Source | Where it is here | How to use it |
|---|------|--------|------------------|---------------|
| 1 | **frontend-design** | [anthropics/skills](https://github.com/anthropics/skills) | `.claude/skills/frontend-design/` | Ask for a UI ("build me a landing page…") and Claude uses it automatically |
| 2 | **Web Interface Guidelines** | [vercel-labs/web-interface-guidelines](https://github.com/vercel-labs/web-interface-guidelines) | `.claude/commands/web-interface-guidelines.md` + `docs/web-interface-guidelines.md` | `/web-interface-guidelines src/**/*.tsx` to review UI code |
| 3 | **Awesome Design MD** | [VoltAgent/awesome-design-md](https://github.com/VoltAgent/awesome-design-md) | `design-systems/<brand>/DESIGN.md` (84 brands) | "Build this page in the style of `design-systems/apple/DESIGN.md`" |
| 4 | **Image to Code (Stitch skills)** | [google-labs-code/stitch-skills](https://github.com/google-labs-code/stitch-skills) | `.claude/skills/` (16 skills: `generate-design`, `react-components`, `shadcn-ui`, `design-md`, `taste-design`, …) | Needs the Stitch MCP, see below |
| 5 | **Playwright MCP** | [microsoft/playwright-mcp](https://github.com/microsoft/playwright-mcp) | `.mcp.json` | Claude can open a browser, click, take screenshots and test your page |

## Setup notes

- **Playwright MCP** needs Node.js 18+. Claude Code asks you to approve the `.mcp.json` server the first time you open the project.
- **Stitch skills** work fully only with the Stitch MCP server, which needs a Google account and an API key:
  1. Follow https://stitch.withgoogle.com/docs/mcp/setup/
  2. Add it in Claude Code: `claude mcp add stitch --transport http <YOUR_STITCH_MCP_URL>`

  Some skills, like `design-md`, `taste-design`, `enhance-prompt` and `shadcn-ui`, still help without Stitch.

## Licenses
frontend-design: see `.claude/skills/frontend-design/LICENSE.txt`, Stitch skills: Apache-2.0 (`.claude/skills/STITCH-LICENSE`), Web Interface Guidelines and Awesome Design MD: MIT (`design-systems/LICENSE`).
