# Create a SearchBar component

Lets create our SearchBar
```
touch src/js/components/container/SearchBar.js
```
Add the following content

```
import React, { Component } from "react";
import ReactDOM from "react-dom";
class FormContainer extends Component {
  constructor() {
    super();   
  }
  render() {
    return (
      <form>
        <input type="search" placeholder="Search..." />
        <label>
          <input type="checkbox" />
          Only show products in stock
        </label>
      </form>
    );
  }
}
export default FormContainer;
```
