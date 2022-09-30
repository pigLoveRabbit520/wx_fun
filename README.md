# 说明
wxWidgets的一个demo，用MinGW编译的，无需vcruntime依赖。

# 编译
1. 系统上需要环境变量`WXWIN`，`WXWIN`指向你的`wxWidgets`目录，例如`C:\Users\pig\Documents\wxWidgets-3.2.0`
2. 进入build目录执行`cmake -G "MinGW Makefiles" ..`
3. `make`