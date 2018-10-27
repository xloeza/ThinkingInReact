# 08 Create your project structure
Lets create a minimal directory structure for organizing the components:

Execute the following command or create it using visual studio:
```
mkdir -p src/js/components/container
```

Lets create our Form Container component:
Execute the following command:

```
touch src/js/components/container/FormContainer.js
```

Add the following content to the FormContainer.js file:
```
import React, { Component } from "react";
import ReactDOM from "react-dom";

class FormContainer extends Component {
  render() {
    return <form id="search-form">Bla bla bla</form>;
  }
}
export default FormContainer;
const wrapper = document.getElementById("create-search-form");
wrapper ? ReactDOM.render(<FormContainer />, wrapper) : false;
```

