# 09 Time to wire things up

Webpack expects the entry point to be ./src/index.js

Execute the following command
```
touch src/index.js
```
Create the file and add the content:

```
import FormContainer from "./js/components/container/FormContainer";
```

With this in place we’re ready to create our bundle by running:
```
npm run build
```
