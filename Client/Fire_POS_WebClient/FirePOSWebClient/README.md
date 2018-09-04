# FirePOSWebClient

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 6.0.0.

## Development server

A good guideline to follow is to split our application into at least three different modules — Core, Shared and Feature

CoreModule
All services which have to have one and only one instance per application (singleton services) should be implemented here. Typical example can be authentication service or user service. Let’s look at an example of CoreModuleimplementation.

SharedModule
All the “dumb” components and pipes should be implemented here. These components don’t import and inject services from core or other features in their constructors. They should receive all data though attributes in the template of the component using them. This all sums up to the fact that SharedModule doesn’t have any dependency to the rest of our application.

FeatureModule
We are going to create multiple feature modules for every independent feature of our application. Feature modules should only import services from CoreModule. If feature module A needs to import service from feature module B consider moving that service into core.

LazyLoading
We should lazy load our feature modules whenever possible. Theoretically only one feature module should be loaded synchronously during the app startup to show initial content. Every other feature module should be loaded lazily after user triggered navigation.



## Code scaffolding

Run `ng generate component component-name` to generate a new component. You can also use `ng generate directive|pipe|service|class|guard|interface|enum|module`.

## Build

Run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory. Use the `--prod` flag for a production build.

## Running unit tests

Run `ng test` to execute the unit tests via [Karma](https://karma-runner.github.io).

## Running end-to-end tests

Run `ng e2e` to execute the end-to-end tests via [Protractor](http://www.protractortest.org/).

## Further help

To get more help on the Angular CLI use `ng help` or go check out the [Angular CLI README](https://github.com/angular/angular-cli/blob/master/README.md).
