### Yaru-blue icons

You can build and install Yaru-blue icons from source using Meson.

### Install:

```bash
# build
meson "build" --prefix=/usr
# install
sudo ninja -C "build" install
```

By default it installs to `/usr/` but you can specify a different directory with a prefix like: `/usr/local` or `$HOME/.local`.

After which you should be able to pick any variant of **Yaru-blue** as your icon theme in **GNOME-Tweaks**, or you can set either from a terminal with:

```bash
# set the icon theme as Yaru-blue
gsettings set org.gnome.desktop.interface icon-theme "Yaru-blue"
```

```bash
# set the icon theme as Yaru-blue-dark
gsettings set org.gnome.desktop.interface icon-theme "Yaru-blue-dark"
```

```bash
# set the icon theme as Yaru-blue-light
gsettings set org.gnome.desktop.interface icon-theme "Yaru-blue-light"
```

### Uninstall:

To uninstall all Yaru-blue icon-themes, simply run the following.

*Note: If you installed it without superuser priveleges just omit the  `sudo`.*

```bash
sudo ninja -C "build" uninstall
```

Once uninstalled you can reset your icon theme to the default setting by running the following.

```bash
# reset icon theme to default
gsettings reset org.gnome.desktop.interface icon-theme

```
### Copying or Reusing

This project has mixed licencing. You are free to copy, redistribute and/or modify aspects of this work under the terms of each licence accordingly (unless otherwise specified).

The Suru icon assets (any and all source `.svg` files or rendered `.png` files) are licenced under the terms of the [Creative Commons Attribution-ShareAlike 4.0 License](https://creativecommons.org/licenses/by-sa/4.0/).

Included scripts are free software licenced under the terms of the [GNU General Public License, version 3](https://www.gnu.org/licenses/gpl-3.0.txt).

## Contributing

Contributions are obviously welcome! If you would like to contribute to this project, please [read this](/CONTRIBUTING.md) regarding contributions.
