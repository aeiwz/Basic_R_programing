# 1. Variables and Data Types
```R
age <- 25
name <- "John"
is_student <- TRUE
```

# 2. Display values of variables
```R
print(age)
print(name)
print(is_student)
```

# 3. Basic Operations
```R
num1 <- 10
num2 <- 5
```

# 4. Calculate and display results
```R
sum_result <- num1 + num2
diff_result <- num1 - num2
prod_result <- num1 * num2
quotient_result <- num1 / num2
```
```R
print(sum_result)
print(diff_result)
print(prod_result)
print(quotient_result)
```

# 5. Data Manipulation
```R
my_vector <- 1:10
```

# 6. Extract elements at specific indices
```R
extracted_elements <- my_vector[c(3, 5, 8)]
```

# 7. Calculate mean and median
```R
mean_result <- mean(my_vector)
median_result <- median(my_vector)
```

# 8. Display results
```R
print(extracted_elements)
print(mean_result)
print(median_result)
```

# 9. Conditional Statements
```R
score <- 75
```
# 10. Check if score is greater than or equal to 60
```R
if (score >= 60) {
  print("Pass")
} else {
  print("Fail")
}
```

# 11. Loops
## 11.1 For loop
```R
for (i in 1:5) {
  print(i)
}
```
## 11.2While loop
```R
counter <- 1
while (counter <= 5) {
  print(counter)
  counter <- counter + 1
}
```

# 12. Functions
## 12.1 Define square function
```R
square <- function(x) {
  return(x^2)
}
```

## 12.2 Use square function
```R
result_square <- square(6)
print(result_square)
```
