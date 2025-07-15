## Generate manifests

```bash
nix-shell --run $SHELL

task package-generate

exit
```

## Run Tests

```bash
nix-shell --run $SHELL

task cluster-create

task test-watch

# Stop the watcher with `ctrl+c`

task cluster-destroy

exit
```

## Publish To Upbound

```bash
nix-shell --run $SHELL

# Replace `[...]` with the Upbound Cloud account
export UP_ACCOUNT=[...]

# Replace `[...]` with the Upbound Cloud token
export UP_TOKEN=[...]

# Replace `[...]` with the version of the package (e.g., `v0.5.0`)
export VERSION=[...]

task package-publish

exit
```

## Testing mirroring

This is to test mirroring from Forgejo git server
