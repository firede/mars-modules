Mars Modules
======================

Mars的模块系统遵循CommonJS规范，所以很多符合CommonJS规范的开源模块可以直接在Mars下使用（比如部分NodeJS模块）。

D-Lab团队官方支持了一些开源模块，可以直接在Mars下调用。

目录结构
----------------

* __repo__: 模块版本库
    * __underscore__
    ( [主页](http://documentcloud.github.com/underscore/) ):
    Underscore.js是一个实用的JavaScript工具框架，提供了与Prototype.js（或Ruby）相似的功能编程支持，但没有对 JavaScript 内置的对象进行扩展。
    * __underscore.string__
    ( [主页](http://epeli.github.com/underscore.string/) ):
    Underscore.string为Javascript提供完整的字符串操作。是Underscore.js的扩展，亦可单独使用。
    * __moment__
    ( [主页](http://momentjs.com/) ):
    Moment.js是一个简单易用的轻量级JavaScript日期处理类库，提供了日期格式化、日期解析等功能，支持多种语言。
    * __mustache__
    ( [主页](https://github.com/janl/mustache.js) ):
    Mustache是一个少量逻辑的模板语言。
    * __haml__
    ( [主页](https://github.com/visionmedia/haml.js) | [Mars版](https://github.com/firede/haml.js) ):
    HAML是一个用来描述任何XHTML文档的标记语言。干净简单的模板引擎，这里是他的JS实现。
    * __htmlparser__
    ( [主页](https://github.com/tautologistics/node-htmlparser) ):
    node-htmlparser是NodeJS下的HTML解析器。
    * __cssom__
    ( [主页](https://github.com/NV/CSSOM) ):
    CSSOM是一个用原生JavaScript写的CSS解析器，它部分实现了CSS对象模型。

使用方法
----------------

在Mars环境下，模板页面通过require来引入一个模块，如：

```javascript
var _ = require("dd://modules/underscore/1.3.3/underscore"),
    n = _.min([6, 2, 8, 9, 3]);
write(n); // 2
```

官方托管模块路径的规则是：

    dd://modules/ + 模块文件路径（repo目录下）

后缀`.js`可不加。
