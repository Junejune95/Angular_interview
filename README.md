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
<ol>
