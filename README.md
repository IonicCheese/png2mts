# PNG2MTS

<img src="misc/demo.png" alt="showcase"/>

A WIP converter that takes a PNG image and converts it to a Luanti schematic.
(WARNING: Success converting images not guaranteed.)

# How to compile
### Installing Dependencies:

Ubuntu/Debian:
```
sudo apt install g++ zlib1g-dev
```

Fedora:
```
sudo dnf install gcc-g++ kernel-devel zlib-devel
```

openSUSE:
```
sudo zypper install gcc-c++
```

Arch:
```
sudo pacman -S base-devel
```

Alpine:
```
sudo apk add build-base zlib-dev
```

Void:
```
sudo xbps-install zlib-devel
```

Windows/MacOS:
good luck have fun (PRs welcome)

### Compiling:
```
g++ -o png2mts -lz -O3 src/main.cpp
```

# How to use
First you need a image to convert. (keep the size <500px in any axis unless your crazy or want even more detail)
And second you need [Minetest/Luanti](https://github.com/luanti-org/luanti) and a way to load schematics (i recemmend [Worldedit](https://github.com/Uberi/Minetest-WorldEdit))

Run `png2mts -i <your image path here> -o <your output path here>` and move the resulting .mts file to your Luanti world's schematic directory (generally at `~/.minetest/worlds/<world name>/schems`)
(example: `png2mts -i ~/luanti.png -o ~/.minetest/worlds/world/schems/luanti.mts`. do be warned that the default color palette is configured to use [Minetest game](https://github.com/luanti-org/minetest_game). you can change palette with `-p <palette path>`)

Run Luanti, load the schematic, and profit!
