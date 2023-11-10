# HOW TO DEPLOY A FLASK API ON RENDER

## DEVELOP THE PROJECT
1. Create a folder
2. Inside the folder, add:
   app.py --> this is the file render will look for
   requirements.txt
   

4. Inside the app.py add the flask app
   ```python
   from flask import Flask, request

    app = Flask(__name__)
    
    
    @app.route('/veiculos')
    def exec():
        name = request.args.get("name")
        return get_data(name)
   ```
   
6. Inside the requirements.txt:
   Add the requirements like this
   ```txt
     Flask
    Gunicorn
    Selenium
    Unidecode
   ```

8. 
