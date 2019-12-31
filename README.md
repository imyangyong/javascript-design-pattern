---
title: README.md
date: 2019-12-28 14:59:21
disqus: false
---

编写可维护代码的一个最重要方面是能够注意到代码中反复出现的主题并对其进行优化。在这个领域，设计模式的知识可以证明是无价的。

## JavaScript Design Patterns

开发人员通常想知道是否有一个理想的模式或一组他们应该在工作流程中使用的模式。这个问题没有一个正确的答案。我们工作的每个 script 脚本和 web 应用程序都可能有其自己的个性化需求，我们需要考虑的是，模式在哪里可以为我们的实现提供真正地价值。

例如，一些项目可能受益于观察者模式提供的解耦好处（它减少了应用程序的相互依赖的程度），而有些项目可能太小，无需解耦。

也就是说，一旦我们牢牢掌握了设计模式和它们最适合的特定问题，就很容易将它们集成到我们的应用程序体系结构中。

在本文中探讨的模式有：

**创建型设计模式**：

- [工厂模式 Factory Pattern](/工厂模式.html)        封装 new 构造函数
- [单例模式 Singleton Pattern](/单例模式.html)      对象池

**结构型设计模式：**

- [外观模式 Facade Pattern](/外观模式.html)	        utils；统一兼容接口
- [命令模式 Command Pattern](/命令模式.html)           封装一系列动作，例子很优秀呦
- [策略模式 Strategy Pattern](/策略模式.html)	        同一类功能，定义不同逻辑算法，用户随意选择
- [职责链模式 Chain Of Responsibility Pattern](/职责链模式.html)	        解耦紧密的if-else判断逻辑，可AOP实现
- [状态模式 State Pattern](/状态模式.html)	        多状态间相互固定切换
- [Mixin 模式 Mixin Pattern](/Mixin模式.html)          多继承 mixin
- [装饰器模式 Decorator Pattern](/装饰器模式.html)      对现有类进行一次包装，增加功能。 等同于 ES7的 装饰器
- [适配器模式 Adapter Pattern](/适配器模式.html)        接口等适配，达到统一目的
- [享元模式 Flyweight](/享元模式.html)                 对象池共享
- [组合模式 Composite Pattern](/组合模式.html)         树形结构，统一接口

**行为设计模式**：

- [代理模式 Proxy Pattern](/代理模式.html)	        虚拟代理占位预加载；缓存机制提升性能
- [观察者模式 Observer Pattern](/观察者模式.html)	发布订阅(发布者发送)
- [中介者模式 Mediator Pattern](/中介者模式.html)    发布订阅(订阅者互发)
