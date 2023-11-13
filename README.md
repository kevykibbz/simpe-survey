### How to Set Up and Run the Application Locally

#### Frontend

1. **Installation of Required Dependencies:**

   ```plaintext
   - sky world
       - backend
           - frontend
               - build
                   - index.html
                   - manifest.json
                   - assets
                       - assets
                       - js
                       - css
                   - robots.txt
                   - assets-manifest,json
           - myenv
           - simple_survey_app
               - onboard (your app name)
               - simple_survey_app
                   - settings.py
                   - urls.py
                   - asgi.py
                   - wsgi.py
                   - __init__.py
               - manage.py
               - static
               - media
   ```

   **For Windows Users:**

   - Navigate to the desired project location using the Windows terminal.
   - Create a folder; name it "sky world" using the `mkdir` command, i.e., `mkdir sky world`.
   - Navigate to it using the `cd` command, i.e., `cd sky world`.
   - In your terminal and while inside "sky world," install virtualenv by running `pip install virtualenv`.
   - After installing the package, type `virtualenv myenv`. The venv name can be anything (e.g., `myenv`, `venv`, etc.). Here, we use `myenv` as our virtual env name.
   - Run the virtual env by typing `.\myenv\scripts\activate` to activate it.
   - After the virtual env is activated, type `git clone https://github.com/kevykibbz/opinion-harbor/tree/main/backend`. It will download the backend project into the "backend" folder.
   - Run `pip install -r requirements.txt` to install all the requirements in the virtualenv.
   - Run `py manage.py makemigrations`.
   - Run `py manage.py migrate`.
   - Run `py manage.py runserver`. This will open the server on the default port `8000`.
   - The application will be up and running at [http://localhost:8000](http://localhost:8000). You can preview it by visiting the link.

2. **Deployment Process**

   #### Using PaaS (e.g., Heroku)

   - Create a Heroku account.
   - Create an app for your project (e.g., `simple-survey-app`).
   - Install Heroku CLI by following [Heroku CLI Installation](https://cli-assets.heroku.com/heroku-x64.exe).
   - Once installed, open the Windows terminal and type `heroku --version` to verify installation.
   - Type `git init`, then type `git add .`, `git commit -m "message"`, `git branch -M main`, then type `heroku login`. It will redirect you to the browser to log in.
   - After successful login via the browser, type `heroku git:remote -a your-heroku-app-name`. In our case, it will be `heroku git:remote -a simple-survey-app`.
   - To verify that the remote has been added successfully, you can run `git remote -v`.
   - In the project root directory, verify that the `Procfile` file is present; otherwise, deployment won't work.
   - After verifying the file is present, type `git push heroku main`. It will push the project to Heroku.
   - Visit the URL given in the Heroku website dashboard once you create an app to view the website.