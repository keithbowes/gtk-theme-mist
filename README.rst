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

    $ cd
    $ install -d .themes
    $ cd .themes
    $ git clone https://gitlab.com/keithbowes/gtk-theme-mist Mist

    $ echo gtk-theme-name="Mist" >> ~/.gtkrc-2.0

For GTK 3.x::

    $ cd
    $ install -d .local/share/themes
    $ cd .local/share/themes
    $ git clone https://gitlab.com/keithbowes/gtk-theme-mist Mist

    $ echo gtk-theme-name=Mist >> ~/.config/gtk-3.0/settings.ini
