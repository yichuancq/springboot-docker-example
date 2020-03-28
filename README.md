#docker-example
### docker国内阿里云安装文件Mac版镜像
#### http://mirrors.aliyun.com/docker-toolbox/mac/docker-for-mac/stable/
### docker镜像源设置，私有源访问设置
### mac下path默认安装为/Users/{$user}/.docker/daemon.json
   
    在 macOS Sierra及以上(Mojave)，我们可以使用快捷键 ⌘⇧.(Command + Shift + .) 来快速（在 Finder 中）显示和隐藏隐藏文件
### 内容如下：
```
{
  "experimental": false,
  "debug": true,
  "registry-mirrors": [
    "http://hub-mirror.c.163.com",
    "https://registry.docker-cn.com",
    "https://docker.mirrors.ustc.edu.cn"
  ],
  "insecure-registries": [
    "registry.lib.c.siac.net"
  ]
}
```
### docker版本查看
```
yichuan@yichuandeMacBook-Pro-2 ~ % docker -v
Docker version 19.03.8, build afacb8b

```
### 修改后重启docker客户端或者用命令重启才能生效，用docker info查看是否修改成功
```
yichuan@yichuandeMacBook-Pro-2 ~ % docker info
Client:
 Debug Mode: false

Server:
 Containers: 10
  Running: 0
  Paused: 0
  Stopped: 10
 Images: 15
 Server Version: 19.03.8
 Storage Driver: overlay2
  Backing Filesystem: <unknown>
  Supports d_type: true
  Native Overlay Diff: true
 Logging Driver: json-file
 Cgroup Driver: cgroupfs
 Plugins:
  Volume: local
  Network: bridge host ipvlan macvlan null overlay
  Log: awslogs fluentd gcplogs gelf journald json-file local logentries splunk syslog
 Swarm: inactive
 Runtimes: runc
 Default Runtime: runc
 Init Binary: docker-init
 containerd version: 7ad184331fa3e55e52b890ea95e65ba581ae3429
 runc version: dc9208a3303feef5b3839f4323d9beb36df0a9dd
 init version: fec3683
 Security Options:
  seccomp
   Profile: default
 Kernel Version: 4.19.76-linuxkit
 Operating System: Docker Desktop
 OSType: linux
 Architecture: x86_64
 CPUs: 2
 Total Memory: 3.846GiB
 Name: docker-desktop
 ID: WX4B:HSWY:DIUF:O3D5:AYKG:ODPE:WQWJ:Q56C:KBVM:BM5L:67F4:OOT5
 Docker Root Dir: /var/lib/docker
 Debug Mode: true
  File Descriptors: 34
  Goroutines: 51
  System Time: 2020-03-28T04:50:27.329847237Z
  EventsListeners: 3
 HTTP Proxy: gateway.docker.internal:3128
 HTTPS Proxy: gateway.docker.internal:3129
 Registry: https://index.docker.io/v1/
 Labels:
 Experimental: false
 Insecure Registries:
  registry.lib.c.siac.net
  127.0.0.0/8
 Registry Mirrors:
  https://6kx4zyno.mirror.aliyuncs.com/
  http://hub-mirror.c.163.com/
  https://registry.docker-cn.com/
  https://docker.mirrors.ustc.edu.cn/
 Live Restore Enabled: false
 Product License: Community Engine
```
### 下一步，开干 ☺️！
