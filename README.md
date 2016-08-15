## CURL

##安装

```
composer require "juju/curl:1.0"

"juju/curl": "~1.0.0"
```

##控制器顶部
```
use \juju\curl\Curl;
```

##控制器调用
```
$ipLocation = new Ip2Location();
$locationModel = $ipLocation->getLocation('8.8.8.8');
print_r($locationModel->toArray());		//数组
print_r($locationModel->total);			//对象
```

## 升级数据库

##控制器顶部
```
use \juju\ip2location\QQWry;

$qqwry = new QQWry();
$result = $qqwry->upgrade();
if($result)
{
	echo '升级成功';
}else{
	echo '升级失败';
}
```