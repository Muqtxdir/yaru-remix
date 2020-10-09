## Build and install themes from source

This will install:
- GTK3 themes
- gnome-Shell theme
- Yaru-remix icons

To try out the theme, follow the instructions:

### packages needed to build yaru-remix
```bash
sudo apt install libgtk-3-dev git meson 
```

### packages for theme modification (Optional):
```bash
# Additionally installs packages needed to work on the gtk,icon theme
sudo apt install sassc inkscape optipng ruby
```

### install:

```bash
# clone this repository
git clone https://github.com/Muqtxdir/yaru-remix.git
```

```bash
cd yaru-remix
```

```bash
# Initialize build system (only required once per repo)
meson build

cd build

# Build and install
sudo ninja install
```

### install for flatpak apps:

```bash
# Yaru-remix
flatpak install flathub org.gtk.Gtk3theme.Yaru-remix
```

```bash
# Yaru-remix-dark
flatpak install flathub org.gtk.Gtk3theme.Yaru-remix-dark
```

```bash
# Yaru-remix-light
flatpak install flathub org.gtk.Gtk3theme.Yaru-remix-light
```

### Apply Theme and Icons:
- To easily switch between the themes use [yaru-remix-theme-toggle](https://github.com/Muqtxdir/yaru-remix-theme-toggle) extension



### Applying Theme and Icons manually:

The theme can now be selected, either using the Gnome Tweaks GUI or by using the following commands:

```bash
# set the gtk-theme as Yaru-remix (or) Yaru-remix-light (or) Yaru-remix-dark
gsettings set org.gnome.desktop.interface gtk-theme "Yaru-remix"
```

```bash
# set the icon theme as Yaru-remix (or) Yaru-remix-light (or) Yaru-remix-dark
gsettings set org.gnome.desktop.interface icon-theme "Yaru-remix"
```

### Uninstall:

- To uninstall all Yaru-remix, simply run the following (Although some files won't be deleted succesfully)

```bash
cd yaru-remix

cd build

sudo ninja uninstall
```
- The remaining can be removed by doing this:

```bash
# deletes all GTK3-theme-folders named Yaru-remix, Yaru-remix-light, Yaru-remix-dark
sudo rm -R /usr/share/themes/Yaru-remix*

# deletes icon-folder named Yaru-remix, Yaru-remix-light, Yaru-remix-dark
sudo rm -R /usr/share/icons/Yaru-remix*

```

- Once uninstalled you can reset your GTK and icon theme to the default setting by running the following.

```bash
# reset gtk theme to default
gsettings reset org.gnome.desktop.interface gtk-theme
```
```bash
# reset icon theme to default
gsettings reset org.gnome.desktop.interface icon-theme
```
