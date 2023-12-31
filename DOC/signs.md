## 应用安装到虚拟机不需要签名

## 安装到真机需要签名,而且还要登录华为的账号

### 1.用自动签名

在IDE里-File-"Project Structure-Signing Configs"，勾选Automatically generate signature，登录自己的华为账号，会在下面的Signing自动生成一个关联了你华为账号的debug签名，并且自动修改根目录build-profile.json5，这时候是可以直接安装到设备的。

**这种方法是日常开发调试用的**

### 2.用调试签名

一句话讲就是要生成csr、p12、cer、p7b这4个文件，在项目里正确引用就可以了。

1. 在IDE-Build-"Generate Key and CSR" 创建两个签名文件：csr、p12
2. 在华为[AppGallery Connect](https://developer.huawei.com/consumer/cn/service/josp/agc/index.html#/) 的用户与访问-证书管理里创建签名：这里选调试签名，建完下载cer文件存好
3. 在华为AppGallery Connect 的用户与访问-设备管理里创建设备：需要填udid，如果是类手机设备输入`hdc shell bm get --udid`即可
4. 在华为AppGallery Connect 的用户与访问-我的应用里建一个应用，先不要进行后续上架流程
5. 在华为AppGallery Connect 的用户与访问-我的项目-HarmonyOS应用-"HAP Provision Profile"管理里添加一个Profile，要选择刚刚的调试设备，下载p7b文件存好
6. 回到IDE里-File-"Project Structure-Signing Configs"添加正确的签名文件路径和信息就好了

### 3.用发布签名安装

步骤和“2.用调试签名”一样，只不过cer和p7b需要选择发布类型。但是不要用发布的签名直接本地生成app给设备安装，否则会提示：`Install Failed: [Info]App install path:D:\RABBIT\LocalCode\Harmony\WebComponent\entry\build\default\outputs\default\entry-default-signed.hap, queuesize:0, msg:error: failed to install bundle. error: signature verification failed due to not trusted app source.`

这个问题在官方论坛很多人都问了，回答是必须要上架市场才能给各种设备安装。如果要上架市场，**需要公司提供“应用版权证书或代理证书”、“隐私政策网址”**