# 云盘strm生成

### 更新记录

- 2.2 fix#12
- 2.1 增加复制非媒体文件开关
- 2.0 修复重复执行的问题
- 1.7 支持m2ts视频格式
- 1.6 支持开启监控延迟
- 1.5 优化异步执行
- 1.4 异步开启目录监控
- 1.3 支持全量运行一次
- 1.2 支持本地模式
- 1.1 支持alist链接模式
- 1.0 监控文件创建，生成strm文件

### 使用说明

目录监控格式：

- 1.监控方式#监控目录#目的目录#媒体服务器内源文件路径
- 2.监控方式#监控目录#目的目录#cd2#cd2挂载本地跟路径#cd2服务地址
- 3.监控方式#监控目录#目的目录#alist#alist挂载本地跟路径#alist服务地址

监控方式：

- fast:性能模式，内部处理系统操作类型选择最优解
- compatibility:兼容模式，目录同步性能降低且NAS不能休眠，但可以兼容挂载的远程共享目录如SMB （建议使用）

路径：

- 监控目录：源文件目录即云盘挂载到MoviePilot中的路径
- 目的路径：MoviePilot中strm生成路径
- 媒体服务器内源文件路径：源文件目录即云盘挂载到媒体服务器的路径

示例：

- MoviePilot上云盘源文件路径 /mount/cloud/aliyun/emby`/tvshow/爸爸去哪儿/Season 5/14.特别版.mp4`

- MoviePilot上strm生成路径 /mnt/link/aliyun`/tvshow/爸爸去哪儿/Season 5/14.特别版.strm`

- 媒体服务器内源文件路径 /mount/cloud/aliyun/emby`/tvshow/爸爸去哪儿/Season 5/14.特别版.mp4`

- 监控配置为：compatibility#/mount/cloud/aliyun/emby#/mnt/link/aliyun#/mount/cloud/aliyun/emby
