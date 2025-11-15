# Label Organization Guide

## Label Categories
| Label Name | Category | Description |
|------------|----------|-------------|
| bug | issue-type | Something isn't working |
| documentation | issue-type | Improvements or additions to documentation |
| enhancement | issue-type | New feature or request |
| question | issue-type | Further information is requested |
| good first issue | community | Good for newcomers |
| help wanted | community | Extra attention is needed |
| duplicate | status | This issue or pull request already exists |
| invalid | status | This doesn't seem right |
| wontfix | status | This will not be worked on |
| has repro | status | A reproducible case has been provided or confirmed |
| external | status | Issue depends on or is blocked by external systems/tools |
| area:core | area | Core functionality of the project |
| area:tools | area | Internal tooling and agent/tools framework |
| area:tui | area | Terminal UI, interactive interface, and input handling |
| area:ide | area | IDE integration (VS Code, IntelliJ, Cursor, etc.) |
| area:model | area | Model behavior, prompting, and inference issues |
| area:mcp | area | Model Context Protocol (MCP) servers and integrations |
| area:security | area | Security, permissions, sandboxing, and policy concerns |
| area:packaging | area | Packaging, installation, update, and distribution |
| area:auth | area | Authentication, credentials, and key management |
| area:api | area | API requests, serialization, transport, and protocol |
| platform:macos | platform | macOS-specific behavior or compatibility |
| platform:linux | platform | Linux-specific behavior or compatibility |
| platform:windows | platform | Windows-specific behavior or compatibility |
| memory | performance | Memory-related behavior or resource usage |
| perf:memory | performance | Performance label specifically focused on memory usage |

## Usage Guidelines
- issue-type labels (bug, enhancement, documentation, question):
  - Apply exactly one that best represents the nature of the issue or PR.
  - Use "bug" for defects, "enhancement" for feature work, "documentation" for docs-only changes, and "question" for information requests.
- status labels (duplicate, invalid, wontfix, has repro, external):
  - Use to clarify triage state and lifecycle. For example, add "has repro" after a reproducible case is confirmed; use "external" when blocked by third-party tools or services; mark "duplicate" or "invalid" during triage; add "wontfix" when the team decides not to act.
- area labels (area:*):
  - Add one or more to indicate the functional domain affected (core, tools, tui, ide, model, mcp, security, packaging, auth, api). Prefer adding multiple area labels if the change spans subsystems.
- platform labels (platform:*):
  - Apply when the issue or change is platform-specific. If cross-platform, omit or add multiple platforms if specific behaviors differ.
- performance labels (memory, perf:memory):
  - Use when behavior or work relates to resource usage or performance, especially memory footprint or leaks.
- community labels (good first issue, help wanted):
  - Use on issues suitable for new contributors or where maintainers would appreciate extra help. Avoid applying to PRs unless the PR continues an initiative marked for community help.

Consistent use:
- Prefer adding area and platform labels in addition to a single primary issue-type label for clearer filtering.
- Keep status labels in sync with triage decisions and resolution.
- Review labels during PR review to ensure they reflect the scope accurately.