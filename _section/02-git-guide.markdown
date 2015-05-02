---
title:  "Git Guide"
date: 2015-05-02
hashlink: git
---

The Git commands that I regularly use.

### Generating SSH Keys: ###

{% highlight c %}
$ cd ~/.ssh #1
$ ls #2
$ ssh-keygen -t rsa -C "email@example.com" #3
# Generating public/private rsa key pair.
# Enter file in which to save the key (/Users/you/.ssh/id_rsa): [Press enter]
$ ssh-add id_rsa #4
# Enter passphrase (empty for no passphrase): [Type a passphrase]
# Enter same passphrase again: [Type passphrase again]
# Your identification has been saved in /Users/you/.ssh/id_rsa.
# Your public key has been saved in /Users/you/.ssh/id_rsa.pub.
# The key fingerprint is:
# 01:0f:f4:3b:ca:85:d6:17:a1:7d:f0:68:9d:f0:a2:db email@example.com

$ pbcopy < ~/.ssh/id_rsa.pub #5

$ ssh -T git@github.com #6
{% endhighlight %}

1. Go to <code>.ssh</code> folder.
2. Lists the files in the <code>.ssh</code> directory.
3. Creates a new ssh key, use the email used for GitHub or BitBucket.
4. Adding the <code>id_rsa</code> file. Type in the passphrase.
5. Copies the contents of the <code>id_rsa.pub</code> file to clipboard.
6. Paste it into SSH keys area in GitHub/BitBucket account settings.
7. Test the SSH keys by logging into GitHub. Use git@bitbucket.org if you don't use GitHub.


### Create and push new repository commands list:

{% highlight c %}
$ mkdir <folder_name> #1
$ cd <extracted_folder> #2
$ git init #3
$ git add . #4
$ git commit -am "Commit message" #5
$ git tag <version_name> #6
$ git push origin master #7
{% endhighlight %}

1. Create the project's folder.
2. Go inside the folder.
3. Make this folder as a local repository; <code>.git</code> created.
4. Add everything under the current directory.
5. Commit everything with meaningful commit message.
6. Make a lightweight, unannotated tag.
7. Push the changes in local repositories to the master branch of the remote repositories.


### Creating the new branch and working on it commands list:

{% highlight c %}
$ git checkout -b <branch_name> #1
//Working on code
$ git checkout -- <filename_that_need_to_be_reverted> #2
$ git add <filename_that_has_been_reverted> #3
//Working on code
$ git diff HEAD #4
$ git commit -a -s #5
//Working on code
$ git reset --soft HEAD^ #6
//Working on code
$ git diff ORIG_HEAD #7
$ git commit -a -c ORIG_HEAD #8
$ git checkout master #9
$ git merge <branch_name> #10
$ git log --since='3 days ago' #11
$ git log <version_name>.. <folder_name> #12
{% endhighlight %}

1. Create a new branch.
2. Revert your botched changes in the reverted file.
3. You need to tell git if you added a new file; removal and modification will be caught if you do <code>git commit -a</code> later.
4. To see what changes you are committing.
5. Commit everything as you have tested, with your sign-off.
6. Take the last commit back, keeping what is in the working tree.
7. Look at the changes since the premature commit we took back.
8. Redo the commit undone in the previous step, using the message you originally wrote.
9. Switch to the master branch.
10. Merge a topic branch into your master branch.`
11. Review commit logs. Can be combined and include <code>--max-count=10</code> (show 10 commits), <code>--until=2005-12-10</code>, etc.
12. View only the changes that touch what’s in curses/ directory, since <version_name> tag.


### Participating in people's repositories commands list:

{% highlight c %}
$ git clone <git_repo_url>
$ cd <folder_name>
$ //Working on code
$ git commit -a -s #1
$ git format-patch origin #2
$ git pull #3
$ git log -p ORIG_HEAD.. <folder_name> #4
$ git pull <other_git_repo_url> ALL #5
$ git reset --hard ORIG_HEAD #6
$ git gc #7
$ git fetch --tags #8
{% endhighlight %}

1. Repeat as needed.
2. Extract patches from your branch.
3. Git pull fetches from origin by default and merges into the current branch.
4. Immediately after pulling, look at the changes done upstream since last time we checked, only in the area we are interested in.
5. Fetch from a specific branch from a specific repository and merge.
6. Revert the pull.
7. Garbage collect leftover objects from reverted pull.
8. From time to time, obtain official tags from the origin and store them under <code>.git/refs/tags/</code>.


### Git resources:

<ul>
	<li><a href="https://github.com/tiimgreen/github-cheat-sheet">GitHub Cheat Sheet</a></li>
	<li><a href="https://www.youtube.com/watch?v=ZDR433b0HJY">Introduction to Git with Scott Chacon of GitHub (On YouTube)</a></li>
	<li><a href="http://gitolite.com/gcs.html#(1)">Git Concept Simplified</a></li>
	<li><a href="http://greenido.wordpress.com/2011/04/20/git-101-quick-start-guide/">Git 101 Quick Start Guide</a></li>
	<li><a href="https://www.kernel.org/pub/software/scm/git/docs/everyday.html">Everyday GIT With 20 Commands Or So</a></li>
	<li><a href="https://confluence.atlassian.com/display/STASH/Basic+Git+commands">Attlasian Basic Git Commands</a></li>
	<li><a href="http://guides.github.com/">GitHub Guides</a></li>
	<li><a href="https://www.atlassian.com/git">Attlasian Git Tutorials</a></li>
	<li><a href="http://audreywatters.com/2013/07/07/how-to-run-your-site-on-github/">Using GitHub to Power A Web Project: How and Why</a></li>
</ul>
