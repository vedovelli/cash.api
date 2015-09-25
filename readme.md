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

3) Configure your virtual host, the server name `cash.api` must point to `path-to-/cash.api/public`: 

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

:unlock: Open, no login required

:lock: Login required

ACTION | URI | Description | Request | Response example
------------ | ------------- | ------------- | ------------- | -------------
:unlock: GET | / | A simple hello world message | {} | Hello World
:unlock: GET | /users | All users | {} | [{id:0,name:'user name',email: 'user@email.com'},...]
:unlock: GET | /user/{id} | Get user by id | {} | {id:1,name:'user name',email: 'user@email.com'}]
:unlock: POST | /user | Save User | {name:'new user',email:'foo@email.com',passwod:'123456'} | {id:120,name:'new user',email:'foo@email.com'}]
:lock: GET | /user/accounts | User accounts | {} | [{id:5,user_id:1,name:'my account',amount:200.00},...]



# Tables

All tables have `created_at` and `updated_at` fields

* User
 * id
 * name
 * email
 * password
 * remember_token

* Account
 * id
 * user_id
 * name
 * amount  (initial amount)
 
* Tag
 * id
 * user_id
 * name
 
* Transaction
 * id
 * account_id
 * user_id
 * amount
 * date
 * description

 
