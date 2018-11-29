# hpbtools
本脚本面向的用户为 **对linux操作不熟悉**,或者**懒于自己手动搭建**的**持有hpb硬件板卡**的节点用户,
它会帮助你方便快速的完成安装,更新,启动,登录控制台,收集日志
如果你想使用 hpbtool 来管理节点，不管您之前是否已经搭建好了ghpb节点, 都需要使用本脚本
重新安装一次, 安装操作非常简单，只需要准备好您的账户的keystore文件并执行`hpbtool install`
即可.

# 安装ghpb
```
$ git clone https://github.com/hpb-project/hpbtools
$ cd hpbtools
$ ./hpbtool help
$ sudo ./hpbtool install
```

# 更新ghpb
```
$ sudo hpbtool update
```

# 进入ghpb控制台
```
$ hpbtool attach
```

# 所有命令
```
hpbtool 用法:
    hpbtool install        安装/重新安装 ghpb程序
    hpbtool update         更新官方最新版发布的 ghpb 程序
    hpbtool start          启动ghpb程序
    hpbtool status         查看ghpb程序是否启动
    hpbtool stop           停止ghpb程序
    hpbtool attach         登录到ghpb控制台
    hpbtool getlog         生成ghpb运行的日志文件
    hpbtool taillog        实时查看ghpb的日志信息
    hpbtool catchlog       查看ghpb运行的历史日志
```
