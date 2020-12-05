使用 `host` 命令以及一些国际公用DNS服务器查找有关 github 域名的ip，并使用 ping 测试 ip 的连通性。

来为 github 生成 hosts 文件，解决 git clone 缓慢的问题。

## 依赖

```
grep cut host uniq
```

- Arch 

```
sudo pacman -S bind
```

## 使用

```bash
git clone https://github.com/caigoul/github-hosts
cd github-hosts
./get
cat hosts >> /etc/hosts
```

## 日志

- /tmp/ping.loh
- /tmp/dns.log

查看 ping 某个域名域名之后的情况：

```bash
$ cat /tmp/ping.log|grep -e 'github.global.ssl.fastly.net.*ms'
ping 151.101.77.194      github.global.ssl.fastly.net ... 233.254 ms
ping 151.101.25.194      github.global.ssl.fastly.net ... 195.898 ms
ping 151.101.229.194     github.global.ssl.fastly.net ... 238.921 ms
```