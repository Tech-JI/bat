# bat

Bat is an useful tool for viewing plain text files in the terminal.

## Reference

The official repository can be found [here](https://github.com/sharkdp/bat). This repository serves as a easy-to-do tutorial for setting up bat.

## Installation

### Windows

**Install [Visual C++ Redistributable](https://support.microsoft.com/en-us/help/2977003/the-latest-supported-visual-c-downloads) first.**

Then there are many package managers that can be used to install bat on Windows, such as `scoop`, `chocolatey`, `winget`, etc.  
At the same time, installation via binary files is also supported. See [Release](https://github.com/sharkdp/bat/releases).

#### Scoop

```bash
scoop install bat
scoop install less
```

#### Chocolatey

```bash
choco install bat
```

#### Winget

```bash
winget install sharkdp.bat
winget install JohnTaylor.less
winget install JohnTaylor.lesskey
```

### macOS (with `brew` or `MacPorts`)

```bash
brew install bat
```

```bash
port install bat
```

### Linux

#### Ubuntu and other Debian-based Linux distributions (with `apt`)

```bash
sudo apt install bat
```

If you install bat this way, please note that the executable may be installed as `batcat` instead of `bat` (due to a name clash with another package). You can set up a `bat -> batcat` symlink or alias to prevent any issues that may come up because of this and to be consistent with other distributions:

```bash
mkdir -p ~/.local/bin
ln -s /usr/bin/batcat ~/.local/bin/bat
```

*Bat can also be installed using `.deb` files, see official repository for more information.*

#### Alpine Linux

```bash
sudo apk add bat
```

#### Arch Linux

```bash
sudo pacman -S bat
```

**Other distributions please refer to the official repository.**

## Configuration

The configuration file's location can be called using `bat --config-file`. A default configuration file can be generated using `bat --generate-config-file`.

Run `bat --help` to see all the available options.

**For Windows users, some features need extra configuration. See official repository if errors occur.**

## Sample

This repo contains sample config file for bat.

```bash
git clone https://github.com/Hydraallen/bat.git ~/.config/bat
```

## Usage

### Display a single file on the terminal

```bash
bat filename
```

### Show non-printable characters

You can use the `-A`/`--show-all` option to show and highlight non-printable characters.
