**[官方文档介绍](https://developer.harmonyos.com/cn/docs/documentation/doc-guides-V3/async-concurrency-overview-0000001632690002-V3)**

### 对于与UI线程的关系

- promise.then和catch的代码块可以直接调用UI线程的内容，比如弹出弹框。

由于只能用setTimeout模拟阻塞，不是真的阻塞所以无法测试对UI线程的阻塞情况

### 代码

注意promise.catch只是为了回调reject的调用，**不能捕获Promise的代码块里的异常（throw Error）**

```tsx
//这个代码由一个Button的onClick事件直接调用
threadFun()
  {
    console.info(`1`);

    const promise = new Promise((resolve, reject) => {
      setTimeout(() => {
        reject("bala")  //此处换成resolve("bala")，输出就是变成got resolve value is bala而已，可见resolve 和 reject作用类似
      }, 3000);
    });

    console.info(`2`);

    promise.then(result => {
      console.info(`got resolve value is ${result}`);
    }).catch(error => {
      console.error(`error: ` + error);
    });

    console.info(`3`);
  }
```

### 输出

```tsx
12-23 23:09:28.781 18066-8812/com.huawei.multipledialog I 0FEFE/JsApp: 1
12-23 23:09:28.781 18066-8812/com.huawei.multipledialog I 0FEFE/JsApp: 2
12-23 23:09:28.781 18066-8812/com.huawei.multipledialog I 0FEFE/JsApp: 3
12-23 23:09:31.782 18066-8812/com.huawei.multipledialog E 0FEFE/JsApp: error: bala
```
