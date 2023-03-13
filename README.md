# R--Ninth-Assignment

> library(readr)
> city <- read_csv("city.csv", show_col_types = FALSE)
New names:                                                                                                   
• `` -> `...1`
> city
# A tibble: 10 × 3
    ...1     u     x
   <dbl> <dbl> <dbl>
 1     1   138   143
 2     2    93   104
 3     3    61    69
 4     4   179   260
 5     5    48    75
 6     6    37    63
 7     7    29    50
 8     8    23    48
 9     9    30   111
10    10     2    50


> k <- c(1,2,3,4,5,6,7,8,9,10)
> Population_in_1920 <- c(138,93,61,179,48,37,29,23,30,2)
> Population_in_1930 <- c(143,104,69,260,75,63,50,48,111,50)

> hist(Population_in_1920, main = "Population of US in 1920", xlab = "Population in 1920", col = "pink")
> plot(k, Population_in_1930)
> plot(k, Population_in_1930, main = "Population of US in 1930")


> library(lattice)
> xyplot(k ~ Population_in_1920, main = "Population of US in 1920", xlab = "Population in 1920", ylab = "k", pch = 21)
> histogram(k ~ Population_in_1930, data = city, main = "Population of US in 1930")


> library(ggplot2)
> d <- ggplot(city, aes(x = k, y = Population_in_1920),main = "Population of US in 1920")+
+    geom_point()
> d + geom_vline(xintercept = 2)
> d <- ggplot(city, aes(x = k, y = Population_in_1930),main = "Population of US in 1930")+
+    geom_point()
> d + geom_vline(xintercept = 5)
