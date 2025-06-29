# Edge Smooth - Smooth Edges with this plugin

Debutted in 2022, ships with many other plugins but now it has a stand alone page.

**Download source code and binaries here**
https://github.com/LinuxBeaver/GEGL-GIMP-PLUGIN_Edge_Smooth/releases/tag/edgesmoothing

![image](https://github.com/user-attachments/assets/f1671623-c4a7-4626-9765-41d2b6860b81)

![image](https://github.com/user-attachments/assets/4eda913a-2310-4ce8-8428-312a13db4f84)


## Directory to put Binaries (They do NOT go in the normal plugins folder)

**Windows**
C:\Users\USERNAME\AppData\Local\gegl-0.4\plug-ins

**Linux** 
`~/.local/share/gegl-0.4/plug-ins`

**Linux (Flatpak)**
`~/.var/app/org.gimp.GIMP/data/gegl-0.4/plug-ins`

Then Restart Gimp and use key / to search for "edge smooth" to find it.  

GIMP 2.10 users will only find this in GEGL Operation drop down list 

## Compiling and Installing

### Linux

To compile and install you will need the GEGL header files (`libgegl-dev` on
Debian based distributions or `gegl` on Arch Linux) and meson (`meson` on
most distributions).

```bash
meson setup --buildtype=release build
ninja -C build

```

### Windows

The easiest way to compile this project on Windows is by using msys2.  Download
and install it from here: https://www.msys2.org/

Open a msys2 terminal with `C:\msys64\mingw64.exe`.  Run the following to
install required build dependencies:

```bash
pacman --noconfirm -S base-devel mingw-w64-x86_64-toolchain mingw-w64-x86_64-meson mingw-w64-x86_64-gegl
```

Then build the same way you would on Linux:

```bash
meson setup --buildtype=release build
ninja -C build
```

