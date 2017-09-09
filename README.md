# Introduction
This repository is to test the chrome extension Gridman - css grid inspector, which seems not to display content inside of web components.

It consist of two web applications.
1. `index.html` which is an application that uses web components (using the `Polymer` library).  It has a single web component `<my-app>` which then displays a css grid (copied from https://gridbyexample.com/examples/code/example21.html)
2. `test.html` which does not use web components and includes the above example directly

When serving the first application to the web browser, `gridman` does not display the grid, but when serving the second it does.
# Installation
It is necessary to install parts of the Polymer library to run the first application.  It also needs a static web server, as loading the files directly from the files system  will not allow the web components to load properly.

The easiest way to achieve this is to `npm install` two modules `bower` and `polymer-cli` - probably globally.  `polymer-cli` is used as a web server, although any other equivalent web server would do.

Inside this directory run 
```
bower install
```
This will install the relevant pieces of polymer to make it work.
# Running

Run the web server with the the following
```
polymer serve
```
This will print the base url used to access the applications - meaning to access the applications you will use something like these 
```
http://localhost:8081/index.html
http://localhost:8081/test.html
```


