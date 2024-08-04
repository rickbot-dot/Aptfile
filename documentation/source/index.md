# What is an Aptfile?

Aptfile is a dependency management system. Aptfile can also solve issues on other APT-based
OSes, e.g. Ubuntu, Kali, Mint, and others.

Also, GUI appstores don't understand APT, so Aptfiles can also contain app information including
the description of it.

## Example

Aptfiles are written in **TOML** so a basic Aptfile could look like this:

```toml
[aptfile]
target = 1.0

[apt.dependencies]
python3 = 3.9
cython3 = "latest"
```

Not all of the Aptfile language is shown in this example. Read these guidelines for a complete
list.

## How to create an Aptfile

Aptfiles are named as either `Aptfile` or `Aptfile.toml`. Keep in mind that Aptfiles should not be placed
in a subfolder, or else the Aptfile will not be recgonized. The name is case-insensitive - use any type
of capitalization you want - UPPERCASE, lowercase, even *DiFfErReNtCaSe*...

```{toctree}
:hidden:
:maxdepth: 1
:caption: Contents:

index
```
```{multi-theme-toctree}
:caption: Themes
```
