# Web组件和前端页面加载

### 鸿蒙设备有系统内置的浏览器内核

WebView组件的使用参考[官方教程](https://developer.huawei.com/consumer/cn/training/course/slightMooc/C101667364948559963)

但不要用`https://liulanmi.com/labs/core.html` 查看内核版本，会显示无法识别。

### Chrome调试前端

可以使用Chrome的调试工具链接：`chrome://inspect/#devices`进行前端调试

#### 前提是

参考[此处](https://developer.harmonyos.com/cn/docs/documentation/doc-guides-V3/web-debugging-with-devtools-0000001508267425-V3?ha_linker=eyJ0cyI6MTcwMzQ5NjIxMTkyNiwiaWQiOiJiNmEzZGFiMzZiYTM1YWFkOWNmNWI1MDE5YjkwMDAwZSJ9)增加

```kotlin
aboutToAppear() {
	webview.WebviewController.setWebDebuggingAccess(true);
}
```

参考[此处](https://developer.harmonyos.com/cn/docs/documentation/doc-references/ts-basic-components-web-0000001333720957#ZH-CN_TOPIC_0000001333720957__domstorageaccess)增加

```kotlin
Web({ src:'www.example.com', controller:this.controller })
      .domStorageAccess(true)
```

配置端口映射

```kotlin
// 添加映射 
hdc fport tcp:9222 tcp:9222 
// 查看映射 
hdc fport ls
```

然后chrome进入：`chrome://inspect/#devices`即可
