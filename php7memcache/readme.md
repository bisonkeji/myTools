注意 下载前先查看phpinfo

　　需要x86 还是64 

　　需要 vc14 还是 vc15


1、安装memcache  
    a)解压压缩包
    b)命令行执行
    c:\memcached\memcached.exe -d install 
    c:\memcached\memcached.exe -d start 

    c:\memcached\memcached.exe -d stop


2、安装memcache php扩展
    根据自己的php版本下载
    下载解压后，
    就到 php/ext 目录下 把 php_memcache.dll 放到里面
    然后在 php 目录下的 php.ini 增加一段内容 
    extension=php_memcache.dll

    加完之后，重启 apache或者nginx

    然后 在php页面输出phpinfo();

    检查 memcache 是否成功加载了。
    如果成功加载了 ，就可以 在一个php页面做 memcache测试了