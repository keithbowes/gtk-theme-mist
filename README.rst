gtk-theme-mist
==============

:Description: Mist theme for gtk2/3
:License: GNU GPLv2 or later
:AUR: https://aur.archlinux.org/packages/gtk3-theme-mist-git/


gtk-2.0
-------

* uses Mist engine
* taken from Arch Linux gtk-engines 2.21.0-1 package
* no functional changes so far (just reformatted to sane style)


gtk-3.0
-------

* uses default gtk3 engine
* based on Mist-Redmond 1.2 (gtk3.8-theme_Mist-Redmond) taken from
  http://gnome-look.org/content/show.php?content=155580
* work in progress (goal is to match gtk2 version as closely as possible)


Install
-------

For GTK 2.x::

    ~/.themes
    ~/.themes/Mist
    ~/.themes/Mist/gtk-2.0
    ~/.themes/Mist/gtk-2.0/gtkrc

    $ cat ~/.gtkrc-2.0
    gtk-theme-name="Mist"
    ...

For GTK 3.x::

    ~/.local/share/themes
    ~/.local/share/themes/Mist
    ~/.local/share/themes/Mist/gtk-3.0
    ~/.local/share/themes/Mist/gtk-3.0/widgets.css
    ~/.local/share/themes/Mist/gtk-3.0/colors.css
    ~/.local/shares/themes/Mist/gtk-3.0/gtk.css

    $ cat ~/.config/gtk-3.0/settings.ini
    [Settings]
    gtk-theme-name=Mist
    ...
