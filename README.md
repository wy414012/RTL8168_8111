### RTL8111/8168 Driver for OS X ###
=======================================================

- 基于 Realtek RTL8111/8168 开源Linux驱动来进行移植
- 该驱动同步于[GitHub Mieze](https://github.com/Mieze/RTL8111_driver_for_OS_X)的基础上修正制作。
- 更改了默认使用的sdk，改为oc引导项目库的自研sdk保证兼容
### 编译说明 ###
- 安装xcode
- 克隆存储库```git clone https://gitee.com/yaming-network/RTL8111_driver_for_OS_X.git```
- 进入存储库```cd RTL8111_driver_for_OS_X```
- 拉取子模块```git submodule update --init --recursive```
- 切换子模块到主分支```git submodule foreach git checkout master```
- 更新子模块```git submodule foreach git pull```
- 编译Debug版本仅用于调试目的才使用```xcodebuild -jobs 1 -configuration Debug```
- 调试错后即可开始编译REL稳定版本```xcodebuild -jobs 1 -configuration Release```

### 兼容性说明###
- 当前支持：10.9+ -- 12.x已测试通过
- 10.9之前需要使用32位构建