# EMT Skills Marketplace

## 1. Purpose

This repository is a marketplace of agent skills that may be helpful for Emergency Medical Teams working within World Health Organization or Union Civil Protection Mechanism frameworks.

## 2. Terms of usage

This marketplace is licensed under [Attribution-NonCommercial-ShareAlike 4.0 International](LICENCE.md).

It was created and is maintained by volunteers, including people who spend their time and risk their lives so others can live. It is shared for humanitarian, preparedness, response, training, and coordination purposes. It is not meant for commercial usage.

Before using any skill operationally, review it, adapt it to your mandate and legal context, and validate it against your team's approved scope, procedures, and authorizations.

## 3. How to use it

This repository is intended to be used as a public GitHub-hosted marketplace:

- GitHub shorthand: `PMM-EMT/emt-skills-marketplace`
- Git URL: `https://github.com/PMM-EMT/emt-skills-marketplace.git`
- Web URL: `https://github.com/PMM-EMT/emt-skills-marketplace`

If your tool supports adding a remote marketplace from a public GitHub repository, prefer that route. It keeps installation and updates tied to the public source. If your tool only supports local skills or ZIP uploads, use the manual fallback for that tool.

Always review a skill before enabling it, especially if it can run scripts, install dependencies, access files, or call external services.

### Anthropic Claude and Claude Desktop

Claude and Claude Desktop support plugins in chat and, on supported plans, allow users to add plugin marketplaces from a GitHub repository or git URL.

Remote marketplace path:

1. Open Claude or Claude Desktop.
2. Open `Customize` from the left sidebar.
3. Go to `Plugins`.
4. In the personal plugins section, click `+`, then choose `Add marketplace`.
5. Choose `Add from a repository`.
6. Enter `https://github.com/PMM-EMT/emt-skills-marketplace.git` or `PMM-EMT/emt-skills-marketplace` if the UI accepts GitHub shorthand.
7. Browse the marketplace and install the skills or plugins you need.

Manual skill fallback:

1. Create a ZIP file for the skill folder. The ZIP should contain the skill folder itself at the archive root:

```bash
zip -r emt-sop-generator.zip emt-sop-generator
```

2. In Claude, enable code execution/file creation if your plan or organization settings require it.
3. Go to `Customize > Skills`.
4. Click `+`, choose `Create skill`, then choose `Upload a skill`.
5. Upload the ZIP file and toggle the skill on.

Anthropic's current help docs describe GitHub-backed plugin marketplaces for Claude and Claude Desktop, ZIP uploads for custom skills, and automatic use of enabled skills when relevant. See [Use plugins in Claude](https://support.claude.com/en/articles/13837440-use-plugins-in-claude), [Use skills in Claude](https://support.claude.com/en/articles/12512180-use-skills-in-claude), and [How to create custom Skills](https://support.claude.com/en/articles/12512198-how-to-create-custom-skills).

### Claude Code

Remote marketplace path:

```text
/plugin marketplace add PMM-EMT/emt-skills-marketplace
/plugin
```

Then open the `Discover` tab, choose this marketplace, inspect the available entries, and install the skill or plugin you need. If you prefer a full git URL, Claude Code also supports git repository URLs:

```text
/plugin marketplace add https://github.com/PMM-EMT/emt-skills-marketplace.git
```

After installing, run:

```text
/reload-plugins
```

Manual skill fallback for personal use across projects:

```bash
git clone https://github.com/PMM-EMT/emt-skills-marketplace.git
mkdir -p ~/.claude/skills
cp -R emt-skills-marketplace/emt-sop-generator ~/.claude/skills/
```

Manual skill fallback for one project:

```bash
git clone https://github.com/PMM-EMT/emt-skills-marketplace.git
mkdir -p /path/to/project/.claude/skills
cp -R emt-skills-marketplace/emt-sop-generator /path/to/project/.claude/skills/
```

Start or restart Claude Code in the target project:

```bash
cd /path/to/project
claude
```

Claude Code can load the skill automatically when the prompt matches the skill description, or you can invoke it directly with `/emt-sop-generator`. Anthropic's Claude Code docs describe adding marketplaces from GitHub repositories with `/plugin marketplace add`, installing plugins through `/plugin`, and local skills at `~/.claude/skills/<skill-name>/SKILL.md` or `.claude/skills/<skill-name>/SKILL.md`. See [Claude Code plugin marketplaces](https://code.claude.com/docs/en/discover-plugins) and [Claude Code Agent Skills](https://code.claude.com/docs/en/skills).

### OpenAI Codex

Remote marketplace path:

```bash
codex plugin marketplace add PMM-EMT/emt-skills-marketplace
codex plugin marketplace list
```

You can also pin a branch or ref:

```bash
codex plugin marketplace add PMM-EMT/emt-skills-marketplace --ref main
```

Then open the Codex plugin directory, choose this marketplace as the source, inspect the available entries, and install what you need. In Codex CLI or the IDE extension, use `/skills` or type `$` to mention a skill explicitly, for example:

```text
Use $emt-sop-generator to draft an EMT SOP in Markdown.
```

Manual skill fallback for personal use across Codex workspaces:

```bash
git clone https://github.com/PMM-EMT/emt-skills-marketplace.git
mkdir -p ~/.agents/skills
cp -R emt-skills-marketplace/emt-sop-generator ~/.agents/skills/
```

Manual skill fallback for one repository:

```bash
git clone https://github.com/PMM-EMT/emt-skills-marketplace.git
mkdir -p /path/to/project/.agents/skills
cp -R emt-skills-marketplace/emt-sop-generator /path/to/project/.agents/skills/
```

Codex can invoke a skill implicitly when the task matches its `description`. The current OpenAI Codex manual describes skills as directories with `SKILL.md`, supports Codex CLI, IDE extension, and Codex app, lists user skills at `$HOME/.agents/skills` and repository skills at `.agents/skills`, and supports adding GitHub-backed plugin marketplaces with `codex plugin marketplace add owner/repo`. See [OpenAI Codex Agent Skills](https://developers.openai.com/codex/skills.md) and [OpenAI Codex plugin marketplaces](https://developers.openai.com/codex/plugins/build.md).
