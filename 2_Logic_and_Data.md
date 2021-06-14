## Coding Logic

### Creating objects
 
R is an object-oriented programming language. That means that it allows you to store single values (think a number or text) as a “variable.” 

This is analogous to putting an object in a box and labeling that box. 

 You can use a caret and dash to assign an object a value. Like this:
 
```{r}
<-  
```

 
## *To do: Create a new object, called “students” and assign the number of students in the room. Note: case (upper or lower) matters*
 

```{r}
> students <- 11
```
 
The object ```students``` has now been stored. Notice that there was no output.

### Print
 
Use the print() command to see what’s stored in an object (or just type it’s name).

For example, you can print text. Try ```print('Hello World!")```.


## *To do: Print the object ```students``` to see what's stored inside.*

```{r}
>  print(students)
>  [1] 11
```
 

### Data Types

There are different data types in programming languages. In R, the simplest are:

* Character: Comprised of text with quotations around it. Ex: “red”
* Numeric: Comprised of numbers
* Boolean: TRUE or FALSE
 
## *To do: Check the type of the object “students” with ```class()```*
 
 
```{r}
> class(students)
```
 
The class should be numeric because we assigned a number to the object ```students```
 
 
### Vectors
A vector is basically a list of objects. For example:

 
```{r}
> list <- c(1,2,3)
```
 
The c stands for "concatenate". 


## *To do: Make a vector of prime numbers using the **concatenate notation** c(x,y,z)*
 
 ```{r}
> prime_numbers <- c(3,5,1)
> prime_numbers
> [1] 3 5 1
```	
 
You can put any kind of data into a vector.
 
## *To do: Overwrite students to make it a list of all our names. Note: text goes in quotation marks)*
 
  ```{r}
> students <- c("name1", "name2", "name3")
```	
        	
 
### Subsetting Vectors
You can “ask” your computer what value is in certain positions in the list using *indexing*. Example:

  ```{r}
>  prime_numbers[3]
> [1] 1
```	

 
## *To do: Index the vector we just made using square brackets. Who is the second student in the list?*

 
### Conditional Subsetting
 
Conditional subsetting uses logical vectors. The below command will a list containing ```TRUE``` or ```FALSE``` depending on if the value matches the statement. 

  ```{r}
>  prime_numbers > 2
> [1]  TRUE  TRUE FALSE

 ```

 
You can also do this outside of lists. For example:
  ```{r}
> 3 > 4
> FALSE
 ```

Here’s where your “how to google lesson” comes in.
 
### *To do: Use your knowledge of conditional subsetting to figure out if our list of prime numbers is longer than 6. Hint: figure out what the command for how long a vector is! Talk to each other and use the internet to figure it out.*


(5 minute break)



 
## Starting with Data
 
The database you're about to download is maintained by the US National Parks services. They publish a list of species confrimed to be present in national parks. We'll use this data to learn how a scientist would use promgramming make sense of this large amount of information and turn it into knowledge we can use. 


 
### Long form Data Structure
You might be used to using excel to create tables that are easy to look at, but when you begin playing with coding and data, you’ll want to use *long form data structure*. This means that we structure our databases so that each observation is a row. 

We also use .csv (also called *comma delimited*) files for R. You can open .csv files with excel, they’re pretty much the same as a regular spreadsheet but don’t save formatting. You can convert excel files to csv with the “save as” option in excel.

## *To do: Download the file ```species.csv``` from this repository into the folder you made earlier.*

Open it up and note the long-form data structure (each observation is a row)! Pretty cool, huh?


### Importing Data

### *To do: Open Rstudio and set your working directory to the folder you made. Use the read.csv command to import the data like below. Save it as the object of your choice.*

  ```{r}
> setwd(‘folder_name’)
> species_data <- read.csv(‘species.csv')
 ```

Sometimes databases are massive. Use head() to view the first few lines of data and get an idea of what it looks like.


### *To do: Use the head() command on the dataframe you just saved. What do you see?*

 
### Indexing
You can use indexing to select out values from your vector, just like in the last section. Indexing a dataframe uses the [row, column] notation.  For example:

  ```{r}
> species_data[1,1] 
 ```

Will display the data in the first row and first column of the data frame. 


## *To do: Use indexing to figure out what the 3rd species in the databse is*



You can also use the dollar sign to achieve a similar results in data tables. The dollar sign works with column names in a table. Like this:

 ```{r}
> species_data$Scientific_name
 ```
 
Which returns all of the species' scientific names in the Scientific_name column.

You can also use commas to indicate selecting the whole row or column.  For example:
 
 ```{r}
> species_data[,1]
 ```
Will display all of the observations in the first column! 


## *To do: Try it out! Use indexing to display only the information gathered by the student's 4th observation (a row)*
