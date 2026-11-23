# Copilot instructions

Work tracking for this repository is Lenovo Jira Data Center, not Jira Cloud.

- Site: https://jira.tc.lenovo.com
- Project: BAIO
- Current initiative: [BAIO-261](https://jira.tc.lenovo.com/browse/BAIO-261), BizOps 25/26 - Data Source Automation Improvements - Phase 2
- Read issues through the `jiraLenovo` MCP server (`jira_get_issue`, `jira_search`). Do not use https://mcp.atlassian.com, Atlassian Cloud API tokens, or the GitHub Copilot for Jira Cloud app.
- The Jira connection is read-only. Do not create, edit, transition, or comment on issues.
- The site is on the Lenovo private network. Use it from a machine that can open https://jira.tc.lenovo.com, including a VPN. A GitHub-hosted runner cannot reach it.
- Treat issue keys such as BAIO-261 as the source of requirements, and cite the key when you use a ticket.
