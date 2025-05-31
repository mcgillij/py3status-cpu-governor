# py3status-cpu-governor
Python module for py3status to show the cpu_governor state in i3

[![Downloads](https://static.pepy.tech/personalized-badge/py3status-cpu-governor?period=total&units=international_system&left_color=blue&right_color=green&left_text=Downloads)](https://pepy.tech/project/py3status-cpu-governor)

This is handy if you manage your governor manually with something like or use [gamemode](https://github.com/FeralInteractive/gamemode)

``` bash
alias performance_mode='echo performance | sudo tee /sys/devices/system/cpu/cpu*/cpufreq/scaling_governor'
alias powersave_mode='echo powersave | sudo tee /sys/devices/system/cpu/cpu*/cpufreq/scaling_governor'
alias schedutil_mode='echo schedutil | sudo tee /sys/devices/system/cpu/cpu*/cpufreq/scaling_governor'
alias cpu_frequency_watch='watch -n.5 "cat /proc/cpuinfo | grep \"^[c]pu MHz\""'
```

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

### With pip, pipenv or poetry
``` bash
pip install py3status-cpu-governor
pipenv install py3status-cpu-governor
poetry add py3status-cpu-governor && poetry install
```

### With `yay`

``` bash
yay -S py3status-cpu-governor
```

### Building Arch package w/PKGBUILD
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
