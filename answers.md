# React Review 3

### 1. Import a Component

App.jsx

```jsx
import Gallery from './components/Gallery.jsx';

```

### 2. Object Destructuring

```jsx
const props = {
  name: 'English Breakfast',
  temperature: 99,
  type: 'Black Tea',
  origin: 'India',
  steepTime: 3, // in minutes
  caffeineContent: 40, // in mg per serving
  flavorNotes: ['Malty', 'Robust'],
  isOrganic: false,
  packaging: 'Tea Bags',
  price: 5.99, // in USD
  stockQuantity: 100,
  rating: 4.5, // out of 5
};

const { name, packaging, temperature } = props;


```

### 3. State in React

State uses internal data to store that data you can use in your components. Anything that changes on your website is considered state and does not reload the page but it re-renders the components. 

### 4. Using state in React

```jsx
import { useState } from 'react';

function Tea(props) {
  const [ isBrewing, setState ] = useState(true);

}
```

Inside the `<Tea />` component, add state that captures whether the Tea is currently brewing.
When the component is first rendered, the brewing state should be `true`.

### 5. Connect the handler

There is an unconnected handler called `checkTime` in the `Tea` component. Connect it to an
appropriate element inside the component.

```jsx
import { useState } from "react";

function Tea(props) {
  const checkTime = () => { props.steepTime > props.startTime ? alert("TEA IS DONE!"); }

  return <>
    <h1>Tea Time</h1>
    <button onClick={checkTime}>Check if tea is ready</button>
  </>
}
```