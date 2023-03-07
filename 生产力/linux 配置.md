# linux 配置

#### 内核相关的配置参数

```bash
# sudo vi /etc/sysctl.conf
# sysctl -p
kernel.shmmax = 4398046511104
kernel.shmmni = 4096
kernel.shmall = 2097152

vm.min_free_kbytes = 524288
vm.vfs_cache_pressure = 200
vm.swappiness = 0
fs.file-max = 6815744
fs.aio-max-nr = 1048576
kernel.sysrq = 1
kernel.sem = 50100 128256000 50100 2560
net.core.rmem_default = 2621440
net.core.wmem_default = 2621440
net.core.rmem_max = 2621440
net.core.wmem_max = 2621440
net.ipv4.tcp_rmem = 4096        655360   2621440
net.ipv4.tcp_wmem = 4096        655360   2621440
```

#### linux的最大打开文件数限制修改方法

```bash
# vi /etc/security/limits.conf
* soft nofile 65535
* hard nofile 65535
```
