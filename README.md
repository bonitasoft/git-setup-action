# git-setup-action
Configure Git user with signing key for Github Actions

## Input

| Name                     | Description                                             |
| ------------------------ |---------------------------------------------------------|
| `keeper-secret-config`   | The Keeper Secret Manager configuration                 |

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
