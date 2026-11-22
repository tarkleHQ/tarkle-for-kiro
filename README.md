# Tarkle MCP

Tarkle is the AI platform for your business files and documents. This connector brings your Tarkle workspaces into your AI assistant, so you can find, read and deliver files from the conversation you are already in.

- MCP server: `https://mcp.tarkle.tech/mcp` (Streamable HTTP, OAuth sign-in)
- Website: https://tarkle.tech
- Docs: https://tarkle.tech/docs/mcp

## What you can do

- **Find any file.** Search the words inside PDFs, Word files and text across a workspace, then read the passage you need.
- **Get answers from your documents.** Ask a question and get an answer written from your files, with the file and page of each source.
- **Work with documents.** Convert files, run OCR, redact, compress, and merge, split or reorder PDF pages. Every edit is saved as a new file.
- **Keep files in order.** Upload, rename and move files. Files you remove go to the recovery bin and can be restored.
- **Deliver files.** Send large files with a share link, put them in a client's portal, and request files from anyone with an upload link.
- **See what happened.** Read the activity log: who viewed, downloaded, moved or shared a file, and when.

Tarkle acts as you, within your role in each workspace. It asks before it creates a public link or moves files to the bin.

## Packages

| Folder | For |
| --- | --- |
| `kiro-power/` | Kiro (Powers) |

## Setup

### Kiro

1. Open Kiro, go to **Powers**, and choose **Add Custom Power**.
2. Choose **Import power from GitHub** and enter this repository's URL, with the `kiro-power` folder. For a local copy, choose **Import power from a folder** and pick `kiro-power/`.
3. Ask Kiro something about your Tarkle files. On the first tool call a browser window opens; sign in to Tarkle and approve the connection. Kiro waits about a minute for the sign-in. If the page then says localhost refused to connect, reconnect the server in Kiro and sign in again.

### Other MCP clients

Add a remote MCP server with the URL `https://mcp.tarkle.tech/mcp`. The client opens the Tarkle sign-in on first use. No API key is needed.

- **Manus:** Settings > Connectors > Custom MCP, then add the URL above.
- **Claude, ChatGPT, Cursor, VS Code and others:** see https://tarkle.tech/docs/mcp for each client's steps.

## Privacy and support

- Privacy Policy: https://tarkle.tech/privacy
- Terms: https://tarkle.tech/terms
- Support: support@tarkle.tech or https://tarkle.tech/contact
