---
title: Mixin模式
date: 2019-12-28 15:17:55
disqus: true
---

# Mixin 模式 Mixin Pattern

在 JavaScript 中，我们只能继承单个对象。每个对象只能有一个 `[[Prototype]]` 原型。并且每个类只可以扩展另外一个类。但是有些时候这种设定（单继承）会让人感到受限制。比如说我有一个 `StreetSweeper` 类和一个 `Bicycle` 类，现在我想要一个 `StreetSweepingBicycle` 类（实现两个父类的功能）。

**有一个概念可以帮助我们，叫做“mixins”。**

根据维基百科的定义，[mixin](https://en.wikipedia.org/wiki/Mixin) 是一个包含许多供其它类使用的方法的类，而且这个类不必是其它类的父类。

换句话说，一个 *mixin* 提供了许多实现具体行为的方法，但是我们不单独使用它，我们用它来将这些行为添加到其它类中。

## 一个 Mixin 实例

在 JavaScript 中构造一个 mixin 最简单的方式就是构造一个拥有许多实用方法的对象，通过这个对象我们可以轻易地将这些实用方法合并到任何类的原型中。

例如，这个叫做 `sayHiMixin` 的 mixin 用于给 `User` 添加一些“言语”。

```javascript
// mixin
let sayHiMixin = {
  sayHi() {
    alert(`Hello ${this.name}`);
  },
  sayBye() {
    alert(`Bye ${this.name}`);
  }
};

// 用法：
class User {
  constructor(name) {
    this.name = name;
  }
}

// 拷贝方法
Object.assign(User.prototype, sayHiMixin);
// or use lodash extend
_.extend(User.prototype, sayHiMixin);

// 现在 User 可以说　hi 了
new User("Dude").sayHi(); // Hello Dude!
```

*Mixin* —— 是一个通用的面向对象编程术语：一个包含其他类的方法的类。

**一些其它语言比如 python 允许通过多继承实现 mixin。JavaScript 不支持多继承，但是可以通过拷贝多个类中的方法到某个类的原型中实现 mixin。**

我们可以使用 mixin 作为一种通过多种行为来增强类的方式，就像我们上面看到的事件处理一样。

如果 Mixins 偶尔会重写原生类中的方法，那么 Mixins 可能会成为一个冲突点。因此通常情况下应该好好考虑 mixin 的命名，以减少这种冲突的可能性。
