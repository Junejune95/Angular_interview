# Angular_interview

<ol>
  <li>
    <b>What is Observable?</b>
    <ul>
      <li>Observable offers support for passing messages between parts of your application. They are used repeatedly in Angular and are the appropriate technique for event handling, asynchronous programming, and handling multiple values.</li>
         <li>Observables are declarative in that you define a function for releasing values, but it is not executed till a consumer subscribes to it. The subscribed consumer then receives notifications before the function completes, or before they unsubscribe</li>
      <li>Observable represents the idea of an invokable collection of future values or events.</li>
      <b>#IN ANGULAR</b>
      <li>
        The HTTP module uses observables to handle AJAX requests and responses
      </li>
      <li>The Router and Forms modules use observables to listen for and respond to user-input events</li>
      <li>An observable can have multiple observers.</li>
      <b> #Lifecycle of Observable</b>
      <li>Creation</li>
      <li>Subscription</li>
      <li>Execution</li>
      <li>Destruction</li>
    </ul>
  </li>
  <li>
    <b>What is Observers?</b>
    <ul>
      <li>
        Observer is a set of callbacks that know how to listen to the values of the Observable.
      </li>
      <li>
        observer subscribes to the observable to receive the stream.
      </li>
      <li>
      RxJS observer is simply set of callback(next,error,complete)
      </li>
      <li>
        It is an object that specifies callback methods to handle the three types of notifications which is an observable can send:
        <ol>
          <li>
            Next: Next notification is required as a handler for every delivered value called zero or greater times after execution starts.
          </li>
          <li>
            Error: Error notification is an optional. It is a handler used for error notification called zero or greater execution of the observable instance.
          </li>
          <li>
            Complete: Complete notification is optional. It is a handler used for the execution of complete notification. Delayed values can keep being delivered to the next handler after execution is complete.
          </li>
        </ol>
      </li>
    </ul>
  </li>
  <li>
    What is Subscription?
    <ul>
      <li>
        Subscription is an observable execution
      </li>
      <li>
        Subscriptions are objects returned when an Observable is subscribed.
      </li>
      <li>
        Subscription is useful mainly to cancel the execution
      </li>
      <li>
        An Observable instance starts publishing values only when anyone subscribes to it. You subscribe by calling the method subscribe () of the instance, passing an observer to receive the notifications.
      </li>
    </ul>
  </li>
  <li>
    <b>What is stream in RxJs?</b>
    <ul>
      <li>Stream in RxJs is asynchronous data emitted from observables.</li>
      <li>Stream is basically a sequence of data value over time.</li>
    </ul>
   </li>
    <li>
      <b>What is Subject?</b>
      <ul>
        <li>
        Subjects are special types of Observers, so you can also subscribe to other Observables and listen to published data
        </li>
        <li>
          he values are multicasted to many Observers
        </li>
        <li>There are two types of Subjects : BehaviorSubject and ReplaySubject.</li>
        <b>ReplaySubject :</b>
        <ul>
          <li>
          . If you want to have the last value replayed to an observer, even if a Subject is already closed, use the ReplaySubject
          </li>
         </ul>
      </ul>
  </li>
      <li>
        What are operators in RxJs?
        <ul>
          <li>
          Operators are logics which manipulate an observable stream and create new observable streams.
          </li>
          <li>
            
An RxJS operator is simply a function which takes a source observable as an input and returns a resulting stream.
          </li>
        </ul>
  </li>
 <li>
   <b>What is metadata?</b><br>
 Metadata is used to decorate a class so that it can configure the expected behavior of the class.
The whole purpose of Angular decorators is to store metadata about a class, method, or property. When you configure a component, you are providing a metadata for that class that tells Angular that you have a component, and that component has a specific configuration.
 </li>
  <li>
       <b>What is decorator?</b><br>
    An angular decorator are function or design pattern,which using we attach metadata to a class decoration,method property or parameter.
    <br>
    -If you decorate “@Component” on the class the class is treated as Angular component<br>
    -If you decorate “@NgModule” on the class it becomes a AngularModule<br>
  </li>
<ol>
