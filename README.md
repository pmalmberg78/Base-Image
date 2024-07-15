# Kanola Base Image

Containerfile for building Kanola-Base, an unofficial Vanilla OS image.

This image is based on top of [`vanillaos/core`](https://github.com/Vanilla-OS/core-image/pkgs/container/core) and offers a basis for further images to be built without any included desktop of its own.
It is intended as an intermediary between upstream core and the downstream images of this Org, to allow any major build issues to be resolved in one place.

## Switch your Installation to this image

> [!CAUTION]
> This WIP image is experimental and isn't suitable for production. If you encounter any bugs during testing, please report them in this repository.

- Edit the `/etc/abroot/abroot.json` file with the `abroot config-editor` command.
- Change the "name" entry from something like `vanilla-os/desktop` to `Kanola-Images/Base-Image` (**Note**: All characters must be in lowercase).
- Now, Run `abroot upgrade` to switch to your custom image.

## Build

```bash
vib build recipe.yml
podman image build -t Kanola-Images/Base-Image .
```
