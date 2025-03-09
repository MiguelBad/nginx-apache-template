# php

## to make it work

edit /etc/httpd/conf/httpd.conf then...

**comment out:**

```
# LoadModule mpm_event_module modules/mod_mpm_event.so
```

**and uncomment**

```
LoadModule mpm_prefork_module modules/mod_mpm_prefork.so
```

**then add the following at the end of file**

```
LoadModule php_module modules/libphp.so
Include conf/extra/php_module.conf
```

## .htaccess

uncomment:
```
LoadModule rewrite_module modules/mod_rewrite.so
```

## to create virtual hosts

in /etc/httpd/conf/httpd.conf, uncomment:

```
Include conf/extra/httpd-vhosts.conf
```

## add hosts

edit /etc/hosts

```
127.0.0.1 mydomain.local
```
