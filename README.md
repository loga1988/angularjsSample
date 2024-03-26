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

one-way binding - changes in the data automatically update the UI, but changes in the UI do not automatically update the data

State -- contain data or information about the component  

class component -- this maintains their state 
functional component -- stateless doesn't maintain its state 

If we make standalone as true then it will not create the module file
standalone -- reducing the need for NGModules

render --> renders the html for a component

CORS -- Cross-Origin resource sharing policy is a mechanism for integrating application 
props --> to pass data between the components 

1) Angular update
   Node version
   Typescript version
   in tsconfig.json remove enableIvy. After v15, Ivy is the only rendering engine
   Update instances of TestBed.inject() that use an InjectFlags parameter to use an InjectOptions parameter. The InjectFlags parameter of TestBed.inject() is deprecated in v15


PS C:\Users\logbaran\workspace\sample-angular-app> ng new my-new-App
? Which stylesheet format would you like to use? SCSS   [ https://sass-lang.com/documentation/syntax#scss                ]
? Do you want to enable Server-Side Rendering (SSR) and Static Site Generation (SSG/Prerendering)? Yes
CREATE my-new-App/angular.json (3038 bytes)
CREATE my-new-App/package.json (1275 bytes)
CREATE my-new-App/README.md (1089 bytes)
CREATE my-new-App/tsconfig.json (936 bytes) -- configuration of the TypeScript compiler important parameters target,module 
CREATE my-new-App/.editorconfig (290 bytes)
CREATE my-new-App/.gitignore (590 bytes)
CREATE my-new-App/tsconfig.app.json (342 bytes)
CREATE my-new-App/tsconfig.spec.json (287 bytes)
CREATE my-new-App/server.ts (1759 bytes)
CREATE my-new-App/.vscode/extensions.json (134 bytes)
CREATE my-new-App/.vscode/launch.json (490 bytes)
CREATE my-new-App/.vscode/tasks.json (980 bytes)
CREATE my-new-App/src/main.ts (256 bytes)
CREATE my-new-App/src/favicon.ico (15086 bytes)
CREATE my-new-App/src/index.html (307 bytes)
CREATE my-new-App/src/styles.scss (81 bytes)
CREATE my-new-App/src/main.server.ts (271 bytes)
CREATE my-new-App/src/app/app.component.html (20239 bytes)
CREATE my-new-App/src/app/app.component.spec.ts (957 bytes)
CREATE my-new-App/src/app/app.component.ts (320 bytes)
CREATE my-new-App/src/app/app.component.scss (0 bytes)
CREATE my-new-App/src/app/app.config.ts (330 bytes)
CREATE my-new-App/src/app/app.routes.ts (80 bytes)
CREATE my-new-App/src/app/app.config.server.ts (361 bytes)
CREATE my-new-App/src/assets/.gitkeep (0 bytes)
√ Packages installed successfully.
warning: in the working copy of 'package-lock.json', LF will be replaced by CRLF the next time Git touches it
warning: in the working copy of 'package.json', LF will be replaced by CRLF the next time Git touches it
Successfully initialized git.


PS C:\Users\logbaran\workspace\sample-angular-app> ng new my-new-App-2 --standalone=false
? Which stylesheet format would you like to use? SCSS   [ https://sass-lang.com/documentation/syntax#scss                ]
? Do you want to enable Server-Side Rendering (SSR) and Static Site Generation (SSG/Prerendering)? Yes
CREATE my-new-App-2/angular.json (3249 bytes)
CREATE my-new-App-2/package.json (1281 bytes)
CREATE my-new-App-2/README.md (1090 bytes)
CREATE my-new-App-2/tsconfig.json (936 bytes)
CREATE my-new-App-2/.editorconfig (290 bytes)
CREATE my-new-App-2/.gitignore (590 bytes)
CREATE my-new-App-2/tsconfig.app.json (342 bytes)
CREATE my-new-App-2/tsconfig.spec.json (287 bytes)
CREATE my-new-App-2/server.ts (1782 bytes)
CREATE my-new-App-2/.vscode/extensions.json (134 bytes)
CREATE my-new-App-2/.vscode/launch.json (490 bytes)
CREATE my-new-App-2/.vscode/tasks.json (980 bytes)
CREATE my-new-App-2/src/main.ts (221 bytes)
CREATE my-new-App-2/src/favicon.ico (15086 bytes)
CREATE my-new-App-2/src/index.html (308 bytes)
CREATE my-new-App-2/src/styles.scss (81 bytes)
CREATE my-new-App-2/src/main.server.ts (71 bytes)
CREATE my-new-App-2/src/app/app-routing.module.ts (255 bytes)
CREATE my-new-App-2/src/app/app.module.ts (467 bytes)
CREATE my-new-App-2/src/app/app.component.html (20239 bytes)
CREATE my-new-App-2/src/app/app.component.spec.ts (1106 bytes)
CREATE my-new-App-2/src/app/app.component.ts (224 bytes)
CREATE my-new-App-2/src/app/app.component.scss (0 bytes)
CREATE my-new-App-2/src/app/app.module.server.ts (332 bytes)
CREATE my-new-App-2/src/assets/.gitkeep (0 bytes)
√ Packages installed successfully.
warning: in the working copy of 'package-lock.json', LF will be replaced by CRLF the next time Git touches it
warning: in the working copy of 'package.json', LF will be replaced by CRLF the next time Git touches it
warning: in the working copy of 'src/app/app.module.ts', LF will be replaced by CRLF the next time Git touches it
Successfully initialized git.

The TestBed is the most important of the Angular testing utilities. The TestBed creates a dynamically-constructed Angular test module that emulates an Angular @NgModule.

The TestBed.configureTestingModule() method takes a metadata object that can have most of the properties of an @NgModule.

To test a service, you set the providers metadata property with an array of the services that you'll test or mock.

TestBed.configureTestingModule({ providers: [ValueService] }); -- provide the service objects 
service = TestBed.inject(ValueService); -- mocking service object
