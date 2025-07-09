# .dotfiles2025

This repository is intended to provide a version controlled set of
configuration files for managing my Linux Mint laptop running the i3
window manager.

Using the repository relies on the use of GNU Stow which is described
as a symlink farm management application. Using this produced and the
repository is described below.

## Repository Structure.

The repository is a folder in the home directory (in this case
.dotfiles2025). Each product managed under this repository is a folder
with the path:

<product>/<full path relative to the 'parent' of the stow
repository/<configuration files>

In the case of the i3wm configuration file the required path is:

~/.config/i3/config

The repository path is:

~/.dotfiles2025/i3/.config/i3/config

When the stow command is run then a symlink is created in the required
location and pointing at the repository version.

The stow command is run in the root folder of the dotfiles repository
as follows:

stow -t ~/ -v -R i3

-t defines the target location

-v verbose output

-R restow (remove and re-install files)
