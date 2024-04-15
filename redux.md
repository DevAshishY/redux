## Questions

**# T1 redux toolkit**

      * State Management: Redux manages application state efficiently.
      * Centralized State Store: All application data is stored in a single place called the store.
      * Predictable Data Flow: Follows a strict unidirectional data flow pattern for better predictability.
      * Functional Programming: Emphasizes pure functions for state manipulation.
      * Immutability: Encourages state updates by creating new copies to maintain data integrity.
      * Middleware: Allows extending Redux's capabilities, like handling asynchronous actions.
      * Developer Tools: Provides tools for debugging and inspecting application state and actions.



------------------------------------------

**# T2 Benefit of redux**

      * Prop Drilling Resolution: Eliminates the need to pass props through multiple components.
      * Centralized State Management: Maintains all application data in a single, easily accessible store.
      * Performance Optimization: Optimizes re-rendering by efficiently managing state updates.
      * Storing Long-Term Data: Facilitates storing data persistently, aiding in managing session or user-specific information.
   

------------------------------------------
**# T3 redux toolkit points**

      * Store:
      
      Centralized location for storing application state.
      Single store per application.
      Reducer needs to be specified to define how state changes in response to actions.
      
      * createSlice:
      Utility function for creating Redux slices, which includes reducer functions and action creators.
      
      *  Reducer:
      Function that specifies how the application's state changes in response to actions.
      Pure functions that take the current state and an action, and return the new state.
      
      *  Action:
      Function returning an action object containing action type and data.
      Facilitates communication between components and the store.
      Actions trigger state changes in the store.
      
      *  useSelector:
      React hook used to extract data from the Redux store state.
      Selects part of the data stored in the Redux store, and subscribes to updates.
      
      *  useDispatch:
      React hook used to dispatch actions to the Redux store.
      Provides a way to dispatch actions from within functional components.
      
      *  Dispatcher:
      Central hub of the application where actions are received and payload is broadcasted to registered callbacks.
      Responsible for sending actions to the reducers to update the state in the store.

------------------------------------------

**# T5 Redux toolkit flow**

      **Step I:** Install Redux Toolkit
      
      Install Redux Toolkit and React Redux packages using npm: npm i @reduxjs/toolkit react-redux
      
      **Step II:** Configure the Store
      
      Set up the Redux store to manage application state.
      
      **Step III:** Provide the Store in React App
      
      Ensure that the Redux store is available to the entire React application by providing it at the top level, typically in the <Provider> component from React Redux.
      
      **Step IV:** Create a Slice in the Store Folder
      
      Define a slice in the store folder, which includes actions and a reducer. This slice represents a portion of the application state.
      
      **Step V:** Adding the useDispatch & useSelector Hooks
      
      Utilize the useDispatch hook to dispatch actions and the useSelector hook to select data from the Redux store.
      
      **Step VI:** Import Slice in the Store
      
      Import the created slice into the Redux store to include its actions and reducer in the overall application state management.
  

------------------------------------------

**# T6 What is Flux Concept In React?**

    facebook widely uses flux architecture concept for developing client-side web applications. It is not a framework or a library. It is simply a new kind of 
    architecture that complements React and the concept of Unidirectional Data Flow. 

------------------------------------------
**# T7 handling asynchronous calls in Redux**

          **Redux Thunk:**
          
          Uses middleware to intercept dispatched functions, allowing for asynchronous logic.
          Action creators return functions instead of plain objects, enabling asynchronous operations.
          Well-suited for simpler async flows and integration with existing Redux codebases.
          
          **Redux Promise:**
          
          Middleware that allows action creators to return promises.
          Actions are dispatched when promises resolve or reject.
          Simplifies handling asynchronous actions with straightforward promise-based logic.
          
          **Redux Saga:**
          
          Uses middleware and generator functions to manage side effects.
          Provides a more complex but powerful approach to handling asynchronous actions.
          Offers fine-grained control over async flows, including cancellation and complex orchestration.

------------------------------------------
**# T8 what is redux thunk**

          Redux Thunk is a middleware for Redux that allows you to write action creators that return functions instead of plain action objects. These functions can perform asynchronous operations, such as API calls or dispatching multiple actions sequentially, before dispatching the final action to update the Redux store. Thunk middleware intercepts these functions, enabling them to interact with the store, dispatch additional actions, or perform async logic. It's a popular choice for handling asynchronous behavior in Redux applications due to its simplicity and compatibility with existing Redux codebases.

------------------------------------------
**# T9 connect and mapStateToProps and mapdispatchToprops**
          
              The connect() function connects a React component to a Redux store.
              It provides its connected component with the pieces of the data it needs from the store, and the functions it can use to dispatch actions to the store.
          
              function connect(mapStateToProps?, mapDispatchToProps?, mergeProps?, options?)
          
          connect() Parameters:accepts four different parameters, all optional. By convention, they are called:
          
          
          mapStateToProps?: Function
          mapDispatchToProps?: Function | Object
          mergeProps?: Function
          options?: Object
          
          **mapStateToProps**
               If a mapStateToProps function is specified, the new wrapper component will subscribe to Redux store updates. This means that any time the store is updated, mapStateToProps will be called. The results of mapStateToProps must be a plain object, which will be merged into the wrapped component’s props. If you don't want to subscribe to store updates, pass null or undefined in place of mapStateToProps.
          
          **mapDispatchToProps**
          Conventionally called mapDispatchToProps, this second parameter to connect() may either be an object, a function, or not supplied.
          
          Your component will receive dispatch by default, i.e., when you do not supply a second parameter to connect():
------------------------------------------
**# T10 redux flow**

    Single Source of Truth:
    In Redux, the entire application state is stored in a single JavaScript object known as the store. This means that all of your application's data resides in one central location. For instance, imagine you're building a social media application. The store would contain information about the current user, posts, comments, likes, etc. Having a single source of truth simplifies debugging and makes it easier to manage application state.

    State is Read-Only:
    In Redux, you cannot directly modify the application state. The only way to change the state is by dispatching actions. Actions are simple objects that describe what happened in the application (e.g., user clicked a button, data received from the server, etc.). Reducers are functions responsible for specifying how the state should change in response to an action. They take the current state and an action as arguments and return the next state. This principle ensures predictability and easier debugging since state changes are isolated to reducers.

    Changes are Made with Pure Functions.

    Reducers in Redux are pure functions, meaning they produce the same output for a given input and have no side effects. Given the same input (state and action), a reducer will always produce the same output (new state). This predictability simplifies testing and reasoning about state changes. For example, if you have a reducer that increments a counter, it will always return the incremented value based on the current state and action, without modifying the original state object.

------------------------------------------
**# T11 explain the differences between `connect()` and `useSelector()`**

    React-Redux, showcasing my understanding of both class-based and functional component approaches to accessing Redux state.

------------------------------------------



## Example


**# T1 redux toolkit**

https://codesandbox.io/p/sandbox/redux-toolkit-5xjlxn 

------------------------------------------

**# T2**



------------------------------------------


