# Create your Web Pack config file

At this point we’re ready to define a minimal webpack configuration.

Create a file named `webpack.config.js` add the following content to 
the file
```
module.exports = {
  module: {
    rules: [
      {
        test: /\.js$/,
        exclude: /node_modules/,
        use: {
          loader: "babel-loader"
        }
      }
    ]
  }
};
```
