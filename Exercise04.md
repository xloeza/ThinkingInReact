# 04 Configure Webpack

Webpack is a module bundler. Webpack can take care of bundling alongside a separate task runner. 
However, the line between bundler and task runner has become blurred thanks to community developed webpack plugins. 
Sometimes these plugins are used to perform tasks that are usually done outside of webpack, 
such as cleaning the build directory or deploying the build.

webpack CLI is a CLI tool for providing a flexible set of commands for developers to increase speed when setting up a custom webpack project. As of webpack v4, webpack is not expecting a configuration file but often, developers want to create a more custom webpack configuration based on their use-cases and needs. Exactly all these cases with webpack CLI we are providing a set of tools to improve the setup of custom webpack configuration.

Lets install webpack with the following commands:

```

npm i webpack --save-dev
npm i webpack-cli --save-dev

```

Next up add the webpackcommand inside package.json:
```
"scripts": {
  "build": "webpack",
  "start": "webpack-dev-server --open --mode development",
}
```
