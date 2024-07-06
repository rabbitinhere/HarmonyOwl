# HarmonyOwl
![image info](/Images/Logo/Logo_64x64.png)  

一个鸿蒙路书项目，提供靠谱、易懂、诚实的开发指导😉 **项目进度1% 欢迎帮助建设本项目**

原则：
1. 用**链接整合**快速引导开发者
2. **官方文档没说但又经常使用的内容**
3. 所有内容均**实际验证过**

### 华为官方链接

[外链：官方论坛](https://developer.huawei.com/consumer/cn/forum/)

[外链：官方小demo合集](https://gitee.com/harmonyos/codelabs)

[外链：官方文档中心搜索](https://developer.huawei.com/consumer/cn/doc/)

[外链：官方API文档](https://developer.harmonyos.com/cn/docs/documentation/doc-references-V3/development-intro-0000001478061813-V3)

### 基础

[鸿蒙的各种版本](/DOC/versions.md)

### 我是新手第一步我该看什么？

可以花两周看一下官方提供的[外链：免费基础能力认证课程](https://developer.huawei.com/consumer/cn/training/result?type1=101718934267126043)

这个课程是视频+文档+demo的形式，对鸿蒙有个了解够用了，看完可以拿一个免费的能力证书。
如果你对Android开发有了解，学习有加成，因为你可以发现很多内容能在Android中找到一一对应关系。

### 证书
华为官方给鸿蒙开发者提供了证书获取渠道：
- 能力认证（免费，应用开发初级有线上教程；应用开发高级没有）
- 职业认证（收费，有线上教程和模考，工程师HCIA 200美元、高级工程师HCIP 300美元，注意3年过期要重新考试，目前官方已经撤掉了相关链接建议观望）

[外链：鸿蒙的能力与职业认证官方入口](https://developer.huawei.com/consumer/cn/training/dev-certification/a617e0d3bc144624864a04edb951f6c4)

### [签名与安装](/DOC/signs.md)

### 语言

[外链：TypeScript快速入门、浅析ArkTS的起源和演进、ArkTS开发实践](https://blog.csdn.net/you4580/article/details/133861569)

[外链：仓颉](https://developer.huawei.com/consumer/cn/forum/topic/0207154349937192038?fid=0109140870620153026)

### UI


#### 屏幕适配单位，参考官方提供的[外链](https://developer.harmonyos.com/cn/docs/design/des-guides/basic-0000001055539104)

#### [外链：UIAbility的使用，相当于Android的Activity](https://developer.huawei.com/consumer/cn/training/course/slightMooc/C101717497122909477)

#### [外链：Web组件的基本使用](https://developer.huawei.com/consumer/cn/training/course/slightMooc/C101705083116217059)

#### [外链：HTTP访问网络](https://developer.huawei.com/consumer/cn/training/course/slightMooc/C101717497918284399)

#### [Web组件和前端页面加载后调试](/DOC/web_view.md)

#### 基础组件

[外链：常用基础组件、Column&Row组件、List组件和Grid组件的使用、Tabs组件](https://developer.huawei.com/consumer/cn/doc/harmonyos-guides-V2/arkts-layout-development-create-list-0000001451074018-V2)

[外链：List和Grid组件的懒加载](https://developer.harmonyos.com/cn/docs/documentation/doc-guides-V3/ui-ts-performance-improvement-recommendation-0000001477981001-V3#ZH-CN_TOPIC_0000001477981001__%E6%8E%A8%E8%8D%90%E4%BD%BF%E7%94%A8%E6%95%B0%E6%8D%AE%E6%87%92%E5%8A%A0%E8%BD%BD)

#### [外链：动画的使用](https://developer.huawei.com/consumer/cn/training/course/slightMooc/C101705081897917056)

### 异步、多线程

异步并发（虚假的多线程，官方解释：代码在执行到一定程度后会被暂停，以便在未来某个时间点继续执行，这种情况下，同一时间只有一段代码在执行。）

[Promise](/DOC/Promise.md)

[async & await](/DOC/async_await.md)

多线程并发（真正的多线程 官方解释：在同一时间段内同时执行多段代码。在主线程继续响应用户操作和更新UI的同时，后台也能执行耗时操作，从而避免应用出现卡顿。）

TaskPool 敬请期待

Worker 敬请期待


### 数据传递

[外链：State、Prop、Link、Provide、Consume,Video组件、弹窗](https://developer.huawei.com/consumer/cn/doc/harmonyos-guides-V5/arkts-state-V5)

### 存储

[外链：首选项存储，相当于Android的SharedPreferences](https://developer.huawei.com/consumer/cn/training/course/slightMooc/C101717498132814493)

[外链：关系型数据库，依赖Sqlite](https://developer.huawei.com/consumer/cn/doc/harmonyos-guides-V5/data-persistence-by-rdb-store-V5)

### 第三方库

[外链：三方库的基本使用](https://developer.huawei.com/consumer/cn/training/course/slightMooc/C101705085912853376)

### 开发工具

[常用HDC命令](/DOC/hdc.md)

[外链：DevEco Studio使用技巧](https://developer.huawei.com/consumer/cn/training/course/slightMooc/C101717494752698457)

[外链：DevEco Studio预览器的使用](https://developer.huawei.com/consumer/cn/training/course/slightMooc/C101717494752698457)

### 音视频

#### 音视频通话

官方没提供音视频通话方案

[外链：官方的指南：开发音频通话功能](https://developer.huawei.com/consumer/cn/doc/harmonyos-guides-V5/audio-call-development-V5)只写了把文件的音频用AudioRenderer播放出来，再用AudioCapturer把麦克风的音频写入文件里，没写怎么**网络传输**

可以了解一下[音视频通讯的各种概念和关系](/DOC/音视频通讯的各种概念和关系.md)
