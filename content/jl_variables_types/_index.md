+++
title = "jl_variables_types"
outputs = ["Reveal"]
[logowg]
src = "/img/wg_white_removed_medium.png"
[logojl]
src = "/img/jl/jl_dots.png"
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

#### <center>Load packages</center>
<br>
First, we need to load some packages.<br>
This will take some time as Julia will pre-compile newly installed or updated packages. Next time you load these packages, it will go a lot faster.
<br><br>
```julia
using CSV
using DataFrames
using Dates
```
<br>
{{%b%}}Dates{{%/b%}} is a package from the standard Julia library (it was installed when you installed Julia).<br>
The other packages are packages that [you should have installed](https://westgrid-julia.netlify.app/school/jl-05-pkg.html).

---

#### <center>Load the data</center>
<br>

Then, we need to load the data.

This will give us an opportunity to talk about variables and types in Julia.

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

The [Julia Style Guide](https://docs.julialang.org/en/v1/manual/style-guide/#Style-Guide-1) recommends the following conventions:

- use lower case
- word separation can be indicated by underscores, but better not use them if the names can be read easily enough without them

---

## <center>Variables</center>
<br>

The first variable we are creating is bound to a string.<br><br>

That string is the path (in your system) of the file {{<b>}}time_series_covid19_confirmed_global.csv{{</b>}}<span style="font-size: 1.5rem;"><sup>1</sup></span>

*relative* to the directory in which your Julia session is running <br> **or** <br> its *absolute* path.<br><br>

<span style="font-size: 1.5rem;"><sup>1</sup>(Part of the data that <a href="https://westgrid-julia.netlify.app/school/jl-03-install.html">you should have installed</a>.)</span>

---

## <center>Variables</center>
<br>

This is what it looks like *on my system* <br> (replace it with the proper path on your machine!)

```julia
file = "../../data/covid/csse_covid_19_data/csse_covid_19_time_series/" *
    "time_series_covid19_confirmed_global.csv"
```
<br><br>
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

---

## <center>Types</center>
<br>

Variables don't have types since they are simply names bound to values.<br>
*Values* have types.

---

## <center>2 main type systems</center>
<br>

##### Static type checking

Type safety (catching errors of inadequate type) performed at compile time
<br><br>
##### Dynamic type checking

Type safety done at runtime

---

## <center>Types</center>
<br>

Julia's type system is *dynamic* (types are unknown until runtime), but types *can* be declared, optionally bringing the advantages of static type systems.
<br><br><br>
This gives users the freedom to choose between an easy and convenient language, or a clearer, faster, and more robust one (or a combination of the two).

---

## <center>Type declaration</center>
<br>



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

```julia
size(dat)
nrow(dat)
ncol(dat)
```

```julia
dat
typeof(dat)
```

```julia
dat."Province/State"
typeof(dat."Province/State")
```

---

#### <center>Select and order columns</center>
<br>

```julia
select!(dat, vcat(2, 1, collect(5:ncol(dat))))
```

---

#### <center>Rename columns</center>
<br>

```julia
:province == Symbol("province")
typeof(:province)
```

```julia
rename!(dat, Dict(1 => :country, 2 => :province))
```

```julia
rename!(dat, Dict([(1, :country), (2, :province)]))
```

---

#### <center>Long format</center>
<br>

```julia
datlong = stack(dat, Not([:country, :province]),
                variable_name = :date,
                value_name = :confirmed)
```

---

#### <center>Convert date</center>
<br>

```julia
datlong.date
```

```julia
datlong.date = Date.(replace.(string.(datlong.date),
                              r"(.*)(..)$" => s"\g<1>20\2"),
                     "m/dd/yy")
```

```julia
datlong
```

---

<center><img src="/img/jl/jl_question.png" width="350"></center>
