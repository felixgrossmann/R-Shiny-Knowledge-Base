# code for using oracle databases in R

### execute a sql-statement
this code allows you to execute a sql-statement and save the data.

```
library(ROracle)

ROracleDB         <- dbDriver("Oracle")
ROracleUser       <- "username"
ROraclePW         <- "password"
ROracleDbName     <- "dbname"
ROracleEnv        <- "environment"
ROracleList       <- list(ROracleDB, ROracleUser, ROraclePW, ROracleDbName, ROracleEnv)
con <- dbConnect(ROracleList[[1]], username = ROracleList[[2]], password = ROracleList[[3]], dbname = ROracleList[[4]])
query <-  "SELECT * FROM table"
data <- dbGetQuery(con, query)
```
