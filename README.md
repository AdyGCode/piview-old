# PiView

A Raspberry Pi system information package.

![PiView Icon](PiView-0.25x.png)

PiView provides the details of the Raspberry Pi currently being interrogated. System information includes, but is not limited to:

- **CPU**: max load across cores, temperature, clock speed
- **GPU**: temperature
- **HARDWARE**: bluetooth, i2c, spi, camera statuses
- **HOST**: boot time, model, name, revision, serial number, uptime
- **NETWORK**: host name, interface names, ip addresses, mac addresses
- **STORAGE**: total disk capacity, free disk capacity, total RAM and free RAM

Also includes a small utility library with:

- conversion of bytes into Kilobytes, Megabytes, Gigabytes and up
- create list with a quartet of integer numbers representing the IPv4 Address

## Changes

See the [CHANGES](CHANGES.md) document for details of updates and changes.

## Requirements

This project requires a number of packages, including:

- psutils

Remaining packages are Python 'built-ins'.

## Building

Building is in 3 stages:

1. Build package
2. Update and build docs
3. Publish package

### Build package

```shell
python3 -m build
```

### Publish package

```shell
python3 -m twine upload --repository PiView-AG dist/*
```

### Build Docs

If you wish to build the docs from scratch, then remove the docs/source/modules.rst and the docs/source/PiView_AG.rst files before using the build steps.

#### First Build
From there, first time through use:

```shell
cd docs
sphinx-apidoc -o source ../PiView_AG -a -f 
sphinx-build -b html source html -a -j 2
```

#### Re-Builds
Subsequent runs, if you are in the documentation (docs) folder already:

```shell
sphinx-apidoc -o source ../PiView_AG -a -f 
make clean && make html
```

## Acknowledgements

A very large thank you to Matt Hawkins upon whose code this package is based: [https://www.raspberrypi-spy.co.uk/](https://www.raspberrypi-spy.co.uk/).

The original code may be found as [mypi.py](https://github.com/tdamdouni/Raspberry-Pi-DIY-Projects/blob/master/MattHawkinsUK-rpispy-misc/python/mypi.py).

## About the Author

Adrian Gould has been coding for over 40 years, starting his coding in Sinclair ZX-80 Basic and Machine Code, through Pascal, Modula-2, Occam, Prolog and many others to the current swathe of Python, C#, PHP, JS, and other languages today.

He believes that it is a continuous process to learn any (coding) language, and will always say he is not an expert.

He is a full time educator who lives and works in Perth, Western Australia.

## Copyright

Copyright Adrian Gould, 2021-. Licensed under
the [Open Software License version 3.0](./LICENSE.txt)
