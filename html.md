1. input “点击输入”是两个过程，onclick的default就是edit。所以可以用于显示并可编辑的文本
2. view 包含 view 则，子view应该立即render.再去fetch
3. on/listenTo都是通过添加events来注册事件的，当一个收听者不再显示或存在，因为events中有它的引用所以
    不会被回收。 **view和model通过remove destroy来stopListening**, collection 只能显式调用__off__了
    - 对于深层的嵌套，只能通过重写stopListen来实现
