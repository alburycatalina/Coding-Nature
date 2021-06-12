## Packages

### What are they?
A packages is an add-on bundle of functions that you can add to your working environment. Many have different specialized functions: making figures, stats, working with websites, etc. Today we’ll be working with a pretty common one for R: dplyr.

### *To do: Start with a new R file and save it in our folder.*


### *To do: Install dplyr! Use the install.packages() function to install “dplyr” in quotes.*

You then need to load the package into your environment in order to use it. Do this
with ```library()```.

#### *Load dplyr into your environment*



### The help function

A pretty neat thing about R is that it comes with all its own documentation. The help function will describe any function to you. Use "?" in front of the function you're interested in to learn more. Try using it now to make sure we installed dplyr correctly. Like this:

```{r}
?dplyr
```
This will pull up an introduction to the package and describe some things you can do with it. Do this with any function you know the name of and get a help page. 


### Dplyr: Select
Use dply’s select() command to pick and choose columns to show in a  new data frame. Example:

```{r}
> new_data1 <- select(shark_data, depth, id)
```

Will show only depth and id from the shark_data table. 

### *To do: Make a new data frame (name of your choice) with only site names, year, and visibility.*

### Dplyr: Filter

Filter lets you select rows by certain factors. 

#### *Talk to each other, use google and the help function to figure out how to use filter() to display all observations in Andros where the visibility was 4.*


(30 min break)


## Packages Cont. 

### Dplyr: Piping 

Think of piping as “and then” statements. A pipe is 2 percentage signs around a greater than sign (%>%). Use it with the summarise function, which allows you to group data in your table and reduce multiple values down to a single value, based on a summary function like maximum value or average. For example:

```{r}
> new_data3 <- shark_data %>% group_by(site_name) %>% summarise(avg = mean(visibility))
```

Finds the mean visibility by site, making a new column “avg”.

#### *Find the total count per site. (Hint: find the command for adding and use it in place of mean) in the code above.*


You can also use the dollar sign to achieve a similar resulrts in data tables. The dollar sign works with column names in a table. Like this:

 ```{r}
> shark_data$site_name
 ```
 
Which returns all site names in the site_name column.
