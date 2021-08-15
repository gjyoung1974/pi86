# pi86 host a 8088 MPU on a Rasberry Pi GPIO

## What's this?
A fork of the excellent/awesome work of Elijah Miller
at: [www.homebrew8088.com](https://www.homebrew8088.com)

### What's changed?    
- building with CMake on 64bit OS (aarch64)

### TODOs:    
- Move from WiringPI to [pigpio](http://www.abyz.me.uk/rpi/pigpio/pigs.html)
- or an ch341 SPI interface for the v1 circuit board model [ch341](https://github.com/gschorcht/spi-ch341-usb)

### How to build

create a build directory:

```sh
mkdir -p build
```

run cmake and generate cmakefiles
```sh
cd ./build && cmake .. && make
```

---
2021 Gordon Young

