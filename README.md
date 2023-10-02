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

