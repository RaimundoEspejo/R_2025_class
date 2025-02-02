# R_2025_class
Auburn University R 

# Creating objects
x <- 2
y <- 3
x + y

# Non-numerical objects
name <- "Raimundo"
name
seven <-"7"
seven
x + seven

# Functions
class(seven)
class(x)
# Creating a vector with the function c()
vec <- c(1, 2, 3, 4, 5, 6, 7)
vec <- c(1:7)
vec2 <- c("Rai", "Zach", "Jie")
vec3 <- c(TRUE, FALSE, TRUE) 

vec2[2]

vec + 2

# Functions to calculate
mean(vec)
sd (vec)
sum (vec)
median (vec)
min (vec)
max (vec)
summary (vec)
abs (vec)
sqrt (vec)
sqrt(sum(vec))
log(vec)
log10(vec)
exp(vec)

# Logical operators to compare numbers
1 > 2
1 < 2
1 == 1 
1 = 1

# Logical operators to find something in objects
t <- 1:10
t[t > 8]

t[(t > 8) | (t < 5)]
t[(t > 8) & (t < 10)]
t[t != 2]
2 %in% t
11 %in% t

# Data types Matrices (can contain only one data class)
mat1 <- matrix(data = c(1, 2, 3), nrow = 3, ncol = 3)
mat1

mat2 <- matrix(data = c("Rai", "Zach", "Jie"), nrow = 3, ncol = 3)
mat2

mat1[1]
mat1[2]
mat1[3]
mat1[4]
mat1[10]

mat1[1, 3]
mat1[1, ]
mat1[, 3]

# Data frames (can contain different data types)
df <- data.frame(mat1[,1], mat2[,1])
df
colnames(df) <- c("value", "name")
df

# Indexing can happen using brackets [ ]
df[1,2]
df[1]
df[, "value"]

df$value[1]
df$name[3]

df$value[df$name == "Jie"]
df$value[df$name %in% c("Jie", "Rai")]
df$value[df$name != "Zach"]

# Subset function will also work
subset(df, name == "Rai")
df$log_value<- log(df$value)
df

# Installing packages
install.packages("tidyverse")
install.packages("phyloseq")
library(tidyverse) 

# Reading data to R
csv <- read.csv(path to your file)
