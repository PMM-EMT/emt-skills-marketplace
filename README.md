# EMT Skills Marketplace

## 1. Purpose

This repository is a marketplace of agent skills that may be helpful for Emergency Medical Teams working within World Health Organization or Union Civil Protection Mechanism frameworks.

## 2. Terms of usage

This marketplace is licensed under [Attribution-NonCommercial-ShareAlike 4.0 International](LICENCE.md).

It was created and is maintained by volunteers, including people who spend their time and risk their lives so others can live. It is shared for humanitarian, preparedness, response, training, and coordination purposes. It is not meant for commercial usage.

Before using any skill operationally, review it, adapt it to your mandate and legal context, and validate it against your team's approved scope, procedures, and authorizations.

## 3. How to use it

Clone or download this repository first:

```bash
git clone https://github.com/PMM-EMT/emt-skills-marketplace.git
cd emt-skills-marketplace
```

Each skill is stored as a folder containing a `SKILL.md` file and optional supporting files such as references, scripts, or platform metadata.

### Anthropic Claude

Use this path for Claude in the web app and the standard Claude chat experience.

1. Create a ZIP file for the skill folder. The ZIP should contain the skill folder itself at the archive root:

```bash
zip -r emt-sop-generator.zip emt-sop-generator
```

2. In Claude, enable code execution/file creation if your plan or organization settings require it.
3. Go to `Customize > Skills`.
4. Click `+`, choose `Create skill`, then choose `Upload a skill`.
5. Upload the ZIP file and toggle the skill on.

Anthropic's current help docs describe custom skills as ZIP-uploaded skill folders and note that Claude uses enabled skills automatically when relevant. See [Use skills in Claude](https://support.claude.com/en/articles/12512180-use-skills-in-claude) and [How to create custom Skills](https://support.claude.com/en/articles/12512198-how-to-create-custom-skills).

### Claude Desktop

Use the same Claude Skills flow in Claude Desktop:

1. Open Claude Desktop.
2. Click `Customize` in the left sidebar.
3. Open `Skills`, then use the `+` button.
4. Upload the skill ZIP as described above, or browse/install skills available to your organization.

Anthropic's directory docs state that the unified directory is available from Claude or Claude Desktop via `Customize`, and that installed skills appear under `Customize > Skills`. See [Browse skills, connectors, and plugins in one directory](https://support.claude.com/en/articles/14328846-browse-skills-connectors-and-plugins-in-one-directory).

### Claude Code

For personal use across projects, copy a skill into your Claude Code personal skills folder:

```bash
mkdir -p ~/.claude/skills
cp -R emt-sop-generator ~/.claude/skills/
```

For one project, copy it into that project's skills folder:

```bash
mkdir -p /path/to/project/.claude/skills
cp -R emt-sop-generator /path/to/project/.claude/skills/
```

Start or restart Claude Code in the target project:

```bash
cd /path/to/project
claude
```

Claude Code can load the skill automatically when the prompt matches the skill description, or you can invoke it directly with `/emt-sop-generator`. Anthropic's Claude Code docs list personal skills at `~/.claude/skills/<skill-name>/SKILL.md` and project skills at `.claude/skills/<skill-name>/SKILL.md`. See [Claude Code Agent Skills](https://code.claude.com/docs/en/skills).

### OpenAI Codex

For personal use across Codex workspaces, copy a skill into your Codex user skills folder:

```bash
mkdir -p ~/.agents/skills
cp -R emt-sop-generator ~/.agents/skills/
```

For one repository, copy it into that repository's skills folder:

```bash
mkdir -p /path/to/project/.agents/skills
cp -R emt-sop-generator /path/to/project/.agents/skills/
```

Start or restart Codex in the target project. In Codex CLI or the IDE extension, use `/skills` or type `$` to mention a skill explicitly, for example:

```text
Use $emt-sop-generator to draft an EMT SOP in Markdown.
```

Codex can also invoke a skill implicitly when the task matches its `description`. The current OpenAI Codex manual describes skills as directories with `SKILL.md`, supports Codex CLI, IDE extension, and Codex app, and lists user skills at `$HOME/.agents/skills` and repository skills at `.agents/skills`. See [OpenAI Codex Agent Skills](https://developers.openai.com/codex/skills.md).
