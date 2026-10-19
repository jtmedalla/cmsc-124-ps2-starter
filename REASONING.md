# Reasoning Before Execution

Write the rule behind each case before you commit your predictions. Replace
every placeholder line below with one to three sentences that name the rule
producing that case's value, type, length, and dimensions. One rule is enough.
After you run and find a miss, add a short correction entry under that case in a
later commit.

## P01
R converts all values in an atomic vector to a common type. It follows the order logical -> integer -> double -> character. Since 3.5 is a double, the other values are converted to double as well.

## P02
R converts all values in an atomic vector to character when one of its elements is a character string. This converts the integer and logical values into character strings.

## P03
When vectors of different lengths are used in an operation, R recycles the shorter vector. The values 1 and 2 repeat as needed so they can be added to all four elements of the longer vector.

## P04
R indexing starts at position 1 and the order of the requested indices determines the order of the selected elements. Selecting positions 3 and 1 returns third before first and the original names are preserved.

## P05
Negative indexing is used to exclude elements from a vector. Since -2L refers to the second position, R removes 7L while keeping the other elements in their original order.

## P06
Logical indexing selects elements that satisfy a specified condition. The condition is.na(x) | x > 10L selects values that are missing or greater than 10, so the other values are excluded.

## P07
A factor represents categorical data using integer codes and predefined levels. The values determine which categories appear in the factor while the specified levels determine the available categories and their order.

## P08
A list can store different types of objects as separate elements and each element can have a name. In this case, scores contains an integer vector while label contains a character value.

## P09
A data frame stores data in rows and columns with each column representing a variable. Its length gives the number of columns while its dimensions describe the number of rows and columns. Its underlying type is list.

## P10
R fills a matrix column by column, and arithmetic operations follow that storage order. When the matrix is added to the shorter vector c(10L, 20L), R recycles the vector's values across the matrix elements.

## P11
The mean() function calculates the average of the supplied values but its default argument is na.rm = FALSE. Since the input contains a missing value and missing values are not removed, the result of the calculation is NA.

## P12
When na.rm = TRUE, the mean() function removes missing values before calculating the average. The values 8 and 10 are used in the calculation because the missing value is ignored.

## P13
The expression 1:3 initially creates an integer vector. When 2.5 is assigned to the second element, R converts the vector to double because integers cannot represent that decimal value.

## P14
The ifelse() function chooses values based on whether a condition is true or false. Here, missing scores are replaced with 0, other scores are doubled and values greater than 15 are then replaced with 15.

## P15
The array() function arranges values into the dimensions specified by its dim argument. Here, the eight integers are arranged into three dimensions of size 2x2x2 with values filled in column-major order. 

## P16
In R, an index of 0L selects no elements from a vector. Since the original vector is an integer vector, the empty result retains the integer type.