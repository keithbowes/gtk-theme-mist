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
  - dconf-editor: The property names are white and essentially unreadable

#### Imported from upstream

My comments are in parentheses

  - focus hint (I have no idea what that means)
  - text on progress bar (test case?)
  - ~~visited links are white~~ (fixed)
  - ComboBoxes: color under cursor should be white
  - CheckBoxes, ComboBoxes: tick disappears (works for me)
  - ~~Buttons: down state~~ (fixed)
  - Buttons in dialogs (what about them?)
  - FileChooser (what about it?)
  - Tooltips (what about them?)
  - Notebook, indent inactive tabs (does that mean that inactive tabs are indented or that they should be?)

## gtk-4.0

  - shares as much code with gtk-3.0 as possible

## Install

For GTK 2.x:

    $ cd
    $ install -d .themes
    $ cd .themes
    $ git clone https://gitlab.com/keithbowes/gtk-theme-mist Mist

    $ echo gtk-theme-name="Mist" >> ~/.gtkrc-2.0

For GTK 3.x and 4.x:

    $ cd
    $ install -d .local/share/themes
    $ cd .local/share/themes
    $ git clone https://gitlab.com/keithbowes/gtk-theme-mist Mist

    $ echo gtk-theme-name=Mist >> ~/.config/gtk-3.0/settings.ini
    $ gsettings set org.gnome.desktop.interface gtk-theme "'Mist'"
