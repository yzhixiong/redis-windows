
# Redis Windows版本

### 借助GitHub Actions强大的自动化构建能力，为我们实时编译适用于Windows系统的Redis最新版本

整个编译过程完全公开透明， 编译脚本在[.github/workflows/](https://github.com/yzhixiong/redis-windows/tree/main/.github/workflows) 目录中，编译日志可在 [Actions](https://github.com/yzhixiong/redis-windows/actions)页面查看。此外，我们在编译结束，新增了哈希值计算环节，计算结果打印在日志中，这是任何人不可修改的，并写入发布页面。您可以核对下载到本地的文件的哈希值，是否与日志和发布页面的一致。本项目绝对纯洁无私货，经得起各位大佬审查。如您有好的想法，也欢迎交流。


### 提供三种运行模式

直接运行项目中的 start.bat 脚本，一键启动

或者使用命令行

还支持以系统服务运行


## 命令行启动
cmd 启动
```shell
redis-server.exe redis.conf
```
powershell 启动
```shell
./redis-server.exe redis.conf
```

## 安装服务
可实现开机自启动
请以管理员身份运行，并将RedisService.exe改为您实际存放的路径

```shell
sc.exe create Redis binpath=C:\Software\Redis\RedisService.exe start= auto
```
启动服务
```shell
net start Redis
```
停止服务
```shell
net stop Redis
```
卸载服务
```shell
sc.exe delete Redis
```

![image](https://user-images.githubusercontent.com/515784/215540157-65f55297-cde2-49b3-8ab3-14dca7e11ee0.png)
