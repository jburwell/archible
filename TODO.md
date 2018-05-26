  * Build a Vagrantfile to provision/test it
  * Can Packer be used to build a custom ISOA 
  * Add support for pulling roles from Galaxy
  * Remove roles
    * desktop
    * network
    * xmonad
    * xorg
    * web
  * Add roles
    * network-manager
    * ntpd
    * yaourt
  * Consider replacing roles with a Galaxy version
    * ssh
    * udev
  * Remove ntp from arch-base
  * Refactor cronie into a separate role (look for a version to pull from Galaxy) -> is cronie the right choice?
  * Merge arch-base/audio into the pulseaudio role
  * Merge arch-base/aur with yaourt
  * Extract arch-base/media into an automount role (look for a version to pull from Galaxy)
  * Extract codecs configuration from arch-base/media to an audio-codecs role
  * Extract sudo from arch-base/user to a sudo role (look for a version to pull from Galaxy)
  * Merge network with the network-manager role
  * Update to network-manager to reflect https://wiki.archlinux.org/index.php/NetworkManager#Using_Gnome-Keyring
  * Convert all roles to use the yaourt plugin
  * Integrate Yubikey support for luks https://github.com/agherzan/yubikey-full-disk-encryption
  * Extract the laptop role to a power management role and validate against https://wiki.archlinux.org/index.php/Power_management
  * Validate the encrypted installtion procedure against https://wiki.archlinux.org/index.php/Dm-crypt/Encrypting_an_entire_system
  * Add hardening.yml role to arch-base or arch-bootstrap based on https://wiki.archlinux.org/index.php/security
  * Evaluate the password generation in arch-bootstrap -- should it use Ansible secrets
  * Remove time sync from arch-bootstrap
  * Parameterize package list for the pacstrap command in arch-bootstrap
  * If submoduls remain necessary, convert to git-subtree
  * Choose display manager -> https://wiki.archlinux.org/index.php/Display_manager

mise
====

  * [i3blocks](https://github.com/vivien/i3blocks)?
  * [good i3 example](https://github.com/da-edra/dotfiles)
  * Roles
    * VLC
    * evince
    * [clementine](https://www.clementine-player.org/)
    * urxvt 
