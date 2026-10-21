# Facebook–Zalo Agent

A Codex skill for preparing and carrying out user-requested Facebook posts and personal Zalo outreach. It asks for each task's purpose, source material, recipient or destination, and uses the supplied SlimAI brand voice by default. It can use another voice or sample when the user supplies one.

## Install in Codex

Use the Codex Skill Installer with this repository path:

```sh
python3 "${CODEX_HOME:-$HOME/.codex}/skills/.system/skill-installer/scripts/install-skill-from-github.py" --repo slimsoftvietnam/zalo-facebook-agent --path skills/zalo-facebook-agent
```

Or ask Codex:

```text
$skill-installer

Install the `zalo-facebook-agent` skill from `slimsoftvietnam/zalo-facebook-agent`, path `skills/zalo-facebook-agent`. Read its instructions and confirm how to invoke it. Do not perform any social media actions during installation.
```

After installation, invoke it with `$zalo-facebook-agent` and state the purpose, provide current source material, and identify the Zalo recipient or Facebook destination. The installed skill uses the SlimAI brand voice by default; provide a different voice or writing sample to override it for a task.

## Safety and task-specific inputs

The skill works through the in-app browser available in the current tool, such as Codex or Claude Code. The user signs in there. Do not provide credentials to the agent. Campaign content, products, recipients, calendars, and trackers must be supplied or identified for each task; demo data is not a standing input.
