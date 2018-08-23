# React

## Key terms

### Component

A function that returns an element.

### Class Component

### Functional Component

### Element

A 'thing' to be shown on the page. e.g. A h1 tag containing some text is an example of an element.

```
const myElement = <h1>Explaining the cosmos with cheetos</h1>
```

### Render

### State

State is data which is owned and manipulated by one component. It is not accessible to any other components. If a component needs to, it may pass some of it's state to a child component as props.

### Props

Props are properties for an element, e.g. words to be substituted into templates, CSS class names, image urls. They're the variables. Components must not mutate their props! This is one of the golden rules of React.

### Unidirectional data flow

Because state is held by one component, and it can only pass the data down to its children, data must always flow "down" the tree.

### ReactDOM

### JSX
