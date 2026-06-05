# 🚑 EMT Skills Marketplace

## 1. Purpose

This repository is a public marketplace of AI agent skills for Emergency Medical Teams (EMTs).

The skills here may be helpful for teams working within the **World Health Organization (WHO)** Emergency Medical Team framework or the **Union Civil Protection Mechanism (UCPM)** framework. They are intended to support humanitarian preparedness, deployment, coordination, documentation, training, and field operations.

In simple terms: this is a shared library of practical AI helpers for people involved in emergency medical response.

## 2. Terms of usage

This marketplace is licensed under [Attribution-NonCommercial-ShareAlike 4.0 International](LICENCE.md).

❤️ This project was created and is maintained by volunteers for people who spend their time and risk their lives so others can live.

It is shared for humanitarian, preparedness, response, training, and coordination purposes. It is **not meant for commercial usage**.

Before using any skill in real operations:

- Check that it fits your team's mandate and approved scope.
- Adapt it to your local laws, procedures, and authorizations.
- Review the output before using it with patients, responders, authorities, or partners.
- Treat AI-generated content as support material, not as a replacement for professional judgement or command responsibility.

## 3. How to use it

### 👋 First: what is this?

A **skill** is a small package of instructions that helps an AI assistant do a specific job better.

A **plugin** is an installable package that can contain one or more skills.

A **marketplace** is a collection of plugins that Claude Code can browse or install from.

A **GitHub repository** is the public online folder where this marketplace is stored.

Use this public marketplace address when Claude Code asks for a repository, marketplace, or GitHub source:

```text
https://github.com/PMM-EMT/emt-skills-marketplace.git
```

Some tools also accept the shorter form:

```text
PMM-EMT/emt-skills-marketplace
```

### ✅ Recommended option

If Claude Code offers **Add marketplace**, **Add from GitHub**, **Add repository**, or **Install plugin from repository**, use that first.

That is usually the simplest option because Claude Code can connect directly to this public GitHub marketplace and keep it easier to update later.

If you are using Claude in the browser or Claude Desktop and do not see marketplace installation, use the manual upload option below.

### 🟣 Claude and Claude Desktop

Use this if you use Claude in the browser or the Claude Desktop app.

Simplest option:

1. Open Claude or Claude Desktop.
2. Open `Customize`.
3. Go to `Plugins`.
4. Choose `Add marketplace` or `Add from a repository`.
5. Paste this address:

```text
https://github.com/PMM-EMT/emt-skills-marketplace.git
```

6. Install the plugin you want to use.

If you do not see an option to add a marketplace, use the manual upload option:

1. Open the repository on GitHub.
2. Click `Code`, then `Download ZIP`.
3. Unzip the downloaded file.
4. Open `plugins/emt-sop-generator-plugin/skills/`.
5. Create a ZIP file from the skill folder you want to use, for example `emt-sop-generator`. On most computers, you can right-click the folder and choose `Compress` or `Send to ZIP`.
6. In Claude, go to `Customize > Skills`.
7. Choose `Create skill` or `Upload a skill`.
8. Upload the ZIP file and turn the skill on.

Claude may then use the skill automatically when your request matches what the skill is designed to do.

Official help pages:

- [Use plugins in Claude](https://support.claude.com/en/articles/13837440-use-plugins-in-claude)
- [Use skills in Claude](https://support.claude.com/en/articles/12512180-use-skills-in-claude)
- [How to create custom Skills](https://support.claude.com/en/articles/12512198-how-to-create-custom-skills)

### 🛠️ Claude Code

Use this if you work with Claude Code in a terminal or code editor.

Simplest option inside Claude Code:

```text
/plugin marketplace add PMM-EMT/emt-skills-marketplace
/plugin install emt-sop-generator-plugin@emt-skills-marketplace
```

After installation, call the skill with its plugin name:

```text
/emt-sop-generator-plugin:emt-sop-generator
```

If you prefer the full repository address:

```text
/plugin marketplace add https://github.com/PMM-EMT/emt-skills-marketplace.git
```

After installing, reload plugins if Claude Code does not show the new plugin immediately:

```text
/reload-plugins
```

Manual fallback:

1. Download or clone this repository.
2. Open a terminal in the downloaded `emt-skills-marketplace` folder.
3. Copy the skill folder into your Claude Code skills folder.

For personal use across all projects:

```bash
mkdir -p ~/.claude/skills
cp -R plugins/emt-sop-generator-plugin/skills/emt-sop-generator ~/.claude/skills/
```

For one project only:

```bash
mkdir -p /path/to/project/.claude/skills
cp -R plugins/emt-sop-generator-plugin/skills/emt-sop-generator /path/to/project/.claude/skills/
```

Claude Code can use a skill automatically when your request matches the skill description. You can also ask for it by name, for example:

```text
Use the emt-sop-generator skill to draft an EMT SOP.
```

For maintainers, validate the marketplace and plugin before release:

```bash
claude plugin validate .
claude plugin validate ./plugins/emt-sop-generator-plugin
```

The plugin uses a semantic version in `plugin.json`. Bump that version whenever releasing plugin changes so existing users receive updates.

Official help pages:

- [Claude Code plugin marketplaces](https://code.claude.com/docs/en/discover-plugins)
- [Claude Code Agent Skills](https://code.claude.com/docs/en/skills)

### 🧭 If you are not sure what to choose

Start with Claude Code's **marketplace** or **GitHub repository** option.

If that does not work, use the manual upload fallback for Claude or Claude Desktop.

If you are supporting an EMT and are unsure whether a skill is appropriate for operational use, ask your team lead, clinical lead, information management lead, or deployment coordinator to review it before use.
