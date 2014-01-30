# Zend Framework 2 Training Course

## Introduction

In January 2014, we received a training course given by [@EvanDotPro](https://github.com/EvanDotPro) in Belgium on how to best use [Zend Framework 2](http://framework.zend.com). This 3-day training was going deeper into the setup, configuration and usage of various modules that were build using ZF2 and how you could quickly got started with the framework.

## Set up

I'm using a MacBook Pro running Mac OS X Mavericks (10.9.1), which means it comes pre-installed with PHP 5.4.17. In order to use some additional features, you most likely need to instal the intl sources and PECL extension (especially if you want to use translations).

## 1. Get the skeleton application

The easiest way to get started is to get the [skeleton ZF2 app from github](https://github.com/zendframework/ZendSkeletonApplication.git) and clone it in your application path. I called my app `eventr` because I lacked inspiration.

    $ git clone https://github.com/zendframework/ZendSkeletonApplication.git eventr

Once you've done that, you can safely remove the "remote" repository as you're not going to need it further.

    $ cd eventr/
    $ git remote remove origin

Now it's also a good time to add 2 very functional modules as submodules into your vendor directory: [ZfcBase](https://github.com/ZF-Commons/ZfcBase) and [ZfcUser](https://github.com/ZF-Commons/ZfcUser).

    $ git submodule add https://github.com/ZF-Commons/ZfcBase.git vendor/ZfcBase
    $ git submodule add https://github.com/ZF-Commons/ZfcUser.git vendor/ZfcUser

Since I'm using PHP 5.4, I can simply use the build-in PHP web server to run my application. All I need to do is enter my `public` directory and choose a free port.

    $ cd public
    $ /usr/bin/php -S 127.0.0.1:1234

This is enough to get yourself up-and-running in no time.