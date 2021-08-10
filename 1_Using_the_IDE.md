# Using the IDE

Open up R to start and we'll show you around the various aspects of the IDE. 

**Running/ executing a command**: This tells the computer to go ahead and follow the instructions you've given (a code snippet)

### The Console
**Console**: Where commands are automatically executed by the computer. In the console, you'll notice a  "more than" sign or "carat" (```>```). This means R is good to go and can accept a command. A plus sign means that the command is incomplete, and you need to say more. Press the ```esc``` key if you want to cancel what you typed to get back to the ```>```. When running a longer piece of code, you maybe be required to stop the code currently running before the IDE will let you edit your current input. This can be done by clicking the STOP symbol.



For example:

```{r}
  > 2 + 2
  > [1] 4
```


 
Note the ```[1]``` before our answer. This tells you that the output is a single value.

What happens if you write an incomplete command?
 
 ```{r}
 > 2 +
 +
```
 
## *To do: Write a complete command with addition, subtraction, or multiplication. Write an incomplete command and finish it on the second line*
 
 
**Script editor**: The script editor makes your code reproducible. Here you can save your code to run later. You can run code directly from the script editor in Rstudio too. Save files here the same way you do a word document. Rstudio is a script editor or IDE, also known as “interactive development environment.” You can type R code directly into the terminal on your computer, but Rstudio helps you to do it in an easy way with some additional tools. You can think of it as Microsoft Word but for code. 

**Working Directory**: The place on your machine where the files you create are saved and the files you read from can be found (more on this later).

### The Four Corners of RStudio

![alt text](https://i.redd.it/o6tq04zyozh11.png)

**Top Left**: Your script editor. From the top left you can select the type of file within RStudio you wish to run. In the case of this tutorial, you can use the plus sign to select for a R script.

**Top Right**: This is your environment! It tells you all of the objects and datafiles that are active within your working directory. It also tells you useful information such as the the type of file, for example numerical or character based.

**Bottom Left**: This is your console! You're now familiar with it from the previous section.

**Bottom Right**: This is the management section. From here you can browse the files within your computer and manually select a working directory. Here is where the help finder will pop up when we use it later in this tutorial. Any plots that are produced will be created here.

### Annotation
You will want to make comments on your code to guide folks who may read/use it in the future. Use the hashtag before writing these. This will run:
 
```{r}
> 2 + 2
> [1] 4
```

 
This will not produce an output.

```{r}
> # 2 + 2
```

 
From now on, make comments on your code explaining what it does. You will thank yourself later when going back to the lesson.  
 
Example:
```{r}
> # R can be used as a calculator
> 2 + 2
> [1] 4
> # The output is four
```

## *To do: Make a new R-script using the button in the top right corner. Write a few comments for yourself explaining what you've just learned. Don't forget to save your file!*

You can also check out [this cheatsheet](http://rstudio.com/resources/cheatsheets/) for more information on how to use the RStudio IDE!

(10 minute break)
