# py3status-cpu-governor
Python module for py3status to show the cpu_governor state in i3

## Screenshot
![py3status cpu_governor](https://raw.githubusercontent.com/mcgillij/py3status-cpu-governor/main/images/cpu_governor.png)

## Pre-reqs
* i3
* py3status

## Installation
### From Git
``` bash
git clone https://github.com/mcgillij/py3status-cpu-governor.git
mkdir -p ~/.i3/py3status && cd ~/.i3/py3status
ln -s <PATH_TO_CLONED_REPO>/src/py3status-cpu-governor/cpu_governor.py ./
```

### With Pip
``` bash
pip install py3status-cpu-governor
```

### Building From AUR (Arch)
``` bash
git clone https://aur.archlinux.org/py3status-cpu-governor.git
cd py3status-cpu-governor.git
makechrootpkg -c -r $HOME/$CHROOT
```

### Installing Arch package
``` bash
sudo pacman -U --asdeps py3status-cpu-governor-*-any.pkg.tar.zst
```

## Configuration

add the following line to your *~/.config/i3/i3status.conf*

``` bash
order += "cpu_governor"
```

And restart your i3 session.
