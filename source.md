### Build and install themes from source

Yaru-blue is fork of [Yaru](https://github.com/ubuntu/yaru)

This installation method is to try out the theme while developing it. If you're not a developer, follow the instructions in the [README.md](./README.md).

### Prerequisite:
```bash
sudo apt install libgtk-3-dev git meson 
```
### Prerequisite for Icon-theme modification (Optional):
```bash
# Additionally installs packages needed to work on the icon theme
sudo apt install libgtk-3-dev git meson sassc inkscape optipng ruby
```

### Install:

```bash
git clone https://github.com/Muqtxdir/yaru-blue.git

cd yaru-blue

# Initialize build system (only required once per repo)
meson build

cd build

# Build and install
sudo ninja install
```
### Apply Theme and Icons:
- To easily switch between the themes use [yaru-blue-theme-toggle](https://github.com/Muqtxdir/yaru-blue-theme-toggle) extension



### Applying Theme manually:

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


### Applying Icons manually:

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

### Uninstall:

To uninstall all Yaru-blue, simply run the following.

```bash
cd yaru-blue

cd build

sudo ninja uninstall
```

Once uninstalled you can reset your GTK and icon theme to the default setting by running the following.

```bash
# reset gtk theme to default
gsettings reset org.gnome.desktop.interface gtk-theme

# reset icon theme to default
gsettings reset org.gnome.desktop.interface icon-theme

```
