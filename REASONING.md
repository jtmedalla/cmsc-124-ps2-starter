# Reasoning Before Execution

Write the rule behind each case before you commit your predictions. Replace
every placeholder line below with one to three sentences that name the rule
producing that case's value, type, length, and dimensions. One rule is enough.
After you run and find a miss, add a short correction entry under that case in a
later commit.

## P01
Atomic vectors are coerved in a fixed order: character -> double -> integer -> logical.
The example in this case makes the vector a double due to 3.5.
Since the atomic vector is one dimensional, its length and the number of columns in dim would be equal.

## P02
Replace this line with the rule that decides this case.

## P03
Since the vectors are of unequal length, R performs recycling.
Each element of the smaller vector is added to its corresponding element in the larger vector. 
Afterwards, the first element of the smaller vector is added again to the next element where the last operation was performed and repeats until all the elements of the larger vector were performed upon. 

## P04
Replace this line with the rule that decides this case.

## P05
Negative indexing indicates elements to be excluded. In this case since R indexing starts at one, 7L is excluded.

## P06
Replace this line with the rule that decides this case.

## P07
Factors are built on top of integer vectors and are used to contain predefined values. Therefore its type would be an integer since it is built on top of integer vectors and its length would be 3 based of the first argument.

## P08
Replace this line with the rule that decides this case.

## P09
The length of the data frame gives the number of columns. 
ID serves as the header so it is not counted in the number of rows. 
Lastly, since data frames are an extension of lists, alongside tibbles, typeof() would return the value list.

## P10
Replace this line with the rule that decides this case.

## P11
Replace this line with the rule that decides this case.

## P12
Replace this line with the rule that decides this case.

## P13
Replace this line with the rule that decides this case.

## P14
Replace this line with the rule that decides this case.

## P15
Replace this line with the rule that decides this case.

## P16
Replace this line with the rule that decides this case.
