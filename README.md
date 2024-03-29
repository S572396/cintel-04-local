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
3.
Run the following commands from a new or available terminal to git add/commit/push changes to GitHub.
Replace "Your commit message" with a meaningful message about the changes you made to the project files
git add .

git commit -m "Your commit message"

git push -u origin main

Action 4: Publish GitHub Pages for the Repo

This is a one-time step. We need to set up your GitHub repo (in the cloud) so that it will host with GitHub Pages. 

The first time you set up an app to use Pages, navigate to the repository on GitHub and configure the settings to publish the app with GitHub Pages.
After configuring the repository once, each time you push changes to the main branch, the app will automatically update.

Go to the repository on GitHub and navigate to the **Settings** tab.
Scroll down and click the **Pages** section down the left.
Select branch main as the source for the site.
Change from the root folder to the docs folder to publish from.
Click Save and wait for the site to build.
Eventually, be patient, (refresh button and io page at top)your app will be published and if you scroll to the top of the Pages tab, you'll see your github.io URL for the hosted web app. Copy this to your clipboard. 
Back on the main repo page, find the About section of the repo (kind of upper right).
Edit the "About" section of the repository to include a link to your hosted web app by using the Pages URL

Action 5. Change the Browser Tab Title 

Back on your machine, in VS Code, open the new docs folder. Edit docs/index.html - find the line that has the <title> and </title> opening and closing tags. The inner text between these two tags will appear in your tab. It's currently the same for everyone. Make this unique. 

Replace the title with your own short custom title - it will display in the browser tab when your app runs. 

 

Action 6. Optional - Add a Custom Favicon
Optional: Add your own custom favicon  (the little icon that appears in the web browser tab) next to the title. Try https://favicon.io/Links to an external site. and create a favicon (the little icon that appears in the web browser tab) using a bit of text (e.g. PP for popper's penguins  - or better yet, your own unique icon). Download the zipfile and extract the files. Take just the favicon.ico file and paste it into your docs folder.  Edit docs/index.html. Just below the title line, add the following link tag like so. This code is the same for all of us - only the favicon appearance is different. 


    <title>PyShiny Penguins</title>
    <link rel="icon" type="image/x-icon" href="./favicon.ico">