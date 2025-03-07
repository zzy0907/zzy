# 自动化 Fabric Minecraft 服务器

这是一个使用 GitHub Actions 自动运行的 Minecraft Fabric 服务器。

## 特点

- 每6小时自动重启一次
- 自动备份世界数据
- 使用 Fabric 1.20.1
- 支持最多20名玩家
- 无需手动维护

## 连接信息

服务器地址将在 Actions 运行时显示在日志中。

## 注意事项

1. 服务器每次运行5分钟后会自动关闭
2. 世界数据会自动保存和备份
3. 可以通过手动触发 workflow 来启动服务器 

## 性能优化

服务器配置了以下优化:
- 使用G1GC垃圾收集器
- 内存分配: 2-3GB
- JVM参数优化以提高性能
- 自动重启机制确保服务器稳定运行

## 如何使用

1. Fork 这个仓库到你的账号
2. 在仓库的 Settings -> Actions -> General 中启用 GitHub Actions
3. 在 Actions 标签页中手动触发 workflow 或等待自动运行
4. 在 Actions 运行日志中查看服务器IP地址

## 添加模组

要添加模组,只需:
1. 在仓库中创建 `server/mods` 目录
2. 上传你想要的模组到该目录
3. 提交更改,服务器将在下次启动时自动加载模组 