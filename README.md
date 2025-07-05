# Cursor AI IDE Installer for Ubuntu 24.04

This repository provides a simple script to install or update the Cursor AI IDE on Ubuntu 24.04. The script supports both automatic download of the latest AppImage and manual installation from a local file.

---

## 📝 Version History

### 1.1 (Current)
**Added figlet Library for Enhanced Terminal Display:**

To improve user experience, the script now uses the `figlet` library to display banners and ASCII art in the terminal. This makes the installation and update process more visually appealing and engaging.

- The script will automatically check for and install `figlet` if it is not already present on your system.
- Banners such as "Cursor AI IDE" and a cat ASCII art are shown at the start of the script for a more welcoming interface.

**Example output:**
```
  / ____/_  ________________  _____   /   |  /  _/  /  _/ __ \/ ____/
 / /   / / / / ___/ ___/ __ \/ ___/  / /| |  / /    / // / / / __/   
/ /___/ /_/ / /  (__  ) /_/ / /     / ___ |_/ /   _/ // /_/ / /___   
\____/\__,_/_/  /____/\____/_/     /_/  |_/___/  /___/_____/_____/   
                                                                     
For Ubuntu 24.04 LTS
-------------------------------------------------                                                                     
  /\_/\
 ( o.o )
  > ^ <
-------------------------------------------------
1. Install Cursor
2. Update Cursor
Note: If the menu reappears after choosing 1 or 2, please check the notification above for any issues.
-------------------------------------------------
```
This helps users quickly recognize the script's purpose and provides a more pleasant terminal experience.

### 1.0 
- Initial release for Ubuntu 24.04
- Automatic download of the latest Cursor AppImage from the official website
- Option to specify a local AppImage file path
- Icon selection during installation
- Easy update process with the same options as installation
- Clean user prompts and error handling

---

## Prerequisites
- Ubuntu 24.04 (or compatible)
- Internet connection
- `sudo` privileges
- `curl`, `wget`, `jq`, and `rsync` (the script will attempt to install them if missing)

---

## ✨ Features
- **Automatic Download:** Fetch and install the latest Cursor AppImage with a single command.
- **Manual Path Option:** Use a previously downloaded AppImage if you prefer.
- **Icon Selection:** Choose your preferred icon during setup.
- **Easy Update:** Update Cursor to the latest version using the same script.

---

## 🎨 Available Icons
- <img src="images/cursor-icon.png" alt="Cursor Icon" width="24"/> `cursor-icon.png` – Standard Cursor logo with blue background
- <img src="images/cursor-black-icon.png" alt="Cursor Black Icon" width="24"/> `cursor-black-icon.png` – Cursor logo with dark/black background

You will be prompted to choose one of these icons during installation.

---

## 🚀 Installation & Update Steps

1. **Download the Script**
    - Clone this repository or download the `manage_cursor.sh` file.
    - Make the script executable:
      ```zsh
      chmod +x manage_cursor.sh
      ```

2. **Run the Script**
    - Start the script:
      ```zsh
      ./manage_cursor.sh
      ```
    - Follow the menu prompts:
      - Choose '1' to **Install Cursor**
      - Choose '2' to **Update Cursor**
    - You will be asked how to provide the Cursor AppImage:
      - **Option 1 (Recommended):** Auto-download the latest version
      - **Option 2:** Specify the local file path
    - You will also be prompted to enter the icon filename (e.g., `cursor-icon.png` or `cursor-black-icon.png`).

3. **Launch Cursor**
    - After installation, find "Cursor AI IDE" in your application menu.
    - Or launch from the terminal:
      ```zsh
      /opt/Cursor/AppRun --no-sandbox
      ```

---

## 🛠️ What the Script Does
- Installs or updates Cursor AI IDE
- Checks for and installs required tools (`curl`, `wget`, `jq`, `rsync`)
- Downloads and extracts the Cursor AppImage to `/opt/Cursor/`
- Downloads your chosen icon to `/opt/Cursor/`
- Creates a desktop entry for easy launching

---

## ❌ Uninstallation
To uninstall Cursor:
1. Remove the application files:
    ```zsh
    sudo rm -rf /opt/Cursor
    ```
2. Remove the desktop entry:
    ```zsh
    sudo rm -f /usr/share/applications/cursor.desktop
    ```

---

## 🧩 Troubleshooting
- Ensure you have `sudo` privileges and an active internet connection.
- Make sure the AppImage file path you provide is correct and accessible.
- Confirm the icon filename exists in the `images` directory of this repository.
- If Cursor fails to start, try running it from the terminal to see any error messages.
- Check script permissions (`chmod +x manage_cursor.sh`).

---

For questions or issues, please open an issue in this repository.
