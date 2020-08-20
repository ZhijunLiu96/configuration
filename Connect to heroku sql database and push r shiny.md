## Connect to SQL database

Language: R

1. Check your heroku database and fill in all those parameters in r scripts
```r
con <- dbConnect(
    RPostgres::Postgres(),
    host = ***,
    port = ***,
    user = ***,
    password = ***,
    dbname = *** )
```

## Push R Shiny dashboard

1. go to the [shinyapp](https://www.shinyapps.io) website

2. Find your name, token, secret

3. Initilize a new R script and write the following lines.
```r
library(rsconnect)
rsconnect::setAccountInfo(name='janezl',
                          token= ***,
                          secret= ***)
setwd('heroku') # your path/folder
rsconnect::deployApp()
```
4. Done