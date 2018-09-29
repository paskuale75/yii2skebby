<p align="center">
    <a href="https://github.com/yiisoft" target="_blank">
        <img src="https://avatars0.githubusercontent.com/u/993323" height="100px">
    </a>
    <br>
    <a href="http://www.skebby.com" target="_blank">
        <img src="https://s3.eu-central-1.amazonaws.com/cdn.skebby.it/system/images/logos/logoSkebby.png">
    </a>
    <h1 align="center">Yii2 Skebby SMS Extension</h1>
    <br>
</p>

Send sms with Skebby and Yii2.


Installation
------------

The preferred way to install this extension is through [composer](http://getcomposer.org/download/).

Either run

```sh
php composer.phar require --prefer-dist paskuale75/yii2skebby "*"
```

or add

```
"paskuale75/yii2skebby": "*"
```

to the require section of your composer.json.

**Component Setup**

To use the Setting Component, you need to configure the components array in your application configuration:
```php
'components' => [
    'skebbysms' => [
                'class'     => \paskuale75\yii2skebby\src\components\Skebbysms::class,
                'username'  =>'MyUsername',
                'password'  =>'MyPassword'
    ],
],
```

Usage:
---------
```php

Create an action in your controller...

public function actionTestSkebby(){
        // User status details
        Yii::$app->skebbysms->getUserStatus(true, false);
}
```
