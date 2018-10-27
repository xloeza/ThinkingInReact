# 11 Create your initial HTML

Next create an HTML file into ./src/index.html(feel free to use whichever CSS library you like):

Execute the following command
```
touch src/index.html
```
Add the following content
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="utf-8">
    <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0-beta.2/css/bootstrap.min.css" >
    <title>React Thinking</title>
</head>
<body>
    <div class="container">
        <div class="row mt-5">
            <div class="col-md-4 offset-md-1">                
                <div id="create-search-form">
                    <!-- form -->
                </div>
            </div>
        </div>
    </div>
</body>
</html>
```

Check the package.json file
```
"build": "webpack --mode production",
    "start": "webpack-dev-server --open --mode development",
```
