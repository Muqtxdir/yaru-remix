### Build and install themes from source

Yaru-remix is fork of [Yaru](https://github.com/ubuntu/yaru)

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
git clone https://github.com/Muqtxdir/yaru-remix.git

cd yaru-remix

# Initialize build system (only required once per repo)
meson build

cd build

# Build and install
sudo ninja install
```
### Apply Theme and Icons:
- To easily switch between the themes use [yaru-remix-theme-toggle](https://github.com/Muqtxdir/yaru-remix-theme-toggle) extension



### Applying Theme manually:

Selecting the GTK theme via:

```bash
# set the icon theme as Yaru-remix
gsettings set org.gnome.desktop.interface gtk-theme "Yaru-remix"
```

```bash
# set the icon theme as Yaru-remix-dark
gsettings set org.gnome.desktop.interface gtk-theme "Yaru-remix-dark"
```

```bash
# set the icon theme as Yaru-remix-light
gsettings set org.gnome.desktop.interface gtk-theme "Yaru-remix-light"
```
The Yaru-remix-theme files go into `/usr/local/share/themes/Yaru-remix`.

The Yaru-remix-dark-theme files go into `/usr/local/share/themes/Yaru-remix-dark`.

The Yaru-remix-light-theme files go into `/usr/local/share/themes/Yaru-remix-light`.


### Applying Icons manually:

Select the icon-themes via:
```bash
# set the icon theme as Yaru-remix
gsettings set org.gnome.desktop.interface icon-theme "Yaru-remix"
```

```bash
# set the icon theme as Yaru-remix-dark
gsettings set org.gnome.desktop.interface icon-theme "Yaru-remix-dark"
```

```bash
# set the icon theme as Yaru-remix-light
gsettings set org.gnome.desktop.interface icon-theme "Yaru-remix-light"
```

The Yaru-remix-icon files go into `/usr/local/share/icons/Yaru-remix`.

The Yaru-remix-dark-icon files go into `/usr/local/share/icons/Yaru-remix-dark`.

The Yaru-remix-light-icon files go into `/usr/local/share/icons/Yaru-remix-light`.

### Uninstall:

To uninstall all Yaru-remix, simply run the following.

```bash
cd yaru-remix

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
