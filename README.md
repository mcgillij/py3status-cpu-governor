# cpu_governor
py3status cpu_governor for i3

## screenshot
![py3status cpu_governor](/images/cpu_governor.png)

## pre-reqs
* i3
* py3status

## installation

``` bash
cp cpu_governor.py ~/.i3/py3status/
```

## configuration

add the following line to your ~/.config/i3/i3status.conf

``` bash
order += "cpu_governor"
```

restart i3
