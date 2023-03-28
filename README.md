# 说明
wxWidgets的一个没多余依赖demo exe，用MinGW编译的，无需vcruntime依赖。

# Prerequisite
* [MinGW](https://sourceforge.net/projects/mingw-w64/files/mingw-w64/)
* 编译wxWidgets的静态库：进入wxWidgets解压目录中`build\msw`目录，执行`mingw32-make -f makefile.gcc SHARED=0 UNICODE=1 BUILD=release`，加`-j`可以利用多核编译，如`-j4`用4个核

# 编译
1. 系统上需要环境变量`WXWIN`，`WXWIN`指向你的`wxWidgets`目录，例如`C:\Users\pig\Documents\wxWidgets-3.2.0`
2. 进入build目录执行`cmake -G "MinGW Makefiles" ..`
3. `make`
