# RazerGenie

Standalone Qt application for configuring your Razer devices under GNU/Linux.

![Screenshot of application](https://z3ntu.github.io/RazerGenie/screenshots/mainwindow.png)

## Installation
Packages are available for these distributions:
* **Arch Linux:** you can install the package from the AUR: [razergenie](https://aur.archlinux.org/packages/razergenie/) or [razergenie-git](https://aur.archlinux.org/packages/razergenie-git/).
* **Debian/Ubuntu/Fedora:** [Download from OBS (openSUSE Build Service)](https://software.opensuse.org//download.html?project=hardware%3Arazer&package=razergenie)

If you are using a distribution not listed here please let me know and I'll try to make a package for that distribution!

## How to compile
```
mkdir build && cd build
# Either:
cmake ..
# Or - to enable experimental (=unfinished) features
cmake -DENABLE_EXPERIMENTAL=ON ..
make
./src/razergenie
# You could install it with 'make install' but that's not recommended as files get left in the filesystem (use a distribution package, if available!).
```

## Dependencies
* Qt5 (+ the modules: DBus, Network & Xml)
* kwidgetsaddons
* razer-drivers
* cmake
* extra-cmake-modules

#### Ubuntu
```
sudo apt install cmake extra-cmake-modules qt5-default libkf5configwidgets-dev
```

#### Arch Linux
```
sudo pacman -S --needed cmake extra-cmake-modules qt5-base kconfigwidgets
```

## TODO
* Implement keyboard gui (individual lighting etc)
* Make images in the device list bigger (probably is pretty complicated with the KPageWidget I am using)
* **Much** more
