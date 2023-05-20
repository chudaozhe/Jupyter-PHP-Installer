主要更新

- 升级box至4.3.8
- 兼容composer2.x
- 兼容php8.1

## 安装zmq扩展
官方的[zmq](https://pecl.php.net/package/zmq)已多年不维护了，并且在php7.4中报错，所以只能选择第三方的了
```
wget https://github.com/stijnvdb88/php-zmq/archive/refs/tags/v4.3.4.tar.gz

tar -xvzf php-zmq-4.3.4.tar.gz 
mv php-zmq-4.3.4 /usr/src/php/ext/php-zmq

#安装依赖
apt-get install -y libzmq3-dev

#安装扩展
docker-php-ext-install php-zmq
```

## 安装Jupyter-PHP-Installer
```
php ./jupyter-php-installer.phar install -v
```

或者，在本项目根目录执行
```
//第一步
composer install

//第二步
composer execute install

#或者

//第二步
php src/EntryPoint/main.php install
```

## 构建 jupyter-php-installer.phar
如果自己修改了代码，需要重新构建`jupyter-php-installer.phar`文件，请按以下步骤进行
```
composer install
cd /tmp
wget https://github.com/box-project/box/releases/download/4.3.8/box.phar
chmod +x /tmp/box.phar
/tmp/box.phar compile -v
```

## 详情
https://www.cuiwei.net/p/1391718888

=====================
# Jupyter-PHP Installer ([Main Page](https://litipk.github.io/Jupyter-PHP-Installer/))

[![Author](http://img.shields.io/badge/author-@castarco-blue.svg?style=flat-square)](https://twitter.com/castarco)
[![Software License](https://img.shields.io/badge/license-MIT-brightgreen.svg?style=flat-square)](LICENSE)
[![Packagist Version](https://img.shields.io/packagist/v/Litipk/jupyter-php.svg?style=flat-square)](https://packagist.org/packages/Litipk/jupyter-php)

## Introduction

[**Jupyter-PHP**](https://github.com/Litipk/Jupyter-PHP) is a PHP kernel for [*Jupyter*](http://jupyter.org). This
repository holds an installer to make easier installing the Jupyter-PHP kernel.

## Getting started

Go to the [main page](https://litipk.github.io/Jupyter-PHP-Installer/) and follow the instructions.

## Learn more

 * [Chat Room](https://gitter.im/Litipk/Jupyter-PHP) : If you want to have a real-time chat with other Jupyter-PHP users or developers, you can do it here.
 * [Group / Mail List](https://groups.io/g/jupyter-php) : If a chat room isn't enough to post your doubts or ideas, you can join to our mail list.

## How to contribute

 * First of all, you can take a look on the [bugtracker](https://github.com/Litipk/Jupyter-PHP-Installer/issues) and decide if there is something that you want to do :wink: . If you think there are missing improvements in this file, then you are invited to modify the TODO list.
 * You can also send us bug reports using the same bugtracker.
 * If you are really interested on helping to improve Litipk\BigNumbers, we recommend to read the [contributing guidelines](https://github.com/Litipk/Jupyter-PHP-Installer/blob/master/CONTRIBUTING.md).


## License

Jupyter-PHP and its installer are licensed under the [MIT License](https://github.com/Litipk/Jupyter-PHP-Installer/blob/master/LICENSE).
