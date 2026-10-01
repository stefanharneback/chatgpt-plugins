# ChatGPT plugins

A public source repository and plugin marketplace maintained by stefanharneback.

## Plugins

| Plugin | Skills | Version |
| --- | --- | --- |
| [Fresh Answer Modes](plugins/fresh-answer-modes/) | latest, latest-short, latest-short-nochange | 1.0.1 |

Fresh Answer Modes guides current-source checks, citations, concise answers, and read-only analysis. It uses the tools already available in the host conversation.

[Website](https://stefanharneback.github.io/chatgpt-plugins/) · [Privacy policy](https://stefanharneback.github.io/chatgpt-plugins/fresh-answer-modes/privacy.html) · [Support](https://github.com/stefanharneback/chatgpt-plugins/issues)

## Repository layout

- plugins/{plugin-name}/: one complete plugin package with its own manifest, skills, assets, and version.
- .agents/plugins/marketplace.json: shared catalog of the packaged plugins.
- docs/{plugin-name}/: public pages specific to each plugin.
- docs/index.html: catalog homepage served by GitHub Pages.

## Install from the repository marketplace

In Codex CLI (Command Line Interface):

    codex plugin marketplace add stefanharneback/chatgpt-plugins
    codex plugin add fresh-answer-modes@stefanharneback-plugins

Start a new session after installation. Public-directory distribution through OpenAI is managed separately for each plugin.

## Add another plugin

Create a new directory under plugins/ with that plugin's complete package. Give it a stable name and an independent version. Add one entry to the shared marketplace and a matching policy page under docs/. Policies must describe the actual data handling of the plugin they cover.

Package only the selected plugin directory for OpenAI upload, with its manifest at the archive root. Do not include unrelated plugins or repository files in that ZIP.

## Website

GitHub Pages publishes the docs/ folder from main. The site contains static HTML (HyperText Markup Language) and no added analytics or tracking scripts.
