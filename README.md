# About
* see tweet: https://twitter.com/ptrthomas/status/1335611577270038528

# Instructions
* clone this repository: `git clone https://github.com/ptrthomas/karate-todomvc.git`
* download `karate-0.9.9.RC2.jar` from [here](https://dl.bintray.com/ptrthomas/karate/)
* rename it to `karate.jar`, place it in the same folder as the files from git
* Java (only a [JRE](http://www.oracle.com/technetwork/java/javase/downloads/index.html) is needed)
  * `java -jar karate.jar -S`
* Docker
  * `docker run --rm -v "$PWD":/src -w /src -p 8080:8080 openjdk:8 java -jar karate.jar -S`
* [jbang](https://www.jbang.dev)
  * `jbang com.intuit.karate:karate-core:0.9.9.RC2 -S`
* navigate to [http://localhost:8080](http://localhost:8080) to view the app
* you can add `-p` to change the port number if needed e.g. `-p 8000`


