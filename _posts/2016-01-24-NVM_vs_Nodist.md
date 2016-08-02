---
layout: post
title: NVM vs. Nodist
comments: True
---



[Node.js](https://nodejs.org) is not Javascript framework! It is a I/O server-side JavaScript environment that uses [Google V8 (C++)]() Javascript engine.So apparently the guy who invented it only released a Linux version of Node.js, when he first wanted to share it with the world..how uncool is that! 

Unfortunately, you will not find facts about what it does here but I can hint you one important fact about node.js is like [PHP]() in the aspect its used to build web servers. 

I love Node.js because it does nothing out-of-the-box basically it uses non-blocking I/O calls therefore enabling it to withstand millions of concurrent connections without incurring the cost of thread context switching. Most importantly, Node.js can be combined with most databases in a similar fashion as of that of MVC server-side development.

Really I use Node.js to push real-time web applications over websockets. I run it over standard port (80) and I always know what is going on. Forget about java applets this is not even close! We are talking about a complete open web stack...

It is in this light that every developer has the terrible ordeal of upgrading his/her tools every time there is new release and keeping older versions when you using say a CMS engine or other web frameworks in dire need of old tech..thats where [NVM](https://github.com/coreybutler/nvm-windows) and [Nodist](https://github.com/marcelklehr/nodist) step in. 

They manage multiple versions of Node.js..not installations because it is not best practice to have more than one installation of [pure Node.js](https://nodejs.org/en/download/) in your development environment. Even a newer release would prompt to overwrite the older version.

![image](https://raw.githubusercontent.com/Gochojr/blogsite/gh-pages/images/nvm_v_%20nodist.png)

So why are there two command-line tools pioneered to do the same thing? Manage Node.js versions? Its simple [Nodist](https://github.com/marcelklehr/nodist) is playing around with BAT files for people who can remember all node and io versions that exist..haha barely the point it was my first but after `nodist install all` I was'nt happy with the number of times I had to keep doing a duplex of commands just to use npm. [NVM](https://github.com/coreybutler/nvm-windows) is more advanced, easy to use, and it comes in three ways of execution. My favourite option of NVM version control is soft link. 

This concept requires putting the soft link in the Windows system PATH as Admin updating its target to the node installation directory you want to use in your favourite command-line terminal. Switching to different versions of node is as simple as switching the soft link target by using the command `nvm use <version> [arch]` that is Node.js version and architecture (3-2bit or 64-bit).

I am running five different versions of Node.js currently and all I have to use in my cygwin is the command: `nvm on` then I pick the version suitable for my development.

Better is that I get to use it with this other tool called [node-windows](https://github.com/coreybutler/node-windows) which acts as big brother for all my Node.js scripts. Basically it runs all my Node.js scripts as Windows services and I get an event-log just in case..

----------

## For more information

- [why-the-hell-would-i-use-node-js](http://www.toptal.com/nodejs/why-the-hell-would-i-use-node-js)
- [This is too shallow for me](https://nodejs.org/en/about/)
- [Can I use it with Visual Studio?](https://code.visualstudio.com/Docs/runtimes/nodejs)
- [I thought you said it can be used with MongoDB?!](https://docs.mongodb.org/getting-started/node/)
- [**WAIT!** I don't know what the hell you are talking about????!!](https://www.udemy.com/understand-nodejs/)

![http://creativecommons.org/licenses/by-nc-sa/4.0/](https://i.creativecommons.org/l/by-nc-sa/4.0/88x31.png 
"Creative Commons - Attribution-NonCommercial-ShareAlike 4.0 International- CC BY-NC-SA 4.0")           [![ <form action="https://www.paypal.com/cgi-bin/webscr" method="post" target="_top">
<input type="hidden" name="cmd" value="_s-xclick">
<input type="hidden" name="hosted_button_id" value="ZQVADBPY2D2D6">
<input type="image" src="https://www.paypalobjects.com/en_US/i/btn/btn_donateCC_LG.gif" border="0" name="submit" alt="PayPal - The safer, easier way to pay online!">
<img alt="" border="0" src="https://www.paypalobjects.com/en_US/i/scr/pixel.gif" width="1" height="1">
</form>](https://www.paypalobjects.com/en_US/i/btn/btn_donateCC_LG.gif)](https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=X6XHVCPMRQEL4)

