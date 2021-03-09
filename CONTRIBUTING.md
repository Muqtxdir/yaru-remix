### Contributing to Yaru-remix

Yaru-remix consists of one project with 3 distinct parts.

- `gnome-shell` directory is the theme for GNOME Shell. This themes stuff like the calendar widget, the Ubuntu dock, the top panel, the login screen and more. It derives from upstream GNOME Shell theme.
- `gtk` contains the themes GTK+2 and GTK+3. This specifies how applications like Files, Terminal, Ubuntu Software look. It derives from upstream Adwaita GTK+2 and GTK+3 themes.
- `icon-theme` contains all the icons, derives from the [Suru icon](https://snwh.org/suru) theme.


### Build and install themes from source
This installation method is to try out the theme while developing it. follow the instructions in the [here](install.md)
If you're not a developer, follow the instructions in the [here](script.md)

### Useful one-liners for icon theme contributors
```bash
# Additionally installs packages needed to work on the icon theme
sudo apt install libgtk-3-dev git meson sassc inkscape optipng ruby
```

SCSS is the actual "source code" of the theme. This is compiled into the CSS files. Edit the SCSS if you want to contribute your changes back to us. SCSS is simple enough to get the hang of if you already know CSS. You can go through [this SCSS tutorial](http://marksheet.io/sass-scss-less.html) to learn more. After making your edits in the SCSS files, you can run `sudo ninja install` in the `yaru-remix/build` folder. That’ll do all the compiling and installing.

Changes to Gnome Shell theme are visible after doing <kbd>Alt</kbd> + <kbd>F2</kbd> and running <kbd>r</kbd> as command. The changes to GTK theme will be visible after running the following commands.

```bash
# To reload GTK theme
# Change to Adwaita theme and back to Yaru
gsettings set org.gnome.desktop.interface gtk-theme Adwaita
gsettings set org.gnome.desktop.interface gtk-theme Yaru-remix
# To reload icon theme
# Change to Humanity icon theme and back to Yaru
gsettings set org.gnome.desktop.interface icon-theme Humanity
gsettings set org.gnome.desktop.interface icon-theme Yaru-remix
```

### Get your copy of Yaru-remix and make a Pull Request (PR)

On the GitHub page (where you are probably reading this), *fork* the Yaru-remix repository, then clone your copy locally on your computer and build it for the first time to verify that everyting is in place.

```bash
git clone https://github.com/yourusername/yaru-remix.git
cd yaru
meson build
sudo -i -H ninja install -C build
```

now create a feature branch for development

```bash
git checkout -b branch-name
```

A good branch name should recall the intended change; if it is a fix for a bug with number 1234 a good name could be something like `issue1234/fix-for-something`

Once you are done with your work, use `git status` to see the list of changed (and eventually new) files and *stage* them with `git add` and commit your work with `git commit`

```bash
$ git status
On branch issue1234/fix-for-something
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

        modified:   CONTRIBUTING.md
...
```

```bash
$ git add CONTRIBUTING.md
```


```$bash
$ git commit
```

Now think about a good *commit message*. The expected format is like the following

> short explaination of the commit
> 
> A more detailed explaination, possibly explaining the current state,
> why a change is needed and how you implemented the change. Try to find
> a good compromise between too short and too long.
> 
> if it is a fix for a bug numbered 1234 inform GitHub system so that it
> can close it automatically when the PR is merged.
>
> closes #1234

Finally, make a Pull Request (PR) from *branch-name*

```bash
git push --set-upstream origin add-git-workflow
```

Open Yaru-remix GitHub repository page, a link to "Create your Pull request" should appear on the main page
