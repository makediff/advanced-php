
# PHP环境变量和加载相关

`include_path`会影响大到`include`和`require`函数的行为。

用上次学到的`php -r "echo ini_get('include_path');"`命令查看当前配置，这种方式获取的值，是有缓存的。


可以用多种方式。

- 通过在`.ini`配置文件中设置，`include_path = .:/usr/local/lib/php:./include`，注意，在`windows`和`Linux`下分隔符是不一样的。

- 另外可以通过`ini_set()`来设置。

- 还可以通过`set_include_path()`和`get_include_path()`来处理。

配置在`ini`文件是长期有效，用函数设置的是临时有效的。

需要注意的是，`PHP`没有一个系统环境变量来设置`include_path`，比如`Python`就有`PYTHONPATH`。

通过`.`和`..`的方式，可以加载相对位置的文件，这种方式不好的地方在于不容易理解，特别是多层的时候，如`../../../../`，会增加出错的概率，所以建议用下面两种方式来解决。

- 定义入口常量，以这个位置开始。如`define("ROOT_PATH", dirname(__FILE__));`。
- 不直接加载文件，通过`auto include hooks`来处理，所有逻辑放这里。


# 获取环境相关变量
`getenv()`

用来获取系统的环境变量。


# 获取命令行参数
`$argv`
如果是在函数里，需要加`global`，如`global $argv`。

`$argc`会返回命令参数的个数。


# `.ini`里一些值得注意的点

# 管道的方式读取数据



# 请思考如下问题
