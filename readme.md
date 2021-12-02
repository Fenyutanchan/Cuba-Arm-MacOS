# 关于 `Cuba` 积分库在 M1 Mac 上的编译安装

## 1. 准备工作

- 首先从 http://www.feynarts.de/cuba/ 处下载 `Cuba-x.y(.z).tar.gz`.
- 解压, 准备安装.
- 我个人建议更新 `config.guess` 与 `config.sub` 两个文件, 它们都可以通过其内部提供的下载信息进行更新.

## 2. 配置并安装

- 现在在解压后的目录下运行 `./configure --prefix=/path/to/`, 我建议配置安装路径, 例如我的安装路径在 `$(HOME)/.local/`.
- 接下来运行 `make && make install` 即可.

## 3. 测试

- 现在我们有 `./demo-c` 与 `./demo-fortran` 两个测试程序, 请运行它们并查看结果.

## 3. 注意事项

- 本次我采用的 `gcc` 是 MacOS 自带的, 如果要用 GNU 工具链请自行配置.
- 由于我在运行 `./configure` 之后生成的 `./makefile` 中注意到其第八行为 `INSTALL = /opt/homebrew/opt/coreutils/libexec/gnubin/install -c`, 因此我强烈建议首先安装 GNU 工具链.