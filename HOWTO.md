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
   
6. Inside the requirements.txt, add the requirements like this
   
   ```txt
    Flask
    Gunicorn
    Selenium
    Unidecode
   ```
   DO NOT include the version for each requirement.
   MAKE SURE TO add Gunicorn
   
8. If using Selenium webdriver.Chrome:
   In the file in which this package is imported, add the following code:
   ```python
   options = webdriver.ChromeOptions()
   options.add_argument('--headless')
   options.add_argument('--disable-gpu')
   
   driver = webdriver.Chrome(options=options)
   ```


## ADD TO A GITHUB REPO
Follow the instructions from Github

## DEPLOYING
1. Create a new web service
   ![image](https://github.com/mclaramarinho/flask-render-deploy/assets/119897667/37785e19-e8fc-40a8-a4cf-886b4bb2d4f7)

2. Deploy from github
   ![image](https://github.com/mclaramarinho/flask-render-deploy/assets/119897667/7db753ec-c84a-469d-887b-066d4fadf5a1)

3. Choose a repo
   ![image](https://github.com/mclaramarinho/flask-render-deploy/assets/119897667/e775fce3-e11a-41b2-bd14-83c1e3364be5)
   
4. Add a name to this deploy
   ![image](https://github.com/mclaramarinho/flask-render-deploy/assets/119897667/83a94c1b-172d-47bf-813b-73ee10258911)

5. Choose a directory to deploy
   ![image](https://github.com/mclaramarinho/flask-render-deploy/assets/119897667/c2986314-32c8-4a65-9dc6-541a9cd3de2d)
   If blank, it will deploy the root dir.
   
7. Leave these fields just like this
   ![image](https://github.com/mclaramarinho/flask-render-deploy/assets/119897667/6823acf4-7b95-48eb-9569-b924f6cf4052)

8. Hit the Create button

9. Wait for the build and deploy

   
