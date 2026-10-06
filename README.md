# BOSS Code Editor Tab

This plugin provides the main code-editing tabs in BOSS. It combines a desktop editor, live file tracking, language-server navigation, Markdown preview, diff views, and optional AI-assisted edits in one plugin.

This repository is a fork of [risa-labs-inc/boss-plugin-editor-tab](https://github.com/risa-labs-inc/boss-plugin-editor-tab).

## Features

- Syntax colouring for more than 50 languages
- Line numbers, code folding, bracket matching, and run-gutter actions
- Save, autosave, and external-file change handling
- Language detection and LSP navigation
- Markdown preview with Mermaid support and sanitised HTML
- Side-by-side and unified diff views
- Inline AI edits, tab completion, and reviewable suggestions
- Composer sessions that collect proposed changes before you accept them
- BOSS theme and keyboard-shortcut integration
- MCP tools for reading and editing files or live editor buffers

AI features use the optional AI Gateway and Secret Manager plugins. The editor still works when those plugins are absent.

## Requirements

- BOSS 9.5.7 or newer
- BOSS Plugin API 1.0.87 or newer
- JDK 17 for local builds

The plugin manifest is stamped from `build.gradle.kts` during the build. Change the Gradle version when preparing a release instead of editing the manifest version by hand.

## Build and test

```bash
./gradlew test
./gradlew buildPluginJar
```

The plugin JAR is written to `build/libs/`. Do not run the BOSS application as part of an automated test. Install the built JAR into BOSS and test the UI manually when needed.

## Installation

Install the released plugin from the BOSS Toolbox. For a local build, copy the generated JAR into `~/.boss/plugins/`, then start BOSS yourself.

## License

Licensed under the [Apache License, Version 2.0](LICENSE).

Copyright 2025-2026 Risa Labs Inc.
