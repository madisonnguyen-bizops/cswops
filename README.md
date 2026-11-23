# cswops

GitHub Copilot reads Lenovo Jira Data Center at https://jira.tc.lenovo.com. That site is not Jira Cloud, so the Atlassian Rovo connector and the GitHub Copilot for Jira app do not apply.

## One-time setup

1. In Jira, open your avatar, then **Profile**, then **Personal Access Tokens**, and create a token. Copy it once. Data Center tokens are not created at id.atlassian.com.
2. Install [uv](https://docs.astral.sh/uv/getting-started/installation/) so `uvx` is on your PATH.
3. Set `JIRA_PERSONAL_TOKEN` in the environment of the machine where Copilot runs. Do not commit the token and do not paste it into chat.
4. Open this repository in VS Code with GitHub Copilot, or start Copilot CLI from the repository root, and trust the folder.
5. Ask Copilot: "Use jiraLenovo to fetch BAIO-261. Do not change the ticket." Confirm the reply comes from that tool result.

Copilot reads `.mcp.json`. The server is `jiraLenovo` (`uvx mcp-atlassian`), limited to the BAIO project, with `READ_ONLY_MODE=true`.

`jira.tc.lenovo.com` is on the Lenovo private network. Run Copilot on a machine that can open that site. GitHub-hosted Copilot cloud agent cannot reach it.

If the server fails with a certificate error from a corporate proxy, set `JIRA_SSL_VERIFY` only after you know the certificate is your company CA. Leave verification on otherwise.
