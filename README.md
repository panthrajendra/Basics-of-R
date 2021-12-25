# Data Analysis Using R

[R](https://en.wikipedia.org/wiki/R_(programming_language)) is a programming language and free software environment for statistical computing and graphics. It is supported by the R Core Team and the R Foundation for Statistical Computing. It is widely used among statisticians and data miners for developing statistical software and data analysis. 

## Table of contents

1. [Basics of R](#Basics%20of%20R)
2. [Common Commands for Data Management](Common%20Commands%20for%20Data%20Management)




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

  ```r
  #Assume a dataset called data has variables V1, V2, and V3, the columns can be named as follows:
  names(data) = c("V1", "V2", "V3")

  #for our dataset, variables are: "childid", "sex", "bweight", "gestage", "momage", "parity", "mdbp", "msbp", "momeduc", "mmedaid", "socio", "dbp5", "sbp5", "ht5", "wt5", "hdl5", "ldl5", "trig5", "smoke5", "medaid5", "socio5"

  names(my_data) = c("childid", "sex", "bweight", "gestage", "momage", "parity", "mdbp", "msbp", "momeduc", "mmedaid", "socio", "dbp5", "sbp5", "ht5", "wt5", "hdl5", "ldl5", "trig5", "smoke5", "medaid5", "socio5")

  #function head will give only first few observation for all variables.

  head(my_data1)
  #output
  ```
  
  ![](/my_data1.png)

## Common Commands for Data Management


- Finding number of observations: `nrow(data)` and number of variable: `ncol(data)` in a certain dataset: data 

  ```r
  nrow(data) # gives total number of rows in the dataset-data. It is also the total number of observationsin the data set data.

  ncol(data) # gives total number of columns in the data set-data. It is also the total number of variables in the data set data. 

  dim(data) # gives the total number of rows and columns at once
  ```
  <span style="color: Skyblue;"> The number of observation in the data set is number of rows and number of variables is number of columns.</span>

- Acessing particular variable (column) or/and observation (row)
  ```r
  #let assume we have a dataset: data and it has column V1, V2, and V3 as three variables. 
  data$V1 # acesses the data in vairable V1 from dataset: data

  data[,c("V1")] # acesses V1 only
  data[,c("V1", "V2")] #acesses V1 and V2 from data
  
  #Using my_data1
  my_data1[, c("childid")] # will acess childid only from my_data1

  my_data1[, c("childid", "socio5", "momeduc")] #will acess childid, socio5, and mumeduc variable form my_data1

  my_data1[1:10,] #will acess first 10 rows and all variables

  my_data1[1:10, 1:5] #will acess first 10 rows/observations and first 5 variables or column

  my_data1[20:40, c(1,3,5,6)] #will acess observation from 20-40 and varibles at position 1, 3, 5, and 6.

  #mydata[rows, columns] general format
```
- 


- 


   
## Data Visualitation

1. Histogram

- Built in R funcition
  ``` R
  hist(data$<var>)
  ```

![](/Rplot.png)

## Stastistical Tools
