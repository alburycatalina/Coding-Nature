# Packages

### What are they?
A packages is an add-on bundle of functions that you can add to your working environment. Many have different specialized functions. For example, there are packages for making figures, doing statistical analyses, working with websites, and much more! Today we’ll be working with a pretty common one for R: ```dplyr```.

```dplyr``` is a package that includes some really useful data manipulation tools. Let's install it and try it out. 



## *To do: Start with a new R file and save it in our folder.*


## *To do: Install dplyr! Use the install.packages() function to install ```“dplyr”``` in quotes.*

You then need to load the package into your environment in order to use it. Do this
with ```library()```.

## *To do: Load dplyr into your environment*



### The help function

A pretty neat thing about R is that it comes with all its own documentation. The help function will describe any function to you. Use "?" in front of the function you're interested in to learn more. Try using it now to make sure we installed dplyr correctly. Like this:

```{r}
?dplyr
```
This will pull up an introduction to the package and describe some things you can do with it. Do this with any function you know the name of and get a help page. 


### Dplyr: Select
Use dply’s select() command to pick and choose columns to show in a  new data frame. Example:

```{r}
> species_data_selected <- select(Common_name, Occurance, Abundance)
```

Will show only the species' common name, occurance, and abundance from the species_data table. 

## *To do: Make a new data frame (name of your choice) with only scientific names, occurrences, and species nativeness.*

### Dplyr: Filter

Filter lets you select rows by certain factors. 

### *To do: Talk to each other, use google and the help function to figure out how to use filter() to display all observations in Haleakala National Park of native species.*


(30 min break)


## Packages Continued

### Dplyr: Piping 

Think of piping as adding "and then” statements to your code. A pipe is 2 percentage signs around a greater than sign (```%>%```). Use it with the summarise function, which allows you to group data in your table and reduce multiple values down to a single value, based on a summary function like maximum value or average. For example:

```{r}
> species_categories <- species_data %>% group_by(Category) %>% summarise(category_count = n())
```

This snippet counts up the number of species per category, making a new dataset with the number of each. 


## *To do: find the total number of species per each nativness level. Are there more native or non-native species?*


