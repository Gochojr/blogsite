---
layout: post
title: custom-gitbash
comments: True
---

[Git BASH](https://git-for-windows.github.io/) is most common BASH emulation for version control all over the world. I am not going to talk about how it works but show you a trick or two on how to customise you gitbash environment to your liking!

![image](http://blog.wuxu92.com/images/post/git.jpg)

By now I assume you already known the directory-file structure of your Git installation. If you have not done this `cd` to you installation and type `tree`..that will give you a good summary where is where. The files we are going to work with are all in file called `etc`. Here we will edit the `bash.bashrc` file, and `profile` file.

### What is the difference between `bash.bashrc` and `profile` or the so called `.bash_profile`

When you execute your `git-bash.exe` you login (type username and password) via console the `profile` is executed to configure your gitbash shell before the initial command prompt whereas `bash.bashrc` is executed before the window command prompt. 

### How to customise your gitbash using `bash.bashrc` and `profile`

**1. Customising `bash.bashrc`**

Here you are going to edit LINE 19: `PS1=...` which holds your prompt. You can change the color and style where the colors have to be follwoed by a `m` now the color code looks like this `\[\e[<color-code>m\]`.

`<color-code>` **MUST** take the combination of:

`attrb1` + `3-foreground-color` or `4-background-color`

Example:

``
\[\e[1;33m\]
``
 
- for `attrb1` = 1 (bold text)
- for `<color-code>` = 3-foreground-color yellow

For a list of colors and attributes [click here!](https://gist.github.com/jgodwin13/fd8c1ad08c716c7ed1e9)

You can also add `PS1` with current git branch, current success state of the last git command, current timestamp `\[\033[01;30m\]\t`, return git status indicator, hostname `\[\033[00;32m\]\h`, git informations and working directory.

**2. Customising `profile`**

Here you can add ssh-agent service execution upon executing your gitbash. I would recommend you to use [OpenSSH](http://www.openssh.com/). Adding a block of code will enable gitbash to auto-launch ssh-agent tool on git. 

Here is an example:

    agent_run_state=$(ssh-add -l >| /dev/null 2>&1; echo $?)
    if   [ $agent_run_state = 2 ]; then
      eval $(ssh-agent -s)
      ssh-add
    elif [ $agent_run_state = 1 ]; then
      ssh-add
    fi


You can also add some manual documentation for yourself to help you if you cannot remember some commands or workarounds. Here is an example:

    echo "Welcome back Joseph
    Git for Windows v2.7.1(2) 
    Release: February 12th 2016
    License: GNU Public License version 2
    Supports earlier versions of git
    Git Command Referrence: https://confluence.atlassian.com/bitbucketserver/basic-git-commands-776639767.html
    Git Remotes: http://git-scm.com/book/en/v2/Git-Basics-Working-with-Remotes
    cURL uses $HOME/_netrc instead of $HOME/.netrc.
    git clone -c core.longPaths=true
    For more information: file:///C:/bin/Git/ReleaseNotes.html
    
    "
Have a look at my customised gitbash:

![image](https://raw.githubusercontent.com/jgodwin13/blogsite/gh-pages/images/custom_bash.png)


### When I launch my gitbash it takes time to get me started?

If you put alot of executables in your `bash.bashrc` maybe launch of ssh-agents plus..etc your git bash will take sometime to load. Some people even put manual documentation that will load on execution which is not available when running `git help` on gitbash.




> **^_^** **---------------->**   [`Have a look at my Holy scroll!`](https://gist.github.com/jgodwin13/fd8c1ad08c716c7ed1e9)

![http://creativecommons.org/licenses/by-nc-sa/4.0/](https://i.creativecommons.org/l/by-nc-sa/4.0/88x31.png 
"Creative Commons - Attribution-NonCommercial-ShareAlike 4.0 International- CC BY-NC-SA 4.0") 
