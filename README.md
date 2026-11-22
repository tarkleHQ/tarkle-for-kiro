# Tarkle for Kiro

<img src="kiro-power/assets/logo.png" alt="Tarkle" width="64" height="64">

Tarkle is AI-powered storage for business files. Teams keep their working files there: product specs, client briefs, brand assets, exports, reports and project handoffs. The Tarkle power brings those files into Kiro, so you can find, read and deliver them without leaving your editor.

- MCP server: `https://mcp.tarkle.tech/mcp` (Streamable HTTP, OAuth sign-in, no API key)
- Website: https://tarkle.tech
- Docs: https://tarkle.tech/docs/mcp

## What you can do

- **Find any file.** Search the words inside PDFs, Word files and text across a workspace, then read the passage you need into your session.
- **Get answers from your files.** Ask a question and get an answer written from your files, with the file and page of each source.
- **Work with documents.** Convert files, run OCR, redact, compress, and merge, split or reorder PDF pages. Every edit is saved as a new file.
- **Keep files in order.** Upload, rename and move files. Files you remove go to the recovery bin and can be restored.
- **Deliver files.** Send a build, an export or a report with a share link, put it in a client's portal, or ask a client for missing files with an upload link.
- **See what happened.** Read the activity log: who viewed, downloaded, moved or shared a file, and when.

Kiro acts as you, within your role in each workspace. It asks before it creates a public link or moves files to the bin.

## Install in Kiro

1. Open Kiro, go to **Powers**, and choose **Add Custom Power**.
2. Choose **Import power from GitHub** and enter `https://github.com/tarkleHQ/tarkle-for-kiro/tree/main/kiro-power`. From a local copy, choose **Import power from a folder** and pick `kiro-power/`.
3. Ask Kiro something about your Tarkle files, for example "List my Tarkle workspaces". On the first tool call a browser tab opens. Sign in to Tarkle and approve the connection.

Kiro waits about a minute for the sign-in. Sign in to https://tarkle.tech first so the approval takes one click. If the tab says localhost refused to connect, the wait ran out: reconnect the server in Kiro and sign in again with the new link.

### Kiro CLI

```bash
kiro-cli powers install ./kiro-power
```

Or add the server on its own:

```bash
kiro-cli mcp add --name tarkle --url https://mcp.tarkle.tech/mcp --scope global --timeout 300000
```

### Other MCP clients

Add a remote MCP server with the URL `https://mcp.tarkle.tech/mcp`. The client opens the Tarkle sign-in on first use. Steps for Claude, ChatGPT, Cursor and VS Code are at https://tarkle.tech/docs/mcp.

## Contents

| Path | What it is |
| --- | --- |
| `kiro-power/plugin.json` | Power manifest: name, description, keywords |
| `kiro-power/mcp.json` | The Tarkle MCP server connection |
| `kiro-power/skills/tarkle/SKILL.md` | How Kiro uses Tarkle's tools |
| `kiro-power/assets/logo.svg`, `logo.png` | Tarkle logo (SVG, and PNG at 816 x 816) |

## Privacy and support

- Privacy Policy: https://tarkle.tech/privacy
- Terms: https://tarkle.tech/terms
- Support: support@tarkle.tech or https://tarkle.tech/contact

## License

Apache License 2.0. See [LICENSE](LICENSE).
