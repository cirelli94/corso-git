# Who am I

- Dev for 5 years
- FOSS enthusiast
- Sorint.lab open\_mind
- New tool: sorry for mistakes!

---

# About Version Control
## Local Version Control Systems
  Local directories?
## Centralized Version Control Systems
  What if the server goes down?
## Distributed Version Control Systems

---

# The Command Line
The command line is the only place you can run all Git commands 

---

# Installing Git
## Linux
`$ sudo dnf install git-all`
`$ sudo apt install git-all`

## MacOS
`$ git --version`

## Windows
https://git-scm.com/download/win

---

# Getting Started
## Your Identity
```
$ git config --global user.name "John Doe"
$ git config --global user.email johndoe@example.com
```

## Check config
```
$ git config --list
user.name=John Doe
user.email=johndoe@example.com
color.status=auto
color.branch=auto
color.interactive=auto
color.diff=auto
...
```

---

# Getting Help
```
$ git help <verb>
$ git <verb> --help
$ man git-<verb>
```

---

# Initializing a Repository in an Existing Directory
```
$ cd /home/user/project
$ git init .
```


---

# Cloning an Existing Repository
```
$ git clone https://github.com/cirelli94/git-course 
```

---

# Recording Changes to the Repository 
![](images/lifecycle.png)

---

## Checking the Status of Your Files
```
$ git status
On branch master
Your branch is up-to-date with 'origin/master'.
nothing to commit, working tree clean
```
Edit something and try again!

---

## Tracking New Files
```
$ git add README.md
```

---

## Staging Modified Files
```
$ git add README.md
$ git status
$ vim README.md
$ git status
```

---

## Viewing Your Staged and Unstaged Changes

`$ git diff`
`$ git diff --staged `

 ---

## Committing Your Changes 

`$ git commit`
`$ git commit -m "Improved README"`
`$ git commit -am "Improved README"`

---

## Removing Files

```
$ rm README.md
$ git status
$ git rm README.md
```

---

## Moving Files 

```
$ git mv README.md README
$ git status
On branch master
Your branch is up-to-date with 'origin/master'.
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

    renamed:    README.md -> README
```

---

# Viewing the Commit History 

```
$ git log
commit aadc28dae072e3df16322dc594801373c7ee564e
Author: afumagalli <afumagalli@sorint.it>
Date:   Fri Feb 18 09:44:26 2022 +0100

    Resolving conflicts

commit 4ec7611ee6a64315dc2b318d0c2bd2eb16ae8722
Author: afumagalli <afumagalli@sorint.it>
Date:   Thu Feb 17 17:34:54 2022 +0100

    Added wsl linter

commit dd2896654cbd918a8b88f95e27bda192940a6e8c
Author: afumagalli <afumagalli@sorint.it>
Date:   Thu Feb 17 15:34:47 2022 +0100

    Added unparam linter

```

---

# Viewing the Commit History 

`$ git log --patch`

`$ git log --stat`

`$ git log --all --decorate --graph`

---

# Undoing Things

```
$ git commit --amend
$ git add forgotten_file
$ git commit --amend
```

---

## Unstaging a Staged File with git restore 
```
$ git restore --staged CONTRIBUTING.md
```

## Unmodifying a Modified File with git restore
```
$ git restore CONTRIBUTING.md
```

---

# Remotes

```
$ git remote -v
origin  git@github.com:cirelli94/ercole.git (fetch)
origin  git@github.com:cirelli94/ercole.git (push)
upstream        git@github.com:ercole-io/ercole.git (fetch)
upstream        git@github.com:ercole-io/ercole.git (push)
```

## Add Remotes

```
$ git remote add a-new-remote git@github.com:cirelli94/my-repo.git           

```

--- 

## Fetch 

```
$ git fetch <remote>
```

## Push to Your Remotes

```
$ git push origin master
```

---

# Git branching
## Create a New Branch

```
$ git branch testing
```

![](images/two-branches.png)

---

# Git branching
## Switching Branches

```
$ git checkout testing
```

---

# Git branching
## Switching Branches

![](images/head-to-testing.png)

---

```
$ vim test.rb
$ git commit -a -m 'made a change'
```
![](images/advance-testing.png)

---

```
$ git checkout master
$ vim test.rb
$ git commit -a -m 'made another change'
```
![](images/advance-master.png)

---

# Merging Fast-forward

![](images/basic-branching-4.png)


---

# Merging Fast-forward

```
$ git merge hotfix
```

![](images/basic-branching-5.png)

---

# Merging

![](images/basic-branching-6.png)

---

# Merging

![](images/basic-merging-1.png)

---

# Merging

![](images/basic-merging-2.png)

---

# Conflicts
```
$ git merge iss53
Auto-merging index.html
CONFLICT (content): Merge conflict in index.html
Automatic merge failed; fix conflicts and then commit the result.
```

```
<<<<<<< HEAD:index.html
<div id="footer">contact : email.support@github.com</div>
=======
<div id="footer">
 please contact us at support@github.com
</div>
>>>>>>> iss53:index.html
```

```
$ git add index.html
$ git commit
```

---

# Branch Management
```
$ git branch
  iss53
* master
  testing
```

---

# Git services
- Gitlab
- Gitea
- Github

---

# Github

Settings > SSH keys > New SSH  key
https://docs.github.com/en/authentication/connecting-to-github-with-ssh/about-ssh

---

# Github

Create a repo

---

# Github

Fork a repo

---

# Github

Create a pull request

---

# Github

Review

---

# Github

Issues
...and comments in PRs


---

# Resources
https://git-scm.com/book/en/v2

# License
All content is licensed under the [Creative Commons Attribution Non Commercial Share Alike 3.0 license](https://creativecommons.org/licenses/by-nc-sa/3.0/).

Images and examples used in this course are taken from https://git-scm.com/book/en/v2
