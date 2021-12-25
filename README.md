# Data Analysis Using R

[R](https://en.wikipedia.org/wiki/R_(programming_language)) is a programming language and free software environment for statistical computing and graphics. It is supported by the R Core Team and the R Foundation for Statistical Computing. It is widely used among statisticians and data miners for developing statistical software and data analysis. 

## Basics of R

- Installing R Studio
  
   R -Studio can be downloaded using the link: [Download R-Studio](https://www.rstudio.com/products/rstudio/download/) 

- [Related Book : R for Data Science](https://jrnold.github.io/r4ds-exercise-solutions/)
  
- Importing Data
  
  ```r
  read.table("data or link")
  #Here is the example of importing data that is saved in same directory as R.script

  my_data = read.csv("my_data.csv")
  
  # this will import and save my_data.csv from the computer as my_data
  

  #here is the example of importing data online 
  my_data1 = read.table("url")
  my_data1 = read.table("http://www.stat.wmich.edu/naranjo/EMdatasets/btt.txt")

  #This will import data from "http://www.stat.wmich.edu/naranjo/EMdatasets/btt.txt" and save as my_data1
  ```
  
  <span style="color: Red;"> If you are importing file from computer, make sure the file to be imported is on same directory as R.script. OTHERWISE it will show error. </span>

- Naming columns/variables for imported file

## Common Commands

- Printing in R `print("text")`

  ```r
   print("I am Learning R-language.")
   ```

  <span style="color: Skyblue;"> This command will print: I am learning R-language.</span>


- Naming var `names(data) = c("var1", "var2", "var3")`

  <span style="color: Skyblue;"> This will help to provide 
  specific names to columns/variables.</span>


- Finding number of observations: `nrow(data)` and number of variable: `ncol(data)` in a certain dataset: data 

  ```r
  nrow(data) # gives total number of rows in the dataset-data. It is also the total number of observationsin the data set data.

  ncol(data) # gives total number of columns in the data set-data. It is also the total number of variables in the data set data. 

  dim(data) # gives the total number of rows and columns at once
  ```
  <span style="color: Skyblue;"> This command will help to find the number of observation in the data set by calculating number of rows.</span>

- Acessing particular variable (column) or/and observation (row)
  ```r
  #let assume we have a dataset: data and it has column V1, V2, and V3 as three variables. 
  data$V1 # acesses the data in vairable V1 from dataset: data

  data[,c("V1")] # acesses V1 only
  data[,c("V1", "V2")] #acesses V1 and V2 from data

- 


   
## Data Visualitation

1. Histogram

- Built in R funcition
  ``` R
  hist(data$<var>)
  ```

![](/Rplot.png)

## Stastistical Tools
