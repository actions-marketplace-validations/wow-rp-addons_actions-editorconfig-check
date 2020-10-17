# actions-editorconfig-check

## Usage

```yaml
- uses: wow-rp-addons/actions-editorconfig-check@v1
  with:
    # List of files to be checked, or a command to execute that will generate such a list.
    #
    # Defaults to the workspace path as set by the `path` input.
    files: ''

    # Working directory for editorconfig-checker.
    # The file list should be relative to this path and output filenames be displayed relative to this path.
    #
    # Default: ${{ github.workspace }}
    path: ''

    # Additional command-line arguments.
    # See <https://github.com/editorconfig-checker/editorconfig-checker#usage>.
    args: ''
```

## Examples

### Check all Lua and XML files in a repository

```yaml
- uses: wow-rp-addons/actions-editorconfig-check@v1
  with:
    files: $(git ls-files '*.lua' '*.xml')
```

### Specify path to a config file

```yaml
- uses: wow-rp-addons/actions-editorconfig-check@v1
  with:
    args: -config path/to/file.json
```
