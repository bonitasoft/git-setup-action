# Git Setup Action

Composite GitHub Action to configure Git to sign commits with Bonita CI technical user.
Intend for internal usage only.

## Inputs

| Name                   | Description                             |
| ---------------------- | --------------------------------------- |
| `keeper-secret-config` | The Keeper Secret Manager configuration |

## Outputs

| Name          | Description                                                    |
| ------------- | -------------------------------------------------------------- |
| `fingerprint` | Fingerprint of the GPG key used to sign commits                |
| `name`        | Name associated with the GPG key used to sign commits          |
| `email`       | Email address associated with the GPG key used to sign commits |

## Usage

```yaml
jobs:
  setup-git:
    runs-on: ubuntu-latest
    steps:
      - name: Setup Git Settings
        uses: bonitasoft/git-setup-action@TAGNAME
        with:
          keeper-secret-config: ${{ secrets.KSM_CONFIG }}
```

## Release new action version

Manually [create a new GitHub release](https://github.com/bonitasoft/git-setup-action/releases/new) from the UI that will automatically trigger the [Release new action version](https://github.com/bonitasoft/git-setup-action/actions/workflows/release-new-action-version.yml) workflow.