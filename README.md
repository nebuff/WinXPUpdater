# ThinkPad T4X WindowsXP Automated Driver Installer

---

## Overview

This tool automatically installs all essential drivers for the **ThinkPad T41** using either a **USB drive or CD**. It installs both drivers from the installation media and previously extracted driver setups from your system.

---

## Install

1. Extract the .zip found in the Latest Release to a USB or DISC
2. Plug-In or Insert the Drive into the WindowsXP Laptop you need Drivers on
3. Run the Install.vbx Script with Admin Privalges
4. Run Though the Software Wizards until it says Install Complete, If it does not and just stops, You can Manually Reboot your Computer

> [!WARNING]
> In the Middle of the Graphics Driver Installer your screen May Blink a Couple times, This is Expected! It is installing the New Drivers

> [!NOTE]
> If you Run into Issues, Please, Please, Please create a Issue in Github

---

## Included Drivers

1. **Graphics** – ATI/Intel video driver
2. **Ethernet** – Network driver
3. **Power Management** – IBM Power Management utilities
4. **Audio** – Sound driver
5. **WiFi** – Wireless driver

The script will run:

* **USB/CD installers** first
* **Extracted drivers** located in `C:\DRIVERS\WIN`

---

## Requirements

* Windows XP Home or Professional
* USB drive or CD containing the `drivers` folder and `setup.vbs` found in the Latest Release
* Administrative privileges to install drivers

---

## Folder Structure

Your USB/CD should look like this:

```
[USB/CD Root]
│
├── setup.vbs
└── drivers
    ├── graphics\setup.exe
    ├── ethernet\setup.exe
    ├── power\setup.exe
    ├── audio\setup.exe
    └── wifi\setup.exe
```

The extracted drivers on your system should be in:

```
C:\DRIVERS\WIN\
├── DISPLAY\Setup\setup.exe
├── ETHERNET\APPS\SETUP\SETUPBD\WIN32\SETUPBD.exe
├── IBMPM\SETUP\setup.exe
└── AUDIO\SETUP.exe
```

---

## Instructions

1. Insert the USB drive or CD containing the installer.
2. Double-click `setup.vbs` to start the installer.
3. The script will show GUI messages for each driver being installed.
4. Already installed drivers are **skipped automatically**.
5. After all installations, a **reboot prompt** will appear:

   * Click **Yes** to reboot immediately
   * Click **No** to reboot later

---

## Notes

* Make sure all driver files are present in the correct folders before running the installer.
* If a driver setup does not complete successfully, rerun the script. or Create a Github Issue
* The installer is designed to run sequentially; do **not close** the popups manually.
