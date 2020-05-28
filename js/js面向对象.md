#Javascript



##instanceof

**instanceof** 运算符用于检测构造函数的 **prototype** 属性是否出现在某个实例对象的原型链上。



##Object.prototype.isPrototypeOf

**isPrototypeOf()** 方法用于测试一个对象是否存在于另一个对象的原型链上。



##原型链

- 所有实例的的 **\__proto__**  指向该构造函数的原型对象。(constructor.prototype)
- 所有的函数(包括构造函数)是 **Function** 的实例，所以所有函数的 **\__proto__** 都指向 **Function** 的原型对象(包括 **Function**本身，因为他也是一个构造函数)。
- 所有的原型对象(包括**Function**的原型对象)都是 **Object **的实例，所以 **\__proto__** 都指向 **Object** 的原型对象。而 **Object** 的原型对象的 **\__proto__** 指向 **null**。

