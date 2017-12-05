# numberRiddle
 a simple number riddle game,but have many javascript basic knowledge
首先我们要对用户输入的值进行判断，首先要判断它是不是数值。

判断数值的方法有很多，我首先想到了typeof方法

我是这样写的

```
var text = document.getElementById('text').value;
console.log(typeof(text))
```
然后报错：typeof is not a function。后来我查到，typeof是一个操作符而不是函数，因此圆括号尽管可以使用，但不是必须的。

然后我又想到先把text的值praseInt成数值类型

```
var text = parseInt(document.getElementById('text').value);
//如果text的值是字符串
console.log(text);//NaN
```
那我想就可以这样了

```
if (num == ''||test==NaN) {
                        alert("请输入"+rendom+"的数字");
                    }
```

但事实是NaN是一个非数值，不与任何值相等。

最后我选择了用正则表达式来判断的方法，十分简单，这里就不讲了。

写这篇问主要是为了记录遗忘的两个javascript基础知识点，然后我在去看了一遍高程的第三章，每一次看高程，都有不一样的新发现。关于新发现，我已经记录在文章[javaScript基础概念小知识点集](http://www.cnblogs.com/huyuzhu/p/7988741.html)中，您可以阅读并提出建议
