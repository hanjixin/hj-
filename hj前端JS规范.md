## 通用约定
#### 注释

原则
As short as possible（如无必要，勿增注释）：尽量提高代码本身的清晰性、可读性。
As long as necessary（如有必要，尽量详尽）：合理的注释、空行排版等，可以让代码更易阅读、更具美感。
* 单行注释
必须独占一行。// 后跟一个空格，缩进与下一行被注释说明的代码一致。
* 多行注释
```
避免使用 /*...*/ 这样的多行注释。有多行注释内容时，使用多个单行注释。
函数/方法注释
函数/方法注释必须包含函数说明，有参数和返回值时必须使用注释标识。；
参数和返回值注释必须包含类型信息和说明；
当函数是内部函数，外部不可访问时，可以使用 @inner 标识；
/**
 * 函数描述
 *
 * @param {string} p1 参数1的说明
 * @param {string} p2 参数2的说明，比较长
 *     那就换行了.
 * @param {number=} p3 参数3的说明（可选）
 * @return {Object} 返回值描述
 */
function foo(p1, p2, p3) {
    var p3 = p3 || 10;
    return {
        p1: p1,
        p2: p2,
        p3: p3
    };
}
```
### 文件注释

文件注释用于告诉不熟悉这段代码的读者这个文件中包含哪些东西。 应该提供文件的大体内容, 它的作者, 依赖关系和兼容性信息。如下:
```
/**
 * @fileoverview Description of file, its uses and information
 * about its dependencies.
 * @author user@meizu.com (Firstname Lastname)
 * Copyright 2009 Meizu Inc. All Rights Reserved.
 */
```
### 命名

* 变量, 使用 Camel (驼峰命名法)命名法。
* var loadingModules = {};
私有属性、变量和方法以下划线 _ 开头。
var _privateMethod = {};
* 常量, 使用全部字母大写，单词间下划线分隔的命名方式。
var HTML_ENTITY = {};
* 函数, 使用 Camel 命名法。
* 函数的参数, 使用 Camel 命名法。
function stringFormat(source) {}

function hear(theBells) {}
* 类, 使用 Pascal（每个单词的首字母大写） 命名法
类的 方法 / 属性, 使用 Camel 命名法
```
function TextNode(value, engine) {
    this.value = value;
    this.engine = engine;
}

TextNode.prototype.clone = function () {
    return this;
};
```

枚举变量 使用 Pascal 命名法。
枚举的属性， 使用全部字母大写，单词间下划线分隔的命名方式。
```
var TargetState = {
    READING: 1,
    READED: 2,
    APPLIED: 3,
    READY: 4
};
```