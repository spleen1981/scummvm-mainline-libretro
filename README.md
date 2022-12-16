# ScummVM mainline libretro core

Libretro core built directly from untouched mainline ScummVM source.

## Purpose
As current official ScummVM libretro core is based on a very old fork of ScummVM, this repository aims to have a libretro core always in sync with ScummVM mainline repository, with a maintenance effort from low to none.
* ScummVM main repo is included as a submodule. To sync the libretro core it should be sufficient to update the submodule and build
* No patch is applied to the submodule
* Submodule updates will be generally committed here following ScummVM official releases (though it can be updated to any commit upstream, considering that adjustment to core `Makefile` and sources in `src` may be required to build)
* Datafiles and themes bundle (`scummvm.zip`) and `core.info` files are built automatically based on current submodule source

## Build
To build with the default configuration type in a shell the following:
```
git clone --recursive https://github.com/spleen1981/scummvm-mainline-libretro
cd scummvm-mainline-libretro
make
```
"Work in progress" engines are not build by default, to include them pass `NO_WIP=0` to make.

## Core options and configuration
All options and configuration of the legacy libretro core are applicable to this one as well, refer to relevant link in Resources.

## Resources
Official ScummVM repository readme is [here](https://github.com/scummvm/scummvm#readme).

Legacy ScummVM libretro core documentation is [here](https://github.com/libretro/scummvm#readme)
