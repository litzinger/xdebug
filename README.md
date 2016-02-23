Run the following commands locally:

    export XDEBUG_CONFIG="remote_connect_back=0 idekey=intellij remote_host=10.0.2.2"
    export PHP_IDE_CONFIG="serverName=mysite.dev"

Make sure to add ?XDEBUG_SESSION_START=PHPSTORM to the remote URL

Make sure the following is added to the remote server's php.ini.

    zend_extension=/usr/lib/php5/20090626/xdebug.so
    xdebug.remote_enable=1
    xdebug.remote_handler=dbgp
    xdebug.remote_port=9000
    xdebug.idekey=PHPSTORM
    xdebug.remote_host=localhost

![](https://github.com/litzinger/xdebug/blob/master/ssh-tunnel.png)

![](https://github.com/litzinger/xdebug/blob/master/php-storm-config.png)