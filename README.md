# Containerizing a Python Flask Application
### Building a docker container running nginx web server

![ye](https://user-images.githubusercontent.com/52897657/82688889-a68ae700-9c27-11ea-9d0a-1fb24f046b76.PNG)  

## Requirements
- Alpine Linux Distribution (Pulled from hub.docker.com)
- Docker installed on your local environment
- IDE (Visual Studio Code recommended)

## All files to be created
- app.py
- requirements.txt
- templates/index.html
- Dockerfile

## Make a project directory to store the files
`mkdir project_folder`

## app.py - Your Flask App
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
## requirements.txt (specify the version of the Flask)
`Flask==0.10.1`

## templates/index.html (Your index.html file)
```html


 
