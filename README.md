generator-tmpww
===============

> Basic Yeoman generator for TMP projects. Projects are set up to use SASS, as well as many best-practices, by default.

This generator will scaffold your project, set up Bower, and create basic Grunt tasks that make your life easier while developing.

## Getting Started
This generator assumes that you are connected to the internet and have the following installed:

* [Node.js](http://nodejs.org/)
* [Yeoman](http://yeoman.io/)

If not, begin by installing [Node.js](http://nodejs.org/).

Next, install Yo, Bower, and Grunt in one fell swoop by entering the following command in your shell:

```shell
npm install -g yo
```

## Installation
This generator will not be published in the NPM directory. Because of this you will need to clone this repository. Decide where you would like to store this generator and run the following command in that directory:

```shell
git clone https://github.com/sethlopezme/generator-tmpww.git
```

This command will create a new folder called `generator-tmpww` and clone this repository into it. Once the repository has been cloned, `cd` into `generator-tmpww` and link it with the following command:

```shell
npm link
```

Now you're ready to go!

## Using the Generator
Create a new directory for your project, and open a shell there. To scaffold your project, enter the following command in your shell:

```shell
yo tmpww "Name of Project Here"
```

Yo will ask you a few short questions about yourself and your project. Then it will completely scaffold your project, including Bower dependencies and Grunt tasks.

### Directory Structure
Your directory will look similar to this:

```shell
$ tree
.
├── .sass-cache/
│   └── *
├── build/
├── dev/
│   ├── components/
│   │   ├── css-reset/
│   │   │   └── *
│   │   ├── html5shiv/
│   │   │   └── *
│   │   ├── jquery/
│   │   │   └── *
│   ├── css/
│   │   └── style.css
│   ├── job-images/
│   │   ├── 0000
│   │   │   └── *
│   ├── resources/
│   │   ├── 0000
│   │   │   └── *
│   ├── sass/
│   │   └── style.scss
│   └── index.html
├── node_modules/
│   └── *
├── .bowerrc
├── .editorconfig
├── .gitignore
├── bower.json
├── gruntfile.js
└── package.json
```

### Bower
When using Bower, your components will be installed in the `dev/components` directory.

#### Installed Dependencies
Bower will automatically install some dependencies for you and they're already included in the index.html file.

* Eric Meyers' CSS Reset
* HTML5 Shiv
* jQuery

During installation, Yo will ask you which version of jQuery you would like to install. The default is `jQuery#1.4.2`.

### Grunt
Yeoman will automatically set up Grunt to do the following:

* Compile your SASS
* Run CSSComb and Autoprefixer on your CSS files
* Serve your files locally at `localhost:9000`
* Enable LiveReload
* Optimize and Zip your images
* Build your project

#### Configuration
Feel free to modify and adjust the configuration of your Grunt tasks. You can do so by editing `gruntfile.js` in the root directory of your project. For simplicity, all of your directories can be edited at the top of the gruntfile in the `projectConfig` variable.

For more information on configuring Grunt tasks, see [here](http://gruntjs.com/configuring-tasks).

#### Development
While developing your project, simply run `grunt` from the shell in order to process your SASS and run CSSComb/Autoprefixr on your CSS once.

To have grunt do this automatically for you and enable LiveReload, run `grunt server` from your shell. This will set up your static server on port `9000`, watch your project for changes, and run the appropriate Grunt tasks.

It's usually easier to use a LiveReload extension. For more information on LiveReload, see [here](http://livereload.com/).

#### Deployment

When your project is complete, and you're ready to deploy, run `grunt build` from your shell. This will run all of the optimization tasks and build your project in the `build` directory. All of your deployment-ready files will be in the `build` directory.

## Release History

* 2013-04-02        v0.2.1          Updated the grunfile for easy configuration. 
                                    Also enabled live-reload to inject css into the document.
* 2013-02-24        v0.2.0          Switched from LESS processing to SASS processing.
* 2013-12-15		v0.1.1			Added HTML5 Shiv dependency for Bower.
* 2013-12-15		v0.1.0			Initial commit to Github.