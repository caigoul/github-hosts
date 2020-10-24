使用 `host` 命令以及一些国际公用DNS服务器查找有关 github 域名的ip，并使用 ping 测试 ip 的连通性。

来为 github 生成 hosts 文件，解决 git clone 缓慢的问题。

## 依赖

```
grep cut host uniq
```

## 使用

```bash
git clone https://github.com/caigoul/github-hosts
cd github-hosts
chmod +x ./get
./get
cat hosts >> /etc/hosts
```