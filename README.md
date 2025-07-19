# gtk-theme-mist

:          |:
:----------|:-------------------
Description|Mist theme for gtk2/3/4
License    |GNU GPLv2 or later

## Directory structure

### assets

Images used.  Currently only for GTK 4 check and radio buttons, as icon themes
can't be used for them anymore.

### gtk-2.0

  - theme for GTK+ 2
  - it should work in GTK+ 2.22 and later (and perhaps earlier)
  - uses [Mist engine](https://wiki.gnome.org/Attic/GnomeArt/Tutorials/GtkEngines/MistEngine)
  - taken from Arch Linux gtk-engines 2.21.0-1 package
  - no functional changes so far (just reformatted to sane style)

### gtk-3.8

  - theme for GTK+ 3.8 to 3.18
  - uses default [gtk3 engine](https://developer.gnome.org/gtk3/stable/GtkThemingEngine.html#GtkThemingEngine.description)
  - based on [Mist-Redmond 1.2
    (gtk3.8-theme\_Mist-Redmond)](http://gnome-look.org/content/show.php?content=155580)
  - goal is to match gtk2 version as closely as possible
  - incomplete
  - no longer maintained

### gtk-3.20

  - theme for GTK+ 3.20 through 3.24.x
  - based on gtk-3.8, but highly extended

### gtk-4.0

  - theme for GTK 4
  - based on gtk-3.20

## Install

### GTK+ 2.x

GTK+ 2's theme engines already includes Mist so you'll likely not have to
install it, but if you do it has to be in ~/.themes:

```
mkdir -p ~/.themes
cd ~/.themes
git clone https://github.com/keithbowes/gtk-theme-mist Mist
```

After that, you'll need to update ~/.gtkrc-2.0:

```
echo gtk-theme-name="Mist" >> ~/.gtkrc-2.0
```

### GTK + 3.x and GTK 4.x

For these versions, it's still possible to put themes in ~/.themes, but you'll
most likely want to put user themes under ~/.local/share (or wherever
$XDG_DATA_HOME points to) as you move away from the archaic GTK+ 2.x:

```
mkdir -p ${XDG_DATA_HOME:=~/.local/share}/themes
cd $XDG_DATA_HOME/themes
git clone https://github.com/keithbowes/gtk-theme-mist Mist
```

Next, you'll need to tell GTK to use Mist.  If your system provides a
[settings-sharing
mechanism](https://docs.gtk.org/gtk4/class.Settings.html#description),
this involves updating gsettings:

```
gsettings set org.gnome.desktop.interface gtk-theme "'Mist'"
```

Otherwise, you'll need to specify the theme in your settings.ini file; for
example, for GTK 4:

```
mkdir -p ${XDG_CONFIG_HOME:=~/.config}/gtk-4.0
echo gtk-theme-name=Mist >> $XDG_CONFIG_HOME/gtk-4.0/settings.ini
```
