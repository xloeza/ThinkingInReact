# 15 Filtering by Category

Lets update our file FormContainer and add the following content

```
import React, { Component } from "react";
import ReactDOM from "react-dom";
import SearchBar from "./SearchBar"
import ProductTable from "./ProductTable"

class FormContainer extends Component { 
  constructor() {
    super();
    let products = [
      {id:1, category: "Sporting Goods", price: "$49.99", stocked: true, name: "Football", show: true},
      {id:2, category: "Sporting Goods", price: "$9.99", stocked: true, name: "Baseball", show: true},
      {id:3, category: "Sporting Goods", price: "$29.99", stocked: false, name: "Basketball", show: true},
      {id:4, category: "Electronics", price: "$99.99", stocked: true, name: "iPod Touch", show: true},
      {id:5, category: "Electronics", price: "$399.99", stocked: false, name: "iPhone 5", show: true},
      {id:6, category: "Electronics", price: "$199.99", stocked: true, name: "Nexus 7", show: true}
    ];    
    this.state = {
      products
    };
    
    this.onFilterStock = this.onFilterStock.bind(this);
    this.onFilterCategory = this.onFilterCategory.bind(this);
  }
  onFilterStock (filter) {
    let { products } = this.state;    
    let newProducts = [...products];    
    if(filter)
    newProducts.forEach(product => {
      product.show = product.stocked
    });
    else
    newProducts.forEach(product => {
      product.show = true;
    });
    this.setState({products: newProducts})
  }
  onFilterCategory(value) {    
    let { products } = this.state;
    let newProducts = [...products];
    let searchVal = value.toUpperCase();

    if (value = '')
      newProducts.forEach(product => {
        product.show = true;
      });
    else 
      newProducts.forEach(product => {        
        if (product.category.toUpperCase().startsWith(searchVal))
          product.show = true;
        else
          product.show = false;
      });
        
    this.setState({ products: newProducts })
  }
  render() {
    let { products=[] } = this.state;    
    return (
      <form id="search-form">
        <SearchBar onFilterStock={this.onFilterStock} onFilterCategory={this.onFilterCategory}/>
        <ProductTable products={products.filter( product => product.show)} />
      </form>
    );
  }
}
export default FormContainer;
const wrapper = document.getElementById("create-search-form");
wrapper ? ReactDOM.render(<FormContainer />, wrapper) : false;

```

Update the SearchBar

```
import React, { Component } from "react";
import ReactDOM from "react-dom";
class SearchBar extends Component {
  render() {
    let { onFilterStock, onFilterCategory } = this.props;
    return (
      <div>
        <input type="search" placeholder="Search..." onChange={ e => { onFilterCategory && onFilterCategory(e.target.value)}}/>
        <label>
          <input
            type="checkbox"
            onClick={e => {
              onFilterStock && onFilterStock(e.target.checked);
            }}
          />
          Only show products in stock
        </label>
      </div>
    );
  }
}
export default SearchBar;
```

