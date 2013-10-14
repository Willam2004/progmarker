Visitor模式理解
=====
什么是visitor模式？引入的场景。
假如我们这里有颗树：

    食物
        |水果
            |苹果
            |梨子
        |蔬菜
            |白菜
            |西红柿
其中他们每个都有个价格的属性，如果用程序的遍历它，将会这样写：
    
    if(node=='食物'){
        listFruit = getChild(0);
        //累加水果的价格
        listVegetable= getChild(1);
        //累加蔬菜的价格
    }

但是如果我们发现又需要累加各种水果和蔬菜的重量时，我们又要重复上面的操作，只是需要计算重量，而如果再增加一种水果，那么价格的计算和重量的计算又都需要进行处理。
## visitor ##
在GOF四人帮里，**visitor**模式是这样定义，为了将操作的集合对象和操作的方式进行**分离**这样增加额外的方法操作下，是不需要修改对象结构。

![enter image description here][1]

## visitor适用场景##
visitor模式适用于操作的对象结构不会经常发生变化，而且是自顶向下的树状结构。在这里很好的使用了递归的操作方式，避免了代码的嵌套


  [1]: http://www.blackwasp.co.uk/images/Visitor.png "Visitor"