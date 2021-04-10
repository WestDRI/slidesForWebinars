+++
title = "jl_variables_types"
outputs = ["Reveal"]
[logowg]
src = "/img/wg_white_removed_medium.png"
[logojl]
src = "/img/jl/jl_dots.png"
[backlink]
href = "https://westgrid-julia.netlify.app/summerschool2020/jl-08-var/"
txt = "Back to Course Page"
[reveal_hugo]
custom_theme = "mh.scss"
custom_theme_compile = true
+++

# <center>Variables and types in <span style="vertical-align: middle"><img src="/img/ml/julia.png" alt="" height="" width="200"></span></center>
<br>
#### <center>Marie-Hélène Burle</center>

###### <center><training@westgrid.ca></center>

###### <center>*June 02, 2020*</center>

---

#### <center>Our first script</center>
<br>

In this course, we will use Covid-19 data to become familiar with Julia's syntax and functioning.

In this lesson, we will write our first Julia script to load and transform data.<br>
As we do so, we will discuss variables and types in Julia.

{{<challenge>}}
Create a file (name and location of your choice) with the extension {{%b%}}.jl{{%/b%}}
{{</challenge>}}

Julia scripts are text files and—by convention—have that extension.

---

#### <center>Load packages</center>
<br>
First, we need to load some packages.<br>
This will take some time as Julia will pre-compile newly installed or updated packages. Next time you load these packages, it will go a lot faster.
<br><br>
```julia
using CSV
using DataFrames
using Dates
using JLD
```
<br>
{{%b%}}Dates{{%/b%}} is a package from the standard Julia library (it was installed when you installed Julia).<br>
The other packages are packages that {{<a "https://westgrid-julia.netlify.app/school/jl-05-pkg.html" "you should have installed">}}.

---

## <center>Variables</center>
<br>

In Julia, variables are names bound to a values.

These names are extremely flexible and can use any Unicode character.

The only rules are:

- they must begin with a letter or with an underscore (a few of the Unicode characters are also accepted)
- they cannot be the names of built-in statements such as {{<c>}}if{{</c>}}, {{<c>}}do{{</c>}}, {{<c>}}try{{</c>}}, {{<c>}}else{{</c>}}

---

## <center>Variables</center>
<br>

The {{<a "https://docs.julialang.org/en/v1/manual/style-guide/#Style-Guide-1" "Julia Style Guide">}} recommends the following conventions:

- use lower case
- word separation can be indicated by underscores, but better not use them if the names can be read easily enough without them

---

## <center>Variables</center>
<br>

The first variable we are creating is bound to a string.<br>

That string is the path (in your system) of the file {{<b>}}time_series_covid19_confirmed_global.csv{{</b>}}<span style="font-size: 1.5rem;"><sup>1</sup></span>

*relative* to the directory in which your Julia session is running <br> **or** <br> its *absolute* path.

{{<challenge>}}
How can you easily tell in which directory your Julia session is running?
{{</challenge>}}

<span style="font-size: 1.5rem;"><sup>1</sup>(Part of the data that <a href="https://westgrid-julia.netlify.app/school/jl-03-install.html">you should have installed</a>.)</span>

---

## <center>Variables</center>
<br>

This is what it looks like *on my system* <br> (replace it with the proper path on your machine!)

```julia
file = "../../data/covid/csse_covid_19_data/csse_covid_19_time_series/" *
    "time_series_covid19_confirmed_global.csv"
```
<br>
*Note:*<br>
{{%c%}}*{{%/c%}} in Julia allows string concatenation, so I used it to break the very long path name. You don't have to do that.

---

#### <center>Ending semi-colon</center>
<br>

You might have noticed that Julia returns the value, even when you assign it to a variable (this is different from the behaviour of R and Python).
<br><br>
To avoid this, add a semi-colon ({{%c%}};{{%/c%}}) at the end:

```julia
file = "../../data/covid/csse_covid_19_data/csse_covid_19_time_series/" *
    "time_series_covid19_confirmed_global.csv";
```

---

## <center>Types</center>
<br>

I mentioned that our first variable was a *string*.

So let's talk about types in Julia.

Note that variables don't have types since they are simply names bound to values. *Values* have types.

---

## <center>2 main type systems</center>
<br>

##### Static type-checking

Type safety (catching errors of inadequate type) performed at compile time
<br><br>
##### Dynamic type-checking

Type safety done at runtime

---

## <center>Types</center>
<br>

Julia's type system is *dynamic* (types are unknown until runtime), but types *can* be declared, optionally bringing the advantages of static type systems.
<br><br><br>
This gives users the freedom to choose between an easy and convenient language, or a clearer, faster, and more robust one (or a combination of the two).
<br><br>
To know the type of an object, use {{%c%}}typeof{{%/c%}}

---

## <center>Type declaration</center>
<br>

Done with {{%c%}}::{{%/c%}}

```julia
<value>::<type>
```
<br>
*Example:*

```julia
2::Int
```

---

#### <center>Load the data</center>
<br>

Now that we have the path of our file, we can create a new variable.<br><br>

This one is a dataframe and holds the confirmed Covid-19 data:

```julia
dat = DataFrame(CSV.File(file))
```

---

#### <center>Let's explore the data</center>
<br>

Some useful functions:
```julia
typeof(dat)

names(dat)

size(dat)
nrow(dat)
ncol(dat)
```

---

#### <center>Indexing</center>
<br>

Without copying (changes made to it **will** change {{%c%}}dat{{%/c%}}):

```julia
dat[!, 1]
dat[!, "Province/State"]
dat[!, :"Province/State"]
dat."Province/State"
```
<br>
Making a copy (changes made to it **will not** change {{%c%}}dat{{%/c%}}):

```julia
dat[:, 1]
```

---

#### <center>Indexing</center>
<br>

{{<challenge>}}
How could you index the 3<sup>rd</sup> row without copying?<br>
How could you index the 3<sup>rd</sup> row making a copy?<br>
The cell of the 2<sup>nd</sup> row and 4<sup>th</sup> column?<br>
(note: this does not make a copy)
{{</challenge>}}

---

#### <center>Converting type</center>
<br>

```julia
typeof(dat."Province/State")
```

This weird type is not what we want. We want a {{%b%}}String{{%/b%}}

The function {{%c%}}string{{%/c%}} converts a value to a {{%b%}}String{{%/b%}}

<br>
Before applying it to our vector, let's play with this function a little:

```julia
string([1, 2, 3])
```

{{<challenge>}}
Is this what we want?<br>
How can we address this?
{{</challenge>}}

---

#### <center>Converting type</center>
<br>

{{<challenge>}}
Which form of indexing (with or without copy) do we want to use to convert our column?<br>
Write the code to convert our first column to {{%b%}}String{{%/b%}}<br>
Are there other columns with weird types we need to convert?
{{</challenge>}}

---

#### <center>Select and order columns</center>
<br>

Let's get rid of columns we won't use and bring the country column to the left:

```julia
select!(dat, vcat(2, 1, collect(5:ncol(dat))))
```

{{<challenge>}}
What does {{%c%}}!{{%/c%}} do?<br>
Why are we using it here?<br>
How can you find out what {{%c%}}vcat{{%/c%}} does?<br>
Try to understand this line of code by playing with it
{{</challenge>}}

---

#### <center>Rename columns</center>
<br>

The function {{%c%}}rename{{%/c%}} uses dictionaries:

<br>
```julia
rename!(dat, Dict(1 => :country, 2 => :province))
```
or
```julia
rename!(dat, Dict([(1, :country), (2, :province)]))
```

---

#### <center>Long format</center>
<br>

Let's transform our data frame into long format:

```julia
datlong = stack(dat, Not([:country, :province]),
                variable_name = :date,
                value_name = :confirmed)
```

---

#### <center>Convert date</center>
<br>

This does not look good:

```julia
datlong.date
```

<br>
We want the date to look like {{%b%}}YYYY-MM-DD{{%/b%}} and to be of type {{%b%}}Date{{%/b%}}

```julia
datlong.date = Date.(replace.(string.(datlong.date),
                              r"(.*)(..)$" => s"\g<1>20\2"),
                     "m/dd/yy")
```

---

#### <center>Our final data frame</center>
<br>

Let's have a look at our final cleaned data frame:

```julia
datlong
```

---

#### <center>Save object</center>
<br>

In the next session, you will start from here.

There are various approaches to do this:

- you could re-run this script before starting to run the next one
- you could load this script within the next one (with {{%c%}}include("this_script.jl"){{%/c%}})
- you could save {{%c%}}datlong{{%/c%}} in a Julia data file and load it in your next script

Let's do that third option.

---

#### <center>Save object</center>
<br>

For this, we are using the package {{<a "https://github.com/JuliaIO/JLD.jl" "JLD">}} which allows to save and load Julia data in {{%b%}}.jld{{%/b%}} files.

Note that a single {{%b%}}.jld{{%/b%}} file can contain several objects.<br>

```julia
save("covid.jld", "confirmed", datlong)
```
This will save the file {{%b%}}covid.jld{{%/b%}} in the working directory of the REPL.<br><br>
You can save it elsewhere by giving an absolute or relative path instead of just a file name. For instance, on my machine, this is where I am saving it:

```julia
save("../../data/covid.jld", "confirmed", datlong)
```

---

<center><img src="/img/jl/jl_question.png" width="350"></center>
