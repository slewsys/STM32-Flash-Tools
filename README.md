# STM32 Flash Tools

These scripts are for flashing STM32 MCU firmware in either DFU or ST-Link mode from the command line.

## Install Host Prerequisites

On Fedora Linux, run:

```
sudo dnf5 group install -y c-development
sudo dnf5 install -y \
          arm-none-eabi-gcc-cs{,-c++} \
          arm-none-eabi-newlib \
          dfu-util \
          file \
          stlink \
          st-stlink-udev-rules \
          usbutils
```

On Debian Linux, run:

```
sudo apt install -y \
          build-essential \
          gcc-arm-none-eabi \
          dfu-util \
          file \
          stlink-tools \
          usbutils
```

On both Fedora and Debian Linux, continue with:

```
pip install ar mpremote pyelftools pyhy
sudo groupadd -rf plugdev
sudo groupadd -rf dialout
sudo gpasswd -a $USER plugdev
sudo gpasswd -a $USER dialout
```
