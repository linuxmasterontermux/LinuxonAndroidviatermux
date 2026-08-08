PROOT-DISTRO (🎩 FEDORA 44)
We are going to use Termux and Termux X11 in order to have a full Fedora 44 Linux Desktop on Android devices.
<details>
<summary><strong> [Commands] How to install Fedora on Termux with proot-distro (No Root)</strong></summary>
The written steps are the following:
Open Termux
Install proot-distro:
pkg update
pkg install proot-distro
Install Fedora:
proot-distro install fedora
Log in to the distro:
proot-distro login fedora
</details>
Log into your Fedora 44 PRoot container and install the KDE Plasma environment:
Log into Fedora:
proot-distro login fedora
Install KDE Plasma Desktop via DNF5:
dnf group install kde-desktop --skip-unavailable -y
Install required X11 session launcher & D-Bus utilities:
dnf install plasma-workspace-x11 xhost xrdb xset dbus-x11 -y
All the scripts in this repository are prepared to run the desktop with audio in an easy way.
First you need to install the following packages in Termux:
pkg update
pkg install x11-repo
pkg install termux-x11-nightly
pkg install pulseaudio
pkg install wget
Then, you just need to download the script, give it permissions to execute, and run it (in Termux, not in proot-distro):
wget https://raw.githubusercontent.com/linuxmasterontermux/LinuxonAndroidviatermux/main/startkde_fedora.sh
chmod +x startkde_fedora.sh
./startkde_fedora.sh
[!NOTE]
By default this script logs into Fedora as root. Make sure the Termux:X11 app is running in the background before executing.
startkde_fedora.sh:
wget https://raw.githubusercontent.com/linuxmasterontermux/LinuxonAndroidviatermux/main/startkde_fedora.sh
