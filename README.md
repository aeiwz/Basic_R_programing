# Basic R programing

## Basic R syntax

1. **Assigning Values**:
   - Assign a value to a variable using `<-` or `=`:
     ```R
     x <- 10
     y = 5
     ```

2. **Basic Arithmetic Operations**:
   - R supports basic arithmetic operations like addition, subtraction, multiplication, and division:
     ```R
     addition_result <- 3 + 2
     subtraction_result <- 7 - 4
     multiplication_result <- 5 * 6
     division_result <- 10 / 2
     ```

3. **Data Types**:
   - R has various data types, including numeric, character, logical, and more. You don't need to explicitly declare types.
     ```R
     num_var <- 42
     char_var <- "Hello, R!"
     logical_var <- TRUE
     ```

4. **Vectors**:
   - Vectors are one-dimensional arrays in R.
     ```R
     numeric_vector <- c(1, 2, 3, 4, 5)
     character_vector <- c("apple", "banana", "cherry")
     ```

5. **Data Frames**:
   - Data frames are two-dimensional data structures that can hold different types of data.
     ```R
     data_frame <- data.frame(Name=c("Alice", "Bob", "Charlie"), Age=c(25, 30, 22))
     ```

6. **Functions**:
   - Define and call functions using `function() {}`:
     ```R
     square <- function(x) {
       return(x^2)
     }
     result <- square(4)
     ```

7. **Conditional Statements**:
   - Use `if`, `else if`, and `else` for conditional logic:
     ```R
     if (x > 5) {
       print("x is greater than 5")
     } else {
       print("x is less than or equal to 5")
     }
     ```

8. **Loops**:
   - Use `for` and `while` loops for iterative tasks:
     ```R
     for (i in 1:5) {
       print(i)
     }

     j <- 1
     while (j <= 5) {
       print(j)
       j <- j + 1
     }
     ```

9. **Packages**:
   - R has a rich ecosystem of packages. You can install and load packages to extend R's functionality:
     ```R
     install.packages("package_name")
     library(package_name)
     ```

10. **Data Import/Export**:
    - Read and write data from/to files like CSV, Excel, or databases using functions like `read.csv()` and `write.csv()`.


---

1. **Data Manipulation**:
   - **dplyr**: The `dplyr` package provides a powerful set of functions for data manipulation tasks like filtering, selecting, grouping, and summarizing data.

   ```R
   library(dplyr)

   # Filter rows
   filtered_data <- data %>%
     filter(column_name > 10)

   # Group and summarize data
   summarized_data <- data %>%
     group_by(group_column) %>%
     summarise(mean_value = mean(value))
   ```

2. **Data Visualization**:
   - **ggplot2**: This package allows you to create sophisticated and customizable data visualizations.

   ```R
   library(ggplot2)

   ggplot(data, aes(x = x_column, y = y_column)) +
     geom_point() +
     geom_line() +
     labs(title = "Scatterplot with Line")
   ```

3. **Statistical Analysis**:
   - R provides numerous packages for statistical analysis, including hypothesis testing, regression analysis, and time series analysis.
   - **lm()**: Fit linear regression models.
   - **t.test()**: Perform t-tests for hypothesis testing.
   - **forecast**: For time series analysis and forecasting.

4. **Functional Programming**:
   - R supports functional programming concepts like anonymous functions (lambdas) and higher-order functions.

   ```R
   square <- function(x) x^2

   # Apply function to each element in a vector
   result <- sapply(1:5, square)
   ```

5. **Object-Oriented Programming (OOP)**:
   - R supports OOP with S3 and S4 classes. You can create your own classes and methods.

   ```R
   setClass("Person", representation(name = "character", age = "numeric"))
   person <- new("Person", name = "Alice", age = 30)
   ```

6. **Parallel and Multithreaded Computing**:
   - R supports parallel computing for tasks that can be split into smaller parts.

   ```R
   library(parallel)

   # Parallelize a loop
   result <- mclapply(1:10, function(x) x^2)
   ```

7. **Error Handling**:
   - Use `tryCatch()` for robust error handling and debugging.

   ```R
   tryCatch({
     # Code that may produce an error
     error_prone_function()
   }, error = function(e) {
     # Handle the error
     cat("An error occurred:", conditionMessage(e))
   })
   ```

8. **Advanced Data Structures**:
   - R supports more complex data structures like lists, matrices, and arrays.

   ```R
   my_list <- list(name = "John", age = 25)
   my_matrix <- matrix(1:9, nrow = 3, ncol = 3)
   ```


