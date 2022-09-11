# PhpAnalysis
PHP中文分词器

## 安装插件
```
composer require kjcy8/phpanalysis
```

## 示例
```
use phpanalysis\PhpAnalysis;

PhpAnalysis::$loadInit = false;
$pa = new PhpAnalysis('utf-8', 'utf-8', true);

//载入词典
$pa->LoadDict();

//执行分词
$pa->SetSource('在西安国际港站，8台龙门吊正在同时吊装来自世界各地的集装箱。');
$pa->differMax = true;
$pa->unitWord = true;
$pa->StartAnalysis(true);

$okresult = $pa->GetFinallyResult(',', false);

print_r($okresult);
```
