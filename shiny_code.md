# shiny code

### single app instances
this code is needed to create a single app instance: 

```
library(shiny)

server <- function(input, output, session) {}
ui <- fluidPage()
shinyApp(ui = ui, server = server)
```

### outsourcing parts of your app code in various R files
it is possible to outsource parts of your code in various R files. this makes sense in large shiny projects where the huge amount of code 
rows is confusing. this way you can structure your code. example:

```
source(file.path("folder", "example.R"),  local = TRUE)$value
```

- working directory
