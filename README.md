# Common env ![Build](https://github.com/nmarghetti/common_env/workflows/Build/badge.svg)

---

- [Description](#description)
- [Setup](#setup)
  - [Portable environment for Windows](#portable-environment-for-windows)
  - [Common configuration only](#common-configuration-only)
- [Features](#features)
- [Git](#git)
  - [Git guide](readme/README_git_guide.md)
- [Cmder](#cmder)
  - [Cmder shortcuts](#cmder-shortcuts)
- [Customization](#customization)
- [Usefull links](#usefull-links)

---

## Description

This project aim to facilitate the setup of a common environment for people with completely different computer skills (developper, tester, business analyst, etc.). It's first part facilitate a common usage of GIT and python for **Linux**, **macOS** and **Windows**. The second part, for Windows users, is focused on installing a portable tools environment.

1. **Common core**

   - **Git**: common configuration and aliases to simplify git usage, check this [**_GIT GUIDE_**](readme/README_git_guide.md).
   - **Python**: brings a simple way to create, list and switch between several python environments (eg. between python 2.x 3.x)

1. **Windows**

For Windows user it brings a portable environment with several applications already configured and integrated in [PortableApps](https://portableapps.com/) which also offer a huge catalog of other portable applications. Check the Features section to know more.

## Setup

### Portable environment for Windows

Download [**setup.cmd**](https://raw.githubusercontent.com/nmarghetti/common_env/master/tools/setup.cmd) and [setup.ini](https://raw.githubusercontent.com/nmarghetti/common_env/master/tools/setup.ini) (Right click -> "Save Link As...") into a folder preferably with no space (eg. "C:\PortableEnv"), execute setup.cmd and follow the instruction written in the terminal.

```text
C:/PortableEnv
├── setup.cmd
└── setup.ini
```

Check this [**installation guide**](readme/README_setup.md) for more details.

### Common configuration only

The common setup is as easy as follow:

```bash
# Clone the repository
git clone https://github.com/nmarghetti/common_env.git

# Run the setup
./common_env/scripts/setup.sh
```

## Features

1. ### **Common core**

   The common part works for the following environment:

   - Linux via bash or zsh
   - macOS via bash or zsh
   - Windows
     - [WSL](https://docs.microsoft.com/en-gb/windows/wsl/install-win10) (Windows Subsystem for Linux)
     - [Bash on Unbuntu on Windows](https://ubuntu.com/wsl) (that requires WSL)
     - Powershell by invoking wsl or bash (requires the corresponding one above)

   Either you are on **Windows**, **Linux** or **macOS** and using **bash** or **zsh**, you would get:

   - **Python** virtual environment easy to handle with few simple shell functions:
     - **pylist**: list your available python venv
     - **pycreate** [python_path][version]: create a venv name _version_ with python from _python_path_
     - **pyset** version: activate the venv _version_ (it has to exist from list given by "pylist")
     - **pyunset**: deactivate current venv
   - **Git** configured with some core settings and many useful aliases
     - core settings about whitespace, EOL, filemode, symlinks, long path, etc.
     - main coloration
     - many aliases to handle several usecases and for each it displays the full real git command invoked

1. ### **macOS**

   On macOs it will also install some extra package to have necessary GNU tools such as readlink, awk, sed, etc.

1. ### **Windows portable env**

If you are on Windows, you can get a portable development environment (it is not hardly installed in the system, all the applications are portable) with the following tools especially configured:

- **Visual Studio Code** with several extensions
- **Git for Windows** (Git-bash)
- **Cmder**
- **Python** (2.7)
- **Python** (3.8)
- **Node.js**
- C/C++ tools: **CMake**, **GCC**

You could optionnally get a bunch of other applications from [PortableApps](https://portableapps.com/):

- Notepad++
- Google Chrome
- Mozilla Firefox
- PuTTY
- 7-Zip
- Process Explorer
- etc.

Visual Studio Code and the other tools are configured to work together. It brings a common configuration between developpers to ensure to format source code, configuration file or even README the same way.\
Each developper can contribute to the tools and everyone would benefit from it.\
Any developper could join and install quickly everything like the others with only few simple steps.

## Git

If you are looking for an easy way to start with Git, you can follow [**this guide**](readme/README_git_guide.md).

You can define those environment variables to customize git:

- GIT_CMD_NOCOLOR=1 to not display real git command for aliases in color (as it can be a bit slow)
- GIT_CMD_NOECHO=1 to not display real git command for aliases

## Cmder

### Cmder shortcuts

1. Tasks

   - alt+shift+1: open task 1 --> open Git-bash
   - alt+shift+2: open task 2 --> ssh remote machine 1
   - etc.

1. Split screen

   - ctrl+alt+right arrow: split vertically
   - ctrl+alt+down arrow: split horizontally
   - ctrl+shift+arrow (up, down, left, right): change the focus to the terminal of the arrow direction
   - ctrl+alt+shift+arrow (up, down, left, right): increase the size of the current terminal in the arrow direction

1. Tabs

   - ctrl+tab: focus on next tab on the right
   - ctrl+shift+tab: focus on next tab on the left
   - win+alf+arrow (left, right): move the current tab to the arrow direction

## Usefull links

1. **Git**

   - [Git for Windows](https://git-scm.com/), [Git command description](https://git-scm.com/docs/git), [Git cheatsheet](https://ndpsoftware.com/git-cheatsheet.html)
   - [Reference Manual](https://git-scm.com/docs), [Pro Git online book](https://git-scm.com/book/en/v2), [Tutorials](https://git-scm.com/doc/ext)

1. **Python**

   - [Homepage](https://www.python.org/)
   - Documentation: [Python2.7](https://docs.python.org/2.7/) / [Python 3.x](https://docs.python.org/3/)
   - Portable Python packaging
     - PortablePython (not developped anymore): [homepage](https://portablepython.com/), [download](https://portablepython.com/wiki/Download/)
     - [WinPython](http://winpython.github.io/)
     - [PythonAnywhere](https://www.pythonanywhere.com/)
   - Other Python packaging
     - [Anaconda](https://www.anaconda.com/distribution/)
     - [Miniconda](https://docs.conda.io/en/latest/miniconda.html)
     - [Python(x-y)](http://python-xy.github.io/)

1. **Visual Studio Code**

   - [Portable mode](https://code.visualstudio.com/docs/editor/portable)
   - [Setup network](https://code.visualstudio.com/docs/setup/network)
   - [Command Line Interface](https://code.visualstudio.com/docs/editor/command-line)

1. **PortableApps**

   - [Homepage](https://portableapps.com/)
   - [App setting](https://portableapps.com/development/portableapps.com_format#appinfo)

1. **Other**

   - [Cmder](https://cmder.net/): [ConEmu](https://conemu.github.io/), [Clink](https://mridgers.github.io/clink/)
   - [Bash/Unix/Linux tutorial](https://www.tutorialspoint.com/unix_commands/bash.htm)
   - [Batch tutorial](https://www.tutorialspoint.com/batch_script/index.htm)
