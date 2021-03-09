alioss-upload extension  for laravel-admin
======
扩展laravel-admin的表单，实现web直传阿里OSS

## 安装
```
composer require de-memory/alioss-upload
php artisan vendor:publish --provider=Encore\AliOssUpload\AliOssUploadServiceProvider
```
## 配置
在config/admin.php文件的extensions，加上属于这个扩展的一些配置
```php
'extensions' => [
        'alioss-upload' => [
            'OSS_ACCESS_ID' => '*****',
            'OSS_ACCESS_KEY' => '**************',
            'OSS_ENDPOINT' => 'oss-cn-shanghai.aliyuncs.com',
            'OSS_BUCKET' => '*****',
            'OSS_HOST' => 'http://****.oss-cn-shanghai.aliyuncs.com',
            'OSS_URL' => 'http://***.oss-cn-shanghai.aliyuncs.com' // 自定义域名（CDN）
        ]
    ],
```
## 使用
在form表单中使用它
```php
$form->aliOss('pic', '图片')->attribute('file');  // 单图（默认）
$form->aliOss('pic2', '图片2')->attribute('images'); // 多图
```

## 说明
不知道什么情况原先的airan/alioss-upload无法使用，为了方便自己发布了一个alioss-upload。
如果侵权请私密我，或者联系我QQ：972985083

