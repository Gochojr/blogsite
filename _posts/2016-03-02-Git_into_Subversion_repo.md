---
layout: post
title: Git into Subversion repo
comments: True
---

### How do I integrate a Git repo with a local Subversion repo?

Git has a feature that works with Subversion repos called `git-svn`. It is intended to check out existing code from Subversion and work on it, not publishing a Git tree into a Subversion repo.

I will use [VisualSVN Server for Windows](https://www.visualsvn.com/server/getting-started/) to show you how to integrate your git repo on GitHub to SVN repo (allow Subversion open-source revision control system to get all your files+refs on git commands) 

Here we go:

Lets create an empty subversion repo using Windows command prompt:

    echo %cd%> svnadmin create my_svn_repo
    echo %cd%> cd my_svn_repo
    echo %cd% my_svn_repo> svn mkdir trunks tags branches
    echo %cd% my_svn_repo> svn commit -m "am hacking this hehehe!"

OR we can use VisualSVN Server Management console to create [Regular FSFS repo](https://www.visualsvn.com/support/topic/00080/) using the 'Create new repository' action wizard:

![image](https://raw.githubusercontent.com/jgodwin13/blogsite/gh-pages/images/image1.png)

![image](https://raw.githubusercontent.com/jgodwin13/blogsite/gh-pages/images/image2.png)

Finally set the access control security for the repo and open it in browser to see empty svn file. Then create directories `trunks` `tags` `branches`

Now lets go to your 'git-cloned' file and `cd` to that file:


    echo %cd%> cd my_git_repo
    echo %cd% my_git_repo> vim .git/config

Now add this below what you see without any spacing above it:

    [svn-remote "svn"]
    url = http://HOSTNAME@PC/svn/my_svn_repo/trunk/
    fetch = :refs/remotes/git-svn
    
Afterwards lets do some magic with what we just added:

    echo %cd% my_git_repo> git svn fetch
    echo %cd% my_git_repo> git checkout -b svn git-svn
    echo %cd% my_git_repo> git merge master
    echo %cd% my_git_repo> git show-ref trunk
    
Now for the finale spell:

    echo %cd% my_git_repo> git git log --pretty=oneline master | tail -n1
    echo %cd% my_git_repo> git svn dcommit
    echo %cd% my_git_repo> git checkout master
    echo %cd% my_git_repo> git rebase svn
    echo %cd% my_git_repo> git branch -d svn
    echo %cd% my_git_repo> git svn dcommit

![http://creativecommons.org/licenses/by-nc-sa/4.0/](https://i.creativecommons.org/l/by-nc-sa/4.0/88x31.png 
"Creative Commons - Attribution-NonCommercial-ShareAlike 4.0 International- CC BY-NC-SA 4.0") 

