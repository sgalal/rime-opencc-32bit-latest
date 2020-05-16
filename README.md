# rime-opencc-32bit-latest

Recipe: ℞ `sgalal/rime-opencc-32bit-latest`

Customize rime input schemata to use the latest [OpenCC](https://github.com/BYVoid/OpenCC) dictionaries (32-bit)

For 64-bit version, see [sgalal/rime-opencc-latest](https://github.com/sgalal/rime-opencc-latest).

## Why

The OpenCC shipped with rime installer is not the latest version. Using the latest version will improve the accuracy of OpenCC conversion.

## How

This repository contains the latest version of OpenCC dictionaries. These files will be copied to the rime user directory by the [plum](https://github.com/rime/plum) configuration manager.

## Usage

With plum installed:

```sh
$ bash rime-install sgalal/rime-opencc-32bit-latest
```

Without plum:

```sh
$ curl -fsSL https://git.io/rime-install | bash -s -- sgalal/rime-opencc-32bit-latest
```

## Build Script

See [CI Build](https://ci.appveyor.com/project/chromezh/opencc).

## Version

OpenCC [`fb3618d`](https://github.com/BYVoid/OpenCC/commit/fb3618d29c494dc39d616b6351cd23dc0464133a)
