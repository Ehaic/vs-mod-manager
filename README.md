# Vintage Story Mods: Pelican Panel plugin

Browse, install, update and remove [Vintage Story](https://www.vintagestory.at/) mods from the [ModDB](https://mods.vintagestory.at) on a game server's page in the [Pelican Panel](https://pelican.dev).

This repository only hosts the **built releases** of the plugin (`releases/`) and the update feed (`update.json`). The zips are built and published automatically from tagged versions.

## Install

In the panel: **Admin → Plugins → Import from URL**, paste the latest zip:

`https://raw.githubusercontent.com/Ehaic/vs-mod-manager/main/releases/vs-mod-manager-LATEST.zip`

(the exact file name of the current version is in [`update.json`](update.json)), then click **Install** on the plugin.

## Updates

The plugin's `update_url` points at [`update.json`](update.json). When a newer version is published, the panel shows the update icon in Admin → Plugins, and **Update** installs it (the panel verifies the sha256). From a shell: `php artisan p:plugin:update vs-mod-manager`.

## Logging

Every change and every failure is logged to the panel log (`storage/logs/laravel-*.log`) in lines that start with `vs-mod-manager:`. Turn on *Debug logging* in the plugin's settings for ModDB API timings and install steps.
