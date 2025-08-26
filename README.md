# FoldCraftLauncher APK Tracker

This repository automatically tracks and stores APK files from the [FoldCraftLauncher](https://github.com/FCL-Team/FoldCraftLauncher) releases.

## How it works

A GitHub Action workflow runs every hour to:

1. Check for the latest release of FoldCraftLauncher
2. If a new release is found:
   - Download all assets from the release
   - Extract and commit only the `.apk` files to the `apk_files/` directory
   - Update the version tracker
3. If no new release is found, do nothing

## Directory Structure

- `apk_files/` - Contains all the APK files from the latest release
- `.github/workflows/` - Contains the automation workflow
- `.latest_version` - Tracks the latest processed version (automatically maintained)

## Usage

The workflow runs automatically every hour, but can also be triggered manually through the GitHub Actions interface.

APK files are organized in the `apk_files/` directory, making them easily accessible for download.

## License

This project is licensed under the MIT License - see the LICENSE file for details.
