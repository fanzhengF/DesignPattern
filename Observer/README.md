##观察者模式

### 概述
观察者模式，一个比较好理解的类比就是博客订阅。被订阅的博客是主体，而订阅了该博客的用户是客体，或者称为观察者。当主体发生改变，比如主体有新的文章，那么就需要通知所有的客体，使得客体能得到通知并更新订阅的内容。而客体是通过一种“注册订阅”的功能来告诉主体它想当一个观察者，意思就是告诉主体，“我对你的数据感兴趣，一有变化请通知我”。当然，客体也可以“取消订阅”，然后不再获得主体的通知。关于客体的一切，主体只知道客体实现了某个接口。主体不需要知道客体的具体类是谁、做了什么。任何时候都可以增加新的客体，而且主体不会受到影响。因为它们两者是松耦合的。要做到主体和客体之间相互独立地被复用，可以采用观察者模式。观察者就定义了对象之间的一对多依赖，当一个对象改变状态时，它的所有依赖者都会收到通知并自动更新。

### 结构
![观察者模式结构图](http://7u2eqw.com1.z0.glb.clouddn.com/观察者模式结构图.jpg)

### 实现
设计一个Subject接口和Observer接口。实例化两个Observer。两个Observer分别订阅Subject，然后在Subject实例的内容发生改变时，订阅了Subject的Observer就可以得到通知。

### 总结与分析
通过观察者模式，把对象之间的一对多依赖关系变得松散，程序变得易维护和更有弹性，更能应对变化。
