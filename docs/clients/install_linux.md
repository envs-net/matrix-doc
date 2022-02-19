---
title: "Install on Linux"
date: 2021-08-03T20:30:00+02:00
---

# Install Element Desktop on Linux
We recommend using the package manager of your System to install Element Desktop. The following commands will install element desktop. You can enter them on the command line.

### Debian/Ubuntu
```sh
sudo apt install -y wget apt-transport-https
sudo wget -O /usr/share/keyrings/element-io-archive-keyring.gpg https://packages.element.io/debian/element-io-archive-keyring.gpg
echo "deb [signed-by=/usr/share/keyrings/element-io-archive-keyring.gpg] https://packages.element.io/debian/ default main" | sudo tee /etc/apt/sources.list.d/element-io.list
sudo apt update

sudo apt install element-desktop
```

### Fedora
```sh
sudo dnf install -y dnf-plugins-core distribution-gpg-keys
sudo dnf copr enable taw/element
sudo dnf install -y element --refresh
```

### Arch Linux
```sh
sudo pacman -Sy element-desktop
```

### NixOS
```sh
nix-env -iA nixos.element-desktop
```

### macOS homebrew
```sh
brew install element
```