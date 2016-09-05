# Query and Insert From Hive

## Dependencies
- R package `RJDBC` -> allows R to connect to any DBMS that has a JDBC driver
- Impala JDBC Drivers

## Usage

- Fill in the variable `hiveConnectionUrl`, the url used to open a connection on Hive
- Replace the value `Hive_Jdbc_Folder_Path` with the name of the hive drivers folder in the function `JDBC()`
- If your system is a Windows, add this code in the beginning in your script :

  - Load/Download DBI library :
  `if(!require("DBI")){ 
  install.packages("DBI", repos = "http://cran.r-project.org")
  library("DBI")
  }`

  - JAVA_HOME = "" :
  `if(Sys.getenv("JAVA_HOME")!="")
    Sys.setenv(JAVA_HOME="")`

  - Load/Download rJava library :
  `if(!require("rJava")){
    install.packages("rJava", repos = "http://cran.r-project.org")
    library("rJava")
  }`
