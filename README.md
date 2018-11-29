# hpbtools
本脚本面向的用户为 **对linux操作不熟悉**,或者**懒于自己手动搭建**的**持有hpb硬件板卡**的节点用户,
它会帮助你方便快速的完成安装,更新,启动,登录控制台,收集日志
如果你想使用 hpbtool 来管理节点，不管您之前是否已经搭建好了ghpb节点, 都需要使用本脚本
重新安装一次, 安装操作非常简单，只需要准备好您的账户的keystore文件并执行`hpbtool install`
即可.

# 安装ghpb
```
$ sudo apt-get install -y git
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
# 安装示例
安装过程中主要的就是输入 **keystore文件所在路径,账户地址(要以0x开头),账户的密码(不是系统的账户密码,是hpb账户的密码)** 三个内容,其他的全部是自动执行.
>
[14:45:28] 注意:
[14:45:28]   本脚本将会删除 /opt/ghpb-bin 下的所有内容并将最新版的 ghpb 安装到 /opt/ghpb-bin 目录下. 
[14:45:28] 如果你之前在其他位置已经安装过，请不要再使用之前的版本，以免发生冲突.
[14:45:28] 请确保你已经将账户的keystore文件存放到本机器的某个目录下,稍后将会用到它.
[14:45:28] ghpb 程序需要用到 UDP/TCP 下的30303 和30403两个端口，请确保它们是开放状态.
确定要继续安装吗? [y/N] **y**
安装 git wget curl vim
[14:45:30] 检查并删除已经安装的文件
Removed symlink /etc/systemd/system/multi-user.target.wants/ghpb@root.service.
[14:45:31] 停掉当前运行的所有ghpb程序
[14:45:31] 创建安装目录
<<< 请输入账户keystore所在路径并按[Enter]结束: **/home/hpb/UTC--2018-11-28T08-50-27.316949579Z--75242c38918f089aa2d0f50f89a2052ef3dcda74**
<<< 请输入账户地址并按[Enter]结束: **0x75242c38918f089aa2d0f50f89a2052ef3dcda74**
<<< 请输入账户的密码并按[Enter]结束: **123**
[14:45:51] 开始检查内核
[14:45:57] 内核检查通过
[14:45:57] 检测到已安装 ntp
[14:45:57] 同步本地时间
[14:45:58] 启动ntp服务
[14:45:58] 下载最新版ghpb
[14:46:00] 当前最新版本为 ghpb-v1.0.2.3
[14:46:32] 下载gensis.json
[14:46:33] 初始化节点
INFO [11-29|14:46:33]  HPB : Create New HpbConfig object 
INFO [11-29|14:46:33]  HPB : Allocated cache and file handles  database=/opt/ghpb-bin/node/data/ghpb/chaindata cache=16 handles=16
INFO [11-29|14:46:33]  HPB : Writing custom genesis block 
INFO [11-29|14:46:33]  HPB : Successfully wrote genesis state  database=chaindata                              hash=9c3704…f39966
[14:46:33] 拷贝keystore文件
[14:46:33] 创建密码文件
[14:46:33] 设置ghpb开机启动
Created symlink from /etc/systemd/system/multi-user.target.wants/ghpb@root.service to /etc/systemd/system/ghpb@.service.
[14:46:33] 清除临时目录
[14:46:33] 启动ghpb
[14:46:38] ghpb已经启动,你可以输入 hpbtool attach 进入ghpb控制台


