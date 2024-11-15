# ` RTK (Redux Tool-Kit)`

`Makes RR job easier`

## `Basic steps: `

### `Install RTK`

```
npm install @reduxjs/toolkit react-redux
```

### `Create a slice `

- Create a slice with a. name, b. state, c. reducers

```
import { createSlice } from '@reduxjs/toolkit';

const counterSlice = createSlice({
  name: 'counter',
  initialState: {
    value: 0,
  },
  reducers: {
    increment: (state) => {
      state.value += 1;
    },
    decrement: (state) => {
      state.value -= 1;
    },
    incrementByAmount: (state, action) => {
      state.value += action.payload;
    },
  },
});

export const { increment, decrement, incrementByAmount } = counterSlice.actions;

export default counterSlice.reducer;
```

### `Configure the Store`

```
import { configureStore } from '@reduxjs/toolkit';
import counterReducer from '../features/counter/counterSlice';

export const store = configureStore({
  reducer: {
    counter: counterReducer,
  },
});

export default store;
```

### `Provide the Store to Your App`

```
import React from 'react';
import ReactDOM from 'react-dom';
import { Provider } from 'react-redux';
import App from './App';
import store from './app/store';

ReactDOM.render(
  <Provider store={store}>
    <App />
  </Provider>,
  document.getElementById('root')
);
```

### `Redux State and Dispatch Actions in a Component`

```
import React, { useState } from 'react';
import { useSelector, useDispatch } from 'react-redux';
import { increment, decrement, incrementByAmount } from './counterSlice';

const Counter = () => {
  const count = useSelector((state) => state.counter.value);
  const dispatch = useDispatch();
  const [incrementAmount, setIncrementAmount] = useState(0);

  return (
    <div>
      <h1>Counter: {count}</h1>
      <button onClick={() => dispatch(increment())}>Increment</button>
      <button onClick={() => dispatch(decrement())}>Decrement</button>
      <input
        type="number"
        value={incrementAmount}
        onChange={(e) => setIncrementAmount(Number(e.target.value))}
      />
      <button onClick={() => dispatch(incrementByAmount(incrementAmount || 0))}>
        Increment by Amount
      </button>
    </div>
  );
};

export default Counter;
```
