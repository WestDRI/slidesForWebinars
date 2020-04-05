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

###### <div align="right" style="color: black">Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>3 components</center>
<br>
![](/img/git/diagrams/git01.png)

---

###### <div align="right" style="color: black">Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>3 components</center>
<br>
![](/img/git/diagrams/git02.png)

---

###### <div align="right" style="color: black">Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>What files are we talking about?</center>
<br>
![](/img/git/diagrams/git03.png)

---

###### <div align="right" style="color: black">Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>Now, let's consider the *state* of files</center>
<br>
![](/img/git/diagrams/git04.png)

---

###### <div align="right" style="color: black">Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>When nothing is modified in the working tree...</center>
<br>
![](/img/git/diagrams/git05.png)

---

###### <div align="right" style="color: black">Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>...we say that the working tree is "clean"</center>
<br>
![](/img/git/diagrams/git06.png)

---

###### <div align="right" style="color: black">Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>Let's create a new file</center>
<br>
![](/img/git/diagrams/git07.png)

---

###### <div align="right" style="color: black">Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>This is what happens when we run <span style="font-family: monospace; font-size: 1.2rem; padding: 0.4rem; box-shadow: 0px 0px 3px rgba(0,0,0,0.3); border-radius: 5%; background-color: #fff; color: #000000">git add file1</span></center>
<br>
![](/img/git/diagrams/git08.png)

---

###### <div align="right" style="color: black">Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center><span style="font-family: monospace; font-size: 1.2rem; padding: 0.4rem; border-radius: 5%; border: 0.5pt solid #d9d9d9; box-shadow: 0px 0px 2.5px rgba(0,0,0,0.3); color: #000000">file1</span> is now ready to be committed</center>
<br>
![](/img/git/diagrams/git09.png)

---

###### <div align="right" style="color: black">Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>We take a "snapshot": <span style="font-family: monospace; font-size: 1.2rem; padding: 0.4rem; box-shadow: 0px 0px 3px rgba(0,0,0,0.3); border-radius: 5%; background-color: #fff; color: #000000">git commit -m "&lt;description of the commit&gt;"</span></center>
<br>
![](/img/git/diagrams/git10.png)

---

###### <div align="right" style="color: black">Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>We have archived <span style="font-family: monospace; font-size: 1.2rem; padding: 0.4rem; border-radius: 5%; border: 0.5pt solid #d9d9d9; box-shadow: 0px 0px 2.5px rgba(0,0,0,0.3); color: #000000">file1</span> in that particular version</center>
<br>
![](/img/git/diagrams/git11.png)

---

###### <div align="right" style="color: black">Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>Of course <span style="font-family: monospace; font-size: 1.2rem; padding: 0.4rem; border-radius: 5%; border: 0.5pt solid #d9d9d9; box-shadow: 0px 0px 2.5px rgba(0,0,0,0.3); color: #000000">file1</span> is still in our working tree</center>
<br>
![](/img/git/diagrams/git12.png)

---

###### <div align="right" style="color: black">Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>but our working tree is clean since there is no new change</center>
<br>
![](/img/git/diagrams/git13.png)

---

###### <div align="right" style="color: black">Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>What happens if we make an edit to <span style="font-family: monospace; font-size: 1.2rem; padding: 0.4rem; border-radius: 5%; border: 0.5pt solid #d9d9d9; box-shadow: 0px 0px 2.5px rgba(0,0,0,0.3); color: #000000">file1</span>?</center>
<br>
![](/img/git/diagrams/git14.png)

---

###### <div align="right" style="color: black">Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>or if we create a new file?</center>
<br>
![](/img/git/diagrams/git15.png)

---

###### <div align="right" style="color: black">Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>The working tree is not clean anymore</center>
<br>
![](/img/git/diagrams/git15.png)

---

###### <div align="right" style="color: black">Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>and shows modified files</center>
<br>
![](/img/git/diagrams/git15.png)

---

###### <div align="right" style="color: black">Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>We can stage some or all of these new changes</center>
<br>
![](/img/git/diagrams/git15.png)

---

###### <div align="right" style="color: black">Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>For instance, let's stage the edit of <span style="font-family: monospace; font-size: 1.2rem; padding: 0.4rem; border-radius: 5%; border: 0.5pt solid #d9d9d9; box-shadow: 0px 0px 2.5px rgba(0,0,0,0.3); color: #000000">file1</span>: <span style="font-family: monospace; font-size: 1.2rem; padding: 0.4rem; box-shadow: 0px 0px 3px rgba(0,0,0,0.3); border-radius: 5%; background-color: #fff; color: #000000">git add file1</span></center>
<br>
![](/img/git/diagrams/git16.png)

---

###### <div align="right" style="color: black">Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>For instance, let's stage the edit of <span style="font-family: monospace; font-size: 1.2rem; padding: 0.4rem; border-radius: 5%; border: 0.5pt solid #d9d9d9; box-shadow: 0px 0px 2.5px rgba(0,0,0,0.3); color: #000000">file1</span>: <span style="font-family: monospace; font-size: 1.2rem; padding: 0.4rem; box-shadow: 0px 0px 3px rgba(0,0,0,0.3); border-radius: 5%; background-color: #fff; color: #000000">git add file1</span></center>
<br>
![](/img/git/diagrams/git17.png)

---

###### <div align="right" style="color: black">Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>Let's now make a new edit to <span style="font-family: monospace; font-size: 1.2rem; padding: 0.4rem; border-radius: 5%; border: 0.5pt solid #d9d9d9; box-shadow: 0px 0px 2.5px rgba(0,0,0,0.3); color: #000000">file1</span></center>
<br>
![](/img/git/diagrams/git18.png)

---

###### <div align="right" style="color: black">Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>As you can see, <span style="font-family: monospace; font-size: 1.2rem; padding: 0.4rem; border-radius: 5%; border: 0.5pt solid #d9d9d9; box-shadow: 0px 0px 2.5px rgba(0,0,0,0.3); color: #000000">file1</span> now shows up in 2 states</center>
<br>
![](/img/git/diagrams/git18.png)

---

###### <div align="right" style="color: black">Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>We don't have to stage an entire file</center>
<br>
![](/img/git/diagrams/git19.png)

---

###### <div align="right" style="color: black">Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>We can select hunks with <span style="font-family: monospace; font-size: 1.2rem; padding: 0.4rem; box-shadow: 0px 0px 3px rgba(0,0,0,0.3); border-radius: 5%; background-color: #fff; color: #000000">git add -p file1</span></center>
<br>
![](/img/git/diagrams/git19.png)

---

###### <div align="right" style="color: black">Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>The staging area is where the next commit gets organized</center>
<br>
![](/img/git/diagrams/git20.png)

---

###### <div align="right" style="color: black">Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>We can pick and choose what to commit together</center>
<br>
![](/img/git/diagrams/git20.png)

---

###### <div align="right" style="color: black">Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>This allows to archive snapshots with key sets of changes</center>
<br>
![](/img/git/diagrams/git21.png)

---

###### <div align="right" style="color: black">Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>instead of random mixed bags of changes</center>
<br>
![](/img/git/diagrams/git22.png)

---

###### <div align="right" style="color: black">Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>A version of a file is only archived once it is committed</center>
<br>
![](/img/git/diagrams/git22.png)

---

###### <div align="right" style="color: black">Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>as information in the staging area can be overwritten</center>
<br>
![](/img/git/diagrams/git22.png)

---

###### <div align="right" style="color: black">Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>For instance, let's make a new edit in <span style="font-family: monospace; font-size: 1.2rem; padding: 0.4rem; border-radius: 5%; border: 0.5pt solid #d9d9d9; box-shadow: 0px 0px 2.5px rgba(0,0,0,0.3); color: #000000">file1</span></center>
<br>
![](/img/git/diagrams/git23.png)

---

###### <div align="right" style="color: black">Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>and stage it with <span style="font-family: monospace; font-size: 1.2rem; padding: 0.4rem; box-shadow: 0px 0px 3px rgba(0,0,0,0.3); border-radius: 5%; background-color: #fff; color: #000000">git add -p file1</span></center>
<br>
![](/img/git/diagrams/git24.png)

---

###### <div align="right" style="color: black">Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>and stage it with <span style="font-family: monospace; font-size: 1.2rem; padding: 0.4rem; box-shadow: 0px 0px 3px rgba(0,0,0,0.3); border-radius: 5%; background-color: #fff; color: #000000">git add -p file1</span></center>
<br>
![](/img/git/diagrams/git25.png)

---

###### <div align="right" style="color: black">Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>Now let's make a new edit in the same section</center>
<br>
![](/img/git/diagrams/git26.png)

---

###### <div align="right" style="color: black">Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>and stage it with <span style="font-family: monospace; font-size: 1.2rem; padding: 0.4rem; box-shadow: 0px 0px 3px rgba(0,0,0,0.3); border-radius: 5%; background-color: #fff; color: #000000">git add -p file1</span></center>
<br>
![](/img/git/diagrams/git27.png)

---

###### <div align="right" style="color: black">Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>Our previous version of <span style="font-family: monospace; font-size: 1.2rem; padding: 0.4rem; border-radius: 5%; border: 0.5pt solid #d9d9d9; box-shadow: 0px 0px 2.5px rgba(0,0,0,0.3); color: #000000">file1</span> (with <span style="font-family: monospace; font-size: 1.2rem; padding: 0.4rem; border-radius: 5%; border: 0.5pt solid #d9d9d9; box-shadow: 0px 0px 2.5px rgba(0,0,0,0.3); color: #000000">edit3</span>) is lost</center>
<br>
![](/img/git/diagrams/git28.png)

---

###### <div align="right" style="color: black">Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>Once we commit (<span style="font-family: monospace; font-size: 1.2rem; padding: 0.4rem; box-shadow: 0px 0px 3px rgba(0,0,0,0.3); border-radius: 5%; background-color: #fff; color: #000000">git commit -m "&lt;message&gt;"</span>) however</center>
<br>
![](/img/git/diagrams/git29.png)

---

###### <div align="right" style="color: black">Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>that version enters the project history</center>
<br>
![](/img/git/diagrams/git30.png)

---

###### <div align="right" style="color: black">Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>Not all files should be put under version control</center>
<br>
![](/img/git/diagrams/git30.png)

---

###### <div align="right" style="color: black">Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>Source code and scripts should be version controlled</center>
<br>
![](/img/git/diagrams/git30.png)

---

###### <div align="right" style="color: black">Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>But outputs shouldn't as they can be reproduced easily</center>
<br>
![](/img/git/diagrams/git30.png)

---

###### <div align="right" style="color: black">Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>Imagine that <span style="font-family: monospace; font-size: 1.2rem; padding: 0.4rem; border-radius: 5%; border: 0.5pt solid #d9d9d9; box-shadow: 0px 0px 2.5px rgba(0,0,0,0.3); color: #000000">file2</span> is one such file</center>
<br>
![](/img/git/diagrams/git30.png)

---

###### <div align="right" style="color: black">Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>We don't want to have it clutter our working tree</center>
<br>
![](/img/git/diagrams/git30.png)

---

###### <div align="right" style="color: black">Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>So we tell Git to ignore it by adding it to <span style="font-family: monospace; font-size: 1.2rem; padding: 0.4rem; border-radius: 5%; border: 0.5pt solid #d9d9d9; box-shadow: 0px 0px 2.5px rgba(0,0,0,0.3); color: #000000">.gitignore</span></center>
<br>
![](/img/git/diagrams/git30.png)

---

###### <div align="right" style="color: black">Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>This can be done in the terminal with <span style="font-family: monospace; font-size: 1.2rem; padding: 0.4rem; box-shadow: 0px 0px 3px rgba(0,0,0,0.3); border-radius: 5%; background-color: #fff; color: #000000">echo file2 > .gitignore</span></center>
<br>
![](/img/git/diagrams/git31.png)

---

###### <div align="right" style="color: black">Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center><span style="font-family: monospace; font-size: 1.2rem; padding: 0.4rem; border-radius: 5%; border: 0.5pt solid #d9d9d9; box-shadow: 0px 0px 2.5px rgba(0,0,0,0.3); color: #000000">file2</span> was not deleted, but it has become invisible to Git</center>
<br>
![](/img/git/diagrams/git31.png)

---

###### <div align="right" style="color: black">Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>In the meantime, we now have a new file: <span style="font-family: monospace; font-size: 1.2rem; padding: 0.4rem; border-radius: 5%; border: 0.5pt solid #d9d9d9; box-shadow: 0px 0px 2.5px rgba(0,0,0,0.3); color: #000000">.gitignore</span></center>
<br>
![](/img/git/diagrams/git31.png)

---

###### <div align="right" style="color: black">Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>You can treat it like any other file: stage it and commit it</center>
<br>
![](/img/git/diagrams/git31.png)

---

###### <div align="right" style="color: black">Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>This archiving is nice, but how to return to old versions?</center>
<br>
![](/img/git/diagrams/git31.png)

---

###### <div align="right" style="color: black">Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>We can't do so now as we have uncommitted changes</center>
<br>
![](/img/git/diagrams/git31.png)

---

###### <div align="right" style="color: black">Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>We need to commit or stash them first</center>
<br>
![](/img/git/diagrams/git31.png)


---

###### <div align="right" style="color: black">Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>Stashing puts changes out of the way temporarily</center>
<br>
![](/img/git/diagrams/git31.png)

---

###### <div align="right" style="color: black">Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>We stash with <span style="font-family: monospace; font-size: 1.2rem; padding: 0.4rem; box-shadow: 0px 0px 3px rgba(0,0,0,0.3); border-radius: 5%; background-color: #fff; color: #000000">git stash push</span></center>
<br>
![](/img/git/diagrams/git32.png)

---

###### <div align="right" style="color: black">Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>Our working tree is now clean</center>
<br>
![](/img/git/diagrams/git34.png)

---

###### <div align="right" style="color: black">Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>So we can check out an old version of our repo</center>
<br>
![](/img/git/diagrams/git34.png)

---

###### <div align="right" style="color: black">Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>Let's return to our second commit</center>
<br>
![](/img/git/diagrams/git34.png)

---

###### <div align="right" style="color: black">Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>We do this with: <span style="font-family: monospace; font-size: 1.2rem; padding: 0.4rem; box-shadow: 0px 0px 3px rgba(0,0,0,0.3); border-radius: 5%; background-color: #fff; color: #000000">git checkout &lt;commit hash 2<sup>nd</sup> commit&gt;</span></center>
<br>
![](/img/git/diagrams/git33.png)

---

###### <div align="right" style="color: black">Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>The hash of a commit is a unique string that identifies it</center>
<br>
![](/img/git/diagrams/git33.png)

---

###### <div align="right" style="color: black">Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>Now look at our working tree</center>
<br>
![](/img/git/diagrams/git33.png)

---

###### <div align="right" style="color: black">Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>**B A M!**</center>
<br>
![](/img/git/diagrams/git34.png)

---

###### <div align="right" style="color: black">Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>Once we have checked out our second commit</center>
<br>
![](/img/git/diagrams/git34.png)

---

###### <div align="right" style="color: black">Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>our working tree is back to that point in history</center>
<br>
![](/img/git/diagrams/git34.png)

---

###### <div align="right" style="color: black">Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>If we want to go back to the latest version of our project</center>
<br>
![](/img/git/diagrams/git34.png)

---

###### <div align="right" style="color: black">Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>all we have to do is to checkout our latest commit</center>
<br>
![](/img/git/diagrams/git35.png)

---

###### <div align="right" style="color: black">Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>with <span style="font-family: monospace; font-size: 1.2rem; padding: 0.4rem; box-shadow: 0px 0px 3px rgba(0,0,0,0.3); border-radius: 5%; background-color: #fff; color: #000000">git checkout &lt;commit hash 3<sup>rd</sup> commit&gt;</span></center>
<br>
![](/img/git/diagrams/git35.png)

---

###### <div align="right" style="color: black">Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>*Et voilà!*</center>
<br>
![](/img/git/diagrams/git36.png)

---

###### <div align="right" style="color: black">Understanding <span style="vertical-align: middle"><img src="/img/git/git_logo.png" alt="" height="" width="60"></span></div>
<br>
#### <center>Finally, to re-apply our stash, we run <span style="font-family: monospace; font-size: 1.2rem; padding: 0.4rem; box-shadow: 0px 0px 3px rgba(0,0,0,0.3); border-radius: 5%; background-color: #fff; color: #000000">git stash pop</span></center>
<br>
![](/img/git/diagrams/git31.png)
