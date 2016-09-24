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
    -> `ng new <project_name> --style=scss`
2. Edit it
    -> Change the Hello world -> Hello AngularToulouse
3. Publish it on github
    -> `ng deploy:github`
4. Create a component
    -> `ng generate component shared/custom`
5. Show the evolution of `app.module.ts`
6. Use the `<custom></custom>` in the `app.component.html` and show it
7. Remove the `<custom></custom>` from html
8. Add a service with `ng g service shared/time --flat false`
    * Serve a date from the service with 
    ```
    getNow(): string {
        return new Date().toString();
      }
    ```
9. Inject the service inside the constructor of the `app.component.ts`
10. Go back to CLI to show the warning message
11. Import the service into the `app.module.ts`
      - with `import {TimeService} from './shared/time/time.service';`
      - with `providers: [TimeService],`
12. Change the value `title` inside the `ngOnInit` to become 
 ```
 ngOnInit(): void {
     this.title = this.timeService.getNow();
   }
 ```
13. I want a specific format, and handle more type of date... so install moment
       - with `npm install moment --save`
14. Import moment in the `TimeService` :
       - with `import * as moment from 'moment';`
15. Change the return of the method `getNow` by : 
    ```
    return moment().format('MMMM Do YYYY, h:mm:ss a');
    ```
16. Simple with only behavior, I want now the material design element
        - Go to the `https://github.com/angular/material2/blob/master/GETTING_STARTED.md`
        - install with `npm install --save @angular2-material/core @angular2-material/button @angular2-material/card`
17. Import into `app.module.ts` : 
         - with `import { MdButtonModule } from '@angular2-material/button';`
         - with `import { MdCardModule } from '@angular2-material/card';`
         - and `imports: [BrowserModule, FormsModule, HttpModule, MdButtonModule.forRoot(), MdCardModule.forRoot()],`
18. Change the file `app.component.html`
         ```
         <div class="container">
           <md-card>
             <md-card-subtitle>Fantastique carte</md-card-subtitle>
             <md-card-title>La date du jour !</md-card-title>
             <md-card-content>
               <p>{{ title }}</p>
             </md-card-content>
           </md-card>
         </div>
         ```
19. Add some scss to the file `app.component.scss`
     ```
     .container {
       width: 400px
     }
     ```
20. Add the AngularToulouse logo in `src/assets/` and add to the template
    -> <img md-card-image src="assets/logo.jpg">
    

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
* Hook to integrate with build system
