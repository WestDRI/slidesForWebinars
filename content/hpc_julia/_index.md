+++
title = "hpc_julia"
outputs = ["Reveal"]
[logowg]
src = "/img/wg_white_removed_medium.png"
alt = "WestGrid logo"
[logocc]
src = "/img/cc_regional_partner_brown_large.png"
alt = "Compute Canada logo"
[reveal_hugo]
custom_theme = "mh.scss"
custom_theme_compile = true
+++

<br>
<br>
<br>

<center><img src="/img/jl_title.png" width="520"></center>

#### <center>Marie-Hélène Burle</center>

##### <center><marie.burle@westgrid.ca></center>

###### <center>*March 04, 2020*</center>

---

### <center>Brief history</center>
<br>

Started in 2009 by Jeff Bezanson, [Stefan Karpinski](https://en.wikipedia.org/wiki/Stefan_Karpinski), [Viral B. Shah](https://en.wikipedia.org/wiki/Viral_B._Shah), and [Alan Edelman](https://en.wikipedia.org/wiki/Alan_Edelman)

Launched in 2012 as free and open source software

Version 1.0 released in 2018

---

### <center>Why another language?</center>
<br>

Computer languages mostly fall into two categories:

**Compiled languages**

**Interpreted languages**

---

### <center>Compiled languages</center>
<br>
![](/img/compiled_language.png)

---

### <center>Interpreted languages</center>
<br>
![](/img/interpreted_language.png)

---

### <center>JIT compilation</center>
<br>

[Just-in-time compilation](https://en.wikipedia.org/wiki/Just-in-time_compilation) (JIT) based on [LLVM](https://en.wikipedia.org/wiki/LLVM)

Source code compiled at run time

---

### <center>Multiple dispatch</center>
<br>

Built-in [multiple dispatch](https://en.wikipedia.org/wiki/Multiple_dispatch): functions apply different methods at run time based on the type of the operands

<br>
Optional type declaration

---

### <center>Documentation</center>
<br>

Julia [website](https://julialang.org/)

The official Julia [manual](https://docs.julialang.org/en/v1/)

Online [training](https://julialang.org/learning/) material

The Julia [YouTube](https://www.youtube.com/user/JuliaLanguage) channel

The Julia [Wikibook](https://en.wikibooks.org/wiki/Introducing_Julia)

A [blog](https://www.juliabloggers.com/) aggregator for Julia

---

### <center>Getting help</center>

Discourse [forum](https://discourse.julialang.org/)

[[julia] ](https://stackoverflow.com/tags/julia)tag on Stack Overflow

[Slack](https://app.slack.com/client/T68168MUP/C67910KEH) team (you need to agree to the community code of conduct at slackinvite.julialang.org to receive an invitation)

[#julialang](https://twitter.com/search?q=%23julialang) hashtag on Twitter

[Subreddit](https://www.reddit.com/r/Julia/)

[Gitter](https://gitter.im/JuliaLang/julia) channel

[#julia](https://webchat.freenode.net/#julia) IRC channel on Freenode

---

### <center>Nice ways to run Julia</center>

#### Emacs

[julia-emacs](https://github.com/JuliaEditorSupport/julia-emacs) with [julia-repl](https://github.com/tpapp/julia-repl)<br>
[ESS](https://github.com/emacs-ess/ESS)<br>
[EIN](http://millejoh.github.io/emacs-ipython-notebook/) to access Jupyter notebooks from Emacs

#### Juno

[A Julia IDE](https://junolab.org/) built on [Atom](https://atom.io/)

#### Jupyter

[Project Jupyter](https://jupyter.org/) has a Julia kernel

---

### <center>REPL</center>
<br>

<center>![](/img/julia_repl.png)</center>

---

### <center>REPL keybindings</center>

```
C-c		cancel
C-d		quit
C-l		clear console

C-u		kill from the start of line
C-k		kill until the end of line

C-a		go to start of line
C-e		go to end of line

C-f		move forward one character
C-b		move backward one character

M-f		move forward one word
M-b		move backward one word

C-d		delete forward one character
C-h		delete backward one character

M-d		delete forward one word
M-Backspace	delete backward one word

C-p		previous command
C-n		next command

C-r		backward search
C-s		forward search
```

---

### <center>Where to find packages?</center>
<br>

<center>Easy [search engine](https://pkg.julialang.org/docs/) for registered packages (all on GitHub)</center>

---

### <center>Managing packages in <span style="font-family: monospace; font-size: 1.8rem; padding: 0.4rem; box-shadow: 0px 0px 3px rgba(0,0,0,0.3); border-radius: 5%; background-color: #fff; color: #000000">Pkg</span> mode</center>
<br>

```jl
add <package>		install a package
rm  <package>		uninstall a package
up  <package>		upgrade a package

st			        check which packages are installed
up			        upgrade all packages
```
<br>
By default, installed in <span style="font-family: monospace; font-size: 1.2rem; padding: 0.4rem; box-shadow: 0px 0px 3px rgba(0,0,0,0.3); border-radius: 5%; background-color: #fff; color: #000000">~/.julia</span>

---

### <center>Loading a package</center>
<br>

```jl
using <package>
```

---

### <center>Data types</center>
<br>

```jl
typeof(2)
typeof(2.0)
typeof("hello")
typeof(true)
```

---

### <center>Indexing</center>
<br>

Indexing starts at 1, not 0
<br><br>

```jl
a = [1 2; 3 4]
a[1, 1]
a[1, :]
```

---

### <center>For loops</center>
<br>

```jl
for i in 1:10
    println(i)
end


for i in 1:3, j = 1:2
    println(i * j)
end
```

---

### <center>Conditionals</center>
<br>

```jl
a = 2
b = 2.0

if a == b
    println("It's true")
else
    println("It's false")
end

# Terse format
a == b ? println("It's true") : println("It's false")
```

---

### <center>Functions</center>

```jl
function addTwo(a)
    a + 2
end

addTwo(3)

# In terse format
addtwo = a -> a + 2

# With default argument
function name(a = "unknown")
    println("My name is $a.")
end

name("Julia")
name()
```

---

### <center>Plotting</center>
<br>
Fun: plots in the command line!
<br>

```jl
using UnicodePlots
histogram(randn(1000), nbins=40)
```
<br>
This can be useful in remote sessions

---

### <center>Plotting</center>
<br>
Nicer looking plots
<br>

```jl
using Plots, Distributions, StatsPlots
gr() # Using the GR framework as backend
x = 1:10; y = rand(10, 2);
p1 = histogram(randn(1000), nbins=40)
p2 = plot(Normal(0, 1))
p3 = scatter(x, y)
p4 = plot(x, y)
plot(p1, p2, p3, p4)
```
<br>
[Nice demos](http://docs.juliaplots.org/latest/) on the <span style="font-family: monospace; font-size: 1.2rem; padding: 0.4rem; box-shadow: 0px 0px 3px rgba(0,0,0,0.3); border-radius: 5%; background-color: #fff; color: #000000">Plots</span> package site

---

# <center>Parallel programming</center>

---

### <center>Launching Julia on multiple threads</center>
<br>
Set the environment variable (in a terminal)

```sh
export JULIA_NUM_THREADS=n
```
<br>
Or launch a Julia session with it (in a terminal)

```sh
export JULIA_NUM_THREADS=n julia
```
<br>
See how many threads are used in a Julia session (in the Julia REPL)

```jl
Threads.nthreads()
```

---

### <center>When is parallelism happening?</center>
<br>
**Non parallel code**

```jl
for i = 1:10
    println("Iteration $i ran on thread $(Threads.threadid())")
end
```
<br>
**Parallel code**

```jl
Threads.@threads for i = 1:10
    println("Iteration $i ran on thread $(Threads.threadid())")
end
```

---

### <center>Effect on timing</center>
<br>
Let's do a simple loop with 10,000,000 iterations

**Non parallel code**

```jl
@time for i = 1:10000000
    i ^ i
end
```
<br>
**Parallel code**

```jl
@time Threads.@threads for i = 1:10000000
    i ^ i
end
```

---

# <center>Let's move on to the cluster</center>

---

### <center>Loading the Julia module</center>
<br>

```sh
# Look for available julia modules
module spider julia

# See modules required to load julia 1.3
module spider julia/1.3.0

# Load required module and julia
module load gcc/7.3.0 julia/1.3.0
```

---

### <center>Job script</center>
<br>

```sh
#!/bin/bash
#SBATCH --job-name=julialoop		# job name
#SBATCH --time=00:01:00				# max walltime 1 min
#SBATCH --cpus-per-task=32   		# number of cores
#SBATCH --mem=1000					# max memory
#SBATCH --output=julialoop.out		# file name for the output
#SBATCH --error=julialoop.err		# file name for errors

echo Running NON parallel loop on $SLURM_CPUS_PER_TASK core
JULIA_NUM_THREADS=$SLURM_CPUS_PER_TASK julia loop.jl
echo Running parallel loop on $SLURM_CPUS_PER_TASK core
JULIA_NUM_THREADS=$SLURM_CPUS_PER_TASK julia ploop.jl
```

---

### <center>Running the job</center>
<br>

```sh
sbatch job_julialoop.sh
```
<br>

### <center>Checking the job status</center>
<br>

```sh
sq
```

PD: pending <br>
R: running






