# Chedam releases

Signed update packages for Chedam store hubs. Hubs read `stable/channel.json` and download the package it names.

- `stable/channel.json` (+ `.sig`): the latest version and recent history.
- `packages/chedam-app-<version>.tar.gz` (+ `.sig`): the app update (hub code, schema migrations, app files).

Every file is signed with Ed25519. A hub installs a package only when its signature matches the public key built into the hub, and it rolls back on its own if the new version does not come up healthy.

This repository holds release files only. The source code is private.
