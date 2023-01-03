# Angular_interview

## Table of Contents


* [RxJS Questions](#rxjs-questions)
* [Decorator Questions](#decorator-questions)
* [Directive Questions](#directive-questions)
* [Component Questions](#component-questions)


#### RxJS Questions:
 1. What is Observable?
    - Observable offers support for passing messages between parts of your application. They are used repeatedly in Angular and are the appropriate technique for event handling, asynchronous programming, and handling multiple values.
    - Observables are declarative in that you define a function for releasing values, but it is not executed till a consumer subscribes to it. The subscribed consumer then receives notifications before the function completes, or before they unsubscribe
    - Observable represents the idea of an invokable collection of future values or events.
    ###### IN ANGULAR
    - The HTTP module uses observables to handle AJAX requests and responses
    - The Router and Forms modules use observables to listen for and respond to user-input events
    - An observable can have multiple observers.
    ###### Lifecycle of Observable
    - Creation
    - Subscription
    - Execution
    - Destruction
  
2. What is Observers?
   - Observer is a set of callbacks that know how to listen to the values of the Observable.
   - Observer subscribes to the observable to receive the stream.
   - RxJS observer is simply set of callback(next,error,complete)
   - It is an object that specifies callback methods to handle the three types of notifications which is an observable can send:
      -  **Next**: Next notification is required as a handler for every delivered value called zero or greater times after execution starts.
      -  **Error**: Error notification is an optional. It is a handler used for error notification called zero or greater execution of the observable instance.
      -  **Complete**: Complete notification is optional. It is a handler used for the execution of complete notification. Delayed values can keep being delivered to the next handler after execution is complete.

3. What is Subscription?
   - Subscription is an observable execution
   - Subscriptions are objects returned when an Observable is subscribed.
   - Subscription is useful mainly to cancel the execution
   -  An Observable instance starts publishing values only when anyone subscribes to it. You subscribe by calling the method subscribe () of the instance, passing an observer to receive the notifications.
  
4. What is stream in RxJs?
   - Stream in RxJs is asynchronous data emitted from observables.
   - Stream is basically a sequence of data value over time.
6. What is Subject?
   - Subjects are special types of Observers, so you can also subscribe to other Observables and listen to published data
   - The values are multicasted to many Observers
   - There are two types of Subjects : BehaviorSubject and ReplaySubject.
7. What are operators in RxJs?

   Operators are logics which manipulate an observable stream and create new observable streams.An RxJS operator is simply a function which takes a source observable as an input and returns a resulting stream.

#### Decorator Questions:

8. What is metadata?

    Metadata is used to decorate a class so that it can configure the expected behavior of the class.The whole purpose of Angular decorators is to store metadata about a class, method, or property. When you configure a component, you are providing a metadata for that class that tells Angular that you have a component, and that component has a specific configuration.

9. What is decorator?

   An angular decorator are function or design pattern,which using we attach metadata to a class decoration,method property or parameter
   
   - If you decorate “@Component” on the class the class is treated as Angular component
   - If you decorate “@NgModule” on the class it becomes a AngularModule
   - **Types of decorator**
     1. Method Decorator - @HostListener
     2. Class Decorator - @NgModule,@Component,@Injectable,@Directive,@Pipe
     3. Parameter Decorator - @Inject,@Host,@Self,@SkipSelf,@Optional
     4. Parameter Decorator - @Input,@Output,@ContentChild & @ContentChildren,@ViewChild & @ViewChildren,@HostBinding

#### Directive Questions:

10. What is directive?[example code link here](https://stackblitz.com/edit/angular-ivy-jq9ojr?file=src/app/app-parent/app-parent.component.html)
    - A directive is a class in Angular that is declared with a @Directive decorator.
    - Every directive has its own behaviour and can be imported into various components of an application.
    - **Types of directives:**
    
      1. **Component directives** 
        - These form the main class in directives. Instead of @Directive decorator we use @Component decorator to declare these directives. These directives have a view, a stylesheet and a selector property.
        - Directives with templates.It’slike a user control.
        
      2. **Structural directives**
        - Change the DOM layout by adding and removing elements.
        - Every structural directive has a ‘ * ’ sign before them.
        - We can apply these directives to any DOM element.
          
          ****ngIf is used to check a boolean value and if it’s truthy,the div element will be displayed.***
          <br>
          ****ngFor is used to iterate over a list and display each item of the list.***
          
      3. Attribute Directives
        - Change the appearance and behaviour of HTML elements.
        - For example, ngStyle( applying styles) or ngClass(applying CSS classes).
  
 11. What is **ng-content**?
     - The ng-content is used when we want to insert the content dynamically inside the component that helps to increase component reusability. Using ng-content we can pass content inside the component selector and when angular parses that content that appears at the place of ng-content.
     - ng-content is used to display children in a template
     - When we need to pass multiple things inside the component selector then we have to provide them unique selector either any id or class so using that unique selector we can access particular content inside the ng-content. So here “select” inside the ng-content is used to take content with matching class name app or app1.
     
 12. What is the difference between **ng-template** and **ng-container**?[example code link here](https://stackblitz.com/edit/angular-ivy-bw1u9f?file=src/app/app.component.html)
 
     ###### ng-template
    
     - The <ng-template> is a template element that Angular uses with structural directives ( *ngIf , *ngFor , [ngSwitch] and custom directives)
     - These template elements only work in the presence of structural directives, which help us to define a template that doesn’t render anything by itself, but conditionally renders them to the DOM.
     -  It helps us create dynamic templates that can be customized and configured.
     ```
             <div> 
                Ng-template Content 
                <div *ngIf=”false else showNgTemplateContent”> 
                   Shouldn't be displayed 
                </div>
             </div>
 
           <ng-template #showNgTemplateContent>
              Should be displayed
           </ng-template>
     ```
     
      ###### ng-container
      - ng-container is an extremely simple directive that allows you to group elements in a template that doesn’t interfere with styles or layout because Angular doesn’t put it in the DOM
      - ng-container is used as a non-rendered container to avoid having to add a span or div.
      - we can use <ng-container> without adding any extra element to the DOM at runtime.
      ```
         <ng-container *ngIf="details">
           <div *ngFor="let info of details">
             {{ info.content }}
           </div>
        </ng-container>
      ```
     

#### Component Questions:

12. What is data binding in Angular?
    
    Data binding is one of the most significant and effective elements for creating communication between the DOM and the component.
    
    **There are Four types of Data binding in Angular:**
    
    1. Property Binding []</b> :  Data flows from component to the view
    2. Expression / Interpolation{{}}</b> : Data flows from componentto the view and we can mix the samewith HTMLtags
    3. Event Binding ()</b> : When you want to send event from the view to the component.
    4. Two-waybinding [()] </b> : Data flows from component to the view and vice versa.
 
13. Explain Components?
    
    In Angular, components are the basic building blocks, which control a part of the UI for any application.A component is defined using the **@Component** decorator.Every component consists of three parts, the template which loads the view for the component, a stylesheet which defines the look and feel for the component, and a class that contains the business logic for the component.


14. What is the difference between a component and a directive?

    | Components | Directive |
    | ------------- | ------------- |
    | To register a component we use @Component meta-data annotation. | To register directives we use @Directive meta-data annotation. |
    | Component is a directive which uses shadow DOM to create encapsulated visual behavior called components. Components are typically used to create UI widgets. | Directive is used to add behavior to an existing DOM element. |
    | Component is used to break up the application into smaller components. | Directive is use to design re-usable components. |
    | Only one component can be present per DOM element. | Many directives can be used per DOM element. |
    | @View decorator or templateurl template are mandatory in the component. | Directive doesn't use View. |

15. How does  share data between two components in Angular?
    - Parent to Child: Sharing Data via Input
 
      This is probably the most common and straightforward method of sharing data. It works by using the @Input() decorator to allow data to be passed via the template.
   
    - Child to Parent: Sharing Data via ViewChild
   
      ViewChild allows a one component to be injected into another, giving the parent access to its attributes and functions. One caveat, however, is that child won’t be available until after the view has been initialized. This means we need to implement the AfterViewInit lifecycle hook to receive the data from the child.
      
     - Child to Parent: Sharing Data via Output() and EventEmitter
     
        Another way to share data is to emit data from the child, which can be listened to by the parent. This approach is ideal when you want to share data changes that occur on things like button clicks, form entires, and other user events.In the child, we declare a  variable with the Output decorator and set it equal to a new event emitter
        
     - Unrelated Components: Sharing Data with a Service
       
       When passing data between components that lack a direct connection, such as siblings, grandchildren, etc, you should have a shared service. When you have data that should aways been in sync, I find the RxJS BehaviorSubject very useful in this situation.
       
       You can also use a regular RxJS Subject for sharing data via the service, but here’s why I prefer a BehaviorSubject.
         
         - It will always return the current value on subscription - there is no need to call onnext
         - It has a getValue() function to extract the last value as raw data.
         -  ensures that the component always receives the most recent data.





14. Explain Module?

    A module is a place where we can group components, directives, services, and pipes. Module decides whether the components, directives, etc can be used by other modules, by exporting or hiding these elements. Every module is defined with a **@NgModule** decorator.
    
    **By default, modules are of two types:**
    1. Root Module - Every application can have only one root module.A root module imports BrowserModule.
    2. Feature Module - It can have one or more feature modules.A feature module imports CommonModule.
    

13. Explain Service?
    
    Angular services are objects that get instantiated just once during the lifetime of an application. They contain methods that maintain data throughout the life of an application, i.e., data is available all the time. The main objective of a service is to organize and share business logic, models, or data and functions with different components of an Angular application. A service can be written once and injected into multiple components,by using dependency injection,into the component's constructor.
    
    ***Note***
    1. Services avoid rewriting of code. A service can be written once and injected into all the components that use that service.
    2. A service could be a function, variable, or feature that an application needs.
 

