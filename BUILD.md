# PiView

A Raspberry Pi system information package.

![PiView Icon](PiView-0.25x.png)

## Building PiView for PyPi

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
