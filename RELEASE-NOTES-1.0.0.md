# Clone Ranger 1.0.0

**Round up your duplicate photos and videos.** Clone Ranger finds exact duplicates by their content (not just
their name), shows them side by side, suggests which copy to keep, and frees the space safely. Nothing happens to
a file until you confirm, and almost everything can be undone.

This is the first public release.

![Clone Ranger](https://raw.githubusercontent.com/agent-denis/clone-ranger/main/docs/screenshots/main-light.png)

## Highlights

- **Finds real duplicates**: same size, quick check, then a full content fingerprint. Hard links and Btrfs reflinks
  are recognised and never counted as space to free.
- **Clear overview**: Cards, List and Grid views, a Details panel, and a viewer with zoom, side-by-side compare,
  grid compare, slideshow and video playback.
- **Smart suggestions**: configurable rules decide which copy to keep (protected and preferred folders, no
  "copy (1)" names, highest resolution, oldest, ...).
- **Select and unselect easily**: *Unselect all* with one click, or unselect a single file or a whole group;
  a selection bar always shows how many files and how much space are selected.
- **Safe actions**: Move to Trash, delete permanently, move and rename (also bulk rename), always with a preview
  first, plus Undo and a full History.
- **Start from scratch**: *Clear history & cache* and *Reset to defaults*, where you choose what to reset:
  search settings, other settings, history, cache, or everything.
- **Modern look**: orange, light blue, yellow and red, with Light and Dark themes that follow your desktop.
- **Private by design**: works completely offline, with no telemetry and no accounts. See
  [PRIVACY.txt](https://github.com/agent-denis/clone-ranger/blob/main/PRIVACY.txt).

## Install

### Fedora 45 (RPM)

Download `clone-ranger-1.0.0-1.fc45.noarch.rpm` below, then double-click it, or run:

```bash
sudo dnf install ./clone-ranger-1.0.0-1.fc45.noarch.rpm
```

Clone Ranger then appears in the Apps menu. For video thumbnails, `ffmpeg-free` is installed along with it
(recommended dependency).

> The RPM is built for **Fedora 45** (Python 3.15). Packages for other Fedora versions will follow through COPR.

### Any other Linux distribution

```bash
git clone https://github.com/agent-denis/clone-ranger.git
cd clone-ranger
./install.sh
```

`install.sh` installs for your user only (no root needed), adds Clone Ranger to the app menu and the
`clone-ranger` command. It needs Python 3.11 or newer. Remove it with `./uninstall.sh`.

**Try it without touching any file:** `clone-ranger --demo`.

## Requirements

- Linux with a graphical desktop (tested on GNOME, Wayland and X11)
- Python 3.11 or newer, PySide6 (Qt 6) and Pillow (installed automatically)
- Optional: FFmpeg for video thumbnails and durations

## Known limitations

- **HEIC/HEIF photos** show no preview in the RPM version, because Fedora doesn't package `pillow-heif`. They are
  still found and compared. The `install.sh` version includes HEIC support.
- **HEVC videos from phones** get no thumbnail with Fedora's `ffmpeg-free`. Playback in the viewer still works.
- Not yet tested on KDE Plasma.

## Files

| File | For | SHA-256 |
|---|---|---|
| `clone-ranger-1.0.0-1.fc45.noarch.rpm` | installing on Fedora 45 | `04824995ddd13650ffc431e4f2a8ad387d8cbf545e32645e7c282d73985d408c` |
| `clone-ranger-1.0.0-1.fc45.src.rpm` | rebuilding the package (packagers) | `7224a744e9ab2f32065f9c0e694a17d88eaf0fe95a5d717c3ae83fbd8c81c2bc` |

Check a download with `sha256sum clone-ranger-1.0.0-1.fc45.noarch.rpm`.

## Licence

Clone Ranger is free software under the **GNU General Public License v3.0 or later**. You may use, study, share
and change it, as long as shared versions stay free under the same licence.

Found a bug or have an idea? [Open an issue](https://github.com/agent-denis/clone-ranger/issues).
