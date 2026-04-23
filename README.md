# CZVR File Updater

A Windows-based updater application for CZVR (Vancouver FIR) navigation data and EuroScope plugin files. This tool automatically checks for updates and manages installations with backup/restore.

## Overview

The CZVR File Updater is designed to simplify the process of keeping your CZVR EuroScope plugin and navigation data current. It features:

- **Automatic Update Detection**: Checks GitHub for the latest available versions
- **Smart Update Management**: Detects missed updates and installs full packages when needed
- **Backup & Restore**: Automatically backs up existing files before installing updates

## Installation

1. Download the latest `CZVR_File_Updater.exe` from the releases page
2. Run the executable
3. On first launch, select where you would like to install the Nav Data
4. Everytime you launch EuroScope the application will check for updates and if it finds any it will launch itself and update
5. That's it!

---

## FAQ - Users

### Q: How do I change my install location?
**A:** Click on the folder path link in the application to select a different install directory

### Q: Can I rename the `CZVR_Files` folder?
**A:** **No, do not rename the `CZVR_Files` folder.** The updater relies on this exact folder name to locate and update your installation. Renaming it will cause the updater to think CZVR is not installed and may result in duplicate installations. If you've already renamed it, rename it back to `CZVR_Files`.

### Q: Where does my data get saved?
**A:** Your EuroScope folder path and installed version are saved in `%APPDATA%\EuroScope\CZVR_File_Updater\`. All CZVR files are installed to your selected EuroScope folder under the `CZVR_Files` subdirectory. Backups are created in: `[File_Folder]\CZVR_Backups\`

### Q: What happens if something goes wrong during installation?
**A:** The updater creates automatic backups before installing updates (except on first install). If installation fails, you can manually restore from the `CZVR_Backups` folder in your EuroScope directory.

### Q: Why did it say "Uh oh, looks like you haven't updated in a bit!"?
**A:** This message appears when you've missed multiple update cycles. The updater will automatically install the complete package instead of a delta update to ensure all files are current. Your backup will be preserved.

### Q: How often should I run the updater?
**A:** The updater runs automatically each time you launch EuroScope and will let you know should there be any updates.

### Q: Can I move my EuroScope folder after installing?
**A:** Yes, but you'll need to tell the updater your new location. If the previously selected folder no longer exists, you'll be prompted to select a new one on the next launch.

### Q: What if the download fails?
**A:** Check your internet connection and try again. If the problem persists, try selecting your EuroScope folder again to refresh the connection. Manual downloads are also available on the GitHub releases page.

### Q: Where should I report bugs?
**A:** Report issues on this repository with details about your EuroScope folder location and the error message displayed.
