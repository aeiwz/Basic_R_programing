# Basic R programing

## Data type

1. **Numeric (Double)**:
   - Numeric data types represent real numbers, including integers and floating-point numbers.
   - Example: `x <- 42.5`

2. **Integer**:
   - Integers are whole numbers without a decimal point.
   - Example: `y <- 10L` (L is used to indicate it's an integer)

3. **Character (String)**:
   - Character data types represent text or strings.
   - Example: `name <- "Alice"`

4. **Logical (Boolean)**:
   - Logical data types represent binary values, either `TRUE` or `FALSE`.
   - Example: `is_valid <- TRUE`

5. **Factor**:
   - Factors are used to represent categorical data. They can have predefined levels.
   - Example: `gender <- factor(c("Male", "Female", "Male"))`

6. **Date and Time**:
   - R provides various data types for date and time, including `Date`, `POSIXct`, and `POSIXlt`.
   - Example: `birth_date <- as.Date("1990-05-15")`

7. **Complex**:
   - Complex data types represent complex numbers with both real and imaginary parts.
   - Example: `z <- 3 + 2i`

8. **List**:
   - Lists are versatile data structures that can hold elements of different types, including other lists.
   - Example: `my_list <- list(name = "John", age = 25, scores = c(90, 85, 78))`

9. **Vector**:
   - Vectors are one-dimensional arrays that can contain elements of the same data type.
   - Example: `numeric_vector <- c(1, 2, 3, 4, 5)`

10. **Matrix**:
    - Matrices are two-dimensional arrays with rows and columns.
    - Example: `my_matrix <- matrix(1:9, nrow = 3, ncol = 3)`

11. **Data Frame**:
    - Data frames are two-dimensional data structures that resemble tables in a database, and they can hold different data types.
    - Example: `my_df <- data.frame(Name = c("Alice", "Bob"), Age = c(30, 25))`

12. **Array**:
    - Arrays are multi-dimensional data structures that can hold elements of the same data type.
    - Example: `my_array <- array(1:12, dim = c(3, 2, 2))`

13. **Function**:
    - Functions are objects that can be assigned to variables and called like regular functions.
    - Example: `square <- function(x) x^2`

14. **Environment**:
    - Environments are used to store variables and their values.
    - Example: `my_env <- new.env()`


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


