+++
title = "git_basics"
outputs = ["Reveal"]
[logowgfix]
src = "/img/wg_white_removed_medium.png"
[logogit]
src = "/img/git/git_icon_black.png"
[reveal_hugo]
custom_theme = "mh.scss"
custom_theme_compile = true
+++

<br>
# <center><span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="300"></span> &nbsp;basics</center>

#### <center>WestGrid Summer School</center>

##### <center>Marie-Hélène Burle</center>

###### <center><training@westgrid.ca></center>

---

###### <div align="right" style="color: black">&emsp;&emsp;Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>3 components</center>
<br>
![](/img/git/diagrams/git01.png)

---

###### <div align="right" style="color: black">&emsp;&emsp;Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>3 components</center>
<br>
![](/img/git/diagrams/git02.png)

---

###### <div align="right" style="color: black">&emsp;&emsp;Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>What files are we talking about?</center>
<br>
![](/img/git/diagrams/git03.png)

---

###### <div align="right" style="color: black">&emsp;&emsp;Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>Now, let's consider the *state* of files</center>
<br>
![](/img/git/diagrams/git04.png)

---

###### <div align="right" style="color: black">&emsp;&emsp;Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>When nothing is modified in our working tree...</center>
<br>
![](/img/git/diagrams/git05.png)

---

###### <div align="right" style="color: black">&emsp;&emsp;Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>...we say that the working tree is "clean"</center>
<br>
![](/img/git/diagrams/git06.png)

---

###### <div align="right" style="color: black">&emsp;&emsp;Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>Let's create a new file</center>
<br>
![](/img/git/diagrams/git07.png)

---

###### <div align="right" style="color: black">&emsp;&emsp;Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>This is what happens when we run <span style="font-family: monospace; font-size: 1.2rem; padding: 0.4rem; box-shadow: 0px 0px 3px rgba(0,0,0,0.3); border-radius: 5%; background-color: #fff; color: #000000">git add file1</span></center>
<br>
![](/img/git/diagrams/git08.png)

---

###### <div align="right" style="color: black">&emsp;&emsp;Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>file1 is now ready to be committed</center>
<br>
![](/img/git/diagrams/git09.png)

---

###### <div align="right" style="color: black">&emsp;&emsp;Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>We take a "snapshot": <span style="font-family: monospace; font-size: 1.2rem; padding: 0.4rem; box-shadow: 0px 0px 3px rgba(0,0,0,0.3); border-radius: 5%; background-color: #fff; color: #000000">git commit -m "&lt;description of the commit&gt;"</span></center>
<br>
![](/img/git/diagrams/git10.png)

---

###### <div align="right" style="color: black">&emsp;&emsp;Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>We have archived file1 in its current state</center>
<br>
![](/img/git/diagrams/git11.png)

---

###### <div align="right" style="color: black">&emsp;&emsp;Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>Of course file1 is still in our working tree</center>
<br>
![](/img/git/diagrams/git12.png)

---

###### <div align="right" style="color: black">&emsp;&emsp;Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>but our working tree is clean since there is no new change</center>
<br>
![](/img/git/diagrams/git13.png)

---

###### <div align="right" style="color: black">&emsp;&emsp;Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>What happens if we make an edit to file1?</center>
<br>
![](/img/git/diagrams/git14.png)

---

###### <div align="right" style="color: black">&emsp;&emsp;Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>or if we create a new file?</center>
<br>
![](/img/git/diagrams/git15.png)

---

###### <div align="right" style="color: black">&emsp;&emsp;Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>The working tree is not clean anymore</center>
<br>
![](/img/git/diagrams/git15.png)

---

###### <div align="right" style="color: black">&emsp;&emsp;Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>and shows modified files</center>
<br>
![](/img/git/diagrams/git15.png)

---

###### <div align="right" style="color: black">&emsp;&emsp;Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>We can stage some or all of these new changes</center>
<br>
![](/img/git/diagrams/git15.png)

---

###### <div align="right" style="color: black">&emsp;&emsp;Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>For instance, let's stage the edit of file1: <span style="font-family: monospace; font-size: 1.2rem; padding: 0.4rem; box-shadow: 0px 0px 3px rgba(0,0,0,0.3); border-radius: 5%; background-color: #fff; color: #000000">git add file1</span></center>
<br>
![](/img/git/diagrams/git16.png)

---

###### <div align="right" style="color: black">&emsp;&emsp;Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>For instance, let's stage the edit of file1: <span style="font-family: monospace; font-size: 1.2rem; padding: 0.4rem; box-shadow: 0px 0px 3px rgba(0,0,0,0.3); border-radius: 5%; background-color: #fff; color: #000000">git add file1</span></center>
<br>
![](/img/git/diagrams/git17.png)

---

###### <div align="right" style="color: black">&emsp;&emsp;Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>Let's make a new edit to file1</center>
<br>
![](/img/git/diagrams/git18.png)

---

###### <div align="right" style="color: black">&emsp;&emsp;Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>We can pick and choose what to commit together</center>
<br>
![](/img/git/diagrams/git19.png)

---

###### <div align="right" style="color: black">&emsp;&emsp;Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>The staging area is where the next commit gets organized</center>
<br>
![](/img/git/diagrams/git20.png)

---

###### <div align="right" style="color: black">&emsp;&emsp;Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>This allows for a sensible history</center>
<br>
![](/img/git/diagrams/git21.png)

---

###### <div align="right" style="color: black">&emsp;&emsp;Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>instead of random mixed bags of changes</center>
<br>
![](/img/git/diagrams/git22.png)

---

###### <div align="right" style="color: black">&emsp;&emsp;Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>You don't have to stage entire files</center>
<br>
![](/img/git/diagrams/git23.png)

---

###### <div align="right" style="color: black">&emsp;&emsp;Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>You can select sections with <span style="font-family: monospace; font-size: 1.2rem; padding: 0.4rem; box-shadow: 0px 0px 3px rgba(0,0,0,0.3); border-radius: 5%; background-color: #fff; color: #000000">git add -p</span></center>
<br>
![](/img/git/diagrams/git24.png)

---

###### <div align="right" style="color: black">&emsp;&emsp;Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>A version of a file is only archived when it is committed</center>
<br>
![](/img/git/diagrams/git24.png)

---

###### <div align="right" style="color: black">&emsp;&emsp;Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>as information in the staging area can be overwritten</center>
<br>
![](/img/git/diagrams/git24.png)

---

###### <div align="right" style="color: black">&emsp;&emsp;Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>For instance, let's make a new edit in file1</center>
<br>
![](/img/git/diagrams/git25.png)

---

###### <div align="right" style="color: black">&emsp;&emsp;Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>and stage it with <span style="font-family: monospace; font-size: 1.2rem; padding: 0.4rem; box-shadow: 0px 0px 3px rgba(0,0,0,0.3); border-radius: 5%; background-color: #fff; color: #000000">git add file1</span></center>
<br>
![](/img/git/diagrams/git26.png)

---

###### <div align="right" style="color: black">&emsp;&emsp;Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>and stage it with <span style="font-family: monospace; font-size: 1.2rem; padding: 0.4rem; box-shadow: 0px 0px 3px rgba(0,0,0,0.3); border-radius: 5%; background-color: #fff; color: #000000">git add file1</span></center>
<br>
![](/img/git/diagrams/git27.png)

---

###### <div align="right" style="color: black">&emsp;&emsp;Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>Now let's make a new edit in the same section</center>
<br>
![](/img/git/diagrams/git28.png)

---

###### <div align="right" style="color: black">&emsp;&emsp;Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>and stage it with <span style="font-family: monospace; font-size: 1.2rem; padding: 0.4rem; box-shadow: 0px 0px 3px rgba(0,0,0,0.3); border-radius: 5%; background-color: #fff; color: #000000">git add file1</span></center>
<br>
![](/img/git/diagrams/git29.png)

---

###### <div align="right" style="color: black">&emsp;&emsp;Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>Our previous edit is lost</center>
<br>
![](/img/git/diagrams/git30.png)

---

###### <div align="right" style="color: black">&emsp;&emsp;Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>Once we commit (<span style="font-family: monospace; font-size: 1.2rem; padding: 0.4rem; box-shadow: 0px 0px 3px rgba(0,0,0,0.3); border-radius: 5%; background-color: #fff; color: #000000">git commit -m "&lt;message&gt;"</span>) however</center>
<br>
![](/img/git/diagrams/git31.png)

---

###### <div align="right" style="color: black">&emsp;&emsp;Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>that version enters the project history</center>
<br>
![](/img/git/diagrams/git32.png)

---

###### <div align="right" style="color: black">&emsp;&emsp;Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>This archiving is nice, but how to return to old versions?</center>
<br>
![](/img/git/diagrams/git32.png)

---

###### <div align="right" style="color: black">&emsp;&emsp;Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>We can't do it now because our changes would be lost</center>
<br>
![](/img/git/diagrams/git32.png)

---

###### <div align="right" style="color: black">&emsp;&emsp;Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>We need to commit or stash them first</center>
<br>
![](/img/git/diagrams/git32.png)

---

###### <div align="right" style="color: black">&emsp;&emsp;Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>Stashing puts changes out of the way temporarily</center>
<br>
![](/img/git/diagrams/git32.png)

---

###### <div align="right" style="color: black">&emsp;&emsp;Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>Let's keep it simple and commit our changes: <span style="font-family: monospace; font-size: 1.2rem; padding: 0.4rem; box-shadow: 0px 0px 3px rgba(0,0,0,0.3); border-radius: 5%; background-color: #fff; color: #000000">git add file2</span></center>
<br>
![](/img/git/diagrams/git33.png)

---

###### <div align="right" style="color: black">&emsp;&emsp;Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>Let's keep it simple and commit our changes: <span style="font-family: monospace; font-size: 1.2rem; padding: 0.4rem; box-shadow: 0px 0px 3px rgba(0,0,0,0.3); border-radius: 5%; background-color: #fff; color: #000000">git add file2</span></center>
<br>
![](/img/git/diagrams/git34.png)

---

###### <div align="right" style="color: black">&emsp;&emsp;Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>and <span style="font-family: monospace; font-size: 1.2rem; padding: 0.4rem; box-shadow: 0px 0px 3px rgba(0,0,0,0.3); border-radius: 5%; background-color: #fff; color: #000000">git commit -m "&lt;message&gt;"</span></center>
<br>
![](/img/git/diagrams/git35.png)

---

###### <div align="right" style="color: black">&emsp;&emsp;Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>We now have a clean working tree</center>
<br>
![](/img/git/diagrams/git36.png)

---

###### <div align="right" style="color: black">&emsp;&emsp;Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>so we can check out an old version</center>
<br>
![](/img/git/diagrams/git36.png)

---

###### <div align="right" style="color: black">&emsp;&emsp;Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>We do this with: <span style="font-family: monospace; font-size: 1.2rem; padding: 0.4rem; box-shadow: 0px 0px 3px rgba(0,0,0,0.3); border-radius: 5%; background-color: #fff; color: #000000">git checkout &lt;commit hash&gt;</span></center>
<br>
![](/img/git/diagrams/git37.png)

---

###### <div align="right" style="color: black">&emsp;&emsp;Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>The hash of a commit is a unique string that identifies it</center>
<br>
![](/img/git/diagrams/git37.png)

---

###### <div align="right" style="color: black">&emsp;&emsp;Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>Now look at our working tree</center>
<br>
![](/img/git/diagrams/git37.png)

---

###### <div align="right" style="color: black">&emsp;&emsp;Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>It currently holds file1 with its edits and file2</center>
<br>
![](/img/git/diagrams/git37.png)

---

###### <div align="right" style="color: black">&emsp;&emsp;Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>but once we have checked out our second commit</center>
<br>
![](/img/git/diagrams/git38.png)

---

###### <div align="right" style="color: black">&emsp;&emsp;Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>our working tree is back to that point in history</center>
<br>
![](/img/git/diagrams/git38.png)

---

<img src="/img/git/git_icon_black.png" style="position: absolute; top: 25%; left: 51.7%; width: 2%;">
# <center><span style="font-variant: small-caps;">Questions?</span></center>
