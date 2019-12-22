# Annotated Sudoku grid database

This repository contains Sudoku grid pictures, each with an associated `.dat` file reprensenting the digits in the grid.

```
images/
    blurry/
    empty/
    filled/
    generated/
    handwritten/
```

Each directory contains a different kind of pictures.

# Random Sudoku grid generator

The script [`generator.py`](generator.py) generates random sudoku grids in `png` format.

> Generated grids are not feasible grids.

It is based on the [`pycairo`](https://github.com/pygobject/pycairo) Python library. It also make use of `numpy` and `img2pdf`.

## Install `pycairo`

Because it depends on the `cairo` C library, the installation of `pycairo` isn't the same for each platform.

* `Ubuntu`/`Debian`
    1. Install `pkg-config` and `cairo`.
        ```bash
        sudo apt install libcairo2-dev pkg-config python3-dev
        ```
    2. Install `pycairo` using `pip`.
        ```bash
        pip3 install pycairo
        ```

* `macOS`
    1. Install `pkg-config` and `cairo`.
        ```bash
        brew install cairo pkg-config
        ```
    2. Fix path according to [`stackoverflow.com`](https://stackoverflow.com/questions/55973489/trouble-installing-pycairo-through-pip3).
        ```bash
        export LDFLAGS="-L/usr/local/opt/libffi/lib"
        export PKG_CONFIG_PATH="/usr/local/opt/libffi/lib/pkgconfig"
        ```
    3. Install `pycairo` using `pip`.
        ```bash
        pip3 install pycairo
        ```

* `Windows`
    1. Download the proper `whl` file on [this site](https://www.lfd.uci.edu/~gohlke/pythonlibs/#pycairo) or use [pycairo-1.18.2-cp37-cp37m-win_amd64.whl](resources/whl/pycairo-1.18.2-cp37-cp37m-win_amd64.whl) instead.
    2. Install it using `pip`.
        ```bash
        pip install pycairo-1.18.2-cp37-cp37m-win_amd64.whl
        ```
