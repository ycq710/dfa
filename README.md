# dfa
敏感词过滤类,内置了原始词库,将敏感词过滤为指定字符串
**描述:**

敏感词过滤为指定字符串


**安装:**

1.新建composer.json文件

2.加入以下内容:

{
    "require": {
        "jiangshengxin/dfa":"dev-master"
    }
}


3.执行命令:

composer install


4.下载完毕以后,进入下载好的vendor/jiangshengxin.这个目录,就是类包目录.
进入这个类包目录,执行CMD命令,生成装载文件,就可以运行了:

composer update

**使用说明:**

require_once __DIR__.'/vendor/autoload.php';

use Dfa\trieTree;

$txt = "测试敏感词过滤,卧槽";//要检测的文字


$str = (new trieTree($txt))->endString;//实例化类 获取处理完毕的字符串

echo $str;//输出转换后的文字





