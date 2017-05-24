# testandplayrepo

**Please do not clone this repository directly. Fork it and `git clone` the forked copy. Look up how to fork a repo.**

## Terminal tips
For mac, we use Terminal.
For windows, you need to install cygwin. (http://www.mcclean-cooper.com/valentino/cygwin_install/)

I'll list some here that you will probably need to know:
* `ls` lets you see the contents in the current directory
* `ls -lah` lists the contents in the current directory with file permissions and more information.
* `cd <directory-name>` goes into a directory
* `cd ..` goes back one directory
* `cd ../directory-1/directory-2` goes back one directory, then goes into the directory-1 folder and then directory-2. Can mix n' match.
* `cd ` goes to root (the top parent folder)
* `pwd` shows you the complete path to your current directory (useful when you've lost track where you are)

Anything else you don't know how to do, just look it up.


## Github tutorial

`git clone <repo-link>` clones the remote repository to your local computer. Look up how to clone github repo.

`git status` to see any changed files.

![Alt text](/img/git_status.png?raw=true "git status")

`git add` files that are ready to be committed.

![Alt text](/img/git_add.png?raw=true "git add")

`git commit -m 'your description of the changes here' `  or go through `git commit`
Your "added" files are now "packaged" and ready to be "pushed" onto the remote(online) repository.

![Alt text](/img/git_commit.png?raw=true "git commit")

`git push` will push your commited files onto the online repo.
`git push <remote-name-url> <branch-name>` for advanced push.

![Alt text](/img/git_push.png?raw=true "git push")

What is really the **online repo** that we are pushing to? By default it should be the url that you used to `git clone` this repo onto your local computer. So if you forked the original repo into your own github account and then git cloned the forked version, then you're pushing probably to the forked version and not the original, which is fine.

We can see what repos we are keeping track of in our current repo. Go to testandplayrepo folder on your local computer and type 
`git remote -v`. This lists all of the remote points we are pointing to.

![Alt text](/img/git_remote.png?raw=true "git remote")

Above, you can see that the url that has the text : (push), was the url you probably used to clone the repo.
Whenever you do push or fetch, your local repository uses these urls to know where to push or fetch from.

But what if we want to make sure our forked repo is updated with the original repo's code? In other words, we want to make sure we are working off of a copy of the code that is up-to-date.
Lets' add a remote link to the original repo using `git remote add <remote-name> <remote-url>`
And then check we are good to go with `git remote -v` again.

![Alt text](/img/git_remote_add.png?raw=true "git remote add")

We can now `git fetch <remote-name>` the changes from the original repo. We now have the fetched changes floating in space somewhere on our computer, but our files are not actually changed yet. `git merge <remote-name>\/<remote-branch>` to merge the fetched data from the remote repo's fetched data and the corresponding remote branch we are merging FROM. The changes are merged onto our current branch.

![Alt text](/img/git_fetch_merge.png?raw=true "git fetch merge")

Above, there weren't any changes in the ntorii original repo, so there was nothing changed.

To check which branch we are currently working on, run `git branch`. Whatever has the star and green text beside it, is the branch we are currently working on.

![Alt text](/img/git_branch.png?raw=true "git branch")


To add a new branch, use `git branch <new-branch-name>`. To switch to that new branch, do `git checkout <branch-name>`. 
![Alt text](/img/git_branch_new_checkout.png?raw=true "git new checout")

Now let's go back to the concept of `git push`. Since we are now dealing with more than 1 remote point (origin and ogorigin) and we have multiple branches on our local environment and on the online repo, we need to be careful about what git push is pushing, and where it is pushing it.

For a more descriptive push, we use `git push <remote-name-url> <branch-name>`. 

Here, I'm explictly saying that I want to push to my forked repo and I'm pushing the contents of my current branch which is new-branch.
![Alt text](/img/git_push_advanced.png?raw=true "git advanced push")


Check the actual contents on github.com to make sure the changes were pushed.

Final notes: 
1. If you don't know how to do something, look it up. If you're scared, just ask. 
2. Are you getting annoyed with the friken type username and password stuff you gotta do everytime you push? Then look up how to setup ssh key with your github repo. 

https://stackoverflow.com/questions/8588768/git-push-username-password-how-to-avoid




















## Optional Setup steps:
1. `Fork` this repository to create a copy on your github account.
2. `git clone` your forked repo into your terminal
3. Use `git remote -v` to check your remote points. You should have the url of your forked copy, not the original of ntorii.
4. Do anything you want at this point.

## Alternate Setup:
1. Do anything you want at this point. (your changes will be prone to being reverted by owner of the main repo)
2. Understand the above sentence.

## Recommended learnings
1. Learn by doing. 
2. Learn how to make changes and commit to main repo.
3. Learn how to setup ssh key.
4. Setup 2-factor authentication on github account.

2 new lines
another line daoh