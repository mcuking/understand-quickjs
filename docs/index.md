# 前言

随着前端和 Node 十余年的高速发展，JavaScript 语言已经无处不在，被广大开发者广泛接受。尤其是 ES6 版本的出现，让 JavaScript 语言更加简洁易用，也更适用于越来越复杂的工程。相信很多 JavaScript 语言爱好者和笔者一样，不满足于仅仅使用 JavaScript 在设定好的容器中（例如浏览器或者 Node）开发应用，更希望能够深入到容器本身，去了解 JavaScript 语言在引擎中是如何被执行的，以便能更好地使用 JavaScript 语言，甚至基于 JavaScript 引擎定制开发特定的运行时等等。

## 本书目的

本书的目的就是通过分析 JavaScript 引擎的源码，来深入掌握 JavaScript 运行的机制。而目前主流的引擎有这几种：谷歌的 V8、苹果的 JavaScriptCore、Mozilla 的 SpiderMonkey、Facebook 针对 React Native 使用场景开发的 Hermes、Fabrice Bellard 个人开发的 QuickJS，而笔者选择 QuickJS 引擎来作为本书的分析对象。主要出于以下几点原因考虑：

1. QuickJS 主要是针对可嵌入的场景下开发的，所以并不支持 JIT (Just In Time 及时编译)，整体实现相比 V8 等会更加简洁，所以更容易学习；

2. QuickJS 是采用 C 语言开发的，相对于使用 C++ 开发的 V8 等引擎来说，语言上的门槛会更低些；

3. QuickJS 已经基本支持了 ES2020 的标准，完全可以应用在实际开发中，相对于一些出于学习目的开发而无法用于实际生产的 JavaScript 引擎，会更加具有权威性。

总之本书主要就是专注在研究 JavaScript 语言是如何在引擎中运行的，所以会尽量避免其他方面的干扰。最后希望读者阅读完本书后，能够对 JavaScript 引擎有更深的了解。
