---
  title: "Introduction to R Programming"
author: "Muhammad Yousaf Riaz"
date: "21 Dec, 2021"
output: html_document
---
  
  
  ##### NOTE: 
  1. Change author name and date to your exercise submission date in above section
2. Your code MUST execute without any errors. 
3. You can add more lines in your code as required.

## Section 1: Data Types and Operations Pt. 1

### Question 1 
**Create the variables with the following composition:**  
  1. A vector containing each letter of your first name as its elements.  
2. A variable that contains your name concatenated from the vector created in (1)  
3. A variable containing a sequence from 100 to 120.  
4. Create a matrix of 3x3 dimensions that contains the even sequence of numbers starting from 2.  
5. Assign names to the variables.  


```{r }
#### Start solution ####
```
v1 <- c("Muhammad", "yousaf")

```{r }

```
as.character(v1)
a<-v1

```{r }

```
b <- (100:200)
b

```{r }

```
m=seq(2,18, by=2)
n<-matrix(m, nrow=3 , ncol=3)
n
```{r }

```
first_name <- a
sequence <- b
even_matrix <- n

```{r }
#### End solution ####
```

### Question 2
**Create a factor variable emp_status:**  
  1. Containing the categorical variables: Employed, Unemployed, Self-Employed, with each level appearing atleast more than 2.  
2. Display the levels and the factor variable as a table.  
3. Unclass the elements of the factor variable.  


```{r }
#### Start solution ####
```
emp_status <- factor(c("employed","unemployed","self-employed","employed","unemployed","self-employed","employed","unemployed","self-employed"),levels=c("unemployed","employed","self-employed"))
x <-emp_status

```{r }

```
levels(x)
table(x)


```{r }

```
unclass(x)

```{r }

```


```{r }
#### End solution ####
```

### Question 3
**Create a dataframe object called bank_customers:**  
  1. the data frame will have three columns: CustomerID, hasAccount, totalBalance  
2. Fill the data as follows  
a. Alicia does not have an account. She is here for inquiry   
b. Nancy is here to check on her account balance of USD 10,000.  
c. Fernando is here to deposit USD 100 in his account which had no balance.  
d. Louis will withdraw all his money from the account that had USD 2,000.   
e. Diane is here for information.   
3. For customers that do not have a value, use NA as placeholder.  
4. Print the number of rows, columns and names for the data frame.  


```{r }
#### Start solution ####
```
bank_customers <- data.frame(CustomerID=1:5, hasAccount=1:5, totalBalance=1:5)

```{r }

```
CustomerID=c("Alicia","Nancy","Fernando","Louis","Diane")

hasAccount=c("No","yes","yes","yes","No")

totalBalance=c("NA",10000,0,2000,"NA")

```{r }

```

bank_customers <- data.frame(CustomerID=CustomerID, hasAccount=hasAccount, totalBalance=totalBalance)

bank_customers

```{r }

```
nrow(bank_customers)
ncol(bank_customers)

```{r }

```
names(bank_customers)

```{r }
#### End solution ####
```

### Good Job! You have successfully completed the section!

## Section 2: Control Structures 

### Question 1
**Create a variable containing a sequence of numbers from 1 to 100:**  
  1. Iterate over the variables and print those numbers which are prime.  

**Create a variable var with a value of 1:**  
  1. Create a while loop and increase the value of var at each iteration.   
2. When you reach the 10th prime number, terminate the loop and print the number.  


```{r }
#### Start solution ####
```
for (i in 1:100){
  if ( i == 1){
    next
  } else if (i == 2){
    print (i)
  } else if( i == 3){
    print(i)
  }else if (i == 5){
    print(i)
  } else if (i == 7){
    print(i)
  } else if (i %% 2 != 0 && i %% 3 != 0 && i %% 5!=0 && i %% 7!= 0){
    print (i)
  }
}

```{r }

```
var <- 1
while ( var < 30){
  var = var + 1
  if (var == 23){
    print(var)
    break
  }
}

```{r }

```


```{r }

```


```{r }

```


```{r }

```


```{r }
#### End solution ####
```

### Question 2
**Create a matrix of size 3x3 called mat_1:**  
  1. Iterate over all the values one by one and print the element as well as the position in the matrix (row, col)


```{r }
#### Start solution ####
```


```{r }

```

```{r }

```
m <- matrix(1:9, 3,3)

for(i in seq_len(nrow(m))){
  
  for(j in seq_len(ncol(m))){
    cat(i,j)
    print(m[i,j])
    
  }
}

```{r }

```


```{r }

```


```{r }

```


```{r }
#### End solution ####
```

### Good Job! You have successfully completed the section!

## Section 3: Functions

### Question 1
**Create a function called gcd that finds the greatest common divisor of two numbers a and b:**  
  1. a and b, should be taken as input.  
2. The function must print the GCD as well as return it.  
3. The output must be saved in a variable called answer.  


```{r }
#### Start solution ####
```


```{r }

```
gcd <- function(a,b){
  r <- 1
  e <- 0
  while (r!=0){
    if ( a > b){
      r <- a %% b
      a <- b
      b <- r
    } else {
      e <- a
      a <- b
      b <- e
    }
  }
  answer <- a
  print(answer)
  return(answer)
  
}




```{r }

```


```{r }

```


```{r }

```


```{r }

```


```{r }
#### End solution ####
```

### Question 2
**Create a function called allConditionsMeet, that checks whether two expressions evaluate to true:**  
  1. a and b, should be taken as input.  
2. the function should check if a and b, both conditions, evaluate to True.  
3. The function must returns a boolean value.  
4. Using a method, print the arguments that function takes.  


```{r }
#### Start solution ####
```


```{r }

```
allconditionsmeet <-function(a,b){
  
  if (a < b){
    y <- sprintf("%d less than %d",a , b)
    x <- print(a < b)
  } else if(a > b){
    y <- sprintf("%d is greater than %d",a , b)
    x <- print(a > b)
  } else if(a == b){
    y <- sprintf("%d is equal to %d",a , b)
    x <- print(a == b)
  }
  print(y)
  return(x)
}


```{r }

```


```{r }

```


```{r }

```


```{r }

```


```{r }
#### End solution ####
```

### Good Job! You have successfully completed the section!

## Section 4: Vectorized Operations

### Question 1
**Create two matrices matrix_1 and matrix_2 of dimensions 2x3 and 3x2:**  
  1. Perform element-wise multiplication.  
2. Perform matrix multipilcation.   

**Create a 2x2 matrix my_mat:**  
  1. Write a function to find the determinant of the matrix.  


```{r }
#### Start solution ####
```


```{r }

```
matrix_1 <- matrix(1:6, 2,3)
u <- c(matrix_1)
matrix_2 <- matrix(7:12, 3,2)
v <- c(matrix_2)
x <- u * v ## multiplying the transpose of matrix_2
x <- matrix(x,)
x
y <- matrix_1 %*% matrix_2
y

```{r }

```


```{r }

```
det_twobytwo <- function(a,b,c,d){
  
  a <- readline(prompt= " Enter the first row and first column number : ")
  a <-as.integer(a)
  b <- readline(prompt= " Enter the first row and second column number : ")
  b <-as.integer(b)
  c <- readline(prompt= " Enter the second row and first column number : ")
  c <-as.integer(c)
  d <- readline(prompt=" Enter the first row and first column number : ")
  d <-as.integer(d)
  
  my_mat <- matrix(1:4, 2,2)
  my_mat[1,1] <- a
  my_mat[1,2] <- b
  my_mat[2,1] <- c
  my_mat[2,2] <- d
  
  calc <- (a * d )-(b * c )
  
  print(my_mat)
  
  return(calc)
}



```{r }

```


```{r }

```


```{r }
#### End solution ####
```

### Good Job! You have successfully completed the section!

## Section 5: Date and Time in R

### Question 1
**Use the current date and time and store them into variables curr_date and curr_time respectively: [use sys]**  
  1. Convert both into date and time objects using the appropriate functions.  
2. Print the weekday, year, second and hour using the appropriate function and variables.  


```{r }
#### Start solution ####
```
curr_date <- Sys.Date()
curr_time <- Sys.time()
curr_time <- as.POSIXlt(curr_time)
curr_date <- as.Date(curr_date)
curr_time$wday
curr_time$year
curr_time$sec
curr_time$hour


```{r }

```


```{r }

```


```{r }

```


```{r }

```


```{r }

```


```{r }
#### End solution ####
```

### Question 2
**Create a variable to store current date/time**  
  1. Create another variable that stores and set the timezone as GMT-5  
2. Find the difference between your current time and the GMT-5 timezone.  


```{r }
#### Start solution ####
```


```{r }

```

y <- as.POSIXct("2022-01-25 22:58:00")
y
x <- as.POSIXct("2022-01-25 22:58:00", tz= "EST")
x
x-y



```{r }

```


```{r }

```


```{r }

```


```{r }

```


```{r }
#### End solution ####
```

### Good Job! You have successfully completed the section!

## Section 6: Loop Functions

### Question 1
**Create a function to calculate mean and standard deviation of the provided data**
  1. Create a sequence of numbers from 100 to 150 store in a variable called numbers.
1. Use lapply, sapply, apply and tapply to implement the functions on "numbers" [only on the second half of the sequence for tapply]


```{r }
#### Start solution ####
```

mean_std_lapply<- function(){
  
  numbers <- 100:150
  numbers <- list(numbers)
  
  m <- lapply(numbers, mean)
  s <- lapply(numbers, sd)
  print(m)
  print(s)
  
}


```{r }

```

mean_std_sapply<- function(){
  
  numbers <- 100:150
  numbers <- list(numbers)
  
  m <- sapply(numbers, mean)
  s <- sapply(numbers, sd)
  print(m)
  print(s)
  
}

```{r }

```

mean_std_apply<- function(){
  
  numbers <- matrix(100:150,1,)
  m <- apply(numbers,1, mean)
  s <- apply(numbers,1, sd)
  print(m)
  print(s)
  
}

```{r }

```

mean_std_tapply<- function(){
  
  numbers <- c(101:150)
  numbers
  a <- gl(2,25)
  b <- tapply(numbers,a,mean)
  b[2]
  c <- tapply(numbers,a, sd)
  c[2]
  print(b[2])
  print(c[2])
  
}

```{r }

```


```{r }

```


```{r }
#### End solution ####
```

### Question 2
**Create a matrix of dimensions 4x4**
  1. Find the row-wise and column-wise mean of the matrix.
2. Print the values.


```{r }
#### Start solution ####
```


```{r }

```
a <- matrix(2:17,4,4)
row_mean <- apply(a,1, mean)
row_mean
col_mean <- apply(a,2,mean)
col_mean


```{r }

```


```{r }

```


```{r }

```


```{r }

```


```{r }
#### End solution ####
```

### Good Job! You have successfully completed the section!

## Section 7: Data Split

### Question 1
**Using the data frame Orange:**  
  1. Using split function to break down the dataset on circumference and store it in 'split_data' variable.   
2. Print the values for split_data where circumference is 30 and 75.  
3. Find the average age of the tree when the circumference is 30 and when circumference is 214.  


The dataset is loaded and the variable Orange contains the respective dataset.  


```{r }
library(datasets)
```


```{r }
head(Orange)
```


```{r }
#### Start solution ####
```


```{r }

```
table(Orange)

table(Orange$circumference)


split_data <- split(Orange,Orange$circumference)

split_data[c('30','75')]

y <- split_data[c('30','214')]

y

sapply(y, function(x) colMeans(x[,c("age", "circumference")]))


```{r }

```


```{r }

```


```{r }

```


```{r }

```


```{r }
#### End solution ####
```
