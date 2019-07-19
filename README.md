# cross-compile-aarch64
Example C++ code to cross compile from Ubuntu 18.04 x64 (AMD/Intel based) to an ARM64 based platform. Tested with Intel NUC i7 to ODROID N2.

## Setup

```bash
# c cross compiler
sudo apt-get install gcc-aarch64-linux-gnu

# c++ cross compiler
sudo apt-get install g++-aarch64-linux-gnu 
```

## Compile Example on x64

```bash
git clone https://github.com/mixxen/cross-compile-aarch64.git
cd cross-compile-aarch64
aarch64-linux-gnu-g++ hello_world.cpp -o hello_world
```

## Run Example on ARM64

```bash
scp hello_world user-name@arm64-device-ip:~
ssh user-name@arm64-device-ip
./hello_world
```