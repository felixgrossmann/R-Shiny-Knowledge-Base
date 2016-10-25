# collection of usefull R code

### various functions:
- paste("a", "b", sep = "") : returns the merged value of all elements with a seperator, in this case: "ab"
- sort(vector) : sorts the vector
- unique(vector) : returns all unique values of the vector

### select rows / replace column cells by condition
```
data$col[which(data$col == 1)] <- 0
```

### select columns / delete columns by name
```
data[,!(names(data) %in% c(col1, col2))]
```

### long and wide data
