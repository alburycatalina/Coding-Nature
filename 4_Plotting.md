## Plotting

Let’s show off this data with some Base R plotting! We can use the ```barplot()``` command to make a barplot from our data. 

```barplot``` accepts quite a few *arguments*. You can check them with ```?barplot```. An important ones that you can use are  ```names.arg```. 

### *To do: Plot the data in the data frame you made previously with the number of species per category. Hint: use the dollar sign indexing that we learned earlier (ex: data$column). Use google and talk to each other to find out what the ```names.arg``` argument does.*

```{r}
> barplot(height,
    names.arg = )
```
	

Example: 

```{r}
> barplot(dataframe$data,
    names.arg = dataframe$more_data)
```

Hmmm... we see something strange when we plot this data. What is it? Can we fix it?

## *To do: Find out how to remove the additional row with missing values using dplyr or indexing.*

Well done! Plot it again and take a look at what you get now!

## *To do: Use the help function to find out how to add some axis labels that make sense to the plot.*

Let’s save your plot as a pdf for later. Use the save button above the plot to do so. 

(5 min break)
