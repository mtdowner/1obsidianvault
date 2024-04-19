---
Program: Installing Python on Linux
---
[[Install Python on Linux]]

## Table of Contents

- [How to Install Python on Windows](https://realpython.com/installing-python/#how-to-install-python-on-windows)
    - [How to Check Your Python Version on Windows](https://realpython.com/installing-python/#how-to-check-your-python-version-on-windows)
    - [What Your Options Are](https://realpython.com/installing-python/#what-your-options-are)
    - [How to Install From the Microsoft Store](https://realpython.com/installing-python/#how-to-install-from-the-microsoft-store)
    - [How to Install From the Full Installer](https://realpython.com/installing-python/#how-to-install-from-the-full-installer)
- [How to Install Python on macOS](https://realpython.com/installing-python/#how-to-install-python-on-macos)
    - [How to Check Your Python Version on a Mac](https://realpython.com/installing-python/#how-to-check-your-python-version-on-a-mac)
    - [What Your Options Are](https://realpython.com/installing-python/#what-your-options-are_1)
    - [How to Install From the Official Installer](https://realpython.com/installing-python/#how-to-install-from-the-official-installer)
    - [How to Install From Homebrew](https://realpython.com/installing-python/#how-to-install-from-homebrew)
- [How to Install Python on Linux](https://realpython.com/installing-python/#how-to-install-python-on-linux)
    - [How to Check Your Python Version on Linux](https://realpython.com/installing-python/#how-to-check-your-python-version-on-linux)
    - [What Your Options Are](https://realpython.com/installing-python/#what-your-options-are_2)
    - [How to Install on Ubuntu and Linux Mint](https://realpython.com/installing-python/#how-to-install-on-ubuntu-and-linux-mint)
    - [How to Install on Debian Linux](https://realpython.com/installing-python/#how-to-install-on-debian-linux)
    - [How to Install on openSUSE](https://realpython.com/installing-python/#how-to-install-on-opensuse)
    - [How to Install on CentOS and Fedora](https://realpython.com/installing-python/#how-to-install-on-centos-and-fedora)
    - [How to Install on Arch Linux](https://realpython.com/installing-python/#how-to-install-on-arch-linux)
    - [How to Build Python From Source Code](https://realpython.com/installing-python/#how-to-build-python-from-source-code)
- [How to Install Python on iOS](https://realpython.com/installing-python/#how-to-install-python-on-ios)
- [How to Install Python on Android](https://realpython.com/installing-python/#how-to-install-python-on-android)
- [Online Python Interpreters](https://realpython.com/installing-python/#online-python-interpreters)
- [Conclusion](https://realpython.com/installing-python/#conclusion)

**In this tutorial you’ll learn how to:**

- Check which **version** of Python, if any, is installed on your machine
- Install or update Python on **Windows**, **macOS**, and **Linux**
- Use Python on **mobile devices** like phones or tablets
- Use Python on the Web with **online interpreters**

## How to Install Python on Windows[](https://realpython.com/installing-python/#how-to-install-python-on-windows "Permanent link")

There are three installation methods on Windows:

1. The Microsoft Store
2. The full installer
3. Windows Subsystem for Linux

### How to Check Your Python Version on Windows[](https://realpython.com/installing-python/#how-to-check-your-python-version-on-windows "Permanent link")

To check if you already have Python on your Windows machine, first open a command-line application, such as PowerShell.

**Tip:** Here’s how you open PowerShell:

1. Press the Win key.
2. Type `PowerShell`.
3. Press Enter.

Alternatively, you can right-click the _Start_ button and select _Windows PowerShell_ or _Windows PowerShell (Admin)_.

You can also use `cmd.exe` or [Windows Terminal](https://www.microsoft.com/en-us/p/windows-terminal/9n0dx20hk701?activetab=pivot:overviewtab).

With the command line open, type in the following command and press Enter:

Windows Command Prompt

`C:\> python --version Python 3.8.4`

Using the `--version` switch will show you the version that’s installed. Alternatively, you can use the `-V` switch:

Windows Command Prompt

`C:\> python -V Python 3.8.4`

In either case, if you see a version less than `3.8.4`, which was the most recent version at the time of writing, then you’ll want to upgrade your installation.

**Note:** If you don’t have a version of Python on your system, then both of the above commands will launch the Microsoft Store and redirect you to the Python application page. You’ll see how to complete the installation from the Microsoft Store in the next section.

If you’re interested in where the installation is located, then you can use the `where.exe` command in `cmd.exe` or PowerShell:

Windows Command Prompt

`C:\> where.exe python C:\Users\mertz\AppData\Local\Programs\Python\Python37-32\python.exe`


> [!NOTE] Title
> Contents
Note that the `where.exe` command will work only if Python has been installed for your user account.

### What Your Options Are[](https://realpython.com/installing-python/#what-your-options-are "Permanent link")

As mentioned earlier, there are three ways to install the official Python distribution on Windows:

1. **Microsoft Store package:** The most straightforward installation method on Windows involves installing from the Microsoft Store app. This is recommended for beginner Python users looking for an easy-to-set-up interactive experience.
    
2. **Full Installer:** This approach involves downloading Python directly from the [Python.org website](https://www.python.org/). This is recommended for intermediate and advanced developers who need more control during the setup process.
    
3. **Windows Subsystem for Linux (WSL):** The WSL allows you to run a Linux environment directly in Windows. You can learn how to enable the WSL by reading the [Windows Subsystem for Linux Installation Guide for Windows 10](https://docs.microsoft.com/en-us/windows/wsl/install-win10).

In this section, we’ll focus on only the first two options, which are the most popular installation methods in a Windows environment.

If you want to install in the WSL, then you can read the [Linux section](https://realpython.com/installing-python/#how-to-install-python-on-linux) of this tutorial after you’ve installed the Linux distribution of your choice.

**Note:** You can also complete the installation on Windows using alternative distributions, such as [Anaconda](https://www.anaconda.com/), but this tutorial covers only official distributions.

Anaconda is a popular platform for doing scientific computing and data science with Python. To learn how to install Anaconda on Windows, check out [Setting Up Python for Machine Learning on Windows](https://realpython.com/python-windows-machine-learning-setup/).

The two official Python installers for Windows aren’t identical. The Microsoft Store package has some important limitations.

#### Limitations of the Microsoft Store Package[](https://realpython.com/installing-python/#limitations-of-the-microsoft-store-package "Permanent link")

The official Python documentation has this to say about the Microsoft Store package:

> The Microsoft Store package is an easily installable Python interpreter that is intended mainly for interactive use, for example, by students. ([Source](https://docs.python.org/3/using/windows.html#the-microsoft-store-package))

The key takeaway here is that the Microsoft Store package is “intended mainly for interactive use.” That is, the Microsoft Store package is designed to be used by students and people learning to use Python for the first time.

In addition to targeting beginning Pythonistas, the Microsoft Store package has limitations that make it ill-suited for a professional development environment. In particular, it [does not have full write access to shared locations](https://docs.python.org/3/using/windows.html#known-issues) such as `TEMP` or the registry.

#### Windows Installer Recommendations[](https://realpython.com/installing-python/#windows-installer-recommendations "Permanent link")

If you’re new to Python and focused primarily on learning the language rather than building professional software, then you should install from the Microsoft Store package. This offers the shortest and easiest path to getting started with minimal hassle.

On the other hand, if you’re an experienced developer looking to develop professional software in a Windows environment, then the official Python.org installer is the right choice. Your installation won’t be limited by Microsoft Store policies, and you can control where the executable is installed and even [add Python to `PATH`](https://realpython.com/add-python-to-path/) if necessary.

### How to Install From the Microsoft Store[](https://realpython.com/installing-python/#how-to-install-from-the-microsoft-store "Permanent link")

If you’re new to Python and looking to get started quickly, then the Microsoft Store package is the best way to get up and running without any fuss. You can install from the Microsoft Store in two steps.

#### Step 1: Open the Python App Page in the Microsoft Store[](https://realpython.com/installing-python/#step-1-open-the-python-app-page-in-the-microsoft-store "Permanent link")

Open the Microsoft Store app and search for `Python`.

You’ll likely see multiple versions that you can choose to install:

[![The Microsoft Store search results for "Python"](https://files.realpython.com/media/Screen_Shot_2020-07-16_at_11.06.17_AM.4b41c401c5aa.png)](https://files.realpython.com/media/Screen_Shot_2020-07-16_at_11.06.17_AM.4b41c401c5aa.png)

Select _Python 3.8_, or the highest version number you see available in the app, to open the installation page.

**Warning:** Make sure that the Python application you’ve selected is created by the **Python Software Foundation**.

The official Microsoft Store package will always be free, so if the application costs money, then it’s the **wrong** application.

Alternatively, you can open PowerShell and type the following command:

Windows Command Prompt

`C:\> python`

If you don’t already have a version of Python on your system, then when you press Enter, the Microsoft Store will automatically launch and take you to the latest version of Python in the store.

#### Step 2: Install the Python App[](https://realpython.com/installing-python/#step-2-install-the-python-app "Permanent link")

After you’ve selected the version to be installed, follow these steps to complete the installation:

1. Click _Get_.
    
2. Wait for the application to download. When it’s finished downloading, the _Get_ button will be replaced with a button that says _Install on my devices_.
    
3. Click _Install on my devices_ and select the devices on which you’d like to complete the installation.
    
4. Click _Install Now_ and then _OK_ to start the installation.
    
5. If the installation was successful, then you’ll see the message “This product is installed” at the top of the Microsoft Store page.
    

Congratulations! You now have access to Python, including [`pip`](https://realpython.com/what-is-pip/) and [IDLE](https://realpython.com/python-idle/)!

### How to Install From the Full Installer[](https://realpython.com/installing-python/#how-to-install-from-the-full-installer "Permanent link")

For professional developers who need a full-featured Python development environment, installing from the full installer is the right choice. It offers more customization and control over the installation than installing from the Microsoft Store.

You can install from the full installer in two steps.

#### Step 1: Download the Full Installer[](https://realpython.com/installing-python/#step-1-download-the-full-installer "Permanent link")

Follow these steps to download the full installer:

1. Open a browser window and navigate to the Python.org [Downloads page for Windows](https://www.python.org/downloads/windows/).
    
2. Under the “Python Releases for Windows” heading, click the link for the _Latest Python 3 Release - Python 3.x.x_. As of this writing, the latest version was Python 3.8.4.
    
3. Scroll to the bottom and select either _Windows x86-64 executable installer for 64-bit_ or _Windows x86 executable installer for 32-bit_.
    

If you aren’t sure whether to select the 32-bit or the 64-bit installer, then you can expand the box below to help you decide.

32-bit or 64-bit Python?Show/Hide

When the installer is finished downloading, move on to the next step.

#### Step 2: Run the Installer[](https://realpython.com/installing-python/#step-2-run-the-installer "Permanent link")

Once you’ve chosen and downloaded an installer, run it by double-clicking on the downloaded file. A dialog box like the one below will appear:

[![Windows installation dialog](https://files.realpython.com/media/Screen_Shot_2020-07-16_at_11.19.15_AM.6e62bfc6eede.png)](https://files.realpython.com/media/Screen_Shot_2020-07-16_at_11.19.15_AM.6e62bfc6eede.png)

There are four things to notice about this dialog box:

1. The default install path is in the [`AppData/` directory](https://superuser.com/questions/656003/why-is-python-for-windows-not-installed-in-programfiles-c-program-files) of the current Windows user.
    
2. The _Customize installation_ button can be used to customize the installation location and which additional features get installed, including `pip` and IDLE.
    
3. The _Install launcher for all users (recommended)_ checkbox is checked default. This means every user on the machine will have access to the [`py.exe` launcher](https://docs.python.org/3/using/windows.html#launcher). You can uncheck this box to restrict Python to the current Windows user.
    
4. The _Add Python 3.8 to `PATH`_ checkbox is unchecked by default. There are [several reasons](https://discuss.python.org/t/could-we-add-python-to-system-path-by-default/3067) that you might not want Python on `PATH`, so make sure you understand the implications before you check this box.
    

The full installer gives you total control over the installation process.

**Warning:** If you don’t know what [`PATH`](https://realpython.com/add-python-to-path/) is, then it’s highly recommended that you **do not** install with the full installer. Use the [Microsoft Store package](https://realpython.com/installing-python/#how-to-install-from-the-microsoft-store) instead.

Customize the installation to meet your needs using the options available on the dialog box. Then click _Install Now_. That’s all there is to it!

Congratulations—you now have the latest version of Python 3 on your Windows machine!

## How to Install Python on macOS[](https://realpython.com/installing-python/#how-to-install-python-on-macos "Permanent link")

Python 2 comes preinstalled on older versions of macOS. This is no longer the case for current versions of macOS, [starting with macOS Catalina](https://developer.apple.com/documentation/macos-release-notes/macos-catalina-10_15-release-notes#Scripting-Language-Runtimes).

There are two installation methods on macOS:

1. The official installer
2. The Homebrew package manager

In this section, you’ll learn how to check which version of Python, if any, is installed on your macOS device. You’ll also learn which of the two installation methods you should use.

### How to Check Your Python Version on a Mac[](https://realpython.com/installing-python/#how-to-check-your-python-version-on-a-mac "Permanent link")

To check which Python version you have on your Mac, first open a command-line application, such as [Terminal](https://realpython.com/courses/using-terminal-macos/).

**Tip:** Here’s how you open Terminal:

1. Press the Cmd+Space keys.
2. Type `Terminal`.
3. Press Enter.

Alternatively, you can open Finder and navigate to _Applications → Utilities → Terminal_.

With the command line open, type in the following commands:

Shell

`# Check the system Python version $ python --version  # Check the Python 2 version $ python2 --version  # Check the Python 3 version $ python3 --version`

If you have Python on your system, then one or more of these commands should respond with a version number.

For example, if Python 3.8.4 were already set up on your computer, then the `python3` command would display that version number:

Shell

`$ python3 --version Python 3.8.4`

Alternatively to `--version`, you can use the shorter `-V` switch:

Shell

`$ python3 -V Python 3.8.4`

Either of these switches will give you the version number of the Python installation that the command is associated with.

You’ll want to get the latest version of Python if any of these conditions is true:

- None of the above commands returns a version number.
- The only version you see displayed is in the Python 2.X series.
- You have a version of Python 3 that isn’t the latest available, which was version 3.8.4 as of this writing.

### What Your Options Are[](https://realpython.com/installing-python/#what-your-options-are_1 "Permanent link")

There are two ways to install the official Python distribution on macOS:

1. **The official installer:** This method involves downloading the official installer from the Python.org website and running it on your machine.
    
2. **The Homebrew package manager:** This method involves downloading and installing [the Homebrew package manager](https://brew.sh/) if you don’t already have it installed, and then typing a command into a terminal application.
    

Both the official installer and the Homebrew package manager will work, but only the official installer is maintained by the Python Software Foundation.

**Note:** You can also complete the installation on macOS using alternative distributions, such as [Anaconda](https://www.anaconda.com/), but this tutorial covers only official distributions.

Anaconda is a popular platform for doing scientific computing and data science with Python. To learn how to install Anaconda on macOS, check out the [macOS installation guide](https://docs.anaconda.com/anaconda/install/mac-os/) from the official Anaconda documentation.

The distributions installed by the official installer and the Homebrew package manager aren’t identical. Installing from Homebrew has some limitations.

#### Limitations of Installing From Homebrew[](https://realpython.com/installing-python/#limitations-of-installing-from-homebrew "Permanent link")

The Python distribution for macOS available on Homebrew [doesn’t include the Tcl/Tk dependency](https://github.com/Homebrew/homebrew-core/pull/34424) required by the Tkinter module. Tkinter is the standard library module for developing [graphical user interfaces in Python](https://realpython.com/python-gui-tkinter/) and is in fact an interface for the [Tk GUI toolkit](https://www.tcl.tk/), which isn’t part of Python.

Homebrew doesn’t install the Tk GUI toolkit dependency. Instead, it relies on an existing version installed on your system. The system version of Tcl/Tk may be outdated or missing entirely and could prevent you from importing the Tkinter module.

#### macOS Installer Recommendations[](https://realpython.com/installing-python/#macos-installer-recommendations "Permanent link")

The Homebrew package manager is a popular method for installing Python on macOS because it’s easy to manage from the command line and offers commands to upgrade Python without having to go to a website. Because Homebrew is a command-line utility, it can be automated with bash scripts.

However, the Python distribution offered by Homebrew isn’t controlled by the Python Software Foundation and could change at any time. The most reliable method on macOS is to use the official installer, especially if you plan on doing [Python GUI programming with Tkinter](https://realpython.com/python-gui-tkinter/).

### How to Install From the Official Installer[](https://realpython.com/installing-python/#how-to-install-from-the-official-installer "Permanent link")

Installing Python from the official installer is the most reliable installation method on macOS. It includes all the system dependencies needed for developing applications with Python.

You can install from the official installer in two steps.

#### Step 1: Download the Official Installer[](https://realpython.com/installing-python/#step-1-download-the-official-installer "Permanent link")

Follow these steps to download the full installer:

1. Open a browser window and navigate to the Python.org [Downloads page for macOS](https://www.python.org/downloads/mac-osx/).
    
2. Under the “Python Releases for Mac OS X” heading, click the link for the _Latest Python 3 Release - Python 3.x.x_. As of this writing, the latest version was Python 3.8.4.
    
3. Scroll to the bottom and click _macOS 64-bit installer_ to start the download.
    

When the installer is finished downloading, move on to the next step.

#### Step 2: Run the Installer[](https://realpython.com/installing-python/#step-2-run-the-installer_1 "Permanent link")

Run the installer by double-clicking the downloaded file. You should see the following window:

[![The macOS installation window.](https://files.realpython.com/media/Screen_Shot_2020-07-15_at_8.31.24_AM.2e5b82dbc195.png)](https://files.realpython.com/media/Screen_Shot_2020-07-15_at_8.31.24_AM.2e5b82dbc195.png)

Follow these steps to complete the installation:

1. Press _Continue_ a few times until you’re asked to agree to the software license agreement. Then click _Agree_.
    
2. You’ll be shown a window that tells you the install destination and how much space it will take. You most likely don’t want to change the default location, so go ahead and click _Install_ to start the installation.
    
3. When the installer is finished copying files, double-click the _Install Certificates_ command in the finder window to make sure your SSL root certificates are updated.
    

Congratulations—you now have the latest version of Python 3 on your macOS computer!

### How to Install From Homebrew[](https://realpython.com/installing-python/#how-to-install-from-homebrew "Permanent link")

For users who need to install from the command line, especially those who won’t be using Python to develop graphical user interfaces with the Tkinter module, the Homebrew package manager is a good option. You can install from the Homebrew package manager in two steps.

#### Step 1: Install Homebrew[](https://realpython.com/installing-python/#step-1-install-homebrew "Permanent link")

If you already have Homebrew installed, then you can skip this step. If you don’t have Homebrew installed, then use the following procedure to install Homebrew:

1. Open a browser and navigate to [http://brew.sh/](http://brew.sh/).
    
2. You should see a command for installing Homebrew near the top of the page under the tile “Install Homebrew.” This command will be something like the following:
    
    Shell
    
    `$ /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"`
    
    Highlight the command with your cursor and press Cmd+C to copy it to your clipboard.
    
3. Open a terminal window and paste the command, then press Enter. This will begin the Homebrew installation.
    
4. Enter your macOS user password when prompted.
    

Depending on your Internet connection, it may take a few minutes to download all of Homebrew’s required files. Once the installation is complete, you’ll end up back at the shell prompt in your terminal window.

**Note:** If you’re doing this on a fresh install of macOS, you may get a pop-up alert asking you to **install Apple’s command line developer tools.** These tools are necessary for installation, so you can confirm the dialog box by clicking _Install_.

After the developer tools are installed, you’ll need to press Enter to continue installation of Homebrew.

Now that Homebrew is installed, you’re ready to install Python.

#### Step 2: Install Python[](https://realpython.com/installing-python/#step-2-install-python "Permanent link")

Follow these steps to complete the installation with Homebrew:

1. Open a terminal application.
    
2. Type in the following command to upgrade Homebrew:
    
    Shell
    
    `$ brew update && brew upgrade`
    

Installing with Homebrew is now as straightforward as running the command `brew install python3`. This will download and set up the latest version of Python on your machine.

You can make sure everything went correctly by testing if you can access Python from the terminal:

1. Open a terminal.
    
2. Type `pip3` and press Enter.
    
3. You should see the help text from [Python’s `pip` package manager](https://realpython.com/what-is-pip/). If you get an error message running `pip3`, then go through the install steps again to make sure you have a working installation.
    

Congratulations—you now have Python on your macOS system!

## How to Install Python on Linux[](https://realpython.com/installing-python/#how-to-install-python-on-linux "Permanent link")

There are two installation methods on Linux:

1. Using your operating system’s package manager
2. Building Python from source code

In this section, you’ll learn how to check which version of Python, if any, is on your Linux computer. You’ll also learn which of the two installation methods you should use.

### How to Check Your Python Version on Linux[](https://realpython.com/installing-python/#how-to-check-your-python-version-on-linux "Permanent link")

Many Linux distributions come packaged with Python, but it probably won’t be the latest version and may even be Python 2 instead of Python 3. You should check the version to make sure.

To find out which version of Python you have, open a [terminal](https://realpython.com/courses/using-terminal-linux/) window and try the following commands:

Shell

`# Check the system Python version $ python --version  # Check the Python 2 version $ python2 --version  # Check the Python 3 version $ python3 --version`

If you have Python on your machine, then one or more of these commands should respond with a version number.

For example, if you already had Python 3.6.10 on your computer, then the `python3 --version` command would display that version number:

Shell

`$ python3 --version Python 3.8.4`

Alternatively to `--version`, you can use the shorter `-V` switch:

Shell

`$ python3 -V Python 3.8.4`

Either of these switches will give you the version number of the Python installation that the command is associated with.

You’ll want to get the latest version of Python if your current version is in the Python 2.X series or is not the latest version of Python 3 available, which was 3.8.4 as of this writing.

### What Your Options Are[](https://realpython.com/installing-python/#what-your-options-are_2 "Permanent link")

There are two ways to install the official Python distribution on Linux:

1. **Install from a package manager:** This is the most common installation method on most Linux distributions. It involves running a command from the command line.
    
2. **Build from source code:** This method is more difficult than using a package manager. It involves running a series of commands from the command line as well as making sure you have the correct dependencies installed to compile the Python source code.
    

Not every Linux distribution has a package manager, and not every package manager has Python in its package repository. Depending on your operating system, building Python from source code might be your only option.

**Note:** You can also complete the installation on Linux using alternative distributions, such as [Anaconda](https://www.anaconda.com/), but this tutorial covers only official distributions.

Anaconda is a popular platform for doing scientific computing and data science with Python. To learn how to install Anaconda on Linux, check out the [Linux installation guide](https://docs.anaconda.com/anaconda/install/linux/) in the official Anaconda documentation.

Which installation method you use mainly boils down to whether your Linux OS has a package manager and whether you need to control the details of the installation.

#### Linux Installation Recommendations[](https://realpython.com/installing-python/#linux-installation-recommendations "Permanent link")

The most popular way to install Python on Linux is with your operating system’s package manager, which is a good choice for most users. However, depending on your Linux distribution, Python may not be available through a package manager. In this case, you’ll need to build Python from source code.

There are three main reasons that you might choose to build Python from source code:

1. You can’t download Python from your operating system’s package manager.
    
2. You need to control how Python gets compiled, such as when you want to lower the memory footprint on embedded systems.
    
3. You want to try out beta versions and release candidates of the latest and greatest version before it’s generally available.
    

To complete the installation on your Linux machine, find your Linux distribution below and follow the steps provided.

### How to Install on Ubuntu and Linux Mint[](https://realpython.com/installing-python/#how-to-install-on-ubuntu-and-linux-mint "Permanent link")

In this section, you’ll learn how to install Python using Ubuntu’s `apt` package manager. If you’d like to build Python from source code, skip ahead to the [How to Build Python From Source Code](https://realpython.com/installing-python/#how-to-build-python-from-source-code) section.

**Note:** Linux Mint users can skip to the “Linux Mint and Ubuntu 17 and below” section.

Depending on the version of the Ubuntu distribution you run, the process for setting up Python on your system will vary. You can determine your local Ubuntu version by running the following command:

Shell

`$ lsb_release -a No LSB modules are available. Distributor ID: Ubuntu Description:    Ubuntu 16.04.4 LTS Release:        16.04 Codename:       xenial`

Follow the instructions below that match the version number you see under `Release` in the console output:

- **Ubuntu 18.04, Ubuntu 20.04 and above:** Python 3.8 doesn’t come by default on Ubuntu 18.04 and above, but it is available in the Universe repository. To install version 3.8, open a terminal application and type the following commands:
    
    Shell
    
    `$ sudo apt-get update $ sudo apt-get install python3.8 python3-pip`
    
    Once the installation is complete, you can run Python 3.8 with the `python3.8` command and `pip` with the `pip3` command.
    
- **Linux Mint and Ubuntu 17 and below:** Python 3.8 isn’t in the Universe repository, so you need to get it from a Personal Package Archive (PPA). For example, to install from the [“deadsnakes” PPA](https://launchpad.net/~deadsnakes/+archive/ubuntu/ppa), use the following commands:
    
    Shell
    
    `$ sudo add-apt-repository ppa:deadsnakes/ppa $ sudo apt-get update $ sudo apt-get install python3.8 python3-pip`
    
    Once the installation is complete, you can run Python 3.8 with the `python3.8` command and run `pip` with the `pip3` command.
    

Congratulations! You now have Python 3 set up on your machine!

### How to Install on Debian Linux[](https://realpython.com/installing-python/#how-to-install-on-debian-linux "Permanent link")

Before you can install Python 3.8 on Debian, you’ll need to install the `sudo` command. To install it, execute the following commands in a terminal:

Shell

`$ su $ apt-get install sudo $ sudo vim /etc/sudoers`

After that, open the `/etc/sudoers` file using the `sudo vim` command or your favorite text editor. Add the following line of text to the end of the file, replacing `your_username` with your actual username:

Text

`your_username ALL=(ALL) ALL`

Now you can skip ahead to the [How to Build Python From Source Code](https://realpython.com/installing-python/#how-to-build-python-from-source-code) section to finish installing Python.

### How to Install on openSUSE[](https://realpython.com/installing-python/#how-to-install-on-opensuse "Permanent link")

Building from source is the most reliable way to set up Python on openSUSE. To do that, you’ll need to install the development tools, which can be done in `YaST` via the menus or by using `zypper`:

Shell

`$ sudo zypper install -t pattern devel_C_C`

This might take a while to complete as it installs over 150 packages. Once it’s completed, skip ahead to the [How to Build Python From Source Code](https://realpython.com/installing-python/#how-to-build-python-from-source-code) section.

### How to Install on CentOS and Fedora[](https://realpython.com/installing-python/#how-to-install-on-centos-and-fedora "Permanent link")

Python 3.8 isn’t available in the CentOS and Fedora repositories, so you’ll have to build Python from source code. Before you compile Python, though, you need to make sure your system is prepared.

First, update the [`yum` package manager](http://yum.baseurl.org/):

Shell

`$ sudo yum -y update`

Once `yum` finishes updating, you can install the necessary build dependencies with the following commands:

Shell

`$ sudo yum -y groupinstall "Development Tools" $ sudo yum -y install gcc openssl-devel bzip2-devel libffi-devel`

When everything is finished installing, skip ahead to the [How to Build Python From Source Code](https://realpython.com/installing-python/#how-to-build-python-from-source-code) section.

### How to Install on Arch Linux[](https://realpython.com/installing-python/#how-to-install-on-arch-linux "Permanent link")

Arch Linux is fairly diligent about keeping up with Python releases. It’s likely you already have the latest version. If not, use the following command to update Python:

Shell

`$ packman -S python`

When Python is finished updating, you should be all set!

### How to Build Python From Source Code[](https://realpython.com/installing-python/#how-to-build-python-from-source-code "Permanent link")

Sometimes your Linux distribution doesn’t have the latest version of Python, or maybe you just want to be able to build the latest, greatest version yourself. Here are the steps you need to take to build Python from source:

#### Step 1: Download the Source Code[](https://realpython.com/installing-python/#step-1-download-the-source-code "Permanent link")

To start, you need to get the Python source code. Python.org makes this fairly straightforward. If you go to the [Downloads](https://www.python.org/downloads/source/) page, then you’ll see the latest source for Python 3 at the top. Just make sure you don’t grab Legacy Python, Python 2!

When you select the Python 3 version, you’ll see a “Files” section at the bottom of the page. Select _Gzipped source tarball_ and download it to your machine. If you prefer a command-line method, you can use `wget` to download the file to your current directory:

Shell

`$ wget https://www.python.org/ftp/python/3.8.4/Python-3.8.4.tgz`

When the tarball finishes downloading, there are a few things you’ll need to do to prepare your system for building Python.

#### Step 2: Prepare Your System[](https://realpython.com/installing-python/#step-2-prepare-your-system "Permanent link")

There are a few distro-specific steps involved in building Python from scratch. The goal of each step is the same on all distros, but you might need to translate to your distribution if it doesn’t use `apt-get`:

1. First, update your package manager and upgrade your packages:
    
    Shell
    
    `$ sudo apt-get update $ sudo apt-get upgrade`
    
2. Next, make sure you have all of the build requirements installed:
    
    Shell
    
    `# For apt-based systems (like Debian, Ubuntu, and Mint) $ sudo apt-get install -y make build-essential libssl-dev zlib1g-dev \        libbz2-dev libreadline-dev libsqlite3-dev wget curl llvm \        libncurses5-dev libncursesw5-dev xz-utils tk-dev  # For yum-based systems (like CentOS) $ sudo yum -y groupinstall "Development Tools" $ sudo yum -y install gcc openssl-devel bzip2-devel libffi-devel`
    
    It’s fine if you already have some of the requirements installed on your system. You can execute the above commands and any existing packages will not be overwritten.
    

Now that your system is ready to go, it’s time to start building Python!

#### Step 3: Build Python[](https://realpython.com/installing-python/#step-3-build-python "Permanent link")

1. Once you have the prerequisites and the TAR file, you can unpack the source into a directory. Note that the following command will create a new directory called `Python-3.8.3` under the one you’re in:
    
    Shell
    
    `$ tar xvf Python-3.8.4.tgz $ cd Python-3.8.4`
    
2. Now you need to run the `./configure` tool to prepare the build:
    
    Shell
    
    `$ ./configure --enable-optimizations --with-ensurepip=install`
    
    The `enable-optimizations` flag will enable some optimizations within Python to make it run about 10 percent faster. Doing this may add twenty or thirty minutes to the compilation time. The `with-ensurepip=install` flag will install `pip` bundled with this installation.
    
3. Next, you build Python using `make`. The `-j` option simply tells `make` to split the building into parallel steps to speed up the compilation. Even with the parallel builds, this step can take several minutes:
    
    Shell
    
    `$ make -j 8`
    
4. Finally, you’ll want to install your new version of Python. You’ll use the `altinstall` target here to avoid overwriting the system Python. Since you’re installing into `/usr/bin`, you’ll need to run as root:
    
    Shell
    
    `$ sudo make altinstall`
    

It might take a while to finish installation. Once it’s done, you can verify that Python is set up correctly.

#### Step 4: Verify Your Installation[](https://realpython.com/installing-python/#step-4-verify-your-installation "Permanent link")

Test that the `python3.8 --version` command returns the latest version:

Shell

`$ python3.8 --version Python 3.8.4`

If you see `Python 3.8.4`, then you’re all set!

If you have some extra time on your hands, you can also run the [test suite](https://devguide.python.org/runtests/) to make sure everything is working properly on your system.

To run the test suite, type the following command:

Shell

`$ python3.8 -m test`

You’ll probably want to find something else to do for a while, as your computer will be running tests for some time. If all the tests pass, then you can be confident that your brand-new Python build is working as expected!


## Python 3.12

```bash
apt update && apt upgrade -y
apt install software-properties-common -y
add-apt-repository ppa:deadsnakes/ppa

apt update
apt install python3.12

python3.12 --version
# 3.12.0

curl -sS https://bootstrap.pypa.io/get-pip.py | python3.12 
- [ ] - [ ] 

pip3.12 -V
# pip 23.2.1 from /usr/local/lib/python3.12/site-packages/pip (python 3.12)
```
