**[官方文档介绍](https://developer.harmonyos.com/cn/docs/documentation/doc-guides-V3/async-concurrency-overview-0000001632690002-V3)**

一个封装Promise的语法糖

await代码的并列下一行，会等待await的执行完毕后再执行，比直接用Promise的代码少。**但是没有把Promise封装到不可见。**

会把reject函数的调用变成抛异常，可以被try catch捕获 

### 对于与UI线程的关系

- await执行之后，下一行可以直接调用UI线程的内容，比如弹出弹框。

由于只能用setTimeout模拟阻塞，不是真的阻塞所以无法测试对UI线程的阻塞情况

### 代码

```tsx
这个代码由一个Button的onClick事件直接调用
async myAsyncFunction() {
    console.info("run");
    try {
      const result = await new Promise((resolve, reject) => {
        setTimeout(() => {
          resolve('Hello, world!');
          // reject("bala")   如果上一行注释，这一行放开，则下面的catch就会执行，并且输出error catch : bala
        }, 1000);
      });
      console.info(String(result));
      this.customDialogController.open();
    }
    catch (e) {
      console.info(" error catch : " + String(e));
    }
  }
```

### 输出

```tsx
12-23 23:36:33.869 25125-10731/com.huawei.multipledialog I 0FEFE/JsApp: run
12-23 23:36:34.871 25125-10731/com.huawei.multipledialog I 0FEFE/JsApp: Hello, world!
```
