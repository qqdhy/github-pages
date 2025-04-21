# GitHub



## Q&A

### GitHub打不开

#### 原因

DNS解析被墙

#### 解决方案

1. 用 ping 命令找到github.com的IP

```shell
panda18@Panda16 ~ % ping github.com
PING github.com (20.205.243.166): 56 data bytes
64 bytes from 20.205.243.166: icmp_seq=0 ttl=107 time=125.111 ms
64 bytes from 20.205.243.166: icmp_seq=1 ttl=107 time=162.588 ms
64 bytes from 20.205.243.166: icmp_seq=2 ttl=107 time=159.371 ms
```

2. 在 hosts 文件中加入 github.com DNS

* Windows: `C:\Windows\System32\drivers\etc\hosts`
* MacOS, Linux: `/etc/hosts`

增加

```
20.205.243.166 github.com
```

3. 刷新DNS缓存

* Windows `ipconfig /flushdns`
* MacOS `sudo dscacheutil -flushcache` `sudo killall -HUP mDNSResponder`

