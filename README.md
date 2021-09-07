# About
This is the [React TodoMVC](http://todomvc.com/examples/react/) sample re-written in "KarateJS" - an experimental app-server implemented as part of the [Karate](https://github.com/intuit/karate) project.

"KarateJS" is a simple server-side framework that requires you to only write HTML and JS and nothing else.

## Features:
* Pure-HTML, XD-friendly preview-able templates powered by [Thymeleaf](https://www.thymeleaf.org)
* Compose complex views out of re-usable HTML templates
* AJAX and partial DOM rendering powered by [htmx](https://htmx.org)
* Server-side JS powered by [Graal JS](https://www.graalvm.org)
* All code for a "view" can fit in a single HTML file
* ES6 JS can be included within IDE-friendly `<script>` tags
* Server powered by [Armeria](https://armeria.dev)
* CLI powered by [picocli](https://picocli.info)
* Hot reload !
* Only a JRE needed
* Can run serverless / within an AWS Lambda
* Pluggable HTTP-session store (can be wired up to e.g. DynamoDB with very little effort)
* also see [this tweet](https://twitter.com/ptrthomas/status/1335611577270038528) and [this one](https://twitter.com/KarateDSL/status/1434487117426532356) too

## Running Locally
* clone this repository: `git clone https://github.com/ptrthomas/karate-todomvc.git` or [download a ZIP](https://github.com/ptrthomas/karate-todomvc/archive/main.zip)
* Use [jbang](https://jbang.dev)
  * if jbang installed run: `jbang karate -S`
  * if not installed: `curl -Ls https://sh.jbang.dev | bash -s - karate -S`
* Manually:
  * Download `karate-1.1.0.jar` from [here](https://github.com/intuit/karate/releases/tag/v1.1.0)
  * rename it to `karate.jar`, place it in the same folder as the files from git
  * Java (only a [JRE](http://www.oracle.com/technetwork/java/javase/downloads/index.html) is needed)
    * `java -jar karate.jar -S`
* or Docker (and Java does not need to be installed)
  * `docker run --rm -v "$PWD":/src -w /src -p 8080:8080 openjdk:8 java -jar karate.jar -S`
* navigate to [http://localhost:8080](http://localhost:8080) to view the app
* you can add `-p` to change the port number if needed e.g. `-p 8000`
