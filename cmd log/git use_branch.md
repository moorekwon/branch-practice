```bash
mkdir dev
cd dev
git clone url주소
cd refactored-spoon
touch index.html
vi index.html
git add index.html
git commit
mkdir static
touch static/style.css
vi static/style.css
vi index.html
git add static/style.css
git commit
gid add index.html
git commit
git push -u origin master
```

```bash
git remote
git remote get-url origin
git branch
git remote -v
```

```bash
cd dev
node -v
npm -v
npm install -g hexo-cli
sudo npm install -g hexo-cli
hexo --version
hexo --help
hexo init ghblog(폴더이름)
cd ghblog
npm install
hexo server
hexo new post how-to-start-hexo(글제목)
vi source/_posts/how-to-start-hexo.md
hexo generate
npm install --save-dev hexo-deployer-git
vi _config.yml
-> deploy:
-> type: git
-> repo: https://github.com/moorekwon/moorekwon.github.io.git(존재하는repo이름)
hexo generate
hexo deploy
```

```bash
git clone url주소 themes/next(주소마지막위치)
vi _config.yml
-> theme: next
hexo clean
hexo generate
hexo deploy
```

```bash
cd themes/next
vi _config.yml
-> menu:
	home:
	about:
	archives:
	google: https://www.google.com/ || google(아이콘이름)
hexo clean && hexo generate
hexo deploy
```

```bash
vi themes/next/_config.yml
-> scheme: Gemini (활성화)
hexo clean && hexo generate
hexo deploy
```

```bash
hexo new page about
vi source/about/index.md
```

~~~markdown
# Let me introduce myself

- Name: moorekwon
- Location: Seoul, Korea
- Contacts
	- <a href="https://www.facebook.com/">Facebook</a>
    	- <a href="https://www.developers.facebook.com">Facebook developers</a>
    	
## Languages &&

1. Golang
2. Python
3. node.js

Cras justo odio, dapibus ~.

![](이미지주소)
<img src="" height="">

Nullam id `console.log('hello')` dolor ~.

### go to google

[google](http://www.google.com)
<a href="http://www.google.com">google</a>

``` javascript
for (i = 0; i < 10; i++) {
    console.log('hello')
}
```
~~~

```javascript
cd C:\Program Files\Git\usr\bin
mkdir tree.exe
tree -d
```

```bash
권효진@LAPTOP-R441569V MINGW64 ~
$ mkdir dev

권효진@LAPTOP-R441569V MINGW64 ~
$ cd dev

권효진@LAPTOP-R441569V MINGW64 ~/dev
$ git clone https://github.com/moorekwon/branch-practice.git
Cloning into 'branch-practice'...
remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (3/3), done.

권효진@LAPTOP-R441569V MINGW64 ~/dev
$ cd branch-practice

권효진@LAPTOP-R441569V MINGW64 ~/dev/branch-practice (master)
$ ls
README.md

권효진@LAPTOP-R441569V MINGW64 ~/dev/branch-practice (master)
$ git branch
* master

권효진@LAPTOP-R441569V MINGW64 ~/dev/branch-practice (master)
$ git branch -a
* master
  remotes/origin/HEAD -> origin/master
  remotes/origin/master

권효진@LAPTOP-R441569V MINGW64 ~/dev/branch-practice (master)
$ git branch -r
  origin/HEAD -> origin/master
  origin/master

권효진@LAPTOP-R441569V MINGW64 ~/dev/branch-practice (master)
$ touch index.html

권효진@LAPTOP-R441569V MINGW64 ~/dev/branch-practice (master)
$ ls
index.html  README.md

권효진@LAPTOP-R441569V MINGW64 ~/dev/branch-practice (master)
$ vi index.html

권효진@LAPTOP-R441569V MINGW64 ~/dev/branch-practice (master)
$ git status
On branch master
Your branch is up to date with 'origin/master'.

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        index.html

nothing added to commit but untracked files present (use "git add" to track)

권효진@LAPTOP-R441569V MINGW64 ~/dev/branch-practice (master)
$ git add index.html
g
권효진@LAPTOP-R441569V MINGW64 ~/dev/branch-practice (master)
$ git commit
[master e2dad06] feat: add index.html
 1 file changed, 3 insertions(+)
 create mode 100644 index.html

권효진@LAPTOP-R441569V MINGW64 ~/dev/branch-practice (master)
$ git status
On branch master
Your branch is ahead of 'origin/master' by 1 commit.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean

권효진@LAPTOP-R441569V MINGW64 ~/dev/branch-practice (master)
$ git branch head-init

권효진@LAPTOP-R441569V MINGW64 ~/dev/branch-practice (master)
$ git branch
  head-init
* master

권효진@LAPTOP-R441569V MINGW64 ~/dev/branch-practice (master)
$ git checkout head-init
Switched to branch 'head-init'

권효진@LAPTOP-R441569V MINGW64 ~/dev/branch-practice (head-init)
$ git branch
* head-init
  master

권효진@LAPTOP-R441569V MINGW64 ~/dev/branch-practice (head-init)
$ vi index.html

권효진@LAPTOP-R441569V MINGW64 ~/dev/branch-practice (head-init)
$ vi index.html

권효진@LAPTOP-R441569V MINGW64 ~/dev/branch-practice (head-init)
$ git status
On branch head-init
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   index.html

no changes added to commit (use "git add" and/or "git commit -a")

권효진@LAPTOP-R441569V MINGW64 ~/dev/branch-practice (head-init)
$ git add index.html

권효진@LAPTOP-R441569V MINGW64 ~/dev/branch-practice (head-init)
$ git commit -m "feat: set char to utf-8, viewport, title
> charset: utf-8
> width: device-width
> title: Hellow my world"
[head-init 83ccdde] feat: set char to utf-8, viewport, title charset: utf-8 width: device-width title: Hellow my world
 1 file changed, 5 insertions(+)

권효진@LAPTOP-R441569V MINGW64 ~/dev/branch-practice (head-init)
$ git status
On branch head-init
nothing to commit, working tree clean

권효진@LAPTOP-R441569V MINGW64 ~/dev/branch-practice (head-init)
$ cat index.html
<!doctype html>
<html>
        <head>
                <meta charset="utf-8">
                <meta name="viewport" content="width=device-width, initial-scale=1.0">
                <title>Hello my world</title>
        </head>
</html>

권효진@LAPTOP-R441569V MINGW64 ~/dev/branch-practice (head-init)
$ git checkout master
Switched to branch 'master'
Your branch is ahead of 'origin/master' by 1 commit.
  (use "git push" to publish your local commits)

권효진@LAPTOP-R441569V MINGW64 ~/dev/branch-practice (master)
$ git branch
  head-init
* master

권효진@LAPTOP-R441569V MINGW64 ~/dev/branch-practice (master)
$ cat index.html
<!doctype html>
<html>
</html>

권효진@LAPTOP-R441569V MINGW64 ~/dev/branch-practice (master)
$ git checkout head-init
Switched to branch 'head-init'

권효진@LAPTOP-R441569V MINGW64 ~/dev/branch-practice (head-init)
$ cat index.html
<!doctype html>
<html>
        <head>
                <meta charset="utf-8">
                <meta name="viewport" content="width=device-width, initial-scale=1.0">
                <title>Hello my world</title>
        </head>
</html>

권효진@LAPTOP-R441569V MINGW64 ~/dev/branch-practice (head-init)
$ git remote
origin

권효진@LAPTOP-R441569V MINGW64 ~/dev/branch-practice (head-init)
$ git checkout master
Switched to branch 'master'
Your branch is ahead of 'origin/master' by 1 commit.
  (use "git push" to publish your local commits)

권효진@LAPTOP-R441569V MINGW64 ~/dev/branch-practice (master)
$ cat index.html
<!doctype html>
<html>
</html>

권효진@LAPTOP-R441569V MINGW64 ~/dev/branch-practice (master)
$ git branch body-init

권효진@LAPTOP-R441569V MINGW64 ~/dev/branch-practice (master)
$ git branch
  body-init
  head-init
* master

권효진@LAPTOP-R441569V MINGW64 ~/dev/branch-practice (master)
$ git checokut body-init
git: 'checokut' is not a git command. See 'git --help'.

The most similar command is
        checkout

권효진@LAPTOP-R441569V MINGW64 ~/dev/branch-practice (master)
$ git checkout body-init
Switched to branch 'body-init'

권효진@LAPTOP-R441569V MINGW64 ~/dev/branch-practice (body-init)
$ vi index.html

권효진@LAPTOP-R441569V MINGW64 ~/dev/branch-practice (body-init)
$ cat index.html
<!doctype html>
<html>
</html>

권효진@LAPTOP-R441569V MINGW64 ~/dev/branch-practice (body-init)
$ vi index.html

권효진@LAPTOP-R441569V MINGW64 ~/dev/branch-practice (body-init)
$ git add .

권효진@LAPTOP-R441569V MINGW64 ~/dev/branch-practice (body-init)
$ git commit -m "feat: add body tag
> I added body tag in index.html"
[body-init f90baa2] feat: add body tag I added body tag in index.html
 1 file changed, 2 insertions(+)

권효진@LAPTOP-R441569V MINGW64 ~/dev/branch-practice (body-init)
$ cat index.html
<!doctype html>
<html>
        <body>
        </body>
</html>

권효진@LAPTOP-R441569V MINGW64 ~/dev/branch-practice (body-init)
$ vi index.html

권효진@LAPTOP-R441569V MINGW64 ~/dev/branch-practice (body-init)
$ git add index.html
gi
권효진@LAPTOP-R441569V MINGW64 ~/dev/branch-practice (body-init)
$ git commit -m "feat: add h1, p to show results
> I added h1, p to index.html with chrome."
[body-init 2a369ae] feat: add h1, p to show results I added h1, p to index.html with chrome.
 1 file changed, 2 insertions(+)

권효진@LAPTOP-R441569V MINGW64 ~/dev/branch-practice (body-init)
$ cat index.html
<!doctype html>
<html>
        <body>
                <h1>Home</h1>
                <p>Welcome hoem.</p>
        </body>
</html>

권효진@LAPTOP-R441569V MINGW64 ~/dev/branch-practice (body-init)
$ git checkout master
Switched to branch 'master'
Your branch is ahead of 'origin/master' by 1 commit.
  (use "git push" to publish your local commits)

권효진@LAPTOP-R441569V MINGW64 ~/dev/branch-practice (master)
$ cat index.html
<!doctype html>
<html>
</html>

권효진@LAPTOP-R441569V MINGW64 ~/dev/branch-practice (master)
$ git merge head-init
Updating e2dad06..83ccdde
Fast-forward
 index.html | 5 +++++
 1 file changed, 5 insertions(+)

권효진@LAPTOP-R441569V MINGW64 ~/dev/branch-practice (master)
$ cat index.html
<!doctype html>
<html>
        <head>
                <meta charset="utf-8">
                <meta name="viewport" content="width=device-width, initial-scale=1.0">
                <title>Hello my world</title>
        </head>
</html>

권효진@LAPTOP-R441569V MINGW64 ~/dev/branch-practice (master)
$ git branch
  body-init
  head-init
* master

권효진@LAPTOP-R441569V MINGW64 ~/dev/branch-practice (master)
$ git merge body-init
Auto-merging index.html
CONFLICT (content): Merge conflict in index.html
Automatic merge failed; fix conflicts and then commit the result.

권효진@LAPTOP-R441569V MINGW64 ~/dev/branch-practice (master|MERGING)
$ vi index.html

권효진@LAPTOP-R441569V MINGW64 ~/dev/branch-practice (master|MERGING)
$ git status
On branch master
Your branch is ahead of 'origin/master' by 2 commits.
  (use "git push" to publish your local commits)

You have unmerged paths.
  (fix conflicts and run "git commit")
  (use "git merge --abort" to abort the merge)

Unmerged paths:
  (use "git add <file>..." to mark resolution)
        both modified:   index.html

no changes added to commit (use "git add" and/or "git commit -a")

권효진@LAPTOP-R441569V MINGW64 ~/dev/branch-practice (master|MERGING)
$ git add index.html

권효진@LAPTOP-R441569V MINGW64 ~/dev/branch-practice (master|MERGING)
$ git commit
[master 641c53e] Merge branch 'body-init'

권효진@LAPTOP-R441569V MINGW64 ~/dev/branch-practice (master)
$ git status
On branch master
Your branch is ahead of 'origin/master' by 5 commits.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean

권효진@LAPTOP-R441569V MINGW64 ~/dev/branch-practice (master)
$ git push origin master
Enumerating objects: 16, done.
Counting objects: 100% (16/16), done.
Delta compression using up to 4 threads
Compressing objects: 100% (13/13), done.
Writing objects: 100% (15/15), 1.69 KiB | 144.00 KiB/s, done.
Total 15 (delta 1), reused 0 (delta 0)
remote: Resolving deltas: 100% (1/1), done.
To https://github.com/moorekwon/branch-practice.git
   1ee98cb..641c53e  master -> master

권효진@LAPTOP-R441569V MINGW64 ~/dev/branch-practice (master)
$ cat index.html
<!doctype html>
<html>
        <head>
                <meta charset="utf-8">
                <meta name="viewport" content="width=device-width, initial-scale=1.0">
                <title>Hello my world</title>
        </head>
        <body>
                <h1>Home</h1>
                <p>Welcome hoem.</p>
        </body>
</html>

권효진@LAPTOP-R441569V MINGW64 ~/dev/branch-practice (master)
$ checkout head-init
bash: checkout: command not found

권효진@LAPTOP-R441569V MINGW64 ~/dev/branch-practice (master)
$ git checkout head-init
Switched to branch 'head-init'

권효진@LAPTOP-R441569V MINGW64 ~/dev/branch-practice (head-init)
$ cat index.html
<!doctype html>
<html>
        <head>
                <meta charset="utf-8">
                <meta name="viewport" content="width=device-width, initial-scale=1.0">
                <title>Hello my world</title>
        </head>
</html>

권효진@LAPTOP-R441569V MINGW64 ~/dev/branch-practice (head-init)
$ git status
On branch head-init
nothing to commit, working tree clean

권효진@LAPTOP-R441569V MINGW64 ~/dev/branch-practice (head-init)
$ git push -u origin head-init
Total 0 (delta 0), reused 0 (delta 0)
remote:
remote: Create a pull request for 'head-init' on GitHub by visiting:
remote:      https://github.com/moorekwon/branch-practice/pull/new/head-init
remote:
To https://github.com/moorekwon/branch-practice.git
 * [new branch]      head-init -> head-init
Branch 'head-init' set up to track remote branch 'head-init' from 'origin'.

권효진@LAPTOP-R441569V MINGW64 ~/dev/branch-practice (head-init)
$ cat index.html
<!doctype html>
<html>
        <head>
                <meta charset="utf-8">
                <meta name="viewport" content="width=device-width, initial-scale=1.0">
                <title>Hello my world</title>
        </head>
</html>

권효진@LAPTOP-R441569V MINGW64 ~/dev/branch-practice (head-init)
$ git checkout body-init
Switched to branch 'body-init'

권효진@LAPTOP-R441569V MINGW64 ~/dev/branch-practice (body-init)
$ cat index.html
<!doctype html>
<html>
        <body>
                <h1>Home</h1>
                <p>Welcome hoem.</p>
        </body>
</html>

권효진@LAPTOP-R441569V MINGW64 ~/dev/branch-practice (body-init)
$ git push -u origin master
Everything up-to-date
Branch 'master' set up to track remote branch 'master' from 'origin'.

권효진@LAPTOP-R441569V MINGW64 ~/dev/branch-practice (body-init)
$ cat index.html
<!doctype html>
<html>
        <body>
                <h1>Home</h1>
                <p>Welcome hoem.</p>
        </body>
</html>

권효진@LAPTOP-R441569V MINGW64 ~/dev/branch-practice (body-init)
$ git push -u orign body-init
fatal: 'orign' does not appear to be a git repository
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.

권효진@LAPTOP-R441569V MINGW64 ~/dev/branch-practice (body-init)
$ git checkout master
Switched to branch 'master'
Your branch is up to date with 'origin/master'.

권효진@LAPTOP-R441569V MINGW64 ~/dev/branch-practice (master)
$ cat index.html
<!doctype html>
<html>
        <head>
                <meta charset="utf-8">
                <meta name="viewport" content="width=device-width, initial-scale=1.0">
                <title>Hello my world</title>
        </head>
        <body>
                <h1>Home</h1>
                <p>Welcome hoem.</p>
        </body>
</html>

권효진@LAPTOP-R441569V MINGW64 ~/dev/branch-practice (master)
$ git checkout body-init
Switched to branch 'body-init'

권효진@LAPTOP-R441569V MINGW64 ~/dev/branch-practice (body-init)
$ git push -u origin body-init
Total 0 (delta 0), reused 0 (delta 0)
remote:
remote: Create a pull request for 'body-init' on GitHub by visiting:
remote:      https://github.com/moorekwon/branch-practice/pull/new/body-init
remote:
To https://github.com/moorekwon/branch-practice.git
 * [new branch]      body-init -> body-init
Branch 'body-init' set up to track remote branch 'body-init' from 'origin'.

권효진@LAPTOP-R441569V MINGW64 ~/dev/branch-practice (body-init)
$ git checkout head-init
Switched to branch 'head-init'
Your branch is up to date with 'origin/head-init'.

권효진@LAPTOP-R441569V MINGW64 ~/dev/branch-practice (head-init)
$ git pull origin master
From https://github.com/moorekwon/branch-practice
 * branch            master     -> FETCH_HEAD
Updating 83ccdde..641c53e
Fast-forward
 index.html | 4 ++++
 1 file changed, 4 insertions(+)

권효진@LAPTOP-R441569V MINGW64 ~/dev/branch-practice (head-init)
$ cat index.html
<!doctype html>
<html>
        <head>
                <meta charset="utf-8">
                <meta name="viewport" content="width=device-width, initial-scale=1.0">
                <title>Hello my world</title>
        </head>
        <body>
                <h1>Home</h1>
                <p>Welcome hoem.</p>
        </body>
</html>

권효진@LAPTOP-R441569V MINGW64 ~/dev/branch-practice (head-init)
$ git status
On branch head-init
Your branch is ahead of 'origin/head-init' by 3 commits.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean

권효진@LAPTOP-R441569V MINGW64 ~/dev/branch-practice (head-init)
$ git remote
origin

권효진@LAPTOP-R441569V MINGW64 ~/dev/branch-practice (head-init)
$ vi index.html

권효진@LAPTOP-R441569V MINGW64 ~/dev/branch-practice (head-init)
$ git add index.html

권효진@LAPTOP-R441569V MINGW64 ~/dev/branch-practice (head-init)
$ git commit -m "feat: add style tag in index.html
> I added style tag in index.html
> set colors
> bg: #000000;
> ft: #ffffff;"
[head-init 2fb6b61] feat: add style tag in index.html I added style tag in index.html set colors bg: #000000; ft: #ffffff;
 1 file changed, 6 insertions(+)

권효진@LAPTOP-R441569V MINGW64 ~/dev/branch-practice (head-init)
$ git push origin head-init
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 415 bytes | 59.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
fTo https://github.com/moorekwon/branch-practice.git
   83ccdde..2fb6b61  head-init -> head-init

권효진@LAPTOP-R441569V MINGW64 ~/dev/branch-practice (head-init)
$ cat index.html
<!doctype html>
<html>
        <head>
                <meta charset="utf-8">
                <meta name="viewport" content="width=device-width, initial-scale=1.0">
                <title>Hello my world</title>
                <style>
                        body {
                                background-color: #000000;
                                color: #ffffff;
                        }
                </style>
        </head>
        <body>
                <h1>Home</h1>
                <p>Welcome hoem.</p>
        </body>
</html>

권효진@LAPTOP-R441569V MINGW64 ~/dev/branch-practice (head-init)
$ git checkout master
Switched to branch 'master'
Your branch is up to date with 'origin/master'.

권효진@LAPTOP-R441569V MINGW64 ~/dev/branch-practice (master)
$ cat index.html
<!doctype html>
<html>
        <head>
                <meta charset="utf-8">
                <meta name="viewport" content="width=device-width, initial-scale=1.0">
                <title>Hello my world</title>
        </head>
        <body>
                <h1>Home</h1>
                <p>Welcome hoem.</p>
        </body>
</html>

권효진@LAPTOP-R441569V MINGW64 ~/dev/branch-practice (master)
$ git merge head-init
Updating 641c53e..2fb6b61
Fast-forward
 index.html | 6 ++++++
 1 file changed, 6 insertions(+)

권효진@LAPTOP-R441569V MINGW64 ~/dev/branch-practice (master)
$ cat index.html
<!doctype html>
<html>
        <head>
                <meta charset="utf-8">
                <meta name="viewport" content="width=device-width, initial-scale=1.0">
                <title>Hello my world</title>
                <style>
                        body {
                                background-color: #000000;
                                color: #ffffff;
                        }
                </style>
        </head>
        <body>
                <h1>Home</h1>
                <p>Welcome hoem.</p>
        </body>
</html>

권효진@LAPTOP-R441569V MINGW64 ~/dev/branch-practice (master)
$ git status
On branch master
Your branch is ahead of 'origin/master' by 1 commit.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean

권효진@LAPTOP-R441569V MINGW64 ~/dev/branch-practice (master)
$ git push origin master
Total 0 (delta 0), reused 0 (delta 0)
To https://github.com/moorekwon/branch-practice.git
   641c53e..2fb6b61  master -> master

권효진@LAPTOP-R441569V MINGW64 ~/dev/branch-practice (master)
$ git branch
  body-init
  head-init
* master

권효진@LAPTOP-R441569V MINGW64 ~/dev/branch-practice (master)
$ git branch -D body-init
Deleted branch body-init (was 2a369ae).

권효진@LAPTOP-R441569V MINGW64 ~/dev/branch-practice (master)
$ git branch
  head-init
* master

권효진@LAPTOP-R441569V MINGW64 ~/dev/branch-practice (master)
$ git branch -D head-init
Deleted branch head-init (was 2fb6b61).

권효진@LAPTOP-R441569V MINGW64 ~/dev/branch-practice (master)
$ git branch
* master

권효진@LAPTOP-R441569V MINGW64 ~/dev/branch-practice (master)
$ git status
On branch master
Your branch is up to date with 'origin/master'.

nothing to commit, working tree clean

권효진@LAPTOP-R441569V MINGW64 ~/dev/branch-practice (master)
$ git checkout -b develop
Switched to a new branch 'develop'

권효진@LAPTOP-R441569V MINGW64 ~/dev/branch-practice (develop)
$ git branch
* develop
  master

권효진@LAPTOP-R441569V MINGW64 ~/dev/branch-practice (develop)
$ git checkout -b feat/layout
Switched to a new branch 'feat/layout'

권효진@LAPTOP-R441569V MINGW64 ~/dev/branch-practice (feat/layout)
$ git branch
  develop
* feat/layout
  master

권효진@LAPTOP-R441569V MINGW64 ~/dev/branch-practice (feat/layout)
$ vi index.html

권효진@LAPTOP-R441569V MINGW64 ~/dev/branch-practice (feat/layout)
$ git add index.html

권효진@LAPTOP-R441569V MINGW64 ~/dev/branch-practice (feat/layout)
$ git commit -m "feat: wrap main contents with div
> div-wrapper"
[feat/layout 034c309] feat: wrap main contents with div div-wrapper
 1 file changed, 4 insertions(+), 2 deletions(-)

권효진@LAPTOP-R441569V MINGW64 ~/dev/branch-practice (feat/layout)
$ git push -u origin feat/layout
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 388 bytes | 55.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'feat/layout' on GitHub by visiting:
remote:      https://github.com/moorekwon/branch-practice/pull/new/feat/layout
remote:
To https://github.com/moorekwon/branch-practice.git
 * [new branch]      feat/layout -> feat/layout
Branch 'feat/layout' set up to track remote branch 'feat/layout' from 'origin'.

권효진@LAPTOP-R441569V MINGW64 ~/dev/branch-practice (feat/layout)
$ cat index.html
<!doctype html>
<html>
        <head>
                <meta charset="utf-8">
                <meta name="viewport" content="width=device-width, initial-scale=1.0">
                <title>Hello my world</title>
                <style>
                        body {
                                background-color: #000000;
                                color: #ffffff;
                        }
                </style>
        </head>
        <body>
                <div>
                        <h1>Home</h1>
                        <p>Welcome hoem.</p>
                </div>
        </body>
</html>

권효진@LAPTOP-R441569V MINGW64 ~/dev/branch-practice (feat/layout)
$ git checkout develop
Switched to branch 'develop'

권효진@LAPTOP-R441569V MINGW64 ~/dev/branch-practice (develop)
$ git merge feature/layout
merge: feature/layout - not something we can merge

권효진@LAPTOP-R441569V MINGW64 ~/dev/branch-practice (develop)
$ git merge feat/layout
Updating 2fb6b61..034c309
Fast-forward
 index.html | 6 ++++--
 1 file changed, 4 insertions(+), 2 deletions(-)

권효진@LAPTOP-R441569V MINGW64 ~/dev/branch-practice (develop)
$ git push origin develop
Total 0 (delta 0), reused 0 (delta 0)
remote:
remote: Create a pull request for 'develop' on GitHub by visiting:
remote:      https://github.com/moorekwon/branch-practice/pull/new/develop
remote:
To https://github.com/moorekwon/branch-practice.git
 * [new branch]      develop -> develop

권효진@LAPTOP-R441569V MINGW64 ~/dev/branch-practice (develop)
$ cat index.html
<!doctype html>
<html>
        <head>
                <meta charset="utf-8">
                <meta name="viewport" content="width=device-width, initial-scale=1.0">
                <title>Hello my world</title>
                <style>
                        body {
                                background-color: #000000;
                                color: #ffffff;
                        }
                </style>
        </head>
        <body>
                <div>
                        <h1>Home</h1>
                        <p>Welcome hoem.</p>
                </div>
        </body>
</html>
```

