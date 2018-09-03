# 什么是数据卷？

  数据卷是一个可供一个或 多个容器使用的特殊目录，它绕过 UFS，可以提供很多有用的特性：

* 数据卷可以在容器之间共享和重用
* 对数据卷的修改会立马生效
* 对数据卷的更新，不会影响镜像
* 卷会一直存在，直到没有容器使用 \*数据卷的使用，类似于 Linux 下对目录或文件进行 mount。

如果删除了挂载的容器，数据卷并不会被自动删除。如果要删除一个数据卷，必须在最后一个还挂载着它的容器时使用docker rm -v命令来指定同时删除关联的容器。这可以让用户在容器之间升级和移动数据卷。


