# 常用HDC命令

相当于Android的adb，用来在PC端与设备（虚拟机）进行命令行的操作

## 目录在

...sdk\hmscore\3.1.0\toolchains

*注意不要用...sdk\openharmony\9\toolchains 否则在打开虚拟机的情况下 执行hdc shell会提示[Fail]ExecuteCommand need connect-key?*

gitee地址

https://gitee.com/openharmony/developtools_hdc_standard#section161941989591

## 常用的HDC命令

### 安装
hdc install -r xxx.hap

### 查看连接设备
hdc list targets

### 卸载应用
hdc app uninstall com.rabbit.demo【替换成你的包名】

### 输出实时日志
hdc hilog

### 进入Shell
HdcExternal shell
*不要用hdc shell，否则会报错：ERR:ohsh para too less!*
