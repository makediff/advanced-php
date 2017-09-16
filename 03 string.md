
# 数字和字符串

PHP里没有对字符串的直接操作，全部都是通过函数来处理的。

很容易用错的几个函数。

`strpos()`和`trim()`。


# 字符串输出和格式化
`\r\n`在单引号内是不会输出回车换行的。

多用`sprintf()`函数处理，用`.`处理字符串连接改起来费劲且不好维护。

再多的时候，用`array()`和`implode`函数解决。


# 字符串可以跨行

```php
$sql = "SELECT * FROM student
WHERE age > 18
ORDER BY id DESC
LIMIT 10";
```

这个特点在组装SQL的时候很有用。PHP还有个`<<<`符号，也能做同样的事，只是这个用法更加便捷。


# 遍历字符串的黑科技

```php
$a = "hello";
$len = strlen($a);
foreach(range(0, $len) as $i){
    echo $a{$i}, "#";
}
```

有了上面的方法，我们就比较容易做这样的事情，比如判断是否以`#`开头。

```php
$line = "# this is a comment";
if ($line{0} == '#'){
    echo "YES";
}
```

当然，我们是不能做赋值操作的。`$line{0}='A';`


PHP中没有类似其他语言的`startswith`和`endswith`，所以常用的解决方法是`strlen`加`substr`来解决。

# 请思考如下问题
