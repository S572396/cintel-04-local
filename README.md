# cintel-04-local

Procedure:
py -m venv .venv
In VS Code, open your .gitignore file. Verify it includes an entry for .venv/ 
.venv\Scripts\Activate
py -m pip install --upgrade pip setuptools

py -m pip install --upgrade -r requirements.txt

shiny run --reload --launch-browser penguins/app.py

Set-ExecutionPolicy -ExecutionPolicy RemoteSigned

create a new folder in the root project folder named penguins. It must be exact. Then move (or copy / paste) your app.py into the penguins folder. 
Action 2: Build Client-Side App
We will build the app to the docs folder of our repository and test it locally.  

With your project virtual environment active in the terminal and the necessary packages installed into our .venv project virtual environment, remove any existing assets and use
 shinylive export to build the app in the penguins folder to the docs folder:

"""
shiny static-assets remove
shinylive export penguins docs
"""
After the app is built, serve the app locally from the docs folder to test before publishing to GitHub Pages.

In the terminal, run the following command from the root of the project folder with the project virtual environment active:


py -m http.server --directory docs --bind localhost 8008

Open a browser (tested with Chrome) and navigate to http://localhost:8008Links to an external site. - or whatever URL it tells you - to view the web app in the docs folder running locally.

Run the following commands from a new or available terminal to git add/commit/push changes to GitHub.
Replace "Your commit message" with a meaningful message about the changes you made to the project files