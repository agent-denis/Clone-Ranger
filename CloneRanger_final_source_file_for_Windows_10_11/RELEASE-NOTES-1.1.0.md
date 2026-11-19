# Clone Ranger 1.1.0

**Clone Ranger now also runs on Windows 10 and 11.** Everything from 1.0.0 is still there: it finds exact
duplicate photos and videos by their content, shows them side by side, suggests which copy to keep and frees the
space safely. Nothing happens to a file until you confirm, and almost everything can be undone.

## Downloads

| File | For |
|---|---|
| `CloneRanger-1.1.0-Setup.exe` | Windows 10 / 11: installs for your user, no administrator rights needed |
| `CloneRanger-1.1.0-portable.zip` | Windows 10 / 11 without installing: unzip and start `Clone Ranger.exe` |
| `clone-ranger-1.1.0-1.fc45.noarch.rpm` | Fedora 45: `sudo dnf install ./clone-ranger-1.1.0-1.fc45.noarch.rpm` |
| `clone-ranger-1.1.0-1.fc44.noarch.rpm` | Fedora 44: `sudo dnf install ./clone-ranger-1.1.0-1.fc44.noarch.rpm` |

Other Linux: `git clone` and `./install.sh` (see the README).

**Windows SmartScreen:** the app isn't code-signed, so on first start Windows says it "protected your PC".
Choose **More info → Run anyway**. You only have to do this once.

## New on Windows

- *Move to Recycle Bin*, and Undo puts the files back just like Explorer's Restore.
- *Show in folder* opens Explorer, and *Entire computer* scans every local and USB drive.
- OneDrive files that are only online are skipped, so a scan never downloads them.
- Renaming follows the Windows file-name rules.
- FFmpeg is included, so video thumbnails work out of the box.

## Fixed

- On small laptop screens, tall pages now scroll and the window opens maximized, so nothing is cut off.
  At 200 % scaling on an 11" screen it's still cramped: 150 % works best.
- The window title no longer shows the app name twice.
- Scanning a whole drive no longer stops on very large file IDs.
- Renaming a file to a name that is a hard link to the same file is refused.
- Linux trash and snapshot folders on disks shared with Linux are skipped on Windows too.

Licence: GPL-3.0-or-later.
