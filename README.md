# DDEV Annertech Tools

Highly opinionated set of configs and commands used by Annertech in our DDEV workflow.

## What it does:

- Provides commands:
- - `branch`: Creates an opinionated git branch name from a Teamwork ticket ID
- - `robo`: Runs robo
- - `behat`: Runs behat
- - `login`: Opens a browser and logs you in to Drupal (works on local environments only)
- - `devmode [on|off]`: Toggles between production and development settings
- Adds actions on DDEV hooks
- Adds git hook to enforce proper commit messages
- Adds custom settings.local.php file on project start and allows easy toggle between production and development mode

## Install

First clean-up previous variations of these files from before they were grouped in an addon.
```
rm -rf .ddev/settings.ddev.annertech.yaml
rm -rf .ddev/config.hooks.yaml
rm -rf .ddev/commands/host/branch
rm -rf .ddev/commands/host/login
rm -rf .ddev/commnads/web/robo
rm -rf .ddev/commnads/web/behat
```

Then get the addon:
```
ddev get annertech/annertech-ddev
```

## Automated Testing commands provided

### Behat

`ddev behat` command is provided and expects behat to be under `PROJECT_ROOT/tests/behat`.

### BackstopJS

We rely on https://github.com/mmunz/ddev-backstopjs to get BackstopJS commands in DDEV. Go look there.
