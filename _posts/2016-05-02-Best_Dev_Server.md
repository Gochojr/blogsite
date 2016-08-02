---
layout: post
title: Best Dev Server
comments: True
---

What you need in a Web server for your web and mobile development? You use XAMPP, MAMP or WAMP because many people around you say its the better option, but is it?

## Requirements of GoTo server for any Web developer
1. Fast Connection handling
2. Better handling of both Static and Dynamic content
3. Centralized configuration for better controlled security
4. Lightweight configuration
5. Scalable

With these requirements you are posed with challenge of choosing a server that has 90% of all these attributes without sacrificing your hardware resources such as memory usage.

## Apache vs Nginx

I know you are wondering why I am not comparing Lighttpd also but its because it is not fully configured to use modules, leaks alot of memory so not practical as a Full stack web server.

The comparison between Apache and Nginx arises when you want to choose a web server and it boils down to performance, and scalability. Apache may have the biggest market share but its challenged by growth of users in World Wide Web. It has a reputation for being bloates, overly complex and performance-limited which is suspectible to DoS attacks. Ever wonder why Organization server is loading a web page very slow? Apache cannot handle concurrent connections so when most of you are queuing your page requests on say Safaricom Career Portal website you are left waiting for minutes even hours to see results of your request. More so Safaricom may have, most likely, limited the number of httpd processes, keepalive connections or limited their durations to keep the website reliable. 

![image](https://assets.wp.nginx.com/wp-content/uploads/2014/03/multiprocess.png)


## [MySQL + PHP] or [MariaDB + PHP] or [PostgreSQL + PHP]

This is entirely subject to self opinion! If you stack supports more DBs the better not considering how bloated it maybe. XAMPP and WAMPserver has never worked for me but if I was asked I would consider WAMP which I can configure PostgreSQL and other modules out of the box without complications.

![image](https://a.fsdn.com/allura/p/wtnmp/icon) WTserver is the new breed! Portable, Preconfigured, Lightweight, Lightning Fast and Stable. It features Nginx server, MariaDB database, Redis cache, PHP 5.6/7.0 (32/64bit script language), Composer dependency manager, pUTTY, Adminer DB manager, WinSCP FTP/SFTP client.

Having used this for three months now I can say it is easily configurable since all config files are in one place. Also I extended it to use [SQL Buddy](http://sqlbuddy.com/) and [WebDAV](http://www.webdav.org/). You can also add [extra packages](https://sourceforge.net/projects/wtnmp/files/extras/) provided by [WTriple](https://sourceforge.net/u/wtriple/profile/).


<button class="button-save large"><a targt="_blank" href="https://sourceforge.net/projects/wtnmp/files/latest/download">Download WTserver for Windows</a></button> 



![http://creativecommons.org/licenses/by-nc-sa/4.0/](https://i.creativecommons.org/l/by-nc-sa/4.0/88x31.png 
"Creative Commons - Attribution-NonCommercial-ShareAlike 4.0 International- CC BY-NC-SA 4.0") [![ <form action="https://www.paypal.com/cgi-bin/webscr" method="post" target="_top">
<input type="hidden" name="cmd" value="_s-xclick">
<input type="hidden" name="hosted_button_id" value="ZQVADBPY2D2D6">
<input type="image" src="https://www.paypalobjects.com/en_US/i/btn/btn_donateCC_LG.gif" border="0" name="submit" alt="PayPal - The safer, easier way to pay online!">
<img alt="" border="0" src="https://www.paypalobjects.com/en_US/i/scr/pixel.gif" width="1" height="1">
</form>](https://www.paypalobjects.com/en_US/i/btn/btn_donateCC_LG.gif)](https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=X6XHVCPMRQEL4)

