# Flux单向数据流



[原文链接](https://facebook.github.io/flux/docs/in-depth-overview/)

原文：Flux applications have three major parts: the dispatcher, the stores, and the views (React components)

Flux 由三个主要部分组成：dispatch、store、view。



原文：when a user interacts with a React view, the view propagates an action throught a central dispatcher, to the various stores that hold the application's data and business logic, which updates all of the views that are affected.

当用户与视图交互时，view 通过 dispatch 传播操作到存储数据和业务逻辑的各种 store，store 更新所有受影响的 view。



![image-20200309150017843](./img/image-20200309150017843.png)

原文：The dispatcher, stores and views are independent nodes with distinct inputs and outputs.

dispatch、store、view是各自独立的节点，具有不同的输入和输出。



![flux-simple-f8-diagram-explained-1300w](./img/flux-simple-f8-diagram-explained-1300w.png)

原文：

action creators are helper methods, collected into a library, that create an action from method parameters, assign it a type and provide it to the dispatcher

every action is sent to all stores via the callbacks the stores register with the dispatcher

after stores update themselves in response to an action, they emit a change event.

special views called "controller-views", listen for change events, retrieve the new data from the stores and provide the new data to the entire tree of their child views.