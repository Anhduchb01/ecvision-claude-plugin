<!-- DRAFT v0.1: wording not yet approved (ask_team). Remove this line before any submission. -->

# ecvision-claude-plugin

Claude plugin for [ecvision](https://ecvision.ai): competitor intelligence for Shopify stores. It adds five skills that turn ecvision's daily readings of your store and the rivals you track into answers Claude can give, each with its source and the date it was read.

This repository is a read-only mirror. The source lives in ecvision's private repository, and changes are published here when a version is released. Please do not open pull requests.

## Install

In Claude Code:

```
/plugin install ecvision --marketplace Anhduchb01/ecvision-claude-plugin
```

In Claude (web, desktop or mobile), add the plugin from **Customize > Plugins**, then connect the **ecvision** connector when asked and sign in with your ecvision account.

## What is inside

```
.claude-plugin/marketplace.json   the marketplace that lists the plugin
plugins/ecvision/                 the plugin: manifest, connector reference, five skills
```

See [`plugins/ecvision/README.md`](plugins/ecvision/README.md) for what each skill does, what data the plugin sends, and its limits.

## Requirements

An ecvision account with competitors set up. The plugin is read-only: it never writes to or changes anything in your workspace.
