# HarmonyOwl
![image info](/Images/Logo/Logo_64x64.png)  

一个鸿蒙路书项目，提供靠谱、易懂、诚实的开发指导😉 **项目进度1% 欢迎帮助建设本项目**

原则：本Readme对官方比较完善的知识不重复复制，重点在**官方文档没说但又经常使用的内容**，同时用**链接整合**快速引导开发者。

### 华为官方链接

[外链：官方论坛](https://developer.huawei.com/consumer/cn/forum/)

[外链：官方小demo合集](https://gitee.com/harmonyos/codelabs)

[外链：官方文档中心搜索](https://developer.huawei.com/consumer/cn/doc/)

[外链：官方API文档](https://developer.harmonyos.com/cn/docs/documentation/doc-references-V3/development-intro-0000001478061813-V3)

### 我是新手第一步我该看什么？

可以花两周看一下官方提供的[外链：免费基础能力认证课程](https://developer.huawei.com/consumer/cn/training/dev-cert-detail/101666948302721398)

这个课程是视频+文档+demo的形式，对鸿蒙有个了解够用了，看完可以拿一个免费的能力证书。
如果你对Android开发有了解，学习有加成，因为你可以发现很多内容能在Android中找到一一对应关系。

### 证书
华为官方给鸿蒙开发者提供了证书获取渠道：
- 能力认证（免费，应用开发初级有线上教程；应用开发高级没有）
- 职业认证（收费，有线上教程和模考，工程师200美元、高级工程师300美元，注意3年过期要重新考试）

[外链：鸿蒙的能力与职业认证官方入口](https://developer.huawei.com/consumer/cn/training/dev-certification/a617e0d3bc144624864a04edb951f6c4)

### [签名与安装](/DOC/signs.md)

### 语言

[外链：TypeScript快速入门、浅析ArkTS的起源和演进、ArkTS开发实践](https://developer.huawei.com/consumer/cn/training/course/slightMooc/C101667356568959645)

### UI


#### 屏幕适配单位，参考官方提供的[外链](https://developer.harmonyos.com/cn/docs/design/des-guides/basic-0000001055539104)

#### [外链：UIAbility的使用，相当于Android的Activity](https://developer.huawei.com/consumer/cn/training/course/slightMooc/C101667310940295021)

#### [外链：Web组件的基本使用、HTTP访问网络](https://developer.huawei.com/consumer/cn/training/course/slightMooc/C101667364948559963)

#### [Web组件和前端页面加载后调试](/DOC/web_view.md)

#### 基础组件

[外链：常用基础组件、Column&Row组件、List组件和Grid组件的使用、Tabs组件](https://developer.huawei.com/consumer/cn/training/course/slightMooc/C101667360160710997)

[外链：List和Grid组件的懒加载](https://developer.harmonyos.com/cn/docs/documentation/doc-guides-V3/ui-ts-performance-improvement-recommendation-0000001477981001-V3#ZH-CN_TOPIC_0000001477981001__%E6%8E%A8%E8%8D%90%E4%BD%BF%E7%94%A8%E6%95%B0%E6%8D%AE%E6%87%92%E5%8A%A0%E8%BD%BD)

#### [外链：属性动画的使用](https://developer.huawei.com/consumer/cn/training/course/slightMooc/C101667368091091005)

### 数据传递

[外链：State、Prop、Link、Provide、Consume,Video组件、弹窗](https://developer.huawei.com/consumer/cn/training/course/slightMooc/C101680765314766141)

### 存储

[外链：首选项存储，相当于Android的SharedPreferences](https://developer.huawei.com/consumer/cn/training/course/slightMooc/C101667367018821971)

### 第三方库

[外链：三方库的基本使用](https://developer.huawei.com/consumer/cn/training/course/slightMooc/C101667369405083047)

### 开发工具

[常用HDC命令](/DOC/hdc.md)

[外链：DevEco Studio使用技巧](https://developer.huawei.com/consumer/cn/training/course/slightMooc/C101680766639443507)

[外链：DevEco Studio预览器的使用](https://developer.huawei.com/consumer/cn/training/course/slightMooc/C101680766639443507)

### 音视频

#### 音视频通话

前提：首先需要了解一下[音视频通讯的各种概念和关系](/DOC/音视频通讯的各种概念和关系.md)

[外链：官方的指南：开发音频通话功能](https://developer.harmonyos.com/cn/docs/documentation/doc-guides-V3/audio-call-development-0000001455598596-V3)只写了把文件的音频用AudioRenderer播放出来，再用AudioCapturer把麦克风的音频写入文件里，没写怎么**网络传输**
