# Introduction

This seed project will provide fast, reliable and extensible starter for the development of Angular 2 projects.

* `angular-seed-project-4-arvato` provides the following features:
  * Best practices in file and application organization for [Angular 2](https://angular.io/).
  * Ready to go build system using [Webpack](https://webpack.github.io/docs/) for working with [TypeScript](http://www.typescriptlang.org/).
  * Testing Angular 2 code with [Jasmine](http://jasmine.github.io/) and [Karma](http://karma-runner.github.io/).
  * Coverage with [Istanbul](https://github.com/gotwarlost/istanbul)
  * End-to-end Angular 2 code using [Protractor](https://angular.github.io/protractor/).
  * Stylesheets with [CSS].
  * Error reported with [TSLint](http://palantir.github.io/tslint/).

>Warning: Make sure you're using the latest version of Node.js and NPM

# Getting Started

```bash
# clone our repo
$ git clone http://repolink my-app

# change directory to your app
$ cd my-app

# install the dependencies with npm
$ npm install
# fast install (via Yarn, https://yarnpkg.com)
# First install Yarn as an msi application on dev machine or server as required for the faster install results
$ yarn install  # or yarn

# start the server
$ npm start

go to [http://localhost:8080](http://localhost:8080) in your browser to see the running application.

# start the mock api server in an new command window
$ npm run start-mockapi
go to [http://localhost:3001](http://localhost:3001) in your browser to see mock api running in brower.
```

* [Getting Started](#getting-started)
    * [Introduction](#introduction)
    * [Dependencies](#dependencies)
    * [Installing](#installing)
    * [Developing](#Developing)
    * [Mocking](#mocking)
    * [Testing](#testing)
    * [Production](#production)
* [Frequently asked questions](#faq)
* [TypeScript](#typescript)

# Dependencies

# Installing

* `fork` this repo
* `clone` your fork
* `npm install` or `yarn install` to install all dependencies


# Developing

After you have installed all dependencies you can now start developing with:
* `npm start`
It will start a local server using `webpack-dev-server` which will watch, build (in-memory), and reload for you. The application can be checked at `http://localhost:8080`.

# Mocking

After we have installed our dependecies specially `http-server`, then we can start our mocked api server.
* Run `npm run start-mockapi` in a separate command prompt window than the one in which web server is instantiated

To make schema for our mocked api we need to update **schema** object of `src/app/services/mock/mockdataschema.js` which will use [json-schema-faker](https://www.npmjs.com/package/json-schema-faker). 

It uses below libraries to create fake data for the mocked api.
* [faker.js](https://cdn.rawgit.com/Marak/faker.js/master/examples/browser/index.html)
* [chance.js](http://chancejs.com/)

To test our json schema object created in `src/app/services/mock/mockdataschema.js` we can use utility page @ [json-schema-faker.org](http://json-schema-faker.js.org/)

# Testing

#### 1. Unit Tests

* single run: `npm test`
* live mode (TDD style): `npm run test-watch`

#### 2. End-to-End Tests (aka. e2e, integration)

* single run:
  * in a tab, *if not already running!*: `npm start`
  * in a new tab: `npm run webdriver-start`
  * in another new tab: `npm run e2e`
* interactive mode:
  * instead of the last command above, you can run: `npm run e2e-live`
  * when debugging or first writing test suites, you may find it helpful to try out Protractor commands without starting up the entire test suite. You can do this with the element explorer.
  * you can learn more about [Protractor Interactive Mode here](https://github.com/angular/protractor/blob/master/docs/debugging.md#testing-out-protractor-interactively)

# Production

To build application for production, run:

* `npm run build`

We can now go to `/dist` and deploy that to our server!

To run production build localy:
* install http-server
  * npm install http-server -g
* open the `/dist` directory in command prompt and run the command
  * npm run http-server -o
