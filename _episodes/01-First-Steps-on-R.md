---
title: "First Steps on R"
teaching: 10
exercises: 10
questions:
- "What is R and why is it important to learn it?"
- "What types of data does the R language has?"

objectives:
- "Understand why R is important."
- "Describe the purpose and use of each panel in the RStudio IDE"
- "Locate buttons and options in the RStudio IDE"
- "Define a variable"
- "Assign data to a variable"

keypoints:
- "R is a programming language"
- "RStudio is useful tool for script writting and data-management."
- "A variable can temporarily store data."
---

RStudio: First steps of a wonderful journey 

*It takes courage to sail in uncharted waters*
  -Snoopy
 
## RStudio setup 

### What is R and what can it be used for?

"R" is used to refer to a programming language and the 
software that reads and interprets the instructions written on the 
scripts of this language. It is specialized on statistical 
computing and graphics. RStudio is the most popular program to write
scripts and interact with the R software.

R uses a series of written commands, that is great, believe us! 
When you rely on clicking, pointing, and remembering where and 
why to point here or click there, mistakes are prone to occur. 
Moreover, if you manage to get more data, it is easier to just
*re-run* your script to obtain results. Also, working with scripts 
makes the steps you follow for your analysis clear and shareable. 
Here are some of the advantages for working with R:  

- R code is reproducible
- R produces high-quality graphics
- R has a large community
- R is interdisciplinary 
- R works on data of all colors and sizes
- R is free!

### A nautical chart of RStudio 

RStudio is an [Integrated Development Environment(IDE)](https://en.wikipedia.org/wiki/Integrated_development_environment#:~:text=An%20integrated%20development%20environment%20(IDE,automation%20tools%20and%20a%20debugger.)) 
which we will use to write code,
navigate the files from our computer/cloud, try code, inspect the variables we are 
going to create, and visualize our plots.

Here is what you may look at the first time you open RStudio:
<a href="https://user-images.githubusercontent.com/67386612/118720027-ba433c00-b7ee-11eb-87e5-7496fde5763e.png">
  <img src="https://user-images.githubusercontent.com/67386612/118720027-ba433c00-b7ee-11eb-87e5-7496fde5763e.png" alt=/>
</a>
<em> Figure 1. RStudio interface screenshot. The three windows that appear on the screen provide us with a space in which we can see our console (left side window) where the orders we want to execute are written, observe the generated variables (upper right), and a series of subtabs (lower right): **Files** shows us files that we have used, **Plots** shows us graphics that we are generating, **Packages** shows the packages that we have downloaded, **Help** it gives us the information of packages, commands and/or functions that we do not know, but works only with internet conection, and **Viewer** shows a results preview in R markdown files.</em>

If we click in the option `File` :arrow_right: `New File` :arrow_right: `R Script`, we open up a script and
we get what we can call a _RStudio nautical chart_

<a href="https://user-images.githubusercontent.com/67386612/112203976-c046e300-8bd8-11eb-9ee6-72c95f9134f3.png">
  <img src="https://user-images.githubusercontent.com/67386612/112203976-c046e300-8bd8-11eb-9ee6-72c95f9134f3.png" />
</a>
<em> Figure 2. RStudio interface screenshot. Clockwise from top left: Source, Environment/History, Files/Plots/Packages/Help/Viewer, Console. <em/>

You can enter your online RStudio to see your own environment. Let's copy your instance address into your browser
(Chrome or Firefox) and login into Rstudio.  
The address should look like:  `http://ec2-3-235-238-92.compute-1.amazonaws.com:8787/`  

Although data are already stored in your instance, in case you need to you can donwload them [here](https://drive.google.com/file/d/15dW1sQCIhtmCUvS0IUOMPBH5m1gqNB0m/view?usp=sharing).

### Review of the setup

As we have revisited throughout the lesson, maintaining related data in a single folder
is desirable. In RStudio, this folder is called the **working directory**. It is where R will be looking 
for and saving your files. If you need to check where your working directory is located use `getwd()`.
If your working directory is not what you expected(*i.e. ~/dc_workshop/taxonomy/*), it can always be changed by clicking on the blue 
gear icon:
<a href="https://user-images.githubusercontent.com/67386612/118722611-f7f59400-b7f1-11eb-8ca9-a72561f9c529.png">
  <img src="https://user-images.githubusercontent.com/67386612/118722611-f7f59400-b7f1-11eb-8ca9-a72561f9c529.png" />
</a> on the `Files` tab, and pick the option _Set As Working Directory_. Alternatively, you can use the `setwd()` command for changing it.

Let's use this commands to set our working directoiry where we have stored our files from the previous 
lessons:

~~~
> setwd("~/dc_workshop/taxonomy/")
~~~
{: .language-r}

## Having a dialogue with R

There are two main paths to interact with R in RStudio:
* Using the console.
* Creating and editing script files.

The console is where commands can be typed and executed immediately and where the 
results from executed commands will be shown (like in the Unix shell). If R is ready to accept commands, the R console shows
the `>` prompt. You can type instructions directly into the console and press "Enter", but they will 
be forgotten when you close the session.

For example, let's do some math and save it in R objects. We can store values in variables by
ussing the assignment operator `<-`:
~~~ 
> 4+3
> addition <- 4+3
> subtraction <- 2+1
> total <- addition -subtraction
> total
~~~
{: .language-r}

What would happend if you tap `ctrl` + `l`? Without the lesson page, can you remember what numbers the sum is made of in the variable `addition`?.
**Reproducibility** is in our minds when we program (and when we do science). For this purpose, 
is convenient to type the commands we want to save in the script editor, and save the script periodically. 
We can run our code lines in the script by the shortcut `ctrl` + `Enter` 
(on Mac, `Cmd` + `Return` will work). Thus, the command on the current line, or the instructions
in the currently selected text will be sent to the console and will be executed.

Time can be the enemy or ally of memory. We want to be sure to remember why we wrote the commands
in our scripts, so we can leave comments(lines of no executable text) by beggining a line with `#`:
~~~
# Let's do some math in RStudio. How many times a year do the supermarkets change the bread that they use for
# display?, if they change it every 15 days:
> 365/15
~~~
{: .language-r}
~~~
[1] 24.3333
~~~
{: .output}
