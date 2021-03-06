[![Build Status](https://travis-ci.org/mendixlabs/image-viewer.svg?branch=master)](https://travis-ci.org/mendixlabs/image-viewer)
[![Dependency Status](https://david-dm.org/mendixlabs/image-viewer.svg)](https://david-dm.org/mendixlabs/image-viewer)
[![Dev Dependency Status](https://david-dm.org/mendixlabs/image-viewer.svg#info=devDependencies)](https://david-dm.org/mendixlabs/image-viewer#info=devDependencies)
[![codecov](https://codecov.io/gh/mendixlabs/image-viewer/branch/master/graph/badge.svg)](https://codecov.io/gh/mendixlabs/image-viewer)

# Image viewer
Display an image and optional perform an action on click: mobile friendly enlarge, open a page or call a mircoflow.

## Features
* Supports different data sources:
    * Set static image in the Modeler
    * Retrieve images from a static URL
    * Image from a URL attribute of context object
    * Image from mendix System.Images
* Supports actions:
    * Enlarge and pinch zoom
    * Open page
    * Call microflow
    * Call nanoflow

## Dependencies
Mendix 7.13.1

## Demo project
https://imageviewer.mxapps.io/

## Usage
The widget requires a context.
 ### Data source: Dynamic image
 - On the Data source option of the Data source tab, select the dynamic image.
 - The widget will pick the image from the context object (context object should inherit from system.image entity).
 - Refer to the appearnace section for configuring height and width.

### Data source: Dynamic URL attribute
 - On the Data source option of the Data source tab, select the dynamic URL option if its not already selected by default.
 - Select the attribute from the context objext that contains the URL of the image.
 - Refer to the appearnace section for configuring height and width.

### Data source: Static URL
  - On the Data source option of the Data source tab, select the static URL
  - Specify the URL that points to the image (URL outside of the Mendix system).
  - Refer to the appearnace section for configuring height and width.

### Data source: Static image
  - On the Data source option of the Data source tab, select the static image.
  - Click select button to add static images from the modeller.
  - Refer to the appearnace section for configuring height and width.

## Issues, suggestions and feature requests
We are actively maintaining this widget, please report any issues or suggestion for improvement at https://github.com/mendixlabs/image-viewer/issues.

## Development
Prerequisite: Install git, node package manager, webpack CLI, grunt CLI, Karma CLI

To contribute, fork and clone.

    git clone https://github.com/FlockOfBirds/image-viewer.git

The code is in typescript. Use a typescript IDE of your choice, like Visual Studio Code or WebStorm.

To set up the development environment, run:

    npm install
    
Create a folder named dist in the project root.

Create a Mendix test project in the dist folder and rename its root folder to MxTestProject. Changes to the widget code shall be automatically pushed to this test project. Or get the test project from https://github.com/MendixLabs/image-viewer/releases/latest

    dist/MxTestProject
    
To automatically compile, bundle and push code changes to the running test project, run:

    grunt
    
To run the project unit tests with code coverage, results can be found at dist/testresults/coverage/index.html, run:

    npm test
    
or run the test continuously during development:

    karma start
