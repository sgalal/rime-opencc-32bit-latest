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

Environment: Visual Studio 2019, CMake

Clone repository:

```sh
$ git clone https://github.com/BYVoid/OpenCC.git opencc-dir
```

Build:

```sh
$ (cd opencc-dir && git checkout -f master && git pull)
$ cp -r opencc-dir/data/dictionary .
$ (cd opencc-dir && git checkout -f ver.1.0.6)
$ cp -r dictionary opencc-dir/data
$ cmake -G"Visual Studio 16 2019" -Awin32 -Sopencc-dir -Bbuild -DCMAKE_INSTALL_PREFIX:PATH=.
$ cmake --build build --config Release --target install
$ rm -rf opencc
$ cp -r build/share/opencc .
```

## Version

OpenCC [`fd0636f`](https://github.com/BYVoid/OpenCC/commit/fd0636fa904cae284276eaeb8babb3254cba8398)
