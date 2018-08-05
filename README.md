 一个C#写的四则运算表达式的计算器；<br/>
使用字符解析，没有使用正则或其他文法解析库，并且用了.Net Core 2.1新增的Span库来提升效率，所以只能运行在.Net Core2.1以上的版本。<br/>
```C#
var cacl = new Calculator();
var result = cacl.Sum(" (123.22) +((2-1)*1-(3+(341-5-12-2)  ))-6/2 ");
Assert.IsTrue(result == 123.22 + ((2 - 1) * 1-(3 + (341 - 5 - 12 - 2))) - 6 / 2);
```
