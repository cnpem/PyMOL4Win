# Open Source PyMOL for Windows

Open source PyMOL is available free of charge. A pre-compiled open source PyMOL is available free from [Christoph Gohlke](https://www.cgohlke.com/) of the Department of Biomedical Engineering, University of California, Irvine.

This repository provides a method to install PyMOL v2.6 on Windows. If necessary, a portuguese version of this guide is available [here](https://github.com/LBC-LNBio/PyMOL4Win/blob/main/README_PT.md).

## Download & Installation

Follow these steps to install PyMOL v2.6:

1. Install the latest version of Python (v3.12.x) for Windows from [here](http://www.python.org/downloads/).

_Note_: Make sure the option to add environment variables is selected or add the folder of python.exe to system PATH.

2. Install required Python packages

```cmd
python -m pip install numpy
python -m pip install pmw
python -m pip install pyqt5
```

3. Download pre-compiled Open-Source PyMOL wheel files, compatible with Python 3.12 and Windows 64-bit, from the links below:

- [pymol-launcher](https://github.com/LBC-LNBio/PyMOL4Win/releases/latest/download/pymol_launcher-2.6-cp312-cp312-win_amd64.whl)
- [pymol](https://github.com/LBC-LNBio/PyMOL4Win/releases/latest/download/pymol-2.6.0a0-cp312-cp312-win_amd64.whl)

_Note_: You can check Python version on anaconda by typing `python --version`.

If you are using a different Python version or Windows 32-bits, please there are other pre-compiled versions [here](https://github.com/cgohlke/pymol-open-source-wheels/releases).

The filename structure is the following:

```cmd
pymol‑2.6.0a0‑cp312‑cp312‑win_amd64.whl
         \         \          \
          \         \          \___ for 64 bit Windows
           \         \
            \         \____________ for Python 3.12.x
             \
              \____________________ PyMOL version 2.6.0a0
```

4. Install wheel files

In the CMD window (not PowerShell!), switch to download directory (`C:\Users\<Your Username>\Downloads`):

```cmd
cd Downloads
```

Then, install `pymol_launcher-2.6-cp312-cp312-win_amd64.whl` by typing:

```cmd
python -m pip install --no-index --find-links="%CD%" pymol_launcher-2.6-cp312-cp312-win_amd64.whl
```

Finally, to install `pymol-2.6.0a0-cp312-cp312-win_amd64.whl`, run:

```cmd
pip install --upgrade --no-deps pymol-2.6.0a0-cp312-cp312-win_amd64.whl
```

_Note_: If you downloaded different files in **Step 4**, replace `pymol_launcher-2.6-cp312-cp312-win_amd64.whl` and `pymol-2.6.0a0-cp312-cp312-win_amd64.whl` by the downloaded wheel files.

5. Launch PyMOL v2.6

In the CMD window (not PowerShell!), run:

```cmd
where.exe pymol
pymol
```

Then, PyMOL v2.6 will be launched and ready to go.

6. (Optional) Create a shortcut to PyMOL

```cmd
where.exe pymol
```

The location of `pymol.exe` will be displayed. Navigate to the file location, right-click on `PyMOL.exe`, and copy it to your Desktop.
