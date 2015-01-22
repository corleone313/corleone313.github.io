1. data<->model
   datas <-> collection
   html structure <-> view
#### 事件的清除
2. `on/listenTo`都是通过添加events来注册事件的，当一个收听者不再显示或存在，因为events中有它的引用所以
    不会被回收。 **view和model通过remove destroy来stopListening**, collection 只能显式调用__off__了
    - 对于深层的嵌套，只能通过重写stopListen来实现
    - 定义一个beforeDestroy来包装destroy，包含进off的代码

