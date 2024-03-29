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