# gtk-theme-mist

:          |:
:----------|:-------------------
Description|Mist theme for gtk2/3/4
License    |GNU GPLv2 or later

## gtk-2.0

  - uses Mist engine
  - taken from Arch Linux gtk-engines 2.21.0-1 package
  - no functional changes so far (just reformatted to sane style)

## gtk-3.0

  - uses default gtk3 engine
  - based on [Mist-Redmond 1.2
    (gtk3.8-theme\_Mist-Redmond)](http://gnome-look.org/content/show.php?content=155580)
  - work in progress (goal is to match gtk2 version as closely as possible)

### Known issues

  - No visual indication of the focused notebook tab

## gtk-4.0

  - shares as much code with gtk-3.0 as possible

## Install

### GTK+ 2.x

GTK+ 2's theme engines already includes Mist so you'll likely not have to install it, but if you do it has to be in ~/.themes:

```
install -d ~/.themes
cd ~/.themes
git clone https://github.com/keithbowes/gtk-theme-mist Mist
```

After that, you'll need to update ~/.gtkrc-2.0:

```
echo gtk-theme-name="Mist" >> ~/.gtkrc-2.0
```

### GTK 3.x and 4.x

For these versions, it's still possible to put themes in ~/.themes, but you'll most likely want to put user themes under ~/.local/share (or wherever $XDG_DATA_HOME points to) as you move away from the archaic GTK+ 2.x:

```
cd ${XDG_DATA_HOME:-~/.local/share}
install -d themes
cd themes
git clone https://github.com/keithbowes/gtk-theme-mist Mist
```

Next, you'll need to tell GTK to use Mist.  This usually involves updating gsettings:

```
gsettings set org.gnome.desktop.interface gtk-theme "'Mist'"
```

You can specify the theme in your settings.ini file, but applications don't always pick that up; for example, for GTK 3:

```
echo gtk-theme-name=Mist >> ${XDG_CONFIG_HOME:-~/.config}/gtk-3.0/settings.ini
```
