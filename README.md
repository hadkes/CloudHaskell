This repository serves as the codebase for the subject of Individual Programming for Cloud Application in School of Computer Science and Statistics.

How to build

stack setup && stack build
How to run

Run locally
stack exec cloudhaskell-wordcount-exe local count data
Run in distributed process
stack image container # Build image
docker-compose up
stack exec cloudhaskell-wordcount-exe master 127.0.0.1 count data
Deploy service to the cluster docker stack deploy --compose-file=docker-compose.yml wordcount

Run the manager stack exec cloudhaskell-wordcount-exe master haskell-master count data/ Data is the folder that contains all the txt files to be counted.

Integrate ThreadScope

stack ghc -- -O2 -rtsopts -eventlog -threaded --make src/Lib.hs src/MonoDistrMapReduce.hs src/MapReduce.hs src/CountWords.hs app/Main.hs
app/Main local count data +RTS -N2 -ls