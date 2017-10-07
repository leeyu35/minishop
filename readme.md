   
# Laravel Minishop

## 概述

Laravel Minishop 是针对中国大陆市场而开发的一套免费、开源B2C, B2B电商平台系统。

## 版本

版本号分为四个部分，如1.2.3.4， 分别代表【主要】. 【较小】. 【特色】. 【补丁】来表述版本数字。

【主要】的调整较为罕见，一般指显著地代码重写。该版本的升级一般会导致绝大部分模板插件不能正常使用。

【较小】指针对核心架构的显著改变。该版本号的升级会导致一些第三方模板插件的不能使用。

【特色】一般指扩充功能或特色功能的增加，例如增加支付接口、配送方式等。该版本号的升级一般不会影响第三方模板插件的正常使用。

【补丁】一般是小bug的修复，此类版本号之间的升级一般是安全的，例如从1.2.3.4升级到1.2.3.5

## 安装

    composer config repo.shopes composer https://packagist.shopes.cn
    composer require cloudshop/framework
    php artisan cloudshop:install
    
## License

The Laravel framework is open-sourced software licensed under the [MIT license](http://opensource.org/licenses/MIT).

