# About
This is the [React TodoMVC](http://todomvc.com/examples/react/) sample re-written in "KarateJS" - an experimental app-server implemented as part of the [Karate](https://github.com/intuit/karate) project.

"KarateJS" is a simple server-side framework that requires you to only write HTML and JS and nothing else.

## Features:
* HTML rendered server-side (using [Thymeleaf](https://www.thymeleaf.org))
* Pure-HTML (preview-able) templates (inspired by [Apache Wicket](https://wicket.apache.org))
* All code can fit into a single HTML file with extra logic within `<script ka:lang="js"></script>` tags
* AJAX and partial DOM rendering powered by [htmx](https://htmx.org)
* Server-side JS powered by [Graal JS](https://www.graalvm.org)
* Server powered by [Armeria](https://armeria.dev)
* Hot reload
* Only a JRE needed
* App (including static resources) can run serverless / within an AWS Lambda
* Pluggable HTTP-session store (can be wired up to e.g. DynamoDB with little effort)
* also see: https://twitter.com/ptrthomas/status/1335611577270038528

# Instructions
* clone this repository: `git clone https://github.com/ptrthomas/karate-todomvc.git`
* download `karate-0.9.9.RC2.jar` from [here](https://dl.bintray.com/ptrthomas/karate/) (or use jbang, see below)
* rename it to `karate.jar`, place it in the same folder as the files from git
* Java (only a [JRE](http://www.oracle.com/technetwork/java/javase/downloads/index.html) is needed)
  * `java -jar karate.jar -S`
* Docker
  * `docker run --rm -v "$PWD":/src -w /src -p 8080:8080 openjdk:8 java -jar karate.jar -S`
* [jbang](https://www.jbang.dev)
  * `jbang com.intuit.karate:karate-core:0.9.9.RC2 -S`
* navigate to [http://localhost:8080](http://localhost:8080) to view the app
* you can add `-p` to change the port number if needed e.g. `-p 8000`
