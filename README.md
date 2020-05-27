# Containerizing a Python Flask Application
### Building a docker container running nginx web server

![ye](https://user-images.githubusercontent.com/52897657/82688889-a68ae700-9c27-11ea-9d0a-1fb24f046b76.PNG)  

## Prerequisites
- Alpine Linux Image (Pulled from hub.docker.com)
- Docker installed on your local environment
- IDE (Visual Studio Code recommended)

## All Files to be Created
- app.py
- requirements.txt
- templates/index.html
- Dockerfile

## Make a Project Directory to Store the Files
`mkdir project_folder`

## Creating Your Flask Application File - app.py
```python
from flask import Flask, render_template

app = Flask(__name__)

# functions for your flask app
#
#

@app.route('/')
def index():
  return render_template('index.html')
 
if __name__ == "__main__":
    app.run(host="0.0.0.0")
   ```
## Specifying the Flask version - requirements.txt
`Flask==0.10.1`

## Your index.html file - templates/index.html
```html
<!DOCTYPE html>
<html>
<head>
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>FDM Group Portal</title>
<link rel="stylesheet" href="css/main.css">

</head>
<body>
<div id="blur" style="background-image: url('images/blurb.png');">
<div class="card">
  <img id="logo" src="images/fdm.png" alt="FDM">
  <div class="container">
    <form id="formid" action="/action_page.php">
      <input type="text" id="logemail" name="logemail" placeholder="Email Address" required><br><br>
      <input type="password" id="logpassword" name="logpassword" placeholder="Password" required><br><br>
      <input id="submit" type="submit" value="Login">
    </form>
  </div>
    <img id="city" src="images/city.jpg" alt="Toronto">

  <div class="register">
    <span class="txt1">
      No FDM Account?
    </span>
    <a class="txt2" href="#">
      Register
    </a>
  </div>
    <!---  <p id="head">Toronto Financial District</p> --->
<img id="circ" src="images/circ.PNG" alt="FDM Circles" width="150">
  <div class="a2019-2020">
    <a id="txt3">
        &copy; 2020-2021
    </a>
  </div>
  <div class="author">
    <a id="txt4">
        Developed by Kihoon
    </a>
  </div>
</div>
</body>
</html>
```

## Writing the Dockerfile
> Note: Visual Studio Code has Docker plugins for efficient edits

 
