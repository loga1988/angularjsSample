# Sample project for AngularJS

This project is an application skeleton for a typical [AngularJS][angularjs] web app. You can use it
to quickly bootstrap your angular webapp projects and dev environment for these projects.

Notes for AngularJS understanding

Directives in Angular :
defined as classes adding new elements to the DOM or modifying existing elements in the DOM -- ng-app, ng-controller, ng-repeat

Expressions for data binding to HTML

angularJS framework -- javascript based framework by extending HTML attributes with directives and doing data binding to HTML using expressions

Custom Directive

To register a custom directive, you use the module.directive API. module.directive takes the normalized directive name followed by a factory function. This factory function 
should return an object with the different options to tell $compile how the directive should behave when matched

Built-in Directives

Component Directives -- consists of the template
Structural Directives -- modify DOM layout by adding and subtracting DOM elements 
Attribute Directives -- change the appearance and behavior of another directive

Built in Angular Directives list 

ng-init
ng-disable
ng-switch
ng-style
ng-readonly
ng-repeat
ng-model
ng-bind
ng-if
ng-class
ng-for