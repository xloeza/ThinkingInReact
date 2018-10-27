# 14 Adding data

lets add some static data to our Web Application

[
  {category: "Sporting Goods", price: "$49.99", stocked: true, name: "Football"},
  {category: "Sporting Goods", price: "$9.99", stocked: true, name: "Baseball"},
  {category: "Sporting Goods", price: "$29.99", stocked: false, name: "Basketball"},
  {category: "Electronics", price: "$99.99", stocked: true, name: "iPod Touch"},
  {category: "Electronics", price: "$399.99", stocked: false, name: "iPhone 5"},
  {category: "Electronics", price: "$199.99", stocked: true, name: "Nexus 7"}
];

Lets add this array to the FormContainer

```
import React, { Component } from "react";
import ReactDOM from "react-dom";
import SearchBar from "./SearchBar"
import ProductTable from "./ProductTable"

class FormContainer extends Component { 

  render() { 
    let products = [
      {category: "Sporting Goods", price: "$49.99", stocked: true, name: "Football"},
      {category: "Sporting Goods", price: "$9.99", stocked: true, name: "Baseball"},
      {category: "Sporting Goods", price: "$29.99", stocked: false, name: "Basketball"},
      {category: "Electronics", price: "$99.99", stocked: true, name: "iPod Touch"},
      {category: "Electronics", price: "$399.99", stocked: false, name: "iPhone 5"},
      {category: "Electronics", price: "$199.99", stocked: true, name: "Nexus 7"}
    ];

    return (
      <form id="search-form">
          <SearchBar />
          <ProductTable products={products} />
      </form>
    );
  }
}
export default FormContainer;
const wrapper = document.getElementById("create-search-form");
wrapper ? ReactDOM.render(<FormContainer />, wrapper) : false;

```
File ProductTable.js

________________________________________________________

```

import React, { Component } from "react";
import ReactDOM from "react-dom";
class ProductTable extends Component {
  constructor() {
    super();
  }
  render() {
    let {products} = this.props;
    return (
      <table class="table table-striped">
        <thead>
          <tr>
            <th scope="col">Category</th>  
            <th scope="col">Name</th>
            <th scope="col">Price</th>
          </tr>
        </thead>
        <tbody>
            {products.map( product => (
                <tr>
                    <td>{product.category}</td>
                    <td>{product.price}</td>
                    <td>{product.name}</td>
                </tr>
            ))}
        </tbody>
      </table>
    );
  }
}
export default ProductTable;
```
