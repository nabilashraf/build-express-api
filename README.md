# Build Express Api
A Command line interface for instantly building an express rest api. <br>
Create controllers, models and add routes in matter of seconds.

[![npm version](https://badge.fury.io/js/build-express-api.svg)](https://badge.fury.io/js/build-express-api)

*This CLI only supports Node 6 and over.*

## Installation
Install it once globally:
```sh
$ npm install -g build-express-api
```
## Getting Started
### Initializing the application structure
```sh
$ mkdir my-app
$ cd my-app
$ build-express-api init
```
#### Directory structure
```
my-app
├── package.json
├── rest
    └── controllers
    └── models
    └── server.js
```
Install all the needed dependencies:
```sh
$ npm install
```
*Note: when running all of the further commands, please stay in the my-app directory*
## Creating a new controller
```sh
$ build-express-api create-controller
```
The CLI will now take you through series of questions, the example of building a new controller would be:

![Creating a plain controller](https://github.com/ognjengt/build-express-api/blob/master/assets/createControllerPlain.JPG)

You can choose the **plain controller** or **custom routes** controller from the menu.

**Plain controller** just creates a controller with built in routes in rest/controllers/controllerName.js.

**Custom routes** controller allows you to manually add your routes, the example of building custom routes controller would be:

![Creating a custom routes controller](https://github.com/ognjengt/build-express-api/blob/master/assets/customControllerCreation.JPG)

**Note:** *make sure that you write the routes in the correct (strict JSON) format such as:*

```
{"routeName":"METHOD"}
```

When the controller is created it will automatically be imported in server.js file

## Adding routes to a controller
```sh
$ build-express-api add-routes <controllerName>
```
Example:

![Adding routes to a controller](https://github.com/ognjengt/build-express-api/blob/master/assets/addRoutesComplete.JPG)

## Creating new model
```sh
$ build-express-api create-model
```
Example:

![Creating new model](https://github.com/ognjengt/build-express-api/blob/master/assets/createModelSuccess.JPG)

**Note:** *When creating new model, you don't need to provide the properties in strict JSON format, just separate them with the comma*

This CLI supports only mongoose models for now.

**Note:** The experience this CLI provides does not work as smooth in Git Bash terminal, since it is not an interactive terminal, but if you are using Git Bash inside VS Code, then there are no problems, I found no complications using any other terminal.
