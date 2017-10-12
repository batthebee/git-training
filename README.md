
git Commands
==============

getting help
-------------

```
git <command> --help
git help command
``` 

git config
-----------

configure user 

```
git config [--global] user.name "<your name>"
git config [--global] user.email "<your email>"
```

configure editor 

```
git config [--global] core.editor <editor>
```

set user credentials

either:
    add ssh-key to repository (webinterface)

or:

```
git config [--global] credential.helper "<helper> [<options>]"
```

helpers:
    * cached 
    * store
    * <platform-specific>


configure merge tool 

```
git config [--global] --add merge.tool <tool>
```

configure diff tool

```
git config [--global] --add diff.tool <tool>
```


init repository 
---------------------------

init empty repository 

```
git init
```

adding / removing files 
------------------------

adding files 

```
git add [-i,--interactive] <file(s)>
``` 

remove files 

```
git rm <file(s)>
```

remove files from staging

```
git rm --cached <file(s)>
```

revert files 

```
git checkout -- <file(s)>
```

stash
------

stash local changes 

```
git stash 
```

list stashes

```
git stash list
```

apply stashes 

```
git stash apply
```

remotes
--------

Clone a repository into a new directory

```
git clone <repository> [<directory>]
```

Add remote to local repository

```
$ git remote add origin https://path/to/git-repository.git
```

List remotes 

```
git remote 

```

Get informations about remote 

```
git config --get remote.<remote>.url
git remote show <remote>
```

Push local to remote
```
git push [-u,--set-upsteam <remote> <branch>]
```

Update remotes 

```
git fetch [-all]
```

checkout, branching, merging and rebase  
------------------------------------------

create new branch

```
git branch <branchname> [<start-point>]
```

checkout branch

```
git checkout <branch> [<start-point>]
```

create and checkout new branch

```
git checkout -b <new_branch> [<start-point>]
```

delete branch locally

```
git branch -d,--delete <branch>
```

delete branch remote 

```
$ git push origin -d,--delete <branch_name>
```

rename branch 

```
git branch -m,-M [<oldbranch>] <newbranch>
```

merge one branch into other

```
git merge <branch-to-merge>
```

rebase branch 

```
git rebase [<upstream> [<branch>]]
```

tags
-----

list tags 

```
git tag [-l,--list '<regex>']
```

create tag (simple)

```
git tag <tag>
```

create tag (commented)

```
git tag -a <tag> -m '<commit message>' [<start-point>]
```

delete tag local
```
git tag --delete <tag>
```

delete tag remote 

```
git push --delete <remote> tag
```

exploring history 
-----------------

staging status

```
git status [<options>]
``` 

list logs

```
git log [<version>][..[<version>]]  
```

list logs since

```
git log --since="<since>"
```

log summary

```
git log --stat --summary
```

diff files 

```
git diff [<options>] [<commit>] [<path>...]
```

special 
--------

rewrite last commit message

```
git commit --amend
```

rewrite bulk of commit messages

```
git rebase -i <version>
```

grep content in files

```
git grep <options> ...
```

pick commit from different branche

```
git cherry-pick <commit-id>
```

