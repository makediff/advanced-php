
# PHP数组

PHP数组是List结构和Dict结构的组合，同时有顺序性。

和数组相关的有很多函数，有几个是必须要熟练掌握的。

`array_merge`
`uniq`
`in_array`
`isset`

PHP也支持`+`和`-`来求数组的并集、交集。

# 使用dict有效地避免过多的`IF`判断
是一种用空间换速度的办法。

```php
$fruits = {"apple":1, "pear":1, "orange":1, };
$is_have = isset($fruits["apple"]);
```

PHP里大量地使用数组，特别是多维数组，需要加深理解。

`print_r`可以很方便的把任意多维数组展开，这是一种很高效的`debug`方式，但是会有信息的丢失。看不到数据的类型。

`var_dump`可以看到更加详细的数据，但在有时会过于繁琐。

数组也是一种避免形参过多的方式。
