# LinuxonAndroidviatermux

# Fedora 44 + KDE Plasma on Termux-X11

Run Fedora 44 with the KDE Plasma desktop environment on Android using Termux-X11 and PulseAudio.

---

## 1. Termux Prerequisites

Open standard Termux and run this command to install the required packages (`proot-distro`, `pulseaudio`, `wget`, `x11-repo`):

```bash
pkg update && pkg upgrade -y
pkg install x11-repo -y
pkg install proot-distro pulseaudio wget termux-x11-nightly -y
