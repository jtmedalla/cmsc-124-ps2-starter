# Reasoning Before Execution

Write the rule behind each case before you commit your predictions. Replace
every placeholder line below with one to three sentences that name the rule
producing that case's value, type, length, and dimensions. One rule is enough.
After you run and find a miss, add a short correction entry under that case in a
later commit.

## P01
Atomic vectors are coerved in a fixed order: character -> double -> integer -> logical. The example in this case makes the vector a double due to 3.5. Since the atomic vector is one dimensional, its length and the number of columns in dim would be equal.

## P02
R converts all values in an atomic vector to character when one of its elements is a character string. This converts the integer and logical values into character strings.

## P03
Since the vectors are of unequal length, R performs recycling. Each element of the smaller vector is added to its corresponding element in the larger vector.  Afterwards, the first element of the smaller vector is added again to the next element where the last operation was performed and repeats until all the elements of the larger vector were performed upon. 

## P04
R indexing starts at position 1 and the order of the requested indices determines the order of the selected elements. Selecting positions 3 and 1 returns third before first and the original names are preserved.

## P05
Negative indexing indicates elements to be excluded. In this case since R indexing starts at one, 7L is excluded.

## P06
Logical indexing selects elements that satisfy a specified condition. The condition is.na(x) | x > 10L selects values that are missing or greater than 10, so the other values are excluded.

## P07
Factors are built on top of integer vectors and are used to contain predefined values. Therefore its type would be an integer since it is built on top of integer vectors and its length would be 3 based of the first argument.

## P08
A list can store different types of objects as separate elements and each element can have a name. In this case, scores contains an integer vector while label contains a character value.

## P09
The length of the data frame gives the number of columns. ID serves as the header so it is not counted in the number of rows. Lastly, since data frames are an extension of lists, alongside tibbles, typeof() would return the value list.

## P10
R fills a matrix column by column, and arithmetic operations follow that storage order. When the matrix is added to the shorter vector c(10L, 20L), R recycles the vector's values across the matrix elements.

## P11
The mean() function calculates the average of the values in a vector. Since na.rm = TRUE is not specified, the function does not remove the missing value (NA_real_). Therefore, the result is NA. The result has type double, length 1, and no dimensions.

## P12
When na.rm = TRUE, the mean() function removes missing values before calculating the average. The missing value is ignored, so the mean is calculated using 8 and 10. The result is 9, with type double, length 1, and no dimensions.

## P13
While the initial vector is an integer due to its construction, the value of 2.5 was assigned to it later on. This triggers the coersion changing the value of the vector from integer to double.

## P14
The ifelse() function chooses values based on whether a condition is true or false. Here, missing scores are replaced with 0, other scores are doubled and values greater than 15 are then replaced with 15.

## P15
The array function creates an array from 1 to 8 with dimensions 2x2x2. Thus the length of the array is based on the result when the dimensions are multiplied resulting to 8. 

## P16
In R, an index of 0L selects no elements from a vector. Since the original vector is an integer vector, the empty result retains the integer type.