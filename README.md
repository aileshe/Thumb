# Thumb是什么?
Thumb是一个图片等比例缩放的PHP扩展类，提供了3种可选的自定义缩略剪裁方式，仅需传入原图路径和缩图宽高就可以快速生成不变形的缩略图。

# 安装
通过composer，这是推荐的方式，可以使用composer.json 声明依赖，或者直接运行下面的命令。
```
composer require aileshe/thumb:*
```
放入composer.json文件中
```
    "require": {
        "aileshe/thumb": "*"
    }
```
然后运行
```
composer update
```

# 基本用法
1) 生成一张缩略图
```
    $src = './public/upload/img_12.jpg'; // 原图路径
    $output = './public/upload/img_12_thumb.jpg'; // 输出保存文件名
    $width = 300; // 预生成缩略图的宽
    $height = 200; // 预生成缩略图的高
    \Thumb\Thumb::out($src,$output,$width,$height);
```
2) 生成缩略图直接输出图象到浏览器
```
    $src = './public/upload/img_12.jpg'; // 原图路径
    $width = 300; // 预生成缩略图的宽
    $height = 200; // 预生成缩略图的高
    \Thumb\Thumb::show($src,$width,$height);
```
3) 生成缩略图直接输出图象到浏览器并保存缩略图
```
    $src = './public/upload/img_12.jpg'; // 原图路径
    $output = './public/upload/img_12_thumb.jpg'; // 输出保存文件名
    $width = 300; // 预生成缩略图的宽
    $height = 200; // 预生成缩略图的高
    \Thumb\Thumb::showOut($src,$output,$width,$height);
```

