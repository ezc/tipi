#目录

- [第一章 准备工作和背景知识][prepare-and-background]
	* [第一节 环境搭建][build-env]
	* [第二节 源码布局及阅读方法][code-structure]
	* [第三节 常用代码][common-code-in-php-src]
	* [第四节 小结][01-summary]

- [第二章 用户代码的执行][survey]
	* [第一节 PHP生命周期][php-life-cycle]
	* [第二节 从SAPI开始][sapi-overview]
        + [Apache模块][php-module-in-apache]
        + [嵌入式][embedding-php]
        + [Fastcgi][fastcgi]
	* [第三节 Zend引擎与脚本执行][script-execution]
		+ [词法分析和语法分析][lex-and-yacc]
		+ [opcode][opcode]
		+ [附：找到Opcode具体实现][opcode-handler]
	* [第四节 小结][02-summary]

- [第三章 变量及数据类型][variables]
	* [第一节 变量的内部结构][variables-structure]
		+ [哈希表(HashTable)][variables-hashtable]
		+ [PHP的哈希表实现][variables-hashtable-in-php]
		+ [链表简介][variables-zend-llist]
    * [第二节 常量][const-var]
	* [第三节 预定义变量][pre-defined-variable]
	* [第四节 静态变量][static-var]
	* [第五节 类型提示的实现][type-hint-imp]
	* [第六节 变量的生命周期][var-lifecycle]
		+ [变量的赋值和销毁][var-define-and-init]
		+ [变量的作用域][var-scope]
		+ [global语句][var-global]
	* [第七节 数据类型转换][type-cast]
	* [第八节 小结][03-summary]


- [第四章 函数的实现][function]
    * [第一节 函数的内部结构][function-struct-overview]
        + [函数的内部结构][function-struct]
		+ [函数间的转换][function-union]
    * [第二节 函数的定义,参数及返回值][function-define-pr]
        + [函数的定义][function-define]
		+ [函数的参数][function-param]
        + [函数的返回][function-return]
    * [第三节 函数的调用和执行][function-call]
    * [第四节 匿名函数及闭包][anonymous-function]
    * [第五节 小结][04-summary]

- [第五章 类和面向对象][class]
    * [第一节 类的结构和实现][class-struct]
    * [第二节 类的成员变量及方法][class-member-variables-and-methods]
    * [第三节 访问控制的实现][class-visibility]
    * [第四节 类的继承, 多态及抽象类][class-inherit-abstract]
    * [第五节 魔术方法,延迟绑定及静态成员][class-magic-methods-latebinding]
    * [第六节 PHP保留类及特殊类][class-reserved-and-special-classes]
    * [第七节 对象][class-object]
    * [第八节 命名空间][class-namespace]
    * [第九节 标准类][spl]
    * [第十节 小结][05-summary]

- [第六章 内存管理][memory-management]
	* [第一节 内存管理概述][memory-management-overview]
	* [第二节 PHP中的内存管理][php-memory-manager]
	* [第三节 内存使用：申请和销毁][php-memory-request-free]
	* [第四节 垃圾回收机制][garbage-collection]
		+ [新的垃圾回收机制][new-gc]
	* [第五节 内存管理中的缓存][php-memory-cache]
	* [第六节 写时复制(Copy-On-Write)][copy-on-write]
	* [第七节 小结][06-summary]

- [第七章 Zend虚拟机][zend-vm]
	* [第一节 虚拟机概述][zend-vm-overview]
	* [第二节 语法的实现][php-syntax]
		+ [词法分析][zend-re2c-scanner]
		+ [语法分析][zend-yacc-parser]
		+ [实现自己的语法][zend-custom-php-syntax]
	* [第三节 中间码的执行][opcode-exec]
	* [第四节 源码的加密解密实现][source-code-encrypt]
	* [第五节 小结][07-summary]

- 第八章 线程安全

- 第九章 错误和异常处理

- 第十章 文件和流

- 第十一章 网络编程

- 第十二章 配置文件

- [第十三章 扩展开发][extension-dev]
	* 第一节 扩展开发概述

- 第十四章 PHP新功能
	* 命名空间(Namespace)
	* 匿名函数
	* 闭包
	* Traits

- 第十五章 CPHP以外: PHP编译器
	* HipHop
	* phc
	* Roadsend

- 第十六章 开发实例
	* 第一节 opcode缓存扩展
	* 第二节 性能监控及优化扩展
	* 第三节 扩展PHP语法,为PHP增加语法特性

[prepare-and-background]: 	?p=chapt01/01-00-prepare-and-background
[build-env]: 				?p=chapt01/01-01-php-env-building
[code-structure]: 			?p=chapt01/01-02-code-structure
[common-code-in-php-src]: 	?p=chapt01/01-03-comm-code-in-php-src
[01-summary]: 				?p=chapt01/01-04-summary

[survey]: 				?p=chapt02/02-00-overview
[php-life-cycle]: 		?p=chapt02/02-01-php-life-cycle-and-zend-engine
[sapi-overview]: 		?p=chapt02/02-02-00-overview
[php-module-in-apache]: ?p=chapt02/02-02-01-apache-php-module
[embedding-php]: 		?p=chapt02/02-02-02-embedding-php
[fastcgi]: 				?p=chapt02/02-02-03-fastcgi
[script-execution]: 	?p=chapt02/02-03-00-how-php-script-get-executed
[lex-and-yacc]: 		?p=chapt02/02-03-01-lex-and-yacc
[opcode]: 				?p=chapt02/02-03-02-opcode
[opcode-handler]: 		?p=chapt02/02-03-03-from-opcode-to-handler
[02-summary]: 			?p=chapt02/02-04-summary

[variables]:            ?p=chapt03/03-00-variable-and-data-types
[variables-structure]: 	?p=chapt03/03-01-00-variables-structure
[variables-hashtable]: 	?p=chapt03/03-01-01-hashtable
[variables-hashtable-in-php]: 	?p=chapt03/03-01-02-hashtable-in-php
[variables-zend-llist]: 	?p=chapt03/03-01-03-zend-llist
[const-var]: 			?p=chapt03/03-02-const-var
[pre-defined-variable]:	?p=chapt03/03-03-pre-defined-variable
[static-var]:           ?p=chapt03/03-04-static-var
[type-hint-imp]: 		?p=chapt03/03-05-impl-of-type-hint
[var-lifecycle]:		?p=chapt03/03-06-00-var-lifecycle
[var-define-and-init]:	?p=chapt03/03-06-01-var-define-and-init
[var-scope]: 			?p=chapt03/03-06-02-var-scope
[var-global]: 			?p=chapt03/03-06-03-var-global
[type-cast]: 			?p=chapt03/03-07-type-cast
[03-summary]: 			?p=chapt03/03-08-summary


[function]:            	?p=chapt04/04-00-php-function
[function-struct-overview]:   	?p=chapt04/04-01-00-function-struct-overview
[function-struct]:   	?p=chapt04/04-01-01-function-struct
[function-union]:   	?p=chapt04/04-01-02-function-union
[function-define-pr]:  	?p=chapt04/04-02-00-function-define-param-return
[function-define]:  	?p=chapt04/04-02-01-function-define
[function-param]:       ?p=chapt04/04-02-02-function-param
[function-return]:      ?p=chapt04/04-02-03-function-return
[function-call]:   		?p=chapt04/04-03-function-call
[anonymous-function]:   ?p=chapt04/04-04-anonymous-function
[04-summary]:   		?p=chapt04/04-05-summary

[class]:                ?p=chapt05/05-00-class-and-oop
[class-struct]:         ?p=chapt05/05-01-class-struct
[class-member-variables-and-methods]: ?p=chapt05/05-02-class-member-variables-and-methods
[class-visibility]:         ?p=chapt05/05-03-class-visibility
[class-inherit-abstract]:   ?p=chapt05/05-04-class-inherit-abstract
[class-magic-methods-latebinding]:      ?p=chapt05/05-05-class-magic-methods-latebinding
[class-reserved-and-special-classes]:   ?p=chapt05/05-06-class-reserved-and-special-classes
[class-object]:         ?p=chapt05/05-07-class-object
[class-namespace]:      ?p=chapt05/05-08-class-namespace
[spl]:                  ?p=chapt05/05-09-spl
[05-summary]:           ?p=chapt05/05-10-summary

[memory-management]:		?p=chapt06/06-00-memory-management
[memory-management-overview]:	?p=chapt06/06-01-memory-management-overview
[php-memory-manager]:		?p=chapt06/06-02-php-memory-manager
[php-memory-request-free]:	?p=chapt06/06-03-php-memory-request-free
[garbage-collection]:       ?p=chapt06/06-04-00-garbage-collection
[new-gc]:                   ?p=chapt06/06-04-01-new-garbage-collection
[php-memory-cache]:         ?p=chapt06/06-05-php-memory-cache
[copy-on-write]:            ?p=chapt06/06-06-copy-on-write
[06-summary]:               ?p=chapt06/06-07-summary

[zend-vm]:                  ?p=chapt07/07-00-zend-vm
[zend-vm-overview]:         ?p=chapt07/07-01-zend-vm-overview
[php-syntax]:               ?p=chapt07/07-02-00-php-syntax
[zend-re2c-scanner]:        ?p=chapt07/07-02-01-zend-re2c-scanner
[zend-yacc-parser]:         ?p=chapt07/07-02-02-zend-yacc-parser
[zend-custom-php-syntax]:   ?p=chapt07/07-02-03-custom-php-syntax
[opcode-exec]:              ?p=chapt07/07-03-opcode-exec
[source-code-encrypt]:      ?p=chapt07/07-04-source-code-encrypt
[07-summary]:				?p=chapt07/07-05-summary
