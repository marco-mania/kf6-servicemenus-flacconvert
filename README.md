# KDE service menus for flac file converting

KDE service menus for flac file converting.

## Prerequisites

* [KDE](https://www.kde.org/)
* [FLAC](https://xiph.org/flac/)
* [LAME](https://lame.sourceforge.io/)
* [Opus](https://opus-codec.org/)

## Installation (Plasma 6)

Install the requirements (Arch Linux):

    sudo pacman -S lame flac opus-tools qt6-tools

To install system wide:

    sudo cp servicemenus/* /usr/share/kio/servicemenus/
    sudo cp bin/flacconvert-kdialog /usr/local/bin/

Per user installation:

    cp servicemenus/* ~/.local/share/kio/servicemenus/
    cp bin/flacconvert-kdialog ~/.local/bin

In that case the directory `~/.local/bin` has to be be placed in the search path
environment variable `$PATH`.
E.g. for a Fish shell you can simply call `fish_add_path ~/.local/bin`.
Also make sure your .desktop files are execuatable
`chmod +x ~/.local/share/kio/servicemenus/flacconvert.desktop.desktop`.

Finally you need to restart your plasma session or call:

    kbuildsycoca6

## Uninstall

System wide installation:

    sudo rm /usr/share/kio/servicemenus/flacconvert.desktop.desktop
    sudo rm /usr/local/bin/flacconvert-kdialog

Per user installation:

    rm ~/.local/share/kio/servicemenus/flacconvert.desktop.desktop
    rm ~/./local/bin/flacconvert-kdialog

## Contributing

Pull requests are welcome. For major changes, please open an issue first to
discuss what you would like to change.

Please make sure to update tests as appropriate.

## License

[GPL-3.0+](https://www.gnu.org/licenses/gpl-3.0.de.html)
