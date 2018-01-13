# R name convention

| Object               | Notation      | Length  | Plural   | Prefix   |  Suffix  | Abbreviation | Mask       | Example              |
|----------------------|:-------------:|--------:|:--------:|:--------:|:--------:|:------------:|:-----------|:---------------------|
| File Name            | lowercase     |    30   | No       | No       | .R       | No           | [a-z_]+\.R | predict_ad_revenue.R |
| Function Name        | PascalCase    |    30   | No       | No       | No       | No           | [A-z]+     | CalculateAvgClicks   |
| Variable Name        | camelCase     |    30   | No       | No       | No       | No           | [A-z]+     | avgClicks            |
| Data Frame           | PascalCase    |    30   | No       | df_      | No       | No           | df_[A-z]+  | df_AvgClicks         |
| Factor Variable Name | PascalCase    |    30   | No       | f        | No       | No           | f[A-z]+    | fAvgClicks           |


## Notation and Naming

### File Names
File names should end in uppercase `.R`, word delimeter `'_'`, lowercase notation and, of course, be meaningful.
 
**GOOD:** `predict_ad_revenue.R`

**BAD:** `foo.R`


### Identifiers

Don't use underscores ( _ ) or hyphens ( - ) in identifiers. Identifiers should be named according to the following conventions. Variable names have initial lower case letters. If variable name consists of several words, then they aren't separated, but all words except for the first one begin with capital letters. Function names are formed like variable names but with initial capital letter (FunctionName); constants are named like functions but with an initial k.
 - variableName

   **GOOD:** avgClicks 

   **BAD:** avg_Clicks

 - FunctionName  

   **GOOD:** CalculateAvgClicks 

   **BAD:** calculate_avg_clicks , calculateAvgClicks

 Make function names verbs. 

*Exception: When creating a classed object, the function name (constructor) and class should match (e.g., lm).*
 - kConstantName 


## Syntax

### Line Length
The maximum line length is 80 characters.

### Indentation
When indenting your code, use two spaces. Never use tabs or mix tabs and spaces. 

*Exception: When a line break occurs inside parentheses, align the wrapped line with the first character inside the parenthesis.*

### Spacing
Place spaces around all binary operators (=, +, -, <-, etc.).

*Exception: Spaces around ='s are optional when passing parameters in a function call.*

Do not place a space before a comma, but always place one after a comma.

 **GOOD:** 
```R
df_TabPrior <- table(df[df$days.from.opt < 0, "campaign.id"])
total <- sum(x[, 1])
total <- sum(x[1, ])
```

**BAD:** 
```R
df_TabPrior <- table(df[df$days.from.opt<0, "campaign.id"])  # Needs spaces around '<'
df_TabPrior <- table(df[df$days.from.opt < 0,"campaign.id"])  # Needs a space after the comma
df_TabPrior<- table(df[df$days.from.opt < 0, "campaign.id"])  # Needs a space before <-
df_TabPrior<-table(df[df$days.from.opt < 0, "campaign.id"])  # Needs spaces around <-
total <- sum(x[,1])  # Needs a space after the comma
total <- sum(x[ ,1])  # Needs a space after the comma, not before
```
Place a space before left parenthesis, except in a function call.

**GOOD:**
```R
if (debug)
```
**BAD:**
```R
if(debug)
```

Extra spacing (i.e., more than one space in a row) is okay if it improves alignment of equals signs or arrows (<-).

```R
plot (x    = x.coord,
      y    = dataMat[, MakeColName(metric, ptiles[1], "roiOpt")],
      ylim = ylim,
      xlab = "dates",
      ylab = metric,
      main = (paste(metric, " for 3 samples ", sep = "")))
```
Do not place spaces around code in parentheses or square brackets.

*Exception: Always place a space after a comma.*

**GOOD:**
```R
if (debug)
x[1, ]
```

**BAD:**
```R
if ( debug )  # No spaces around debug
x[1,]  # Needs a space after the comma
```
### Curly Braces

An opening curly brace should never go on its own line; a closing curly brace should always go on its own line. You may omit curly braces when a block consists of a single statement; however, you must consistently either use or not use curly braces for single statement blocks.

**GOOD:**
```R
if (is.null(ylim)) {
  ylim <- c(0, 0.06)
}

xor (but not both)
if (is.null(ylim))
  ylim <- c(0, 0.06)
```
Always begin the body of a block on a new line.

**BAD:**
```R
if (is.null(ylim)) ylim <- c(0, 0.06)
if (is.null(ylim)) {ylim <- c(0, 0.06)}
```
Surround "else" with braces.

An "else" statement should always be surrounded on the same line by curly braces.

**GOOD:**
```R
if (condition) {
  one or more lines
} else {
  one or more lines
}
```

**BAD:**
```R
if (condition) {
  one or more lines
}
else {
  one or more lines
}
```

**BAD:**
```R
if (condition)
  one line
else
  one line
```


### Assignment
Use `<-`, not `=`, for assignment.

**GOOD:**
```
x <- 5
```
**BAD:**
```
x = 5
```


### Semicolons
Do not terminate your lines with semicolons or use semicolons to put more than one command on the same line. (Semicolons are not necessary, and are omitted for consistency with other Google style guides.)


## Organization

### General Layout and Ordering
1.Copyright statement comment
2.Author comment
3.File description comment, including purpose of program, inputs, and outputs
4.source() and library() statements
5.Function definitions
6.Executed statements, if applicable (e.g.,  print, plot)

Unit tests should go in a separate file named "originalfilename_test.R".


### Commenting Guidelines
Comment your code. Entire commented lines should begin with "#" and one space.

Short comments can be placed after code preceded by two spaces, "#", and then one space.
```R
\# Create histogram of frequency of campaigns by pct budget spent.
hist(df$pct.spent,
     breaks = "scott",  # method for choosing number of buckets
     main   = "Histogram: fraction budget spent by campaignid",
     xlab   = "Fraction of budget spent",
     ylab   = "Frequency (count of campaignids)")
```


### Function Definitions and Calls
Function definitions should first list arguments without default values, followed by those with default values. 

In both function definitions and function calls, multiple arguments per line are allowed; line breaks are only allowed between assignments.

**GOOD:**
```R
PredictCTR <- function(query, property, numDays,
                       showPlot = TRUE)
```
**BAD:**
```R
PredictCTR <- function(query, property, numDays, showPlot =
                       TRUE)
```
Ideally, unit tests should serve as sample function calls (for shared library routines).


### Function Documentation
Functions should contain a comments section immediately below the function definition line. These comments should consist of a one-sentence description of the function; a list of the function's arguments, denoted by Args:, with a description of each (including the data type); and a description of the return value, denoted by Returns:. The comments should be descriptive enough that a caller can use the function without reading any of the function's code.

Example Function

```R
CalculateSampleCovariance <- function(x, y, verbose = TRUE) {
  # Computes the sample covariance between two vectors.
  #
  # Args:
  #   x: One of two vectors whose sample covariance is to be calculated.
  #   y: The other vector. x and y must have the same length, greater than one,
  #  with no missing values.
  #   verbose: If TRUE, prints sample covariance; if not, not. Default is TRUE.
  #
  # Returns:
  #   The sample covariance between x and y.
  n <- length(x)
  # Error handling
  if (n <= 1 || n != length(y)) {
    stop("Arguments x and y have different lengths: ",
         length(x), " and ", length(y), ".")
  }
  if (TRUE %in% is.na(x) || TRUE %in% is.na(y)) {
    stop(" Arguments x and y must not have missing values.")
  }
  covariance <- var(x, y)
  if (verbose)
    cat("Covariance = ", round(covariance, 4), ".\n", sep = "")
  return(covariance)
}
```

### TODO Style
Use a consistent style for TODOs throughout your code.
```R
TODO(username): Explicit description of action to be taken
```


### Attach
The possibilities for creating errors when using "attach" are numerous. Avoid it.


### Functions
Errors should be raised using stop().


### Objects and Methods
The S language has two object systems, S3 and S4, both of which are available in R. S3 methods are more interactive and flexible, whereas S4 methods are more formal and rigorous. (For an illustration of the two systems, see Thomas Lumley's "Programmer's Niche: A Simple Class, in S3 and S4" in R News 4/1, 2004, pgs. 33 - 36:  http://cran.r-project.org/doc/Rnews/Rnews_2004-1.pdf.)

Use S3 objects and methods unless there is a strong reason to use S4 objects or methods. A primary justification for an S4 object would be to use objects directly in C++ code. A primary justification for an S4 generic/method would be to dispatch on two arguments.

Avoid mixing S3 and S4: S4 methods ignore S3 inheritance and vice-versa.
