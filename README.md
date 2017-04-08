## This repository serves as the codebase for the subject of Individual Programming for Cloud Application in School of Computer Science and Statistics.

# How to build
```
stack setup 
stack build
```

# How to run

# Run everything (worker and manager) on one node 
```
stack exec mapreduce-haskell-project local count longTestFile.txt
```

# Run in distributed process
```
stack exec mapreduce-haskell-project slave localhost 8081
stack exec mapreduce-haskell-project slave localhost 8082
stack exec mapreduce-haskell-project slave localhost 8083
stack exec mapreduce-haskell-project slave localhost 8084
``` 

# Run manager
```
stack exec mapreduce-haskell-project master localhost 8080 count longTestFile.txt
```
