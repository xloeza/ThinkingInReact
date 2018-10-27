# 05 Configure your transpiler
We are going to configure Babel

babel-node is a CLI that works exactly the same as the Node.js CLI, 
with the added benefit of compiling with Babel presets and plugins before running it.

Execute the following command
```
npm i @babel/core babel-loader @babel/preset-env @babel/preset-react --save
```

Configure your babel environment. Theere are several ways to configure babel, 
this is one way to configure it:
Create the file 
```.babelrc```

Inside create to following content:
```
{
"presets": ["@babel/preset-env", "@babel/preset-react"]
}
```
