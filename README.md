# PHP 入门

- ##### PHP-变量的数据类型###

  - `memory_get_usage`  获取当前PHP消耗的内存。

  - 特殊类型—资源

  - 特殊类型—空类型 `null,NULL` 大小写不敏感，或者被`unset()` 

  - 常量

    - `define()` 自定义常量
    - 系统常量
      1. \__FILE__ :php程序文件名。它可以帮助我们获取当前文件在服务器的物理位置。_
      2. \_\__LINE__ :PHP程序文件行数。它可以告诉我们，当前代码在第几行。
      3. PHP_VERSION:当前解析器的版本号。它可以告诉我们当前PHP解析器的版本号，我们可以提前知道我们的PHP代码是否可被该PHP解析器解析。
      4. PHP_OS：执行当前PHP版本的操作系统名称。它可以告诉我们服务器所用的操作系统名称，我们可以根据该操作系统优化我们的代码。

  - 常用于遍历数组，两种使用方式:不取下标、取下标。

    - `foreach(\$val as \$v)`  //不取下标
    - `foreach(\$students  as \$key=>$val)`   //取下标

  - PHP内置函数 `str_replace`   可实现字符圈的替换

    ```PHP
    $str = 'i am  AAA.';
    $str = str_replace('AAA', 'BBB AAA', $str);
    echo $str; //结果为“i am BBB AAA”
    ```

  - PHP判断函数是否存在

    `function_exists` 判断一下函数是否存在。

    `method_exists` 可以用来检测类的方法是否存在。

  - PHP 类和对象

    ```PHP 
    <?php
    //定义一个类
    class Car {
    	//定义属性
        public $name = '汽车';
        var $name = '汽车';
       //定义方法
        public function getName() {
            //方法内部可以使用$this伪变量调用对象的属性或者方法
            return $this->name;
        }
    }
    //实例化一个car对象
    $car = new Car();
    //也可以采用变量来创建
    $className = 'Car';
    $car->name = '奥迪A6'; //设置对象的属性值
    echo $car->getName();  //调用对象的方法 输出对象的名字
    ```

    *属性声明是由关键字 public，protected 或者 private 开头，后面跟一个普通的变量声明来组成*

    `public`  - 公开

    `protected` - 受保护的

    `private` - 私有的

  - PHP字符串之获取字符串的长度 `strlen` 擅长英文字符，`mb_strlen()` 获取字符串中中文长度

  - PHP字符串之字符串的截取，`substr(字符串变量,开始截取的位置，截取个数）`

    - 中文字符串的截取，`mb_substr(字符串变量,开始截取的位置，截取个数, 网页编码）`

  - 查找字符串 `strpos(要处理的字符串, 要定位的字符串, 定位的起始位置[可选])`

  - ​
