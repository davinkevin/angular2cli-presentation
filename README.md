# Presentation about AngularCLI

## Making your life EA-SI-ER !!!


## Hard to start (and re-start)

* JS Fatigue

* A lot of year ago : <script src="https://code.jquery.com/jquery-1.11.3.js"></script>
http://www.commitstrip.com/fr/2016/05/10/a-moment-of-nostalgia/

* 3 years ago : GruntJs
* 2 years ago : GulpJS
* 1 year ago : Webpack & JSPM

I just want to code !?!

In a project I work on now : 
* 2419 LOC for the APP
* 303 LOC for the build part

Thanks the Ember team :D


## What it can do for me ?

* Create a global folder structure to help you start project
* Generate assets and elements at the right place (CSS(or SASS, SCSS, LESS) | HTML | TS | SPEC)
* Write skeleton of my test
* Run my test at each modification / build
* Help me with my E2E test

### Live Demo : 
1. Create a project
    -> `ng new <project_name>`
2. Edit it
    -> Change the Hello world -> Hello AngularToulouse
3. Publish it on github
    -> `ng deploy:github`
4. Create a component <- Just for fun
    -> `ng g component shared/link`
    
5. Add a service <- To show the `shared folder`
    -> `ng generate service shared/time.service`
    * Serve a date from the service with `new Date()`;

6. show the `ng lint` <- TABS vs SPACE war

## Is it just another yeoman generator ?

* It can auto-complete your command line
    * Like Google Cloud (gcloud) or Git
* `ng doc` to check information about anything in angular
* Where is all my config... In the angular-cli.json (https://github.com/angular/angular-cli/blob/88c77d69275da9328b432c20b836364036792744/docs/design/ngConfig.md)


## What's next ?

* Upgrading against the style-guide
* Support for Javascript, Dart and/or maybe more ?
* Create its own `Template` (blue-print)
* Deploy on docker, or everywhere ! (https://github.com/angular/angular-cli/blob/88c77d69275da9328b432c20b836364036792744/docs/design/docker-deploy.md)
* Install directly from CLI 3rd Party libs

