# Glances

Glances is an open-source system cross-platform monitoring tool. It allows real-time monitoring of various aspects of your system such as CPU, memory, disk, network usage etc. It also allows monitoring of running processes, logged in users, temperatures, voltages, fan speeds etc. It also supports container monitoring, it supports different container management systems such as Docker, LXC. The information is presented in an easy to read dashboard and can also be used for remote monitoring of systems via a web interface or command line interface. It is easy to install and use and can be customized to show only the information that you are interested in.

nicolargo.github.io/glances

<img src="https://nicolargo.github.io/glances/public/images/glances.png" width="30%" height="auto">

## How to use this Makejail

```sh
appjail makejail \
	-j glances \
	-f gh+AppJail-makejails/glances \
	-o virtualnet=":glances default" \
	-o nat \
	-o expose=61208
```

### Arguments

* `glances_tag` (default: `13.5`): see [#tags](#tags).
* `glances_ajspec` (default: `gh+AppJail-makejails/glances`): Entry point where the `appjail-ajspec(5)` file is located.

## Tags

| Tag    | Arch    | Version        | Type   |
| ------ | ------- | -------------- | ------ |
| `13.5` | `amd64` | `13.5-RELEASE` | `thin` |
| `14.2` | `amd64` | `14.2-RELEASE` | `thin` |

## Notes

1. Remember to load the corresponding kernel module to enable an additional feature, such as temperature using the `coretemp` or `amdtemp` kernel module.
