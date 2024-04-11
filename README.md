# HCV

## Requirements

- Ubuntu
- CMake (https://cmake.org/download/)

## Build
```bash
make SIMULATION=native prep
make
make install
```

### Changes vs. Default cFE Build

1. Add a `CMakeLists.txt` file at the top level that adds the `cfe` subdirectory and adds a custom target that ensures `build/tables/staging` exists before install. Without this, the install fails if no tables are in the build (unlikely, but prevents a skeleton build). The toplevel `Makefile` is updated to run cmake on the root directory instead of `cfe`.
2. Changes to defs to include a single cpu and remove unnecessary example files.

## Run
```bash
cd build/exe/cpu1
./core-cpu1
```