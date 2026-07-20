# Thunderbird Mobile Components l10n

This repository contains the Thunderbird Mobile Components localization file tree used by Weblate.

The repository root mirrors localization-relevant paths from the source repository. Shared import and Weblate
management tooling is provided by the `weblate/` submodule. Project-specific tooling settings live in
`l10n-config.json`.

## Tooling

Initialize the tooling submodule after cloning:

```bash
git submodule update --init --recursive
```

Run the import using the source repository and branch train configured in `l10n-config.json`:

```bash
./weblate/scripts/sync import
```

Run Weblate management in dry-run mode:

```bash
./weblate/scripts/weblate update --token "$WEBLATE_TOKEN"
```

Update the tooling submodule manually when needed:

```bash
git submodule update --remote weblate
git diff --submodule
git add weblate
```
