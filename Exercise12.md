# 12 Finishing the environment

Now run the following command
```
npm run build
```
Check the files generated in the dist directory

You don’t want to type npm run and build every time you change a file.

```
npm i webpack-dev-server --save-dev
```
Check the configuration of your package.json

```
"scripts": {
  "start": "webpack-dev-server --open --mode development",
  "build": "webpack --mode production"
}
```
Execute the following command
```
npm start
```

Your environment is Ready to start playing with react
