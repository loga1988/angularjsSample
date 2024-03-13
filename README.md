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

Angular Framework Notes



LifeCycle Hook Events

ngOnChanges  -- when angular sets or resets data-bound input properties
ngOnInit -- Initialize the component and first displays the data-bound properties and sets the input properties
ngDoCheck -- few changes cannot be detected by angular on its own those changes can be detected by this hook event
ngAfterContentInit-- external content into the components view 
ngAfterContentChecked -- checks the external content projected into the components view 
ngAfterViewInit -- Respond after Angular initializes the component's views and child views
ngAfterViewChecked -- Respond after Angular checks the component's views and child views
ngOnDestroy -- Cleanup just before Angular destroys the directive or component primarily unsubscribe Observabes

Encapsulation -- components style encapsulated in component hist element which makes it not to impact the rest of the application 
 i) ViewEncapsulation.ShadowDom
 ii) ViewEncapsulation.Emulated
 iii) ViewEncapsulation.None

 @Input -- passes value from parent to child component
 @Output -- passes value from child to parent 

 Observable -- emits values asynchronously over time . This helps to subscribe data returned by service methods 
 Interpolation -- Interpolation refers to embedding expressions into marked up text
 


 Component Styles
 When you define the component template we can define the component style as well 
Ex:  @Component({
  selector: 'app-root',
  template: `
    <h1>Tour of Heroes</h1>
    <app-hero-main [hero]="hero"></app-hero-main>
  `,
  styles: ['h1 { font-weight: normal; }']
})
export class HeroAppComponent {
/* . . . */
}

Dependency Injection -- mechanism for creating and delivering some parts of an application to other parts of an application that require them

react -- one way binding, virtual DOM, Typescript
angular -- two way binding, Real DOM, Javascript

virtual DOM -- memory representation of Real DOM

REACT interview questions 

State -- contain data or information about the component  

class component -- this maintains their state 
functional component -- stateless doesn't maintain its state 

render --> renders the html for a component

CORS -- Cross-Origin resource sharing policy is a mechanism for integrating application 
props --> to pass data between the components 
