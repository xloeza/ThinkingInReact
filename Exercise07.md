# Install React

React makes it painless to create interactive UIs. Design simple views for each state in your application, and React will efficiently update and render just the right components when your data changes.

Build encapsulated components that manage their own state, then compose them to make complex UIs.Since component logic is written in JavaScript instead of templates, you can easily pass rich data through your app and keep state out of the DOM.

React Example:
```
class HelloMessage extends React.Component {
  render() {
    return (
      <div>
        Hello {this.props.name}
      </div>
    );
  }
}

ReactDOM.render(
  <HelloMessage name="Taylor" />,
  mountNode
);
```

React components implement a render() method that takes input data and returns what to display. This example uses an XML-like syntax called JSX. Input data that is passed into the component can be accessed by render() via this.props.
JSX is optional and not required to use React. Try the Babel REPL to see the raw JavaScript code produced by the JSX compilation step.

Execute the following command
```
npm i react react-dom --save
npm i prop-types --save
```
