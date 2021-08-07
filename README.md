# Basic-Functions-in-R

Basic Functions in R, in this tutorial, we are going to discuss basic statistical or user-defined functions. Functions are very useful in R for faster and safe execution.

Some will be inbuilt functions and others may be user-defined, here we are going to discuss very useful functions in our day-to-day life.

Getting Data

library(datasets)
data<-iris$Sepal.Length

Statistical Functions

The following commands can be used to get the mean, median, quantiles, minimum, maximum, variance, and standard deviation.

mean(data)
median(data)
sd(data)
var(data)
max(data)
min(data)
quantile(data)
summary(data)

the summary function will provide the output based on the type of the dataset.

Control Structures

The following are basic control structures.

if statements

if (condition) {
  # code executed when condition is TRUE
} else {
  # code executed when condition is FALSE
}

for statements

for(i in 1:x)
{ code }

while statements

while (test_expression)
{
statement
}

repeat statements

repeat {
statement
}

break and next statements

if (test_expression) {
break
}

switch statements

switch(expression, case1, case2, case3....)

scan statements

scan(file = "", what = double(), nmax = -1, n = -1, sep = "",
     quote = if(identical(sep, "\n")) "" else "'\"", dec = ".",
     skip = 0, nlines = 0, na.strings = "NA",
     flush = FALSE, fill = FALSE, strip.white = FALSE,
     quiet = FALSE, blank.lines.skip = TRUE, multi.line = TRUE,
     comment.char = "", allowEscapes = FALSE,
     fileEncoding = "", encoding = "unknown", text, skipNul = FALSE)

User-defined function

Just consider one example, the following function takes a single input value and computes its square

The variable x, is a formal parameter of the function.

When the function is called it is passed an argument that provides a value for the formal parameter

Square<-function(x){x*x}
Square(5)
25
Square(10:20)
100 121 144 169 196 225 256 289 324 361 400

Another one example is rep function, you can use for different purposes based on your requirements.


rep("A",4)
rep(1:5,2)
rep(1:5,rep(2,5))

Sorting

order(data)
 [1]  14   9  39  43  42   4   7  23  48   3  30  12  13
 [14]  25  31  46   2  10  35  38  58 107   5   8  26  27
 [27]  36  41  44  50  61  94   1  18  20  22  24  40  45
 [40]  47  99  28  29  33  60  49   6  11  17  21  32  85
 [53]  34  37  54  81  82  90  91  65  67  70  89  95 122
 [66]  16  19  56  80  96  97 100 114  15  68  83  93 102
 [79] 115 143  62  71 150  63  79  84  86 120 139  64  72
 [92]  74  92 128 135  69  98 127 149  57  73  88 101 104
[105] 124 134 137 147  52  75 112 116 129 133 138  55 105
[118] 111 117 148  59  76  66  78  87 109 125 141 145 146
[131]  77 113 144  53 121 140 142  51 103 110 126 130 108
[144] 131 106 118 119 123 136 132

You try for reverse sorting also based on rev function.

rev(order(data))
  [1] 132 136 123 119 118 106 131 108 130 126 110 103  51
 [14] 142 140 121  53 144 113  77 146 145 141 125 109  87
 [27]  78  66  76  59 148 117 111 105  55 138 133 129 116
 [40] 112  75  52 147 137 134 124 104 101  88  73  57 149
 [53] 127  98  69 135 128  92  74  72  64 139 120  86  84
 [66]  79  63 150  71  62 143 115 102  93  83  68  15 114
 [79] 100  97  96  80  56  19  16 122  95  89  70  67  65
 [92]  91  90  82  81  54  37  34  85  32  21  17  11   6
[105]  49  60  33  29  28  99  47  45  40  24  22  20  18
[118]   1  94  61  50  44  41  36  27  26   8   5 107  58
[131]  38  35  10   2  46  31  25  13  12  30   3  48  23
[144]   7   4  42  43  39   9  14

cbind function

Suppose if you want to combine the data frame, matrix or vectors, you can use cbind functions.


a<-c(1,2,3)
b<-c(4,5,6)
cbind(a,b)
     a b
[1,] 1 4
[2,] 2 5
[3,] 3 6

rbind function

Suppose if you want to do row binding then rbind function will be handy.

a<-c(1,2,3)
b<-c(4,5,6)
rbind(a,b)
  [,1] [,2] [,3]
a    1    2    3
b    4    5    6

Conclusion

There are a lot of functions available, above mentioned functions will be useful for solving day-to-day data arrangement problems.

Some useful functions are here

identical()
sum()
paste()
is.na()
is.logical()
stopifnot()
length()
