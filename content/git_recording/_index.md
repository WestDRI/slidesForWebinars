+++
title = "git_recording"
outputs = ["Reveal"]
[logowg]
src = "/img/wg_white_removed_medium.png"
[logogit]
src = "/img/git/git_icon.png"
[backlink]
href = "https://westgrid-cli.netlify.app/summerschool2020/git-07-first/"
txt = "Back to Course Page"
[reveal_hugo]
custom_theme = "mh1.scss"
custom_theme_compile = true
+++

<br>
# <center><span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="300"></span> &nbsp;recording history</center>

#### <center>WestGrid Summer School</center>

##### <center>Marie-Hélène Burle</center>

###### <center><training@westgrid.ca></center>

---

##### <center><font color="#b30059">Run the commands in this lesson on your machine to familiarize yourself with Git!</font></center>

---

###### <center>Remember our 3 components from the previous lesson?</center>
<br>
![](/img/git/diagrams/git01.png)

---

###### <center>How do we create them?</center>
<br>
![](/img/git/diagrams/git01.png)

---

#### <center>Let's try it!</center>
<br>
First, we need to create a project: this means creating a directory.

{{%fragment%}}
Let's call it {{<b>}}git_lesson{{</b>}}.
{{%/fragment%}}

<br>

{{% fragment %}}
<span style="font-size: 1.7rem; color: #e67300"><b>*Make sure never to use spaces when you use Git. It will make your life a lot easier.*</b></span>
{{% /fragment %}}

---

##### <center>Open a terminal</center>
<br>
<b>Windows:</b> &emsp;&nbsp;Git BASH <br>

<b>MacOS:</b> &emsp;&emsp;Terminal <br>

<b>Linux:</b> &emsp;&emsp;&ensp;&nbsp;any terminal emulator

---

##### <center>Create the root of the project</center>
<br>
```sh
cd /path/where/you/want/your/repository
mkdir git_lesson
```
<br>
You can place your project wherever you want on your computer. Simply make sure that you know where it is and that it is somewhere sensible.

{{% fragment %}}
<br>
All files for this project need to be in this directory: it is the **root** of the project. <br>
Git will only "see" files within this directory.

Of course, you can create subdirectories in it to organize your files.
{{% /fragment %}}

---

##### <center>Navigate to the directory in your usual way</center>
<br>
This may be with Windows explorer or Finder.

{{% fragment %}}
Realize that there is nothing special about this directory.
{{% /fragment %}}

---

##### <center>Turn the directory into a repository</center>
<br>
To put our project under version control, we initiate the repository.
<br>
<br>
Make sure that you are in the root of the project!
```sh
cd git_lesson
pwd         # this should return the path to git_lesson
```

{{% fragment %}}
<br>
The directory is empty:

```sh
ls -a		# this should not return any file or directory
```
{{% /fragment %}}

---

##### <center>Initiate the repository</center>
<br>
```sh
git init
```
{{% fragment %}}
<br>
You now have in your root folder a very important directory: {{<b>}}.git{{</b>}}.

```sh
ls -a		 # make sure that you can see the .git directory
```
<br>
{{% /fragment %}}

{{% fragment %}}
*Note: we need the {{<c>}}-a{{</c>}} flag because files and directories starting with a dot are hidden.*
{{% /fragment %}}

---

##### <center>Go see it with your usual tool</center>
<br>

Go back to your directory with Windows explorer or Finder to demystify it.

If you don't see it, make sure to change the options to see hidden files.

---

##### <center>Go have a look at what is inside</center>

---

###### <center>So, what is what?</center>
<br>
![](/img/git/diagrams/git01.png)

---

###### <center>So, what is what?</center>
<br>
![](/img/git/diagrams/git02.png)

---

###### <center>So, what is what?</center>
<br>
![](/img/git/diagrams/git03.png)

---

##### <center>Status of a repository</center>
<br>
Whenever you want to know what is going on in your repository, run:
<br>
```sh
git status
```

{{% fragment %}}
<br>
<font color="#b30059">What is the current status of your repository?</font>
{{% /fragment %}}

---

##### <center><font color="#b30059">Now create 3 files in your new repository</font></center>
<br>
```sh
touch file1.txt
touch file2.txt
touch file3.txt
```

{{% fragment %}}
<br>
You can see your files if you run:
```sh
ls -a
```
{{% /fragment %}}

---

##### <center><font color="#b30059">Add content to your files</font></center>

Add several paragraphs in each of your 3 files.<br>
<br>
You can type random words, copy and paste a few paragraphs from a page web, or use {{<a "https://en.wikipedia.org/wiki/Lorem_ipsum" "Lorem ipsum">}}... it doesn't matter what the content is.<br>
<br>
From the command line, you can use, for instance:
```sh
echo "your text" > file1.txt
```
<br>
If your text is long, pasting it in the terminal can be weirdly slow,<br>
so you can open a text editor (e.g. nano):
```sh
nano file1.txt
```
paste your text, save, and close the editor.<br>

---

##### <center><font color="#b30059">Inspect your repository now</font></center>
<br>

How do you inspect a repository again? \\
Was it something with "status" maybe? If you forgot, go back a few slides.
<br><br>
What has changed?

---

##### <center>You need to start tracking your files</center>
<br>
Before you can do anything, you need to put your files under version control.

For this, you first *stage* them:
```sh
git add .           # stage all changes
git add <file>      # stage <file>
```

---

##### <center>Start tracking your files</center>
<br>
For example, you could stage {{<b>}}file1.txt{{</b>}} first:
```sh
git add file1.txt
```

Run {{%c%}}git status{{%/c%}} to see what happened.

Then you could stage the remaining 2 files with:

```sh
git add .
```

Run {{%c%}}git status{{%/c%}} again.<br><br>

*Note: don't hesitate to use {{%b%}}Tab{{%/b%}} for completion.*

---

##### <center>Take a first snapshot of your project</center>
<br>
Staging does not record the history of your project. The staging area is only a way to organize your next commit by bringing together changes that make sense to re-group in a snapshot of the project.<br><br>

You write the history of your project—something that will not get lost—by *committing*. A commit is one such snapshot of your project.

---

##### <center>Your first commit</center>
<br>
You create a commit with {{<c>}}git commit{{</c>}}.

But Git will not allow a commit without a message describing it. So if you only run the command above, Git will open a text editor in which you can enter your commit message.<br>
<br>
If you want to commit without using a text editor, you must use the {{<c>}}-m{{</c>}} flag and a message within the command:
<br>
```sh
git commit -m "Your commit message"
```

---

##### <center>Commit messages</center>
<br>
Do take the commit messages seriously. They will be key later on to navigate your history.<br>
<br>
Messages such as "New commit" aren't exactly helpful.<br>
Make sure to describe what you did in the changes you are committing.<br>
<br>
Traditionally, the first commit message is "Initial commit".<br>
<br>
So a first commit often looks like this:
```sh
git commit -m "Initial commit"
```
But you can add information, for instance by listing the new files that you added to the project.

---

##### <center>Commit messages good practice</center>
<br>
- Use the present tense<br><br>
- The first line is a summary of the commit and is less than 50 characters long <br><br>
- Leave a blank line below <br><br>
- Add the body of your commit message below that

---

##### <center>Commit messages good practice</center>
<br>
So if you want a more informative message than simply "Initial commit", this would be a good message:

```sh
git commit -m "Initial commit
dquote>
dquote> add file1.txt with bla bla bla
dquote> add file2.txt
dquote> add file3.txt with this and that"
```

---

### <center><font color="#b30059">Make your first commit</font></center>

---

##### <center>SHA-1 checksum</center>
<br>

Each commit is identified by a unique 40-character SHA-1 checksum. People usually refer to it as a "hash".<br>
<br>
The short form of a hash only contains the first 7 characters, which is generally sufficient to identify a commit.<br>
<br>
After you committed, Git gave you the short form of the hash of your first commit.

---

##### <center>SHA-1 checksum</center>
<br>

*Note*

You can get the hash of any ref name (e.g. master, HEAD, etc.) with these commands:

```sh
# Get the full hash
git rev-parse <refname>

# Get the short version of the hash
git rev-parse --short <refname>

# Get <n> digits of the hash
# Note that Git will always at least give you the necessary digits to uniquely identify the hash
git rev-parse --short=<n> <refname>

# Show the entire hash with the digits necessary to uniquely identify it in color
git rev-parse <refname> | GREP_COLORS='ms=34;1' grep $(git rev-parse --short=0 <refname>)
```

---

#### <center><font color="#b30059">Inspect your repository again</font></center>
<br>
<center>What do you see now?</center>

---

##### <center>Getting more information on changes</center>
<br>
Make changes to your files (add text, delete or re-write sections, etc.)

{{%fragment%}}
{{%c%}}git status{{%/c%}} gives you information on which files are modified.
{{%/fragment%}}

{{%fragment%}}
What if you want to see the actual changes?
{{%/fragment%}}

{{% fragment %}}
<br>
The command for this is:
```sh
git diff
```
{{% /fragment %}}

---

##### <center>Getting more information on changes</center>
<br>

By default, {{<c>}}git diff{{</c>}} uses a pager (e.g. {{<c>}}less{{</c>}}).

You scroll down with the {{<b>}}Space{{</b>}} key and you exit with {{<b>}}q{{</b>}}.<br>
<br>

{{% fragment %}}
You can circumvent the pager with:
```sh
git --no-pager diff
```
{{% /fragment %}}

{{% fragment %}}
<br>
<font color="#b30059">Run {{<c>}}git diff{{</c>}} on your repo.</font>
{{% /fragment %}}

---

##### <center>More on staging</center>
<br>
Earlier, we staged our new files to start tracking them with Git.

You will have to stage them again each time you want to commit new changes.

But you don't have to stage all changes to make a new commit as we did earlier. You can stage only one file or a combination of files.

You can even stage only sections of files (called *hunks*) with:
```sh
git add -p <file>   # start interactive session to stage hunks of <file>
```

---

##### <center>Interactive staging</center>
<br>

Try it on one of your files (this will be nicer if you made several modifications in different sections of your file).<br>
<br>
If {{%b%}}file2.txt{{%/b%}} is one of the files in which you made changes:

```sh
git add -p file2.txt
```

---

##### <center>Interactive staging</center>
<br>

After each hunk (fragment with modification), Git will ask you to type one of:

```
y	yes (stage this hunk)
n	no (don't stage this hunk)
a	all (stage this hunk and all subsequent ones in this file)
d	do not stage this hunk nor any of the remaining ones
s	split this hunk (if possible)
e	edit
?	print help
```

There are {{<a "https://git-scm.com/book/en/v2/Git-Tools-Interactive-Staging" "more options">}}, but these are the main ones to remember.

---

##### <center>Ignoring files</center>
<br>
There are files that you should not put under version control.

Output files (e.g. graphs, transformed data, etc.) which can be re-created simply by running a script are a great example.

But you don't want to leave them as untracked files (or you would never have a clean working tree, which is a problem). You need to tell Git to ignore them.

For this, you add them to a file that you create called {{<b>}}.gitignore{{</b>}}

---

##### <center><font color="#b30059">Ignore a file</font></center>
<br>

Create {{<b>}}file4.txt{{</b>}} and add it to {{<b>}}.gitignore{{</b>}}

```sh
touch file4.txt               # write something in it if you want
git status
echo file4.txt >> .gitignore
git status
```

---

###### <center><font color="#b30059">Feel free to keep playing in your repo with these commands until they become more familiar</font></center>
<br>
If you aren't sure about something, try it out. Experiment to understand how Git works.

You can also look up the {{<a "https://stackoverflow.com" "Git book](https://git-scm.com/book/en/v2) and countless great answers on [Stack Overflow">}}.

---

<img src="/img/git/git_icon_black.png" style="position: absolute; top: 15%; left: 52%; width: 2%;">

# <center><span style="font-variant: small-caps;">Questions?</span></center>
<br><br>
Bring all your questions to {{<a "https://westgrid-cli.netlify.app/school/git-08-recording.html" "tomorrow morning's live session">}}. See you there!
