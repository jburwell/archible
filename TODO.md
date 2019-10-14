  * [] Test the project in a virtualbox VM -- Test Kitchen?
  * [] Can Packer be used to build a [custom ISO](https://wiki.archlinux.org/index.php/Remastering_the_Install_ISO)? ([Archiso](https://wiki.archlinux.org/index.php/Archiso))
  * [] Add support for pulling roles from Galaxy
  * [] Remove roles
    * [] desktop
    * [] network
    * [] xmonad
    * [] xorg
    * [] web
  * [] Add roles
    * [] aurman (https://github.com/polygamma/aurman)
    * [] gpg (see https://github.com/viccuad/ansible-configs/tree/master/roles/gnupg for inspiration)
    * [] network-manager
    * [] ntpd?
    * [] aurman
  * [] Consider replacing roles with a Galaxy version
    * [] ssh
    * [] udev
  * [] Remove ntp from arch-base
  * [] Merge arch-base/aur with yaourt
  * [] Convert all roles to use the aurman plugin
  * [] Validate the encrypted installtion procedure against https://wiki.archlinux.org/index.php/Dm-crypt/Encrypting_an_entire_system
  * [] If submodules remain necessary, convert to git-subtree
  * [] Change yaourt ansible patch to aurman
  * [] Review [arch-installer](https://github.com/Trick-17/arch-installer) for ideas about building and automating the ISO build and install process

# install.yml Playbook

  * [] Define logical volumes for /, /usr, /var, /home, and /tmp
  * [] Extract the [LUKS role](https://github.com/emcstack/encrypt-luks) and integrate [Yubikey support](https://github.com/agherzan/yubikey-full-disk-encryption)
  * [] Parameterize package list for the pacstrap command in arch-bootstrap
  * [] Integrate Yubikey support for luks https://github.com/agherzan/yubikey-full-disk-encryption
  * [] Evaluate the password generation in arch-bootstrap -- should it use Ansible secrets
  * [] Refactor cronie into a separate role (look for a version to pull from Galaxy) -> is cronie the right choice?

# arch.yml Playbook

  * [] Extract arch-chroot/bootloader to a grub role and integrate yubikey LUKS support
  * [] Remove pacman configuration from arch-chroot
  * [] Choose display manager -> https://wiki.archlinux.org/index.php/Display_manager
  * [] Extract pacman role from the spark project base to include the paccache service and mirrorlist hook
  * [] Add hardening.yml role to arch-base or arch-bootstrap based on https://wiki.archlinux.org/index.php/security.  Also, look at the hardening role in Spark.
  * [] Merge arch-base/audio into the pulseaudio role
  * [] Extract arch-base/media into an automount role (look for a version to pull from Galaxy)
  * [] Extract codecs configuration from arch-base/media to an audio-codecs role
  * [] Extract sudo from arch-base/user to a sudo role (look for a version to pull from Galaxy)
  * [] Create a journald role based on the journald configuration in Spark/base
  * [] Adapt the tarsnap role from spark
  * [] Extract the laptop role to a power management role and validate against https://wiki.archlinux.org/index.php/Power_management
  * [] Update to network-manager to reflect https://wiki.archlinux.org/index.php/NetworkManager#Using_Gnome-Keyring

# mise

  * [] [i3blocks](https://github.com/vivien/i3blocks)?
  * [] [good i3 example](https://github.com/da-edra/dotfiles)
  * [] Roles
    * [] VLC
    * [] evince
    * [] [clementine](https://www.clementine-player.org/)
    * [] urxvt
    * [] keybase
    * [] tmuxinator
    * [] tmux
      * [] Linux clipboard integration
      * [] Laptop flag to indicate whether or not include the battery meter
    * [] Visual diff tool -- meld, kdiff3, kompare?  Not a lot of great choices
  * [] Host-based group vars
  * [] gnome-screenshot to capture screenshots? (https://www.howtoforge.com/tutorial/taking-screenshots-in-linux-using-gnome-screenshot/ or https://github.com/Roger/escrotum or http://shutter-project.org/)
    * [] Upload screenshot to s3 + shorten URL with bit.ly
  * [] Clipboard Manager (https://hluk.github.io/CopyQ/ or https://github.com/mrichar1/clipster/blob/master/clipster)
