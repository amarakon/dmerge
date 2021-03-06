Dmerge – Dmenu Emerge
================

## Contents

-   [Usage](#usage)
-   [Dependencies](#dependencies)
-   [Installation](#installation)
    -   [Universal](#universal)
    -   [Gentoo](#gentoo)
-   [Uninstallation](#uninstallation)
    -   [Universal](#universal-1)
    -   [Gentoo](#gentoo-1)

Dmerge is a simple command-line utility to Emerge and Unmerge packages
using Dmenu.

## Usage

Any emerge options will work. Any emerge atoms will also work.

``` sh
`# root` dmerge # search for and emerge packages
`# root` dmerge --depclean # search for and deplean packages
`# root` dmerge --unmerge # search for and unmerge packages
`# root` dmerge <atom> # emerge, search for and emerge packages
```

## Dependencies

1.  Portage
2.  eix or portage-utils (eix is recommended because it is faster and
    has more details.)

## Installation

### Universal

``` sh
`# user` git clone https://github.com/amarakon/dmerge
`# user` cd dmerge
`# root` make install
```

### Gentoo

``` sh
`# root` eselect repository add amarlay git https://github.com/amarakon/amarlay
`# root` emerge --sync amarlay
`# root` emerge x11-misc/dmerge
```

## Uninstallation

### Universal

``` sh
`# user` cd dmerge
`# root` make uninstall
```

### Gentoo

``` sh
`# root` emerge -c x11-misc/dmerge
# Remove my overlay (optional)
`# root` eselect-repository remove -f amarlay
`# root` emerge --sync
```
