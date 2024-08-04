# Aptfile

An Aptfile is a file specifying Debian package requirements for a whole single project.

## Motivation

APT isn't really that good for managing dependencies. Aptfile solves this by putting
a list of dependencies into a single file. This shortens `apt install a b c d e f g h`
to just `aptfile get`.

Also, APT packages are harder to be used by GUI app stores, like GNOME Software and KDE
Discover. Aptfiles solve that, by containing information about the package in a single
file.

## Format

Aptfiles are written in [TOML](https://toml.io/en/) format. You can write an Aptfile like this:

```toml
# Aptfile for hello-world

[aptfile]
# Main Aptfile data.
target = 1.0

[apt.dependencies]
# dependencies is freeform. Any package can go in as a value. You can define just the major number,
# the major and minor number, or even all 3 numbers (major, minor, and patch). It is recommended to
# use the major and minor number. This example demonstrates requiring Python 3.9 or newer to run the
# program, including Cython. Written in pip format or "latest".
python3 = 3.9
cython3 = "latest"
```

## Is this an official Debian project?

No. However, it's a fairly new project and could get adopted by the Debian Project one day, and
be used as a Debian packaging standard, as Aptfile gets better and better. **Do not confuse Aptfile with
the `apt-file` utility, coincidentally with the same name.**
