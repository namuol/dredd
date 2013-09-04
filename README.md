# Dredd - API Blueprint testing tool

Dredd is a command-line tool for testing API documentation written in [API Blueprint][] format against its backend implementation. With Dredd you can easiy plug your API documentation into the Continous Integration system like [Travis CI][] or [Jenkins][] and have API documentation up-to-date, all the time. Dredd uses the [Gavel][] for judging if a particular API response is valid or if is not. If you are curious about how decisions are made, please refer to Gavel's [behavior specification][].

![Dredd API Blueprint testing tool](./img/dredd.png)

## Get started testing your API

    $ dredd blueprint.md http://api.myservice.tld
   
## Installation
Node.JS and NPM is required.

    $ npm install dredd

## API Blueprint testability
Dredd can test only API resources specified by *well defined transaction*. Any Non specific resources in the Blueprint e.g. with URI template or query parameters without default or example values are considered as *ambiguous transaction* thus they are resulting in a *warning* during the test run and are skipped.

[API Blueprint]: http://apiblueprint.org/
[Travis CI]: https://travis-ci.org/
[Jenkins]: http://jenkins-ci.org/
[Gavel]: http://blog.apiary.io/2013/07/24/Bam-this-is-Gavel/
[behavior specification]: https://www.relishapp.com/apiary/gavel/docs
