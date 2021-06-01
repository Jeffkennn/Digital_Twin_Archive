<<<<<<< HEAD
# Forge Digital Twin Demo

![Platforms](https://img.shields.io/badge/platform-Windows|MacOS-lightgray.svg)
![Node.js](https://img.shields.io/badge/node-%3E%3D%2010.0.0-brightgreen.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)

[![Viewer](https://img.shields.io/badge/Viewer-v7-green.svg)](http://developer.autodesk.com/)
[![Data-Management](https://img.shields.io/badge/Data%20Management-v1-green.svg)](http://autodesk-forge.github.io)
[![OSS](https://img.shields.io/badge/OSS-v2-green.svg)](http://autodesk-forge.github.io)
[![Model-Derivative](https://img.shields.io/badge/Model%20Derivative-v2-green.svg)](http://autodesk-forge.github.io)

![Intermediate](https://img.shields.io/badge/Level-Intermediate-blue.svg)

Autodesk Forge application demonstrating various use cases in manufacturing, specifically in context of digital twins.

![Screenshot](thumbnail.png)

## Live demo

Master branch is deployed to http://forge-digital-twin.autodesk.io.

## Development

### Prerequisites

- Node.js v10+
- [Forge](https://forge.autodesk.com) application credentials,
  and an _urn_ of a model processed with [Model Derivative APIs](https://forge.autodesk.com/en/docs/model-derivative/v2)
- MongoDB database
  - for example, use the free tier of [MongoDB Atlas](https://www.mongodb.com/cloud/atlas)
  - or run it locally: https://docs.mongodb.com/manual/installation

### Setup

- clone this repository
- install dependencies: `npm install`
- run server with all the required env. variables
  - for example, on macOS:
    ```bash
    export FORGE_CLIENT_ID=<client-id>
    export FORGE_CLIENT_SECRET=<client-secret>
    export FORGE_MODEL_URN=<model-urn>
    export MONGODB_URL=<mongodb-connection-string>
    npm start
    ```
  - or, when using [Visual Studio Code](https://code.visualstudio.com), add this configuration to your _.vscode/launch.json_:
  ```json
        {
            "type": "node",
            "request": "launch",
            "name": "Launch Express Server",
            "program": "${workspaceFolder}/server.js",
            "env": {
                "FORGE_CLIENT_ID": "<client-id>",
                "FORGE_CLIENT_SECRET": "<client-secret>",
                "FORGE_MODEL_URN": "<model-urn>",
                "MONGODB_URL": "<mongodb-connection-string>"
            }
        }
  ```
- go to http://localhost:3000

### Bootstrap theme

The project uses a custom Bootstrap theme. In order to customize it:

- modify _tools/bootstrap-theme/custom.scss_
- run `npm build:client` to update _public/stylesheets/bootstrap.css_
- commit the new version of the CSS file

### Deployment

[![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy)

## Sample data

- The jet engine model used in the live demo can be obtained
from https://knowledge.autodesk.com/sites/default/files/file_downloads/Jet_Engine_Model.zip.

- Create an archive of the `Workspace` folder and translate the archive into SVF with `_Jet Engine Model.iam` as the root file (see tutorial [here](https://forge.autodesk.com/en/docs/model-derivative/v2/tutorials/translate-zip-source-file-to-stl/) and remember to specify the output format as `SVF`)

- Once completed, feed the URN as environment variable and run the sample

## Features

- Heatmaps (using the viewer's theming color API)
- Annotations
- Animations

## Support

For support, please contact forge.help@autodesk.com.

## License

This sample is licensed under the terms of the [MIT License](https://tldrlegal.com/license/mit-license).
Please refer to [LICENSE](LICENSE) for more details.

## Written by

Petr Broz ([@ipetrbroz](https://twitter.com/ipetrbroz)), Varun Patil, Forge Partner Development Group
=======
# gentelella

Gentelella Admin is a free to use Bootstrap admin template.
This template uses the default Bootstrap 4 styles along with a variety of powerful jQuery plugins and tools to create a powerful framework for creating admin panels or back-end dashboards.

Theme uses several libraries for charts, calendar, form validation, wizard style interface, off-canvas navigation menu, text forms, date range, upload area, form autocomplete, range slider, progress bars, notifications and much more.

We would love to see how you use this awesome admin template. You can notify us about your site, app or service by tweeting to [@colorlib](https://twitter.com/colorlib). Once the list will grown long enough we will write a post similar to [this](https://colorlib.com/wp/avada-theme-examples/) to showcase the best examples.


## Theme Demo
![Gentelella Bootstrap Admin Template](https://cdn.colorlib.com/wp/wp-content/uploads/sites/2/gentelella-admin-template-preview.jpg 
"Gentelella Theme Browser Preview")

**[Template Demo](https://colorlib.com/polygon/gentelella/index.html)**

## Documentation

**[Documentation](https://colorlibhq.github.io/gentelella/)**

## Installation via Package Manager

Our goal is to make it installable on different Package Manager! Do you want to use it on your favorite Package Manager and you know how? Pull request all the way! 

As of now, this is some installation available:

**Bower**

```
bower install gentelella --save
```

**npm**

```
npm install gentelella --save
```

**yarn**

```
yarn add gentelella
```
## How to contribute
To contribute, please ensure that you have stable [Node.js](https://nodejs.org/) and [npm](https://npmjs.com) installed.

Test if Gulp CLI is installed by running `gulp --version`.  If the command isn't found, run `npm install -g gulp`.  For more information about installing Gulp, see the Gulp's [Getting Started](https://github.com/gulpjs/gulp/blob/master/docs/getting-started.md).

To have all gulp dependencies run ```npm install```

If `gulp` is installed, follow the steps below.

1. Fork and clone the repo.
2. Run `gulp`, this will open gentelella on your default browser
3. Now you can code, code and code!
4. Submit a pull request

## Gentelella for other platforms and frameworks

* [Gentelella on Ruby on Rails 4](https://github.com/iogbole/gentelella_on_rails) thanks to Israel Ogbole.
* [Gentelella on Rails 5.x](https://github.com/mwlang/gentelella-rails) thanks to Michael Lang
* [Gentelella on Smarty 3](https://github.com/microvb/otp-thing) with one time password generator, validator, and QR code generator that has no web dependencies (self-contained) in PHP thanks to MicroVB INC
* [Gentelella integrated into Symfony 5](https://github.com/mamless/Gentella-admin-Symfony-5) full stack PHP framework thanks to  Mamour Wane.
* [Gentelella on Yii framework 2](https://github.com/yiister/yii2-gentelella) with an asset bundle, a layout template and some widgets.
* [Gentelella on Angular 2](https://github.com/kmkatsma/angular2-webpack-starter-gentelella) Angular Webpack Starter modified to utilize the Gentelella.
* [Gentelella on Aurelia](https://github.com/kmkatsma/aurelia-gentelella) Typescript webpack skeleton modified to utilize the Gentelella.
* [Gentelella on Laravel](https://github.com/Labs64/laravel-boilerplate) PHP / Laravel 5 boilerplate project with Gentelella Admin theme support.
* [Gentelella on Django](https://github.com/GiriB/django-gentelella) Gentelella modified to fit as a Django app
* [Gentelella on Flask](https://github.com/afourmy/flask-gentelella) Gentelella modified to fit as a Flask app
* [Gentelella on CakePHP 3](https://github.com/backstageel/cakephp-gentelella-theme) Gentelella modified to work on CakePHP
* [Gentelella right to left](https://github.com/mortezakarimi/gentelella-rtl) Gentelella modified to work with right to left languages like Persian
* [Gentelella-rtl on Yii framework 2](https://github.com/mortezakarimi/yii2-gentelella-rtl) with an asset bundle, a layout template and some widgets. inspired from [Gentelella on Yii framework 2](https://github.com/yiister/yii2-gentelella)
* [Gentelella by React](https://github.com/thomaslwq/react-admin) Gentelella realized by React

Let us know if you have done integration for this admin template on other platforms and frameworks and we'll be happy to share your work.

## Scripts included:
* Bootstrap
* Font Awesome
* jQuery-Autocomplete
* FullCalendar
* Charts.js
* Bootstrap Colorpicker
* Cropper
* dataTables
* Date Range Picker for Bootstrap
* Dropzone
* easyPieChart
* ECharts
* bootstrap-wysiwyg
* Flot - Javascript plotting library for jQuery.
* gauge.js
* iCheck
* jquery.inputmask plugin
* Ion.RangeSlider
* jQuery
* jVectorMap
* moment.js
* Morris.js - pretty time-series line graphs
* PNotify - Awesome JavaScript notifications
* NProgress
* Pace
* Parsley
* bootstrap-progressbar
* select2
* Sidebar Transitions - simple off-canvas navigations
* Skycons - canvas based wather icons
* jQuery Sparklines plugin
* switchery - Turns HTML checkbox inputs into beautiful iOS style switches
* jQuery Tags Input Plugin
* Autosize - resizes text area to fit text
* validator - HTML from validator using jQuery
* jQuery Smart Wizard

## Other templates and useful resources
* [Free Bootstrap Admin Templates](https://colorlib.com/wp/free-bootstrap-admin-dashboard-templates/ "Bootstrap Admin Templates on Colorlib") - List of the best Free Bootstrap admin dashboard templates that are available for free for personal and commercial use.
* [Free Admin Templates](https://colorlib.com/wp/free-html5-admin-dashboard-templates/ "List of free HTML based admin templates by Colorlib") - Long list of the best free HTML5 powered admin dashboard templates. Available for personal and commercial use.
* [Angular Templates](https://colorlib.com/wp/angularjs-admin-templates/ "Angular Admin Templates on Colorlib") - List of the most popular admin templates based on AngularJS.
* [HTML Admin Templates](https://colorlib.com/wp/html-admin-templates/ "Material Design Admin Templates on Colorlib") - Most of these templates are based on AngularJS and uses a stunning Material design.
* [Bootstrap Admin Templates](https://colorlib.com/wp/bootstrap-admin-templates/ "List of Premium Bootstrap Admin Templates by Colorlib") - List of premium Bootstrap admin templates that uses a minimal flat or material design. Majority of these themes uses AngularJS but HTML5 versions are also available.
* [WordPress Admin Templates](https://colorlib.com/wp/wordpress-admin-dashboard-themes-plugins/ "List of WordPress Admin Dashboard Templates and Plugins by Colorlib") - List of the best WordPress admin dashboard templates and plugins that will add a personal touch to your WordPress dashboard.
* [WordPress Themes](https://colorlib.com/wp/free-wordpress-themes/ "List of Free WordPress themes by Colorlib") - A huge selection of the best free WordPress themes that are all licensed under GPL and are available for personal and commercial use without restrictions.

## License information
Gentelella is licensed under The MIT License (MIT). Which means that you can use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software. But you always need to state that Colorlib is the original author of this template.

Project is developed and maintained by [Colorlib](https://colorlib.com/ "Colorlib - Make Your First Blog") and Aigars Silkalns
>>>>>>> 1758e6847e0a73ecc314c66eab91eede2b99c29b
