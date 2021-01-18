# Test Angular App

1. In tsconfig.json add to compilerOptions :  {      
...
"allowJS" :true,
...
}

2. To use custom elememnts add in @NgModule configuration and import fromm @angular/core: 
{...
    schemas:[CUSTOM_ELEMENTS_SCHEMA],
...
}
3. For polyfills do npm install --save @webcomponents/webcomponentsjs

4. add this to assests in angular.json 
"assets":[
    ...
    {
               "glob": "**/*.js",
               "input": "node_modules/@webcomponents/webcomponentsjs",
               "output": "webcomponets/"
             },
    ...
]

5. add this in head of index.html
...
 <script src="webcomponents/webcomponents-loader.js"></script>
  <script>
   if (!window.customElements){document.write('<!--');}
  </script>
  <script src="webcomponents/custom-elements-es5-adapter.js"></script>
...

6. Do   $  npm install custom-table-1.0.0.tgz

first take the file into your app 


7. import into app.component.ts and use in app.component.html


This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 11.0.7.

## Development server

Run `ng serve` for a dev server. Navigate to `http://localhost:4200/`. The app will automatically reload if you change any of the source files.

## Code scaffolding

Run `ng generate component component-name` to generate a new component. You can also use `ng generate directive|pipe|service|class|guard|interface|enum|module`.

## Build

Run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory. Use the `--prod` flag for a production build.

## Running unit tests

Run `ng test` to execute the unit tests via [Karma](https://karma-runner.github.io).

## Running end-to-end tests

Run `ng e2e` to execute the end-to-end tests via [Protractor](http://www.protractortest.org/).

## Further help

To get more help on the Angular CLI use `ng help` or go check out the [Angular CLI Overview and Command Reference](https://angular.io/cli) page.
