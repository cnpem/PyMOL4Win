# Open Source PyMOL for Windows

Open source PyMOL is available free of charge. A pre-compiled open source PyMOL is available free from [[Christoph Gohlke of the Laboratory for Fluorescence Dynamics, University of California, Irvine](http://www.lfd.uci.edu/~gohlke/pythonlibs/#pymol)](https://www.lfd.uci.edu/~gohlke/pythonlibs/#pymol).

This repository provides a method to install PyMOL v2.6 on Windows. If necessary, a portuguese version of this guide is available [here](https://github.com/LBC-LNBio/PyMOL4Win/blob/main/README_PT.md).

## Download & Installation

Follow these steps to install PyMOL v2.6:

1. Install the latest version of Python (v3.11.x) for Windows from [here](http://www.python.org/downloads/). Make sure the option to add environment variables is selected or add the folder of python.exe to system PATH.
2. Install required Python packages

```bash
python -m pip install numpy
python -m pip install pmw
python -m pip install pyqt5
```

3. Download pre-compiled Open-Source PyMOL wheel files, compatible with Python 3.11 and Windows 64-bit, from the links below:

- [pymol-launcher](https://github.com/LBC-LNBio/PyMOL4Win/releases/latest/download/pymol_launcher-2.1-cp37-cp37m-win_amd64.whl)
- [pymol](https://github.com/LBC-LNBio/PyMOL4Win/releases/latest/download/pymol-2.4.0-cp37-cp37m-win_amd64.whl)

_Note_: You can check Python version on anaconda by typing `python --version`.

If you are using a different Python version or Windows 32-bits, please there are other pre-compiled versions [here](https://www.lfd.uci.edu/~gohlke/pythonlibs/#pymol).

The filename structure is the following:


```bash
pymol‑2.6.0a0‑cp311‑cp311‑win_amd64.whl
         \         \          \
	  \         \          \___ for 64 bit Windows
	   \         \
            \         \____________ for Python 3.7.x
             \
              \____________________ PyMOL version 2.6.0a0
```
