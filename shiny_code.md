# shiny code

### single app instances
this code is needed to create a single app instance: 

```
library(shiny)

server <- function(input, output, session) {}
ui <- fluidPage()
shinyApp(ui = ui, server = server)
```

## server

### reactive filters
```
filteredData <- reactive({
  fildata <- filter(
    dataset, dataset$col1 %in% input$wid1 & dataset$col2 %in% input$wid2
  )
)}
```

### isolated elements
(...!!!...)

## user interface

### application layouts
you can find all possible layout elements in the application layout guide: http://shiny.rstudio.com/articles/layout-guide.html

### widgets
you can find a collection of standard widgets on: http://shiny.rstudio.com/tutorial/lesson3/

## various

### outsourcing parts of your app code in various R files
it is possible to outsource parts of your code in various R files. this makes sense in large shiny projects where the huge amount of code 
rows is confusing. this way you can structure your code. 

example: if the path of your app is like "C:/R/app.R" and your outsourced code is in "C:/R/folder/example.R", you can add the following code where this snips of "example.R" should be inserted.
```
source(file.path("examp", "example.R"),  local = TRUE)$value
```
your working directory has to be set to "C:/R". then the expression above searches in the subordinate folder "examp" for the file "example.R" and adds its code in the place of the source expression. 
