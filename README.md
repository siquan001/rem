# rem.js
一个简单的模块化插件，目前只能在浏览器环境中运行（闲的发慌的也可以做一下Node版本）

## 使用方法
```html
<script src="./rem.js"></script>

<!-- 使用了rem的js 需要注明type="text/rem" -->
<script src="./xxx.js" type="text/rem"></script>
```

```javascript
// xxx.js
var a=_REQUIRE_('./a.js');
```
```javascript
(function(){
  return {
    //...
  }
})();
// a.js
```

## 注意事项

- 你应该注意到了，rem只会直接替换_REQUIRE_(path)为js代码，不做其它更改
- \_REQUIRE\_(path)的path是相对于本文件的路径的
- rem支持解析引用的js文件中的\_REQUIRE\_(path)
- rem不会处理循环引用的问题，出现死循环别怪我没有提醒你
- 引用的js文件需要同源或支持CORS


