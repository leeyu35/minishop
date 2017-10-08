
# Laravel Minishop 微信小商店CRM

<p align="center"><img src="docs/static/logo.png?raw=true" title="Laravel Minishop" height=100></p>

## 概述

Laravel Minishop 基于以下开源程序集成:

* Laravel 5.5
* Wordpress 4.7
* Opencart 3.0
* WeEngine 1.0

Laravel Minishop is a free open source ecommerce platform for online merchants. 

Laravel Minishop provides a professional and reliable foundation from which to build a successful online store.

## 环境依赖

* Mysql 5.7+
* PHP 7.0+
* composer 1.0+
* Apache 服务器需要配置 mod_rewrite, Nginx 需要配置好伪静态规则(与 Laravel 相同)
* PHP mbstring, curl, openssl, mcrypt, gd 等扩展(以安装向导检测信息为准)
* Memcached 或者 Redis 缓存

## 安装


1. 安装需要配置域名(VirtualHost), 将网站根目录设置为 **`public/`** 目录, 例如 Apache 的配置(假设站点主目录为 D:\www\):

    ‼️必须安装在 **域名根目录** 下, 不能在某个网站子目录下(比如: `http://localhost/minishop`) 否则会路径出错

        <VirtualHost *:80>
             DocumentRoot "D:/www/minishop.dev/public"
             ServerName www.minishop.dev
        </VirtualHost>

    请自行配置好 `Composer` 执行环境, 命令行窗口进入 `D:\www\` 目录执行安装:

        composer create-project minishop/minishop minishop.dev
    
    即可将 Laravel Minishop 安装到 `minishop.dev` 目录下, 如果执行时间很长, 可能是你没有配置 Composer 国内镜像, 请在上面的安装命令执行前先执行

        composer config -g repo.packagist composer https://packagist.phpcomposer.com

    配置好你的 Composer 国内镜像再进行安装, 可以参考 [Composer 中国镜像站点](http://www.phpcomposer.com)
    


2. 等待 Composer 代码下载完毕后, 用浏览器访问网站域名(比如: [http://www.minishop.dev/]() ),正常情况下会进入安装向导页面, 填写数据库参数和管理员账号信息(需要先用 phpmyadmin, navicat 等工具创建好数据库)完成安装
    
3. 后台访问网址: `http://您的域名/admin` 后台用户名与密码在安装向导页面设置

    ### Tips
    
    - Apache 服务器需要开启 mod_rewrite 伪静态扩展, 并保证扩展已经正确配置好
    - Nginx 伪静态规则配置请参考 Laravel Nginx 伪静态设置
    - ❤️ Windows 本地集成开发环境推荐使用 Laragon WAMP (用英文安装好以后在设置里切换到中文)
    
        (支持自动配置本地域名并自带`git`,`composer`和微信开发需要的`ngrok`), 
        
        官方网站: [http://laragon.org](http://laragon.org)
    
        直接下载(V3.1)链接: [https://pan.baidu.com/s/1o882L3W](https://pan.baidu.com/s/1o882L3W) 密码: `6isc`
    
## 二次开发

- `app/` 目录下模块文件在用 composer 进行更新时会被删除并重新下载, 

    如果需要修改或者扩展模块里面的类, 可以将类文件按照类的命名空间对应的路径复制到 `fixture/` 目录下修改, 程序会优先加载
    
    例如要扩展 `App\Bootstrap\Bootstrap` 类, 可以把 `app/Bootstrap/Boostrap.php` 复制到 `fixture/App/Bootstrap/Boostrap.php`, 然后修改代码
    
- 静态文件(如 `.js`, `.css`, `.png` 等)以及模板文件(`.twig`, `.blade.php` 等), 请修改 `public/` 目录里的文件, 更新模块时不会被强制覆盖

    更新模块后如果出现页面异常或者报错, 可能需要手动强制更新 `public/` 下的模块文件, 请先备份您修改过的文件然后在项目目录( `public/` 目录的上一层)里执行:
    
        php artisan vendor:publish --tags=public --force 
        

## License

[GNU General Public License version 3 (GPLv3)](https://github.com/opencart/opencart/blob/master/license.txt)

## Links

- [点这里加入群: 665863675﹝Laravel Minishop﹞](https://jq.qq.com/?_wv=1027&k=5qYJy7I)
- [github 发布页面](https://github.com/minishop/minishop)
- [问题反馈](https://github.com/minishop/minishop/issues)
- [文档](https://github.com/minishop/minishop/wiki)
- [参与开发(Pull Request)](https://github.com/minishop/minishop/pulls)
- [Twocent Development Team]()

