# Tenant
## 1 单Teanat
- Tenant是通过向AP服务器上发布war文件来进行构建的
- 在iAP中，单Tenant的情况下，1个war文件 = 1个Tenant
- 每个Tenant都必须对应Storage下的一个专属目录及一个专属DB存储区域来存储信息

## 2 物理多Teanat（分成多个war文件）

1. 样式1 
在一个Resin上配置多个war文件
（适用于服务器资源有限的情况，可以充分使用服务器的资源，但一个Tenant负荷加重，另一个也有影响）

2. 样式2
有多台AP服务器组成分布式环境，每台服务器上只配备一个Resin，每个Resin上只配置一个war文件（性能最好但最花钱）

## 3 虚拟多Teanat（1个war文件中可以有多个tenant）
- 在1个war文件中理论上可以创建不超过100个的tenant（推荐不要超过20个）
- 为了区分Tenant，每个Tenant使用各自的DB存储区域，共享Stroage存储区域
- 每个Tenant共享一个URL,访问同一个URL后在画面上输入TenantID进行登陆
- 各Tenant共享应用程序
- 仅支持Resin

## 脚本开发的两个基础要点

1. 接收到请求后首先执行 “init() 方法”
2. 可以从Function Container向Presentation Page传递值的是“全局变量”。