# Kanola Base Image

Containerfile for building Kanola-Base, an unofficial Vanilla OS image.

This image is based on top of [`vanillaos/core`](https://github.com/Vanilla-OS/core-image/pkgs/container/core) and offers a basis for further images to be built without any included desktop of its own.
It is intended as an intermediary between upstream core and the downstream images of this Org, to allow any major build issues to be resolved in one place.

> [!CAUTION]
> This WIP image is experimental and isn't suitable for production. If you encounter any bugs during testing, please report them in this repository.

> [!IMPORTANT]
> This image is not intended to be used directly. It is used as a base image for other images.
> Like the Vanilla OS Desktop image, etc.

## Build

> [!NOTE]
> The fsguard compiled plugin `.so` file should be downloaded from the [latest release](https://github.com/Vanilla-OS/vib-fsguard/releases/latest) and be placed under a `plugins` directory beside the `recipe.yml` file.

```bash
vib build recipe.yml
podman image build -t kanola-images/base .
```
