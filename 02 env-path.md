
# PHP环境变量和加载相关

`include_path`

`php -r "echo ini_get('include_path');"`来查看当前的配置。

可以通过在`.ini`配置文件中设置，`include_path = .:/usr/local/lib/php:./include`，注意，在`windows`和`Linux`下分隔符是不一样的。

另外可以通过`ini_set()`来设置。

还可以通过`set_include_path()`和`get_include_path()`来处理。

其实以上就分为两种，长期有效的和临时有效的。这种方式获取的值，是有缓存的。


# 获取环境相关变量
`getenv()`

用来获取`export`后的变量值。


# 请思考如下问题