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

A **marketplace** is a collection of skills that an AI tool can browse or install from.

A **GitHub repository** is the public online folder where this marketplace is stored.

Use this public marketplace address when your AI tool asks for a repository, marketplace, or GitHub source:

```text
https://github.com/PMM-EMT/emt-skills-marketplace.git
```

Some tools also accept the shorter form:

```text
PMM-EMT/emt-skills-marketplace
```

### ✅ Recommended option

If your AI tool has an option like **Add marketplace**, **Add from GitHub**, **Add repository**, or **Install plugin from repository**, use that first.

That is usually the simplest option because the tool can connect directly to this public GitHub marketplace and keep it easier to update later.

If your tool does not offer that option, use the manual fallback described below for your tool.

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

6. Install the skill or plugin you want to use.

If you do not see an option to add a marketplace, use the manual upload option:

1. Open the repository on GitHub.
2. Click `Code`, then `Download ZIP`.
3. Unzip the downloaded file.
4. Create a ZIP file from the skill folder you want to use, for example `emt-sop-generator`. On most computers, you can right-click the folder and choose `Compress` or `Send to ZIP`.
5. In Claude, go to `Customize > Skills`.
6. Choose `Create skill` or `Upload a skill`.
7. Upload the ZIP file and turn the skill on.

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
/plugin
```

Then open the marketplace, choose the EMT skills marketplace, and install the skill or plugin you need.

If you prefer the full repository address:

```text
/plugin marketplace add https://github.com/PMM-EMT/emt-skills-marketplace.git
```

After installing, reload plugins:

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
cp -R emt-sop-generator ~/.claude/skills/
```

For one project only:

```bash
mkdir -p /path/to/project/.claude/skills
cp -R emt-sop-generator /path/to/project/.claude/skills/
```

Claude Code can use a skill automatically when your request matches the skill description. You can also ask for it by name, for example:

```text
Use the emt-sop-generator skill to draft an EMT SOP.
```

Official help pages:

- [Claude Code plugin marketplaces](https://code.claude.com/docs/en/discover-plugins)
- [Claude Code Agent Skills](https://code.claude.com/docs/en/skills)

### 🤖 OpenAI Codex

Use this if you work with OpenAI Codex.

Simplest option in Codex CLI:

```bash
codex plugin marketplace add PMM-EMT/emt-skills-marketplace
```

Then open the Codex plugin directory, choose this marketplace as the source, review what is available, and install what you need.

You can check that Codex sees the marketplace with:

```bash
codex plugin marketplace list
```

Manual fallback:

1. Download or clone this repository.
2. Open a terminal in the downloaded `emt-skills-marketplace` folder.
3. Copy the skill folder into your Codex skills folder.

For personal use across Codex workspaces:

```bash
mkdir -p ~/.agents/skills
cp -R emt-sop-generator ~/.agents/skills/
```

For one repository only:

```bash
mkdir -p /path/to/project/.agents/skills
cp -R emt-sop-generator /path/to/project/.agents/skills/
```

Codex can use a skill automatically when your request matches the skill description. You can also mention a skill directly, for example:

```text
Use $emt-sop-generator to draft an EMT SOP in Markdown.
```

Official help pages:

- [OpenAI Codex Agent Skills](https://developers.openai.com/codex/skills.md)
- [OpenAI Codex plugin marketplaces](https://developers.openai.com/codex/plugins/build.md)

### 🧭 If you are not sure what to choose

Start with your tool's **marketplace** or **GitHub repository** option.

If that does not work, use the manual fallback for your tool.

If you are supporting an EMT and are unsure whether a skill is appropriate for operational use, ask your team lead, clinical lead, information management lead, or deployment coordinator to review it before use.
