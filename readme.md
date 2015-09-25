# cash.api

A litte, ready to use, financial accounting api build with Lumen Framework. 

## Motivation

I wrote this api to write my books about angularjs, jquery mobile, jquery, bootstrap, vue.js, webix, extjs and more. This books don't need a server implementation, just a little API to consuming via REST.

## Requirements

* PHP 5.4
* Composer
* Apache Web Server 

## Warning

This is a dummy application to provide a simple api. Don't use this project in a real application.

## Install

1) Download or fork this project 

2) With composer, run `composer install` to download additional libraries

3) Configure your virtual host, the servername `cash.api` must point to `path-to-/cash.api/public`: 

httpd.conf:
```xml
<VirtualHost *>
    ServerName cash.api
    DocumentRoot "-----PATH----TO-----/cash.api/public"
    <Directory "-----PATH----TO-----//cash.api/public">
        Options FollowSymLinks
        AllowOverride All
        Order allow,deny
        Allow from all
    </Directory>
</VirtualHost>
```

hosts:
```txt
127.0.0.1	cash.api
```
4) Restart web server

5) Access http://cash.api/ and see a "Hello World" message.

# API METHODS LIST



