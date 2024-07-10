# Script Requirements

## BASH Version (Tested)

* GNU bash, version 5.1.4(1)-release (x86_64-pc-linux-gnu)

## Required Packages for Script

### Both Linux and Windows OS

* [charmbracelet/gum](https://github.com/charmbracelet/gum)
* [jqlang/jq](https://github.com/jqlang/jq)
* [TomWright/dasel](https://github.com/TomWright/dasel)
* [aria2/aria2](https://github.com/aria2/aria2)
* [Git SCM](https://git-scm.com/)
* [git-ecosystem/git-credential-manager](https://github.com/git-ecosystem/git-credential-manager)
* [restic/restic](https://github.com/restic/restic)
* [rclone/rclone](https://github.com/rclone/rclone)
* [bcpierce00/unison](https://github.com/bcpierce00/unison)
* [WayneD/rsync](https://github.com/WayneD/rsync)

### Linux-OS Only

* [Xfennec/progress](https://github.com/Xfennec/progress)
* [dooblem/bsync](https://github.com/dooblem/bsync)

## Required Commands for Script

### Both Linux and Windows OS

* curl - Used to download or upload data to a server via supported protocols such as HTTP, FTP, IMAP, SFTP, TFTP, IMAP, POP3, SCP, etc.

### Linux-OS (Commands)

* ifconfig - To get IP address of current device
* column - Format output into a column format
* cp - Used to copy one or more files on a Linux system
* mv - Moves files and directories from one directory to another or renames a file or directory
* touch - Used to create, change and modify the timestamps of a file
* mkdir - Create one or more directories specified by the Directory parameter
* rm - Used to remove objects such as files, directories, symbolic links and so on from the file system

## Additional Packages for Script

### Both Linux and Windows OS

* [emuell/restic-browser](https://github.com/emuell/restic-browser)
* [rclone/rclone-webui-react](https://github.com/rclone/rclone-webui-react)
* [kapitainsky/RcloneBrowser](https://github.com/kapitainsky/RcloneBrowser)

# Additional Software

## Both Linux and Windows OS

* [wez/wezterm](https://github.com/wez/wezterm)
* [Xampp](https://www.apachefriends.org/)
* [Docker](https://www.docker.com/)
* [Vagrant](https://www.vagrantup.com/)
* [VirtualBox](https://www.virtualbox.org/)

## Linux OS

## Windows OS

* [Windows Subsystem for Linux](https://learn.microsoft.com/en-us/windows/wsl/install)

# Package/Software Installation

## Antix-OS/Debian/Ubuntu/WSL

* "ifconfig" command (If not available)
  * `sudo apt install net-tools`

* [charmbracelet/gum](https://github.com/charmbracelet/gum)
  * Installation instruction:
```shellscript
# Debian/Ubuntu
sudo mkdir -p /etc/apt/keyrings
curl -fsSL https://repo.charm.sh/apt/gpg.key | sudo gpg --dearmor -o /etc/apt/keyrings/charm.gpg
echo "deb [signed-by=/etc/apt/keyrings/charm.gpg] https://repo.charm.sh/apt/ * *" | sudo tee /etc/apt/sources.list.d/charm.list
sudo apt update && sudo apt install gum
```
  * Check "gum" version: `gum --version`

* [jqlang/jq](https://github.com/jqlang/jq)
  * Install via APT: `sudo apt install jq`
  * Check "jq" version: `jq --version`

* [TomWright/dasel](https://github.com/TomWright/dasel)
  * Download ["dasel" program](https://github.com/TomWright/dasel/releases)
  * Use "wget" to download: `wget <URL>`
  * Rename "dasel": `mv dasel_linux_amd64 dasel`
  * Change permission: `sudo chmod a+x dasel`
  * Move "dasel" to executable path: `sudo mv dasel /usr/local/bin/dasel`
  * Check "dasel" version: `dasel --version`

* [aria2/aria2](https://github.com/aria2/aria2)
  * Install via APT: `sudo apt install aria2`
  * Check "aria2c" version: `aria2c --version`

* [Git SCM](https://git-scm.com/)
  * Install via APT: `sudo apt install git`
  * Check "git" version: `git --version`

* [git-ecosystem/git-credential-manager](https://github.com/git-ecosystem/git-credential-manager)
  * Download DEB file from [GitCredentialManager DEB File](https://github.com/GitCredentialManager/git-credential-manager/releases/download/v2.0.886/gcm-linux_amd64.2.0.886.deb)
  * Use "wget" to download: `wget <URL>`
  * Install: `sudo dpkg -i <path-to-package>`
  * Check version: `git-credential-manager --version`
  * Installation configure: `git-credential-manager configure`
  * Check credential helper: `git config --global credential.helper`
  * Check credential store: `git config --global credential.credentialStore`
  * Uninstallation configure: `git-credential-manager unconfigure`
  * Uninstall: `sudo dpkg -r gcm`

* [restic/restic](https://github.com/restic/restic)
  * Install via APT: `sudo apt install restic` [Install old version]
  * Check "restic" version: `restic version`
  * Update restic: `sudo restic self-update`

* [rclone/rclone](https://github.com/rclone/rclone)
  * Install via APT: `sudo apt install rclone` [Install old version]
  * Install rclone on Linux/macOS/BSD systems: `sudo -v ; curl https://rclone.org/install.sh | sudo bash` [Install new version]
  * Check "rclone" version: `rclone version`

* [bcpierce00/unison](https://github.com/bcpierce00/unison)
  * Install via APT: `sudo apt install unison`
  * Check "unison" version: `unison -version`

* [WayneD/rsync](https://github.com/WayneD/rsync)
  * Rsync is pre-installed in Linux.
  * Check "rsync" version: `rsync --version`

* [Xfennec/progress](https://github.com/Xfennec/progress)
  * Install via APT: `sudo apt install progress`
  * Check "progress" version: `progress --version`

* [dooblem/bsync](https://github.com/dooblem/bsync)
  * Download "bsync" script: `wget https://raw.github.com/dooblem/bsync/master/bsync`
  * Make script executable: `chmod +x bsync`
  * Move script to path: `sudo mv bsync /usr/local/bin/bsync`
  * Check "bsync" is in path: `which bsync`
  * Get help: `bsync --help`

## Windows-OS

* [charmbracelet/gum](https://github.com/charmbracelet/gum)
  * Add scoop bucket: `scoop bucket add main`
  * Install via scoop: `scoop install --global main/charm-gum`
  * Check "gum" version: `gum --version`

* [jqlang/jq](https://github.com/jqlang/jq)
  * Add scoop bucket: `scoop bucket add main`
  * Install via scoop: `scoop install --global main/jq`
  * Check "jq" version: `jq --version`

* [TomWright/dasel](https://github.com/TomWright/dasel)
  * Add scoop bucket: `scoop bucket add extras`
  * Install via scoop: `scoop install --global extras/dasel`
  * Check "dasel" version: `dasel --version`

* [aria2/aria2](https://github.com/aria2/aria2)
  * Add scoop bucket: `scoop bucket add main`
  * Install via scoop: `scoop install --global main/aria2`
  * Check "aria2" version: `aria2c --version`

* [Git SCM](https://git-scm.com/)
  * Add scoop bucket: `scoop bucket add main`
  * Install via scoop: `scoop install --global main/git`
  * Check "git" version: `git --version`

* [git-ecosystem/git-credential-manager](https://github.com/git-ecosystem/git-credential-manager)
  * Pre-Installed with Git-Bash
  * Check "git-credential-manager" version: `git-credential-manager --version`

* [restic/restic](https://github.com/restic/restic)
  * Add scoop bucket: `scoop bucket add main`
  * Install via scoop: `scoop install --global main/restic`
  * Check "restic" version: `restic version`

* [rclone/rclone](https://github.com/rclone/rclone)
  * Add scoop bucket: `scoop bucket add main`
  * Install via scoop: `scoop install --global main/rclone`
  * Check "rclone" version: `rclone version`

* [bcpierce00/unison](https://github.com/bcpierce00/unison)
  * Add scoop bucket: `scoop bucket add main`
  * Install via scoop: `scoop install --global main/unison`
  * Check "unison" version: `unison -version`

* [WayneD/rsync](https://github.com/WayneD/rsync)
  * {9} [Add rsync to Windows git bash](https://prasaz.medium.com/add-rsync-to-windows-git-bash-f42736bae1b3)
  * {10} [How to use rsync on Git Bash](https://shchae7.medium.com/how-to-use-rsync-on-git-bash-6c6bba6a03ca)
  * Open PowerShell in Administrator mode and install Git-Bash: `scoop install --global git`
  * Download `rsync-<version>-x86_64.pkg.tar.zst` from [MSYS2 Repo](https://repo.msys2.org/msys/x86_64/)
  * Download and install [ZStandard compression package](https://facebook.github.io/zstd/) which is used to extract ".tar.zst" file.
  * Extract "rsync.tar.zst" file: `zstd -d rsync-<version>-x86_64.pkg.tar.zst`
  * Alternatively, install [PeaZip](https://peazip.github.io/): `scoop install --global peazip` [Extracts ".tar.zst" file]
  * Copy the `rsync.exe` inside the package from `rsync-<version>-x86_64.pkg\usr\bin\` to `C:\ProgramData\scoop\apps\git\current\usr\bin\`
  * Download and copy the dependent packages
    * [Package: libzst](https://repo.msys2.org/msys/x86_64/libzstd-1.4.7-1-x86_64.pkg.tar.xz)
    * [Package: libxxhash](https://repo.msys2.org/msys/x86_64/libxxhash-0.8.0-1-x86_64.pkg.tar.zst)
  * Open Git-Bash and check "rsync": `rsync --version`

# Move To Path

* Linux: `sudo cp jjk /usr/local/bin/jjk`
* Windows (Git-Bash): `sudo cp jjk /usr/bin/jjk`

# References

* Installation
  * {1} [Charmbracelet Gum Installation](https://github.com/charmbracelet/gum#installation)
  * {2} [Download jq](https://jqlang.github.io/jq/download/)
  * {3} [Dasel Installation](https://daseldocs.tomwright.me/installation)
  * {4} [GitCredentialManager Install Instructions](https://github.com/git-ecosystem/git-credential-manager/blob/release/docs/install.md)
  * {5} [Restic Installation](https://restic.readthedocs.io/en/stable/020_installation.html)
  * {6} [Rclone Install](https://rclone.org/install/)
  * {7} [Progress - How do you install it](https://github.com/Xfennec/progress#how-do-you-install-it)
  * {8} [Bsync Install](https://github.com/dooblem/bsync#install)
  * {9} [Add rsync to Windows git bash](https://prasaz.medium.com/add-rsync-to-windows-git-bash-f42736bae1b3)
  * {10} [How to use rsync on Git Bash](https://shchae7.medium.com/how-to-use-rsync-on-git-bash-6c6bba6a03ca)
