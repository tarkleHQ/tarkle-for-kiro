# Tarkle for Kiro

<img src="assets/logo.png" alt="Tarkle" width="64" height="64">

**Upload, manage and share your business files.**

Upload, store and manage your team's files and folders from Kiro. Share builds, exports and reports, and request documents from your team, clients and partners on your own domain, without leaving your editor.

- MCP server: `https://mcp.tarkle.tech/mcp` (Streamable HTTP, OAuth sign-in, no API key)
- Website: https://tarkle.tech
- Docs: https://tarkle.tech/docs/mcp

## What you can do

- **Manage files and folders.** Upload files from your project, organize them in folders and team folders, rename, move, copy and tag them, and restore an earlier version (Pro) or a file from the recovery bin.
- **Share files.** Share a build, an export or a report with a link, and see the links you already shared.
- **Request documents.** Ask your team, clients or partners for files with an upload link, and see what they sent.
- **Work with clients.** Keep contacts in one place and put files in a client's portal.
- **Run your workspace.** Create a workspace, change its settings, logo and address, connect your own domain, manage members and invitations, and read the activity log.
- **Find files.** Search the words inside files across a workspace and read the passage you need into your session.

Kiro acts as you, within your role in each workspace. It asks before it creates a public link or file request, moves files to the bin, or changes workspace settings, members, invitations, domains or portal access. A workspace owner can turn off groups of actions for AI agents and hide folders from them.

## Install in Kiro

1. Open Kiro, go to **Powers**, and choose **Add Custom Power**. On Kiro web (app.kiro.dev), open **Settings > Powers & MCP > Upload folder** and choose the `tarkle` folder from a copy of this repository.
2. Choose **Import power from GitHub** and enter `https://github.com/tarkleHQ/tarkle-for-kiro/tree/main/tarkle`. From a local copy, choose **Import power from a folder** and pick `tarkle/`.
3. Ask Kiro something about your Tarkle files, for example "List my Tarkle workspaces". On the first tool call a browser tab opens. Sign in to Tarkle and approve the connection.

Kiro waits about a minute for the sign-in. Sign in to https://tarkle.tech first so the approval takes one click. If the tab says localhost refused to connect, the wait ran out: reconnect the server in Kiro and sign in again with the new link.

### Kiro CLI

```bash
kiro-cli powers install ./tarkle
```

Or add the server on its own:

```bash
kiro-cli mcp add --name tarkle --url https://mcp.tarkle.tech/mcp --scope global --timeout 300000
```

### Other MCP clients

Add a remote MCP server with the URL `https://mcp.tarkle.tech/mcp`. The client opens the Tarkle sign-in on first use. Steps for Claude, ChatGPT, Cursor and VS Code are at https://tarkle.tech/docs/mcp.

## Tools

The table lists the 102 tools of the Tarkle MCP server. The power connects to Tarkle's hosted server, so Kiro gets the tools that server offers at the time: ask Kiro to list the Tarkle tools to see them. Which ones a person can use depends on their role in each workspace and on what the workspace owner allows AI agents to do.

| Area | Tools |
| --- | --- |
| Account and workspaces | `tarkle_whoami`, `tarkle_list_workspaces`, `tarkle_get_usage`, `tarkle_list_regions`, `tarkle_create_workspace`, `tarkle_check_workspace_url`, `tarkle_set_workspace_url`, `tarkle_get_workspace_settings`, `tarkle_update_workspace_settings`, `tarkle_set_workspace_logo`, `tarkle_connect_workspace_domain`, `tarkle_check_workspace_domain`, `tarkle_remove_workspace_domain`, `tarkle_get_organization`, `tarkle_update_organization`, `tarkle_set_organization_logo` |
| Find and read | `tarkle_list_files`, `tarkle_list_folders`, `tarkle_search_files`, `tarkle_read_file`, `tarkle_get_download_link`, `tarkle_get_activity`, `tarkle_get_received_emails` |
| Answers and data | `tarkle_ask`, `tarkle_extract_data`, `tarkle_get_extraction`, `tarkle_split_document` |
| Add files | `tarkle_upload_text`, `tarkle_upload_file`, `tarkle_upload_from_url`, `tarkle_start_upload`, `tarkle_get_upload_parts`, `tarkle_get_upload_status`, `tarkle_get_upload_page` |
| Documents | `tarkle_create_document`, `tarkle_fill_template`, `tarkle_edit_office_file`, `tarkle_edit_pdf`, `tarkle_convert_file` |
| Organize | `tarkle_create_folder`, `tarkle_rename_file`, `tarkle_move_file`, `tarkle_copy_file`, `tarkle_rename_folder`, `tarkle_move_folder`, `tarkle_list_versions`, `tarkle_restore_version`, `tarkle_delete_files`, `tarkle_list_bin`, `tarkle_restore_from_bin` |
| Tags and descriptions | `tarkle_update_details`, `tarkle_list_tags`, `tarkle_rename_tag`, `tarkle_delete_tag` |
| Share links and galleries | `tarkle_create_transfer`, `tarkle_list_transfers`, `tarkle_update_transfer`, `tarkle_deliver_transfer_to_contacts`, `tarkle_create_gallery`, `tarkle_get_gallery_status` |
| File requests | `tarkle_create_file_request`, `tarkle_list_file_requests`, `tarkle_get_file_request_submissions`, `tarkle_close_file_request`, `tarkle_reopen_file_request`, `tarkle_delete_file_request` |
| Contacts and client portal | `tarkle_list_contacts`, `tarkle_create_contact`, `tarkle_update_contact`, `tarkle_add_contact_to_organization`, `tarkle_set_portal_access`, `tarkle_resend_portal_invite`, `tarkle_set_portal_storage_limit` |
| People and teams | `tarkle_list_members`, `tarkle_list_roles`, `tarkle_invite_member`, `tarkle_change_member_role`, `tarkle_remove_member`, `tarkle_list_invitations`, `tarkle_resend_invitation`, `tarkle_cancel_invitation`, `tarkle_list_team_folders`, `tarkle_create_team_folder`, `tarkle_add_member_to_team_folder`, `tarkle_remove_member_from_team_folder`, `tarkle_set_team_folder_budget` |
| Brand pages | `tarkle_list_brands`, `tarkle_get_brand`, `tarkle_create_brand`, `tarkle_update_brand`, `tarkle_import_brand_file`, `tarkle_lookup_brand_domain`, `tarkle_connect_brand_domain`, `tarkle_check_brand_domain`, `tarkle_disconnect_brand_domain` |
| Webhooks | `tarkle_list_webhooks`, `tarkle_create_webhook`, `tarkle_update_webhook`, `tarkle_delete_webhook`, `tarkle_test_webhook`, `tarkle_get_webhook_deliveries` |
| Feedback to Tarkle | `tarkle_report_feedback` |

## Contents

| Path | What it is |
| --- | --- |
| `tarkle/POWER.md` | Power instructions and metadata (Kiro web, IDE and CLI) |
| `tarkle/plugin.json` | Power manifest: name, description, keywords |
| `tarkle/mcp.json` | The Tarkle MCP server connection |
| `tarkle/skills/tarkle/SKILL.md` | How Kiro uses Tarkle's tools |
| `assets/logo.svg`, `assets/logo.png` | Tarkle logo (SVG, and PNG at 816 x 816) |

## Privacy and support

- Privacy Policy: https://tarkle.tech/privacy
- Terms: https://tarkle.tech/terms
- Support: support@tarkle.tech or https://tarkle.tech/contact

## License

Apache License 2.0. See [LICENSE](LICENSE).
