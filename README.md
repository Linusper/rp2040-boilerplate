# rp2040-boilerplate

# Dependencies

If pico-sdk is cloned since before, this step can be skipped.

## Install CMake and GCC for ARM

```
sudo apt install cmake gcc-arm-none-eabi libnewlib-arm-none-eabi libstdc++-arm-none-eabi-newlib
```

## Clone Pico SDK

```
git clone https://github.com/raspberrypi/pico-sdk.git
```

## Init submodules

While inside the pico-sdk folder, run the following command:

```
git submodule update --init
```

# Clone repository

```
git clone https://github.com/Linusper/rp2040-boilerplate.git
```

# Remove origin

```
git remote remove origin
```

# Rename

## CMake

Rename the project name in CMakeLists.txt and src/CMakeLists.txt.
Description can be changed too

## Folder

Move up one folder from the rp2040-boilerplate folder and rename it with the following command:

```
mv rp2040-boilerplate new-project-name
```

# Building

## Before building

The project needs to know where the pico-sdk is located.

```
export PICO_SDK_PATH="path/to/pico-sdk/"
```

This is only required once for every shell.

## Using CMake
```
mkdir build
cd build
cmake ..
```
This needs to be done everytime a new file is added. In addition, the file has to be added in src/CMakeLists.txt.

## Using make
Build the binary by using `make` while inside the build folder.
