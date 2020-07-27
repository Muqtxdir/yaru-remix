### Creating & Modifying Icons

All Yaru-remix assets are created using the free and open source vector graphics editor [Inkscape](http://inkscape.org), which is recommended for creating new icons or modifying existing ones.

While other tools exist that are suitable for SVG editing, they often add custom elements to extend the limitatations of standard SVG format, so they are not recommended.

### Icon Names

Use of file names in line with the [FreeDesktop.Org Icon Naming Specification](http://standards.freedesktop.org/icon-naming-spec/icon-naming-spec-latest.html) is encouraged for new icons. Failing that, when possible use generic file names and create symbolic links to the generic icon.

### Focus

The Ubuntu desktop is the target for this icon set. As such, Suru development is currently focused the GNOME desktop, and providing the minimum required set of icons for that experience.

## Adding Icons

New [fullcolor icons](src/fullcolor) (those for applications, etc.) must be created from a template found in the source files or simply be based off of a pre-existing source file. See the [fullcolor README](src/fullcolor/README.md) for more details and new [symbolic icons](src/scalable) icons must be added to the source plate SVG found in the source files. See the [symbolic README](src/scalable/README.md) for more details.
