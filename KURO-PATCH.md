# KURO patch

This fork keeps the upstream Claude Usage Extension behavior while applying a small UI-only patch.

## Changes

- Do not render the four promotional/support footer links in the usage sidebar.
- Keep usage percentages blue instead of switching to warning colors.
- Do not render the weekly-position triangle marker above the inline usage bar.
- Preserve usage calculations, reset times, limits, tooltips, and other extension behavior.

## Upstream

Upstream repository:

`https://github.com/lugia19/Claude-Usage-Extension`

The local source checkout keeps an `upstream` remote so upstream updates can be reviewed and merged before publishing a new KURO release.

## Update rule

KURO releases use a fourth numeric version segment (for example `5.6.0.1`) so the customized release stays distinct while remaining comparable by the launcher.

Do not overwrite the KURO patch with an upstream release automatically.

When upstream publishes a new version:

1. fetch/merge upstream,
2. resolve only the small KURO UI diff if needed,
3. run syntax/build checks,
4. publish a matching Electron release from this fork,
5. let the customized launcher update from this fork.
