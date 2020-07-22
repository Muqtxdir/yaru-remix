### Build and install themes from source

Yaru-blue is fork of [Yaru](https://github.com/ubuntu/yaru)

This installation method is to try out the theme while developing it. If you're not a developer, follow the instructions in the [README.md](./README.md).

### Prerequisite:
```bash
# apt install libgtk-3-dev git meson sassc
```
### Download the repository from github:
```bash
git clone https://github.com/Muqtxdir/yaru-blue.git
cd yaru-blue
# Initialize build system (only required once per repo)
meson build
cd build
# Build and install
sudo ninja install
```

### Icon-theme Tools:
```bash
# Additionally installs packages needed to work on the icon theme
sudo apt install libgtk-3-dev git meson sassc inkscape optipng ruby
```
### Applying Theme:

Selecting the GTK theme via:

```bash
# set the icon theme as Yaru-blue
gsettings set org.gnome.desktop.interface gtk-theme "Yaru-blue"
```

```bash
# set the icon theme as Yaru-blue-dark
gsettings set org.gnome.desktop.interface gtk-theme "Yaru-blue-dark"
```

```bash
# set the icon theme as Yaru-blue-light
gsettings set org.gnome.desktop.interface gtk-theme "Yaru-blue-light"
```
The Yaru-blue-theme files go into `/usr/local/share/themes/Yaru-blue`.

The Yaru-blue-dark-theme files go into `/usr/local/share/themes/Yaru-blue-dark`.

The Yaru-blue-light-theme files go into `/usr/local/share/themes/Yaru-blue-light`.


### Applying Icons:

Select the icon-themes via:
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

The Yaru-blue-icon files go into `/usr/local/share/icons/Yaru-blue`.

The Yaru-blue-dark-icon files go into `/usr/local/share/icons/Yaru-blue-dark`.

The Yaru-blue-light-icon files go into `/usr/local/share/icons/Yaru-blue-light`.

### Reverting Theme:

Selecting the default-GTK theme via:

```bash
# To reload GTK theme
# Change to Adwaita theme and back to Yaru
gsettings set org.gnome.desktop.interface gtk-theme Adwaita
gsettings set org.gnome.desktop.interface gtk-theme Yaru
```

### Reverting Icons:

Selecting the deafult-icons themes via: 

```bash
# To reload GTK theme
# Change to Adwaita theme and back to Yaru
gsettings set org.gnome.desktop.interface icon-theme Adwaita
gsettings set org.gnome.desktop.interface icon-theme Yaru
```

### Uninstall:

To uninstall all Yaru-blue, simply run the following.

*Note: If you installed it without superuser priveleges just omit the  `sudo`.*

```bash
sudo ninja uninstall
```

Once uninstalled you can reset your icon theme to the default setting by running the following.

```bash
# reset gtk theme to default
gsettings reset org.gnome.desktop.interface gtk-theme

# reset icon theme to default
gsettings reset org.gnome.desktop.interface icon-theme

```
