+++
title = "git_recording"
outputs = ["Reveal"]
[logowg]
src = "/img/wg_white_removed_medium.png"
[logogithalfpage]
src = "/img/git/git_icon_black.png"
[reveal_hugo]
custom_theme = "mh.scss"
custom_theme_compile = true
+++

<br>
# <center><span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="300"></span> &nbsp;recording history</center>

#### <center>WestGrid Summer School</center>

##### <center>Marie-Hélène Burle</center>

###### <center><training@westgrid.ca></center>

---

# <center><font color="#b30059">This is an interactive session.<br>Make sure to follow along!</font></center>

---

#### <center>Remember our 3 components from the previous lesson?</center>
<br>
![](/img/git/diagrams/git01.png)

---

#### <center>How do we get to this?</center>
<br>
![](/img/git/diagrams/git01.png)

---

### <center>Let's try it!</center>
<br>
First, we need to create a project: this means creating a directory.

{{% fragment %}}
Let's call it {{<b>}}git_lesson{{</b>}}.

<span style="font-size: 1.7rem; color: #e67300">*Make sure never to use spaces when you use Git. It will make your life a lot easier.*</span>
{{% /fragment %}}

---

### <center>Open a terminal</center>
<br>
<b>Windows:</b> &emsp;&nbsp;Git BASH <br>

<b>MacOS:</b> &emsp;&emsp;Terminal <br>

<b>Linux:</b> &emsp;&emsp;&ensp;&nbsp;any terminal emulator

---

### <center>Create the root of the project</center>
<br>
```sh
cd /path/where/you/want/your/repository
mkdir git_lesson
```
<br>
You can place your project wherever you want on your computer. Simply make sure that you know where it is and that it is somewhere sensible.

{{% fragment %}}
<br>
All files for this project will need to be in this directory: it is the **root** of the project.

Of course, you can create subdirectories in it to organize your files.
{{% /fragment %}}

---

### <center>Navigate to the directory in your usual way</center>
<br>
This may be with Windows explorer or Finder.

{{% fragment %}}
Realize that there is nothing special about this directory.
{{% /fragment %}}

---

### <center>Turning a project into a repository</center>

To put our project under version control, we initiate the repository.
<br>
<br>
##### Make sure that you are in the root of the project!
```sh
cd git_lesson
pwd         # this should return the path to git_lesson
```

{{% fragment %}}
<br>
The directory is empty:

```sh
ls -a	    # this should not return any file or directory
```
{{% /fragment %}}

---

### <center>Initiate the repository</center>
<br>
```sh
git init
```
{{% fragment %}}
<br>
You now have in your root folder a very important directory: {{<b>}}.git{{</b>}}.

```sh
ls -a	     # make sure that you can see the .git directory
```
<br>
{{% /fragment %}}

{{% fragment %}}
*Note: we need the {{<c>}}-a{{</c>}} flag because files and directories starting with a dot are hidden.*
{{% /fragment %}}

---

### <center>Go see it with your usual tool</center>
<br>

Go back to your directory with Windows explorer or Finder to demystify it.

If you don't see it, make sure to change the options to see hidden files.

---

#### <center>Let's have a look at what is inside</center>

---

#### <center>So, what is what?</center>
<br>
![](/img/git/diagrams/git01.png)

---

#### <center>So, what is what?</center>
<br>
![](/img/git/diagrams/git02.png)

---

#### <center>So, what is what?</center>
<br>
![](/img/git/diagrams/git03.png)

---

### <center>Status of a repository</center>
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

### <center><font color="#b30059">Let's create 3 files in our new repository</font></center>
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

### <center><font color="#b30059">Add content to your files</font></center>

Add several paragraphs in each of your 3 files (from the command line or in a manner more familiar to you).<br>
<br>
You can type random words, copy and paste a few paragraphs from a page web, or use [Lorem ipsum](https://en.wikipedia.org/wiki/Lorem_ipsum)... it doesn't matter what the content is.<br>
<br>
From the command line, you can use, for instance:
```sh
echo "your text" > file1.txt
```
<br>
If your text is long, pasting it in the terminal can be weirdly slow,<br>
so you can also run:
```sh
nano file1.txt
```
paste your text, save, and close nano <br>
(or whatever text editor you like to use).

---

### <center><font color="#b30059">Inspect your repository now</font></center>
<br>

What has changed?

---

### <center>Getting more information on changes</center>
<br>
What if you want to see the actual changes <br>
(and not just the names of the files which changed)?<br>

{{% fragment %}}
<br>
The command for this is:
```sh
git diff
```
{{% /fragment %}}

---

### <center>Getting more information on changes</center>
<br>

By default, {{<c>}}git diff{{</c>}} uses a pager (e.g. {{<c>}}less{{</c>}}).<br>
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

### <center>Staging</center>
<br>
These are the commands to stage all modifications in the working tree, a file, or part of a file:
```sh
git add .           # stage all changes
git add <file>      # stage <file>
git add -p <file>   # start interactive session to stage hunks of <file>
```

---

### <center>Ignoring files</center>
<br>
And to tell Git to ignore files, we add them to the {{<b>}}.gitignore{{</b>}} file.

---

### <center><font color="#b30059">Ignore and stage</font></center>
<br>

Add {{<b>}}file1.txt{{</b>}} to {{<b>}}.gitignore{{</b>}}.<br>
<br>
Then stage {{<b>}}file2.txt{{</b>}}, {{<b>}}file3.txt{{</b>}}, and {{<b>}}.gitignore{{</b>}}.<br><br>
*Note: {{<b>}}.gitignore{{</b>}} does not exist yet. You will create it.*

---

### <center><font color="#b30059">Inspect your repository again</font></center>
<br>
What do you see now?

---

### <center><font color="#b30059">What do you get when you run {{<c>}}git diff{{</c>}}?</font></center>
<br>

{{% fragment %}}
To see the changes in files that have been staged, you need to run:<br>
```sh
git diff --staged
```
{{% /fragment %}}

{{% fragment %}}
<br>
<font color="#b30059">Git it a try.</font>
{{% /fragment %}}

---

### <center>Committing</center>
<br>
You create a commit with {{<c>}}git commit{{</c>}}. But Git will not allow a commit without a message describing it.
<br>
So if you only run the above command, Git will open a text editor in which you can enter your commit message.<br>
<br>
If you want to commit without using a text editor, you must use the {{<c>}}-m{{</c>}} flag and a message within the command:
<br>
```sh
git commit -m "Your commit message"
```

---

### <center>Commit messages</center>
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
You can also list what files are in this initial commit.

---

### <center>Commit messages good practice</center>
<br>
- Use the present tense<br><br>
- The first line is a summary of the commit and is less than 50 characters long <br><br>
- Leave a blank line below <br><br>
- Add the body of your commit message below that

---

### <center><font color="#b30059">Make your first commit</font></center>

---

### <center>SHA-1 checksum</center>
<br>

Each commit is identified by a unique 40-character SHA-1 checksum. People usually refer to it as a "hash".<br>
<br>
The short form of a hash only contains the first 7 characters, which is generally sufficient to identify a commit.<br>
<br>
After you committed, Git gave you the short form of the hash of your first commit.

---

### <center><font color="#b30059">Inspect your repository again</font></center>
<br>
What do you see now?

---

<img src="/img/git/git_icon_black.png" style="position: absolute; top: 25%; left: 51.7%; width: 2%;">

# <center><span style="font-variant: small-caps;">Questions?</span></center>
