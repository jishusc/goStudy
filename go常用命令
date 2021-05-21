goland报错：package XXX is not in GOROOT (X:\XXX\Go\src\XXX)
原因分析：
因为它是报需要寻找GOROOT下的包，应该是路径问题，或者环境设置问题，输入go env检查了一下环境，发现GO111MODULE=on，编译器没有去gopath下找包。
gomod 和 gopath 两个包管理方案，并且相互不兼容，在 gopath 查找包，按照 goroot 和多 gopath 目录下 src/xxx 依次查找。在 gomod 下查找包，解析 go.mod 文件查找包，mod 包名就是包的前缀，里面的目录就后续路径了。在 gomod 模式下，查找包就不会去 gopath 查找，只是 gomod 包缓存在 gopath/pkg/mod 里面。
————————————————
版权声明：本文为CSDN博主「之芫」的原创文章，遵循CC 4.0 BY-SA版权协议，转载请附上原文出处链接及本声明。
原文链接：https://blog.csdn.net/Magic_Ninja/article/details/113929379

go env -w GO111MODULE=off

