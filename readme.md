# Apt-Pacman Wrapper

Are you moving from a Debian/Ubuntu based distro to Arch Linux or an Arch-based distro? Do you know someone who is? This script is for you or for them.

These architecture-agnostic scripts precisely duplicate the behavior of `apt`, `apt-get`, `apt-cache`, `apt-mark`, and `apt-file`, provided `/usr/bin/pacman` exists. `aptitude` is on the horizon as well.

These scripts include error checking and should be pretty hard to break. They do not need to be updated when the rest of the system is updated, so you can safely install and forget.

Inspired by cookiengineer's [`apt-pac`](https://gist.github.com/cookiengineer/94265370d66ea73f4782f80c231e126c) script and its forks.

These scripts are written based on [the package management Rosetta on Arch Wiki](https://wiki.archlinux.org/title/Pacman/Rosetta).

## Installation

Copy all the scripts to `/usr/local/bin/` and run `sudo chmod +x /usr/local/bin/apt*` (assuming you have `sudo` installed.)
Note that other binary location directories will also work, but installing wrapper scripts like this to `/usr/local/bin/` is better practice.

## Usage

Most commands you read about on Debian and Ubuntu forums should work without modification. The one command which does something different is `apt update` or `apt-get update`: since Arch is not designed for partial upgrades, this automatically runs a full system upgrade, consistent with Arch documentation.
Feel free to use `--help` on any command to see what functions are implemented.
