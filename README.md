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
  <li>
<ol>
