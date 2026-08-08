# 📚 Index

## PROOT-DISTRO (🎩 FEDORA 44)

<br>

---  
---  

<br>

## 🏁 First steps <a name=first-steps></a>
We are going to use Termux and Termux X11 in order to have a full Fedora 44 Linux Desktop on our Android devices.

<details>
<summary><strong> [Commands] How to install Fedora on Termux with proot-distro (No Root)</strong></summary>

1. Open Termux
2. Install proot-distro
```
pkg update
pkg install proot-distro
```
3. Install Fedora
```
proot-distro install fedora
```
4. Log in to the distro
```
proot-distro login fedora
```
</details>

---  
<br>

## ⚙️ Installing Desktops <a name=installing-desktops></a>

Log into your Fedora 44 PRoot container and install the KDE Plasma environment:

```
proot-distro login fedora
dnf group install kde-desktop --skip-unavailable -y
dnf install plasma-workspace-x11 xhost xrdb xset dbus-x11 -y
```

---  
<br>

## 💻 Running the Desktops for use with Termux X11 <a name=running-desktops></a>
All the scripts in this repository are prepared to run the desktop with audio in an easy way.

First you need to install the following packages in Termux:
```
pkg update
pkg install x11-repo
pkg install termux-x11-nightly
pkg install pulseaudio
pkg install wget
```

Then, you just need to download the script, give it permissions to execute, and run it (in Termux, not in proot-distro):
```
wget [https://raw.githubusercontent.com/linuxmasterontermux/LinuxonAndroidviatermux/main/startkde_fedora.sh](https://raw.githubusercontent.com/linuxmasterontermux/LinuxonAndroidviatermux/main/startkde_fedora.sh)
chmod +x startkde_fedora.sh
./startkde_fedora.sh
```

---  
<br>

## ⬇️ Download scripts easily: <a name=easy-download></a>

> [!NOTE]  
> By default this script logs into Fedora as root. Make sure the Termux:X11 app is running in the background before executing.

* startkde_fedora.sh
```
wget [https://raw.githubusercontent.com/linuxmasterontermux/LinuxonAndroidviatermux/main/startkde_fedora.sh](https://raw.githubusercontent.com/linuxmasterontermux/LinuxonAndroidviatermux/main/startkde_fedora.sh)
```

