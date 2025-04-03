# KDE Service Menus for FLAC Audio File Processing

Convert your FLAC audio files to Opus or MP3 files.

---

## Prerequisites

Ensure the following tools are installed to use these service menus:

- [FLAC](https://xiph.org/flac/)
- [Opus](https://opus-codec.org/downloads/)
- [LAME](https://lame.sourceforge.io/)

---

## Installation (Plasma 6)

### Install Dependencies (Arch Linux)

Run the following command to install the required software:

```bash
sudo pacman -S flac opus lame
```

### System-Wide Installation

Copy the files to the system directories:

```bash
sudo cp servicemenus/* /usr/share/kio/servicemenus/
sudo cp bin/* /usr/local/bin/
```

### Per-User Installation

For a user-specific setup, copy the files as follows:

```bash
cp servicemenus/* ~/.local/share/kio/servicemenus/
cp bin/* ~/.local/bin
```

Ensure the `~/.local/bin` directory is included in your `$PATH` environment variable.  
Additionally, make the `.desktop` files executable:

```bash
chmod +x ~/.local/share/kio/servicemenus/flacconvert.desktop
```

Finally, restart your Plasma session or execute the following command:

```bash
kbuildsycoca6
```

---

## Uninstallation

### System-Wide Uninstallation

Remove the installed files:

```bash
sudo rm /usr/share/kio/servicemenus/flacconvert.desktop
sudo rm /usr/local/bin/flacconvert-kdialog
```

### Per-User Uninstallation

Delete the corresponding files:

```bash
rm ~/.local/share/kio/servicemenus/flacconvert.desktop
rm ~/.local/bin/flacconvert-kdialog
```

---

## Contributing

Contributions are welcome! Please follow these guidelines:

- For major changes, open an issue first to discuss your ideas.
- Ensure that any required tests are updated as appropriate.

We look forward to your pull requests!

---

## License

This project is licensed under [GPL-3.0+](https://www.gnu.org/licenses/gpl-3.0.html).
