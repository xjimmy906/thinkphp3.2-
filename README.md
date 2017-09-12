# thinkphp3.2-
thinkphp3.2单字母函数汇总（全）
```
/**
 * A函数用于实例化控制器 格式：[资源://][模块/]控制器
 * @param string $name 资源地址
 * @param string $layer 控制层名称
 * @param integer $level 控制器层次
 * @return Controller|false
 */
function A($name,$layer='',$level='')

/**
 * 执行某个行为
 * @param string $name 行为名称
 * @param string $tag 标签名称（行为类无需传入） 
 * @param Mixed $params 传入的参数
 * @return void
 */
function B($name, $tag='',&$params=NULL)

/**
 * 获取和设置配置参数 支持批量定义
 * @param string|array $name 配置变量
 * @param mixed $value 配置值
 * @param mixed $default 默认值
 * @return mixed
 */
function C($name=null, $value=null,$default=null)

/**
 * D函数用于实例化模型类 格式 [资源://][模块/]模型
 * @param string $name 资源地址
 * @param string $layer 模型层名称
 * @return Model
 */
function D($name='',$layer='')

/**
 * 抛出异常处理
 * @param string $msg 异常消息
 * @param integer $code 异常代码 默认为0
 * @throws Think\Exception
 * @return void
 */
function E($msg, $code=0)

/**
 * 快速文件数据读取和保存 针对简单类型数据 字符串、数组
 * @param string $name 缓存名称
 * @param mixed $value 缓存值
 * @param string $path 缓存路径
 * @return mixed
 */
function F($name, $value='', $path=DATA_PATH)

/**
 * 记录和统计时间（微秒）和内存使用情况
 * 使用方法:
 * <code>
 * G('begin'); // 记录开始标记位
 * // ... 区间运行代码
 * G('end'); // 记录结束标签位
 * echo G('begin','end',6); // 统计区间运行时间 精确到小数后6位
 * echo G('begin','end','m'); // 统计区间内存使用情况
 * 如果end标记位没有定义，则会自动以当前作为标记位
 * 其中统计内存使用需要 MEMORY_LIMIT_ON 常量为true才有效
 * </code>
 * @param string $start 开始标签
 * @param string $end 结束标签
 * @param integer|string $dec 小数位或者m
 * @return mixed
 */
function G($start,$end='',$dec=4)

/**
 * 获取输入参数 支持过滤和默认值
 * 使用方法:
 * <code>
 * I('id',0); 获取id参数 自动判断get或者post
 * I('post.name','','htmlspecialchars'); 获取$_POST['name']
 * I('get.'); 获取$_GET
 * </code>
 * @param string $name 变量的名称 支持指定类型
 * @param mixed $default 不存在的时候默认值
 * @param mixed $filter 参数过滤方法
 * @param mixed $datas 要获取的额外数据源
 * @return mixed
 */
function I($name,$default='',$filter=null,$datas=null)

/**
 * 获取和设置语言定义(不区分大小写)
 * @param string|array $name 语言变量
 * @param string $value 语言值
 * @return mixed
 */
function L($name=null, $value=null)

/**
 * M函数用于实例化一个没有模型文件的Model
 * @param string $name Model名称 支持指定基础模型 例如 MongoModel:User
 * @param string $tablePrefix 表前缀
 * @param mixed $connection 数据库连接信息
 * @return Model
 */
function M($name='', $tablePrefix='',$connection='')

/**
 * 设置和获取统计数据
 * 使用方法:
 * <code>
 * N('db',1); // 记录数据库操作次数
 * N('read',1); // 记录读取次数
 * echo N('db'); // 获取当前页面数据库的所有操作次数
 * echo N('read'); // 获取当前页面读取次数
 * </code>
 * @param string $key 标识位置
 * @param integer $step 步进值
 * @return mixed
 */
function N($key, $step=0,$save=false)

/**
 * 远程调用控制器的操作方法 URL 参数格式 [资源://][模块/]控制器/操作
 * @param string $url 调用地址
 * @param string|array $vars 调用参数 支持字符串和数组
 * @param string $layer 要调用的控制层名称
 * @return mixed
 */
function R($url,$vars=array(),$layer='')

/**
 * 缓存管理
 * @param mixed $name 缓存名称，如果为数组表示进行缓存设置
 * @param mixed $value 缓存值
 * @param mixed $options 缓存参数
 * @return mixed
 */
function S($name,$value='',$options=null)

/**
 * 获取模版文件 格式 资源://模块@主题/控制器/操作
 * @param string $template 模版资源地址
 * @param string $layer 视图层（目录）名称
 * @return string
 */
function T($template='',$layer='')

/**
 * URL组装 支持不同URL模式
 * @param string $url URL表达式，格式：'[模块/控制器/操作#锚点@域名]?参数1=值1&参数2=值2...'
 * @param string|array $vars 传入的参数，支持数组和字符串
 * @param string|boolean $suffix 伪静态后缀，默认为true表示获取配置值
 * @param boolean $domain 是否显示域名
 * @return string
 */
function U($url='',$vars='',$suffix=true,$domain=false)

/**
 * 渲染输出Widget
 * @param string $name Widget名称
 * @param array $data 传入的参数
 * @return void
 */
function W($name, $data=array())

```
