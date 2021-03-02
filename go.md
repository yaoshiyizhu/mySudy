# go fyne 编译
```bash
env CC=x86_64-w64-mingw32-gcc CGO_ENABLED=1 GOOS=windows go build -o main_x64.exe -ldflags="-H windowsgui"
````
```bash
/usr/lib/gcc/x86_64-pc-cygwin/10/../../../../x86_64-pc-cygwin/bin/ld: cannot find -lmingwex
/usr/lib/gcc/x86_64-pc-cygwin/10/../../../../x86_64-pc-cygwin/bin/ld: cannot find -lmingw32
```
出现上面问题，安装cygwin64 和tdm-gcc两环境
### 下载切换到http://tdm-gcc.tdragon.net/download环境，然后再系统环境变量path里把tdragon的位置上移到cygwin上面，让系统调用gcc时先识别tdragon的gcc，或者直接把cygwin的环境路径直接删除了，或者直接从goland里的settings->Go->GoPath里添加tdragon的路径
