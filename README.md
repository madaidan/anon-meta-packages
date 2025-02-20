# Recommended packages for hosts with nonfreedom hardware design #

A metapackage, which includes nonfree firmware useful for hosts with
nonfreedom hardware design.

These are not useful in Qubes, since this would be up to Qubes.

Safe to remove, if you know what you are doing.

Package: non-qubes-vm-enhancements-cli
Architecture: all
Depends: power-savings-disable-in-vms, shared-folder-help, swappiness-lowest,
keyboard-configuration, kbd, acpi-support, console-common, console-setup,
initramfs-tools, os-prober, grub-live | grub-live-boot, cryptsetup, zulucrypt-cli,
libzulucrypt-plugins, ${misc:Depends}
Replaces: non-qubes-vm-enhancements
Description: Recommended packages for terminal based VMs CLI
# Recommended packages for terminal based VMs CLI #

A metapackage, which includes recommended packages which are useful within
CLI based non-Qubes virtual machines.
These are not useful in Qubes, since Qubes
already has native implementations for those.

Safe to remove, if you know what you are doing.

Package: non-qubes-vm-enhancements-gui
Architecture: all
Depends: non-qubes-vm-enhancements-cli, zulucrypt-gui, rads, non-qubes-vm-audio,
${misc:Depends}
Description: Recommended packages for graphical VMs GUI
# Recommended packages for graphical VMs GUI #

A metapackage, which includes recommended packages which are useful within
GUI based non-Qubes virtual machines.
These are not useful in Qubes, since Qubes
already has native implementations for those.

Safe to remove, if you know what you are doing.

Package: non-qubes-vm-audio
Architecture: all
Depends: libasound2, alsa-utils, pulseaudio, pavucontrol, ${misc:Depends}
Description: Recommended packages for Audio Support in non-Qubes
# Recommended packages for Audio Support in non-Qubes #

A metapackage, which includes recommended packages which are useful within
non-Qubes virtual machines audio support.

These are not useful in Qubes, since Qubes
already has its own native audio implementation.

Safe to remove, if you know what you are doing.

Package: kicksecure-dependencies-cli
Priority: required
Architecture: all
Depends: bzip2, file, lsof, most, pciutils, strace, sysfsutils,
less, haveged, jitterentropy-rngd, locales, apt-transport-tor,
sdwdate, bootclockrandomization, timesanitycheck,
timezone-utc, busybox,
security-misc,
bash-completion, command-not-found, zsh, nano, wget, dnsutils, iputils-ping,
apparmor-utils, apparmor-profile-anondist,
firejail, firetools, firejail-profiles, iproute2, iptables, hardened-malloc,
udisks2, secure-delete, sudo, net-tools,
gpl-sources-download, whonix-repository,
scurl, openvpn,
usability-misc, menu, man-db, open-link-confirmation,
whonix-initializer,
${misc:Depends}
Replaces: anon-shared-packages-dependencies, anon-shared-packages-recommended,
hardened-packages-dependencies-cli
Description: Dependencies for hardened systems CLI
# Dependencies for hardened systems CLI #

A metapackage, which installs command line interface (CLI) packages which
should be installed on hardened systems.

Do not remove.

Package: whonix-shared-default-applications-gui
Architecture: all
Pre-Depends: whonix-legacy
Depends: sdwdate-gui, msgcollector-gui, anon-iceweasel-warning, anon-icon-pack,
whonix-setup-wizard, ${misc:Depends}
Replaces: anon-shared-default-applications
Description: Recommended packages for Whonix-Gateway and Whonix-Workstation GUI
# Recommended packages for Whonix-Gateway and Whonix-Workstation GUI #

A metapackage, which installs recommended graphical user interface (GUI)
default applications, which are useful in a default installation of a
Whonix-Gateway or Whonix-Workstation desktop.

Safe to remove, if you know what you are doing.

Package: whonix-gateway-default-applications-gui
Architecture: all
Pre-Depends: whonix-legacy
Depends: onioncircuits, anon-connection-wizard, tor-control-panel, ${misc:Depends}
Replaces: anon-gateway-default-applications, whonix-gateway-default-applications
Description: Recommended desktop packages for Whonix-Gateway GUI
# Recommended desktop packages for Whonix-Gateway GUI #

A metapackage, which installs graphical user interface (GUI) packages,
which are recommended for a graphical Whonix-Gateway.

Safe to remove, if you know what you are doing.

Package: kicksecure-desktop-environment-essential-gui
Architecture: all
Depends: xserver-xorg, xserver-xorg-video-qxl, xserver-xorg-video-fbdev,
xserver-xorg-video-vesa, libgl1-mesa-dri, upower, gtk2-engines-pixbuf,
xauth, xpra | xserver-xephyr | xvfb,
${misc:Depends}
Replaces: anon-shared-desktop, hardened-desktop-environment-essential-gui
Description: Desktop Depends GUI
# Desktop Depends GUI #

A metapackage, which installs dependencies for desktop environments,
such as KDE, GNOME, etc.

kicksecure-desktop-environment-essential-xfce depends on this package.

Package: kicksecure-desktop-environment-essential-xfce
Architecture: all
Depends: kicksecure-desktop-environment-essential-gui,
xfce4, lightdm,
gnome-brave-icon-theme,
whonix-xfce-desktop-config, ${misc:Depends}
Replaces: hardened-desktop-environment-essential-xfce
Description: Recommended applications for hardened Xfce Desktop Environment
# Recommended applications for hardened Xfce Desktop Environment #

A metapackage, which installs minimal, yet complete enough
to contain a very basic Xfce Desktop Environment.

Safe to remove.

Package: kicksecure-desktop-applications-xfce
Architecture: all
Depends: libexo-1-0, xfce4-terminal, mousepad,
lxqt-sudo, policykit-1, policykit-1-gnome | polkit-1-auth-agent,
p7zip-full, zip, unzip, xz-utils, unar, xarchiver,
thunar, thunar-archive-plugin, thunar-volman,
${misc:Depends}
Replaces: hardened-desktop-applications-xfce
Description: Recommended applications for hardened Xfce desktop GUI
# Recommended applications for hardened Xfce desktop GUI #

A metapackage, which installs minimal, yet complete enough
to contain the very basics, Xfce applications.

Safe to remove.

Package: apparmor-profiles-kicksecure
Replaces: apparmor-profiles-whonix, apparmor-profiles-hardened-debian
Architecture: all
Depends: apparmor-profile-icedove,
apparmor-profile-torbrowser,
apparmor-profile-xchat,
apparmor-profile-gwenview, apparmor-profile-okular, ${misc:Depends}
Description: AppArmor profiles developed by the Kicksecure Team
# AppArmor profiles developed by the Kicksecure Team #

A metapackage, which installs apparmor profiles developed by the Hardened
Debian team.

Increases security.

Safe to remove, if you know what you are doing.

Package: whonix-gateway-packages-dependencies-pre
Priority: required
Architecture: all
Depends: whonix-gw-network-conf, anon-base-files,
${misc:Depends}
Description: Dependencies for Whonix-Gateway that changes network related files
# Dependencies for Whonix-Gateway that changes network related files #

A metapackage, which installs packages which Whonix-Gateway
depends on. Can not be merged into whonix-gateway-packages-dependencies due to
conflicts with chroot build process.

Do not remove.

Package: whonix-gateway-packages-dependencies-cli
Priority: required
Architecture: all
Pre-Depends: whonix-legacy
Depends: tor, anon-gw-base-files, ipv4-forward-disable,
ipv6-disable, anon-gw-anonymizer-config,
whonix-gateway-packages-dependencies-pre,
tor-geoipdb, nyx, obfsproxy, obfs4proxy, flashproxy-client,
fteproxy, onion-grater,
${misc:Depends}
Replaces: anon-gateway-packages-dependencies, whonix-gateway-packages-dependencies,
anon-gateway-packages-recommended, whonix-gateway-packages-recommended
Description: Dependencies for Whonix-Gateway CLI
# Dependencies for Whonix-Gateway CLI #

A metapackage, which installs packages which Whonix-Gateway
depends on.

Do not remove.

Package: whonix-shared-packages-dependencies-cli
Architecture: all
Pre-Depends: whonix-legacy
Depends: whonix-base-files, anon-apt-sources-list, whonix-firewall,
whonixsetup,
${misc:Depends}
Replaces: whonix-shared-packages-dependencies
Description: Dependencies for Whonix-Gateway and Whonix-Workstation CLI
# Dependencies for Whonix-Gateway and Whonix-Workstation CLI #

A metapackage, which installs packages which both, Whonix-Gateway
and Whonix-Workstation, depend on.

Do not remove.

Package: whonix-shared-packages-recommended-cli
Architecture: all
Depends: kicksecure-dependencies-cli, whonixcheck, tor-ctrl, uwt,
anon-apps-config, ${misc:Depends}
Replaces: whonix-shared-packages-recommended
Description: Recommended packages for Whonix-Gateway and Whonix-Workstation CLI
# Recommended packages for Whonix-Gateway and Whonix-Workstation CLI #

A metapackage, which includes recommended packages to ensure, Whonix
standard tools are available and other useful recommended packages.

Safe to remove, if you know what you are doing.

Package: whonix-workstation-packages-dependencies-pre
Priority: required
Architecture: all
Depends: whonix-ws-network-conf, anon-ws-dns-conf, anon-base-files,
${misc:Depends}
Description: Dependencies for Whonix-Workstation that changes network related files
# Dependencies for Whonix-Workstation that changes network related files #

A metapackage, which installs packages which Whonix-Workstation
depends on. Can not be merged into whonix-workstation-packages-dependencies
due to conflicts with chroot build process.

Do not remove.

Package: whonix-workstation-packages-dependencies-cli
Priority: required
Architecture: all
Pre-Depends: whonix-legacy
Depends: anon-ws-base-files, whonix-workstation-packages-dependencies-pre,
${misc:Depends}
Replaces: anon-workstation-packages-dependencies, whonix-workstation-packages-dependencies
Description: Dependencies for Whonix-Workstation CLI
# Dependencies for Whonix-Workstation CLI #

A metapackage, which installs packages which Whonix-Workstation
depends on.

Do not remove.

Package: whonix-workstation-packages-recommended-cli
Architecture: all
Depends: anon-gpg-tweaks, anon-ws-disable-stacked-tor, pwgen,
python-msgpack, bindp, codecrypt, gnupg2, gnupg-agent, dirmngr,
magic-wormhole, diceware, makepasswd, ${misc:Depends}
Description: Recommended packages for Whonix-Workstation CLI
# Recommended packages for Whonix-Workstation CLI #

A metapackage, which installs packages, which are recommended for
command line interface (CLI) Whonix-Workstation, because they are
useful for a Tor Workstation.

Feel free to remove if you know what you are doing.

Package: whonix-workstation-packages-recommended-gui
Architecture: all
Depends: hexchat, vlc, hunspell-en-us, gpa,
mat2, keepassxc,
libimage-exiftool-perl, gir1.2-gtk-3.0,
pinentry-qt | pinentry-x11,
mupdf, ristretto,
tb-default-browser, tb-starter, tb-updater, youtube-dl,
qtox, onionshare, xchat-improved-privacy, binaries-freedom,
whonix-workstation-packages-recommended-cli, whonix-ws-irc-chat-support,
whonix-welcome-page, whonix-ws-start-menu-additions, ${misc:Depends}
Replaces: anon-workstation-packages-recommended, whonix-workstation-packages-recommended,
anon-workstation-default-applications, whonix-workstation-default-applications-gui
Description: Recommended packages for Whonix-Workstation GUI
# Recommended packages for Whonix-Workstation GUI #

A metapackage, which installs packages, which are recommended for
graphical user interface (GUI) Whonix-Workstation, because they are
useful for a Tor Workstation.

Feel free to remove if you know what you are doing.

Package: whonix-gateway-shared-packages-shared-meta
Architecture: all
Pre-Depends: whonix-legacy
Depends: kicksecure-dependencies-cli,
whonix-shared-default-applications-gui,
whonix-shared-packages-dependencies-cli,
whonix-shared-packages-recommended-cli,
whonix-gateway-default-applications-gui,
whonix-gateway-packages-dependencies-cli,
${misc:Depends}
Description: Whonix-Gateway Shared Packages
# Whonix-Gateway Shared Packages #

A metapackage, which installs packages, for a Whonix-Default-Gateway.

It is shared between Qubes-Whonix and Non-Qubes-Whonix.

Feel free to remove if you know what you are doing.

Package: whonix-workstation-shared-packages-shared-meta
Architecture: all
Pre-Depends: whonix-legacy
Depends: kicksecure-dependencies-cli,
whonix-shared-default-applications-gui,
whonix-shared-packages-dependencies-cli,
whonix-shared-packages-recommended-cli,
whonix-workstation-packages-dependencies-cli,
whonix-workstation-packages-recommended-cli,
whonix-workstation-packages-recommended-gui,
${misc:Depends}
Description: Whonix-Workstation Shared Packages
# Whonix-Workstation Shared Packages #

A metapackage, which installs packages, for a Whonix-Default-Workstation.

It is shared between Qubes-Whonix and Non-Qubes-Whonix.

Feel free to remove if you know what you are doing.

Package: non-qubes-whonix-gateway-cli
Priority: required
Architecture: all
Pre-Depends: whonix-legacy
Depends: non-qubes-vm-enhancements-cli,
kicksecure-dependencies-cli,
whonix-shared-packages-dependencies-cli,
whonix-shared-packages-recommended-cli,
whonix-gateway-packages-dependencies-cli,
anon-connection-wizard, tor-control-panel, ${misc:Depends}
Description: Default Packages for Non-Qubes-Whonix-Gateway CLI
# Default Packages for Non-Qubes-Whonix-Gateway CLI #

A metapackage, which installs packages, for a
Non-Qubes-Whonix-Default-Gateway without graphical user interface (GUI).

Do not remove.

Package: whonix-gateway-rpi
Priority: required
Architecture: all
Pre-Depends: whonix-legacy
Depends: non-qubes-whonix-gateway-cli, raspi3-firmware, fake-hwclock, wpasupplicant, firmware-iwlwifi, firmware-atheros, firmware-brcm80211, firmware-ralink, firmware-realtek, iw, linux-image-arm64 (>= 4.16), ${misc:Depends}
Description: Default packages for Whonix-Gateway-RPi CLI
# Default packages for Whonix-Gateway-RPi CLI #

A metapackage, which installs packages for a CLI
Raspberry Pi 3 Whonix-Gateway.

Do not remove.

Package: qubes-whonix-gateway
Priority: required
Architecture: all
Depends: whonix-gateway-shared-packages-shared-meta, qubes-whonix,
qubes-whonix-shared-packages-recommended,
qubes-whonix-gateway-packages-recommended,
kicksecure-desktop-applications-xfce,
${misc:Depends}
Replaces: whonix-gateway
Description: Default packages for Qubes-Whonix-Gateway
# Default packages for Qubes-Whonix-Gateway #

A metapackage, which installs packages, for a
Qubes-Whonix-Default-Gateway.

Only depends on whonix-gateway-shared-packages-shared-meta,
because installing kicksecure-desktop-environment-essential-gui is not required
in Qubes-Whonix.

Do not remove.

Package: qubes-whonix-workstation
Priority: required
Architecture: all
Depends: whonix-workstation-shared-packages-shared-meta, qubes-whonix,
qubes-whonix-shared-packages-recommended,
qubes-whonix-workstation-packages-recommended,
kicksecure-desktop-applications-xfce,
${misc:Depends}
Replaces: whonix-workstation
Description: Default packages for Qubes-Whonix-Workstation
# Default packages for Qubes-Whonix-Workstation #

A metapackage, which installs packages, for a
Qubes-Whonix-Default-Workstation.

Only depends on whonix-workstation-shared-packages-shared-meta,
because installing kicksecure-desktop-environment-essential-gui is not required
in Qubes-Whonix.

Do not remove.

Package: non-qubes-whonix-gateway-kde
Architecture: all
Pre-Depends: whonix-legacy
Depends: non-qubes-whonix-gateway-xfce, ${misc:Depends}
Replaces: whonix-gateway, non-qubes-whonix-gateway
Section: oldlibs
Description: transitional package Whonix-Gateway KDE
# transitional package Whonix-Gateway KDE #

Whonix KDE is no longer supported.

Use package non-qubes-whonix-gateway-xfce instead.
Legacy. This is a transitional package.

It can be removed by installing package non-qubes-whonix-gateway-xfce.

sudo apt-get install non-qubes-whonix-gateway-xfce

Package: non-qubes-whonix-gateway-xfce
Priority: required
Architecture: all
Pre-Depends: whonix-legacy
Depends: non-qubes-vm-enhancements-cli,
non-qubes-vm-enhancements-gui,
non-qubes-whonix-gateway-cli,
kicksecure-desktop-environment-essential-xfce,
kicksecure-desktop-applications-xfce,
whonix-shared-default-applications-gui,
whonix-gateway-default-applications-gui,
${misc:Depends}
Description: Default Packages for Non-Qubes-Whonix-Gateway Xfce GUI
# Default Packages for Non-Qubes-Whonix-Gateway Xfce GUI #

A metapackage, which installs packages, for a
Non-Qubes-Whonix-Default-Gateway with Xfce.

Depends on kicksecure-desktop-environment-essential-xfce because that is
required in Non-Qubes-Whonix Xfce in order to get graphical desktop
environment.

Do not remove.

Package: non-qubes-whonix-workstation-kde
Architecture: all
Pre-Depends: whonix-legacy
Depends: non-qubes-whonix-workstation-xfce, ${misc:Depends}
Replaces: whonix-workstation, non-qubes-whonix-workstation
Section: oldlibs
Description: transitional package Whonix-Workstation KDE
# transitional package Whonix-Workstation KDE #

Use the package non-qubes-whonix-workstation-xfce instead.
Legacy package. This is a transitional package.

Install non-qubes-whonix-workstation-xfce, remove this package.

sudo apt-get install non-qubes-whonix-workstation-xfce

Package: non-qubes-whonix-workstation-xfce
Priority: required
Architecture: all
Pre-Depends: whonix-legacy
Depends: non-qubes-vm-enhancements-gui,
non-qubes-whonix-workstation-cli,
kicksecure-desktop-environment-essential-xfce,
kicksecure-desktop-applications-xfce,
whonix-shared-default-applications-gui,
whonix-workstation-packages-recommended-gui,
${misc:Depends}
Description: Default Packages for Non-Qubes-Whonix-Workstation Xfce GUI
# Default Packages for Non-Qubes-Whonix-Workstation Xfce GUI #

A metapackage, which installs packages, for a
Non-Qubes-Whonix-Default-Workstation with Xfce.

Depends on kicksecure-desktop-environment-essential-xfce because that is
required in Non-Qubes-Whonix Xfce in order to get graphical desktop
environment.

Do not remove.

Package: non-qubes-whonix-workstation-cli
Priority: required
Architecture: all
Pre-Depends: whonix-legacy
Depends: non-qubes-vm-enhancements-cli,
kicksecure-dependencies-cli,
whonix-shared-packages-dependencies-cli,
whonix-shared-packages-recommended-cli,
whonix-workstation-packages-dependencies-cli,
whonix-workstation-packages-recommended-cli,
kloak,
${misc:Depends}
Description: Default Packages for Non-Qubes-Whonix-Workstation CLI
# Default Packages for Non-Qubes-Whonix-Workstation CLI #

A metapackage, which installs packages, for a
Non-Qubes-Whonix-Default-Workstation without graphical user interface (GUI).

Do not remove.

Package: kicksecure-packages-dependencies-pre
Priority: required
Architecture: all
Depends: anon-base-files, kicksecure-network-conf, ${misc:Depends}
Description: Dependencies for Kicksecure that changes network related files
# Dependencies for Kicksecure that changes network related files #

A metapackage, which installs packages which Kicksecure depends on. Can not
be merged into another package due to conflicts with chroot build process.

Do not remove.

Package: kicksecure-cli
Replaces: hardened-debian-cli
Priority: required
Architecture: all
Depends: kicksecure-dependencies-cli,
anon-base-files, kicksecure-base-files, anon-apt-sources-list,
${misc:Depends}
Description: Kicksecure command line interface CLI
# Kicksecure command line interface CLI #

A metapackage, which installs packages, for Kicksecure CLI.

Do not remove.

Package: kicksecure-cli-vm
Priority: required
Architecture: all
Depends: kicksecure-cli, non-qubes-vm-enhancements-cli,
kicksecure-network-conf, ${misc:Depends}
Description: Kicksecure command line interface CLI VMs
# Kicksecure command line interface CLI VMs #

A metapackage, which installs packages, for Kicksecure CLI Virtual Machines.

Do not remove.

Package: kicksecure-xfce
Replaces: hardened-debian-xfce
Priority: required
Architecture: all
Depends: kicksecure-cli,
kicksecure-desktop-environment-essential-xfce,
kicksecure-desktop-applications-xfce,
mupdf, ristretto, keepassxc, binaries-freedom,
sdwdate-gui, secbrowser, tb-default-browser,
${misc:Depends}
Description: Kicksecure Xfce GUI
# Kicksecure Xfce GUI #

A metapackage, which installs packages, for Kicksecure Xfce.

Do not remove.

Package: kicksecure-xfce-vm
Priority: required
Architecture: all
Depends: kicksecure-cli-vm, non-qubes-vm-enhancements-gui,
kicksecure-xfce, ${misc:Depends}
Description: Kicksecure Xfce GUI for VMs
# Kicksecure Xfce GUI for VMs #

A metapackage, which installs packages, for Kicksecure Xfce in Virtual
Machines.

Do not remove.

Package: non-qubes-whonix-gateway
Architecture: all
Pre-Depends: whonix-legacy
Depends: non-qubes-whonix-gateway-xfce, ${misc:Depends}
Section: oldlibs
Description: transitional package Whonix-Gateway
# transitional package Whonix-Gateway #

KDE was deprecated in Whonix.

Use non-qubes-whonix-gateway-xfce instead.
This is a transitional package. Legacy.

Install non-qubes-whonix-gateway-xfce and remove this.

sudo apt-get install non-qubes-whonix-gateway-xfce

Package: non-qubes-whonix-workstation
Architecture: all
Pre-Depends: whonix-legacy
Depends: non-qubes-whonix-workstation-xfce, ${misc:Depends}
Section: oldlibs
Description: transitional package Whonix-Workstation
# transitional package Whonix-Workstation #

Use non-qubes-whonix-workstation-xfce instead.
This is a transitional package. Legacy.

It can be removed by installing package non-qubes-whonix-workstation-xfce.

sudo apt-get install non-qubes-whonix-workstation-xfce

Package: whonix-host-packages-dependencies-pre
Priority: required
Architecture: all
Depends: anon-base-files, ${misc:Depends}
Description: Dependencies for Whonix Host that changes network related files
# Dependencies for Whonix Host that changes network related files #

A metapackage, which installs packages which Whonix Host depends on. Can not
be merged into another package due to conflicts with chroot build process.

Do not remove.

Package: whonix-host-xfce-kvm-freedom
Architecture: all
Pre-Depends: whonix-legacy
## TODO
## whonix-gateway-xfce-qcow2, whonix-workstation-xfce-qcow2,
Depends: kicksecure-xfce, xfce4-xkb-plugin, xfce4-screenshooter,
arc-theme,
iw, network-manager-gnome, network-manager,
firefox-esr, gnome-system-monitor, gparted,
whonix-libvirt,
anon-base-files,
${misc:Depends}
Description: Whonix Host packages for Freedom Hardware Design
# Whonix Host packages for Freedom Hardware Design #

Designed to run on hardware with Freedom Hardware Design.

Do not remove.

Package: whonix-host-xfce-kvm-nonfreedom
Architecture: all
Pre-Depends: whonix-legacy
Depends: whonix-host-xfce-kvm-freedom, firmware-nonfreedom, ${misc:Depends}
Section: non-free/metapackages
Description: Whonix Host packages for nonfreedom hardware design
# Whonix Host packages for nonfreedom hardware design #

Designed to run on hardware with nonfreedom hardware design.

Do not remove.

Package: dummy-contrib
Architecture: all
Depends: ${misc:Depends}
Section: contrib/metapackages
Description: dummy contrib package
# dummy contrib package #

A metapackage, without contents to populate the contrib repository.

This package itself is not nonfree.
This package itself is Free, Open, Freedom, Libre Software.

Useful for testing vrms without installation of an actual contrib package.

Safe to remove.

Package: dummy-nonfree
Architecture: all
Depends: ${misc:Depends}
Section: non-free/metapackages
Description: dummy nonfree package
# dummy nonfree package #

A metapackage, without contents to populate the nonfree repository.

This package itself is not nonfree.
This package itself is Free, Open, Freedom, Libre Software.

Useful for testing vrms without installation of an actual nonfree package.

Safe to remove.
## How to install `anon-meta-packages` using apt-get ##

1\. Download [Whonix's Signing Key]().

```
wget https://www.whonix.org/patrick.asc
```

Users can [check Whonix Signing Key](https://www.whonix.org/wiki/Whonix_Signing_Key) for better security.

2\. Add Whonix's signing key.

```
sudo apt-key --keyring /etc/apt/trusted.gpg.d/whonix.gpg add ~/patrick.asc
```

3\. Add Whonix's APT repository.

```
echo "deb https://deb.whonix.org buster main contrib non-free" | sudo tee /etc/apt/sources.list.d/whonix.list
```

4\. Update your package lists.

```
sudo apt-get update
```

5\. Install `anon-meta-packages`.

```
sudo apt-get install anon-meta-packages
```

## How to Build deb Package ##

Replace `apparmor-profile-torbrowser` with the actual name of this package with `anon-meta-packages` and see [instructions](https://www.whonix.org/wiki/Dev/Build_Documentation/apparmor-profile-torbrowser).

## Contact ##

* [Free Forum Support](https://forums.whonix.org)
* [Professional Support](https://www.whonix.org/wiki/Professional_Support)

## Donate ##

`anon-meta-packages` requires [donations](https://www.whonix.org/wiki/Donate) to stay alive!
