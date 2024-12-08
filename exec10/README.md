## Redux Counter Application

The Redux Counter Application is a straightforward example of managing state using Redux. It demonstrates how Redux can be used to handle the state of a simple counter. Users can increment, decrement, and reset the counter with the help of Redux actions and state management.

---

### Features
- Increment the counter value.
- Decrement the counter value.
- Reset the counter value to 0.
- Leverages Redux for centralized state management.

---

### Key Redux Concepts Illustrated
This app demonstrates essential Redux principles, including:

#### 1. **State**
- The global state in Redux holds the counter value, which is shared and managed across the application.

#### 2. **Store**
- A Redux store is the central hub where the app's state resides, ensuring consistency in state updates.

#### 3. **Reducer**
- Reducers define how the state should change when specific actions are dispatched.

#### 4. **Action**
- Actions carry information describing how the state should change.

#### 5. **Dispatch**
- Dispatch sends actions to the Redux store to trigger state updates according to the reducer's logic.

#### 6. **Subscribe**
- Components automatically reflect state changes by using React-Redux hooks like `useSelector`.

---

### Application Workflow

#### **1. State**
- The application's state is managed globally and initialized with a `counter` key set to `0`. 
- This state is updated through the `counterReducer`.

#### **2. Store**
- The Redux store is set up using the `createStore` function.
- It can combine multiple reducers using `combineReducers` if needed.
- Integrates with Redux DevTools for efficient debugging.

#### **3. Actions**
- Actions are simple objects containing a `type` property to define state changes. This app uses the following actions:
  - **INCREMENT**: Increases the counter by 1.
  - **DECREMENT**: Decreases the counter by 1.
  - **RESET**: Resets the counter to 0.
- Action creators simplify the creation of these action objects.

#### **4. Reducer**
- The `counterReducer` updates the state based on the action type:
  - Incrementing, decrementing, or resetting the counter.
- Reducers ensure predictable and immutable state changes.

#### **5. Dispatch**
- The `dispatch` method triggers actions, updating the Redux store based on the reducer's logic.
- In React, the `useDispatch` hook is used to call `dispatch`.
- For example:
  - Clicking "Increment" triggers `dispatch(increment())`, sending the `INCREMENT` action to the store.

