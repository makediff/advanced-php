# 有关空值

针对不同的类型，如果是没有东西的，则视为空值。

- string, ""
- int, 0
- array, array() or [] or {}
- bool, false

通过`empty()`可以处理。


`isset()`和`empty()`的区别？


不太建议用PHP做强类型的事情，所以不要：

```php
if ($a!=""){

}
```

而是要考虑到各种边界情况，不管`$a`是何种类型的值，只要是没有值，就认为是失败。写程序要减少思考的负担。

```php
if(empty($a)){
    echo "Error";
}
```

从设计的层面来避免这个问题。

```php
$a = "hello";
if($a == 0){
    echo "YES";
}
```

`{"status":0,}`作为成功的标志，但是要考虑到上面的问题。

```php
if($ret&& isset($ret["stauts"])&& "0"==$ret["status"]){
    echo "success";
}
```
