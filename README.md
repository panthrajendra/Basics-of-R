# Data Analysis Using R

[R](https://en.wikipedia.org/wiki/R_(programming_language)) is a programming language and free software environment for statistical computing and graphics. It is supported by the R Core Team and the R Foundation for Statistical Computing. It is widely used among statisticians and data miners for developing statistical software and data analysis. 

## Basics of R

- Installing R Studio
  
   R -Studio can be downloaded using the link: [Download R-Studio](https://www.rstudio.com/products/rstudio/download/) 

- [Related Book : R for Data Science](https://jrnold.github.io/r4ds-exercise-solutions/)
  
- Importing and Exporting Data
  
  ```R 
  read.table("data or link")
  ```

  ```R 
  read.csv("file.csv")
  ```
  

## Common Commands

-  Printing data `print("Data analysis using R")`

        This command will help to print.

- Naming var ` col.names = c("var1", "var2", "var3")`

        This will help to provide specific names ot columns/variables

- Finding number of observations `nrow(data)`

       This command will help to find the number of observation in the data set by calculating number of rows. 


   
## Data Visualitation

1. Histogram

- Built in R funcition
  ``` R
  hist(data$<var>)
  ```

![](/Rplot.png)

## Stastistical Tools
