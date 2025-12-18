# 🐕 KingOdin rEFInd Theme

**KingOdin** is a dark, minimalist **rEFInd boot manager theme** inspired by Odin, the goodest boy and best companion.
Designed for **ultrawide displays**, clean manual boot entries, and a distraction-free boot experience.

This theme favors clarity, simplicity, and stability over heavy visual clutter.

---

## ✨ Features

* 🖤 Dark, cinematic background
* 🖥️ Optimized for **3440×1440 (21:9)** and **1920×1080**
* 🧼 Minimal UI (labels, hints, arrows hidden by default)
* 🐧 Clean Linux & Windows icon set
* 🔧 Designed for **manual boot entries** (recommended)
* 🐾 Tribute theme — Odin watches over your boots
---

## 🖼️ Previews

> Ultrawide (3440×1440) and standard (1920×1080) backgrounds are included.

```
bg/
├── background_3440x1440.png
├── background_1920x1080.png
├── background.png          # default
└── background_empty.png    # black fallback
```

---

## 📁 Folder Structure

```
KingOdin/
├── bg/           # Background images
├── icons/        # OS + tool icons
├── selection/    # Selection highlight images
└── theme.conf    # Main theme configuration
```

---

## 🚀 Installation

1. Copy the theme folder into your rEFInd themes directory:

```bash
sudo cp -r KingOdin /boot/EFI/refind/themes/
```

2. Edit your `refind.conf` and include the theme:

```ini
include themes/KingOdin/theme.conf
```

3. Reboot and enjoy 🐕

---

## ⚙️ Manual Boot Entries (Recommended)

I personally found it **much easier and more reliable** to disable auto-detection and define OS entries manually.

### Why?

* Prevents duplicate icons
* Avoids incorrect loader detection
* Makes icon control predictable
* Easier troubleshooting

In your `refind.conf`:

```ini
scanfor manual
```

Then define your OS entries directly in `theme.conf`.

---

## ⚠️ Important Warning (Please Read)

When using **manual menu entries**, be careful when editing:

* Loader paths
* Kernel/initrd paths
* UUIDs

An incorrect path can prevent rEFInd from booting an OS.

### If that happens:

1. Enter your system BIOS / firmware boot menu
2. Boot directly into the OS (Linux or Windows)
3. Fix the paths in `theme.conf`

rEFInd itself will **not** be damaged by a bad entry.

---

## 🧩 Example Menu Entries

These are **examples only** and are commented out by default in `theme.conf`.

```ini
#menuentry "CachyOS" {
#    loader /vmlinuz-linux-cachyos
#    initrd /initramfs-linux-cachyos.img
#    options "root=UUID=XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX rw splash"
#    icon os_cachyos.png
#}

#menuentry "Windows" {
#    loader /EFI/Microsoft/Boot/bootmgfw.efi
#    icon os_win11.png
#}
```

---

## 🐾 About Odin

KingOdin is named in tribute to Odin — my greatest friend and the best dog a human could ask for.
This theme exists because of him.

---

## 📜 License

MIT License
You’re free to use, modify, and share this theme.

If you improve it, consider sharing it back ❤️

---

## 🙏 Credits

* rEFInd by **Roderick W. Smith**
* Icons adapted from community rEFInd icon sets
* Theme concept and customization by **KingVeder**

---

