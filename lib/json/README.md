
# JSON

为运行环境提供 `JSON` 支持。

---


## 使用说明

在 IE6 等浏览器中，未提供 `JSON` 全局对象。通过该组件，可以补足：

```js
seajs.config({
    alias: {
        'json': 'json/1.0.2/json'
    },
    // 只在需要时进行预加载
    preload: [ this.JSON ? '' : 'json' ]
});


define(function(require, exports) {

    var data = JSON.parse('{ "name": "Frank Wang" }');
    data.age = 80;

    var str = JSON.stringify(data);
    // ==> '{"name":"Frank Wang","age":80}'

});
```
