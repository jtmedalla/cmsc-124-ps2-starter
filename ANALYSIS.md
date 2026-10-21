# Vector and Scalar Evaluation

## `clean_scores_vector()`

The clean scores vector treats the data as a vector, so assignments using conditionals apply to each element of the vector. Tracing an example input of c(Ada = 8, Grace = NA_real_, Linus = 12, Barbara = 4), the behavior of the function can be observed line by line.

The statement `adjusted <- ifelse(is.na(scores), 0, scores * 2)` goes through every element of the vector and checks whether its value is `NA`. If it is `NA`, it changes it to `0`. Otherwise, it multiplies the score by `2`. This creates a new vector, preserving the names and saving the result to `adjusted`.

The next statement, `adjusted[adjusted > 20] <- 20`, selects values greater than `20` using an index vector and replaces them with `20`. The adjusted values are then returned to the caller.

## `clean_scores_scalar()`

The scalar implementation processes each score individually using a for loop. It first copies the scores into an output vector while preserving their names. For each element, is.na(value) checks whether the score is missing. If it is missing, the function assigns 0. Otherwise, min(2 * value, 20) doubles the score and caps it at 20.

Ada's score becomes 16, Grace's becomes 0, Linus's becomes 20, and Barbara's becomes 8. Both implementations produce the same results for this input.

## How Recycling Affects the Implementation of Clean Scores

In R, recycling occurs when an operation combines vectors of unequal lengths. For example, c(5, 10, 15) * c(2, 3) produces c(10, 30, 30) because R repeats the shorter vector's values to match the longer vector. R also issues a warning because the longer vector's length is not a multiple of the shorter vector's length.

The current cleaning functions use scalar constants such as 2 and 20, so they do not have this mismatched-vector problem. However, using a vector of multipliers or limits with an unintended length could cause values to be processed incorrectly.

## Scalar vs. Vector

Scalar data in R consists of a single value, whereas vectors are ordered collections of values. Since R is commonly used for statistics and graphics, it frequently processes collections of data for analysis.

In this task, the vector implementation is preferable because it applies the same cleaning rules to multiple scores concisely. The scalar implementation is also valid and makes the processing of each element explicit. However, when all scores follow the same rules, the vector approach is shorter and easier to maintain. The scalar approach may be useful when individual elements require more complex processing.