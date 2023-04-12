Redirect connections from different ports at one ipv4 address to unique random ipv6 address from \64 subnetwork. Based on 3proxy

## Requirements
- Centos 7
- Ipv6 \64

## Installation
[Video tutorial](https://www.youtube.com/watch?v=F6hhNfFKQEk, used as Centos setup

1. `bash <(curl -s "https://raw.githubusercontent.com/quayvlog/proxyv6/main/install.sh")`

1. After installation dowload the file `proxy.zip`
   * File structure: `IP4:PORT:LOGIN:PASS`
   * You can use this online [util](https://www.youtube.com/watch?v=F6hhNfFKQEk
) to change proxy format as you like


https://wiki.iphoster.net/wiki/3proxy_-_Warning:_current_open_file_ulimits_are_too_low,_maxconn_requires_at_least_16384_for_every_running_service


```
# vi /etc/security/limits.conf
# End of file
*               soft    nofile          500000
*               hard    nofile          500000
root            hard    nofile          500000
root            soft    nofile          500000


# reboot
# ulimit -n
500000

# sockstat  | grep 3proxy | wc -l
```


The source : 3proxy
