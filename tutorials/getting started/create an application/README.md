# Honeycomb for Beginners: Getting Started

### Tutorials

* [Part 1: Creating your first Honeycomb Web Application](https://github.com/Schalltech/honeycomb-tutorials/blob/master/tutorials/getting%20started/README.md#honeycomb-for-beginners-getting-started)

## Part 1: How to create your first Honeycomb web application

<img src="https://raw.githubusercontent.com/Schalltech/honeycomb-tutorials/master/tutorials/getting%20started/create%20an%20application/images/create-app-11.png">

In the following tutorial you'll learn:

* how to create a basic Honeycomb Web Application
* how to add a page to your Honeycomb Web Application
* how to add a micro app to a pages layout
* how to style a micro app and its container
* how to access your Honeycomb Web Application on the cloud

Micro apps you will use in this tutorial

Name | Description 
:---- | :-----
ma-label | The label micro app represents a caption for an item in a user interface.

### Create the Hello World Application
Generating Micro-Apps is fast and easy through the use of the Honeycomb CLI. It takes care of all the boiler plate setup that allows your micro-app to play nicely with lerna and the mono-repo. To create a new micro-app, simply call the following command.

```
yarn create:micro-app
```
This will launch the CLI in your terminal. You should see something similar as the screenshot below.
