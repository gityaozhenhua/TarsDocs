# 目录

> - [版本说明](#chapter-1)

# 1 <span id="chapter-1"></span>版本说明

使用 TARS 其实涉及到以下几部分:

- TARS 框架部署
- 使用各 TARS 各语言的库实现业务代码

这里主要描述 TARS 框架的版本, TARS 框架主要由三部分组成: TarsCpp, TarsFramework, TarsWeb, 其中 TarsFramework 编译是依赖 TarsCpp 的(通过 submodule 形式引入), 因此确定了 TarsFramework 的版本就确定了使用的 TarsCpp 的版本.

在新版的 Web 平台右上角, 可以看到目前框架的 TarsFramework 和 TarsWeb 的版本!

但是注意以下几点:

- Docker 形式部署时, 拉取的镜像: `tarscloud/framework:$tag`, 这里这个$tag 并不是对应的 TarsFramework 的版本
- `tarscloud/framework`包含了 TarsFramework 也包含了 TarsWeb, 因此无法用 TarsFramework 的版本号来标示
- `tarscloud/framework:$tag` 的 tag 是`https://github.com/TarsCloud/Tars` 对应的 tag 号
- 所有相关代码最终都以 submodule 形式被 Tars 这个 git 所引用, 且 docker 的镜像是通过 Tars 这个 git 的 action 自动编译出来的, 因此对应的该版本号!
