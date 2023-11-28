Hi and welcome to this guided project titled "OpenAI
for Beginners: Programmatic Prompting".
My name is Angelo Paolillo and I will be your instructor
for this guided project.
I am a digital consultant, developer and educator
with over 17 years of experience working for Google, IBM
and LinkedIn,
as well as managing my own business.
During the execution of this project, your screen will be
split in two.
On the left hand side, you'll find your workspace, a pre
configured cloud desktop loaded, right into your browser,
no download required and already equipped with everything
needed for the completion of your project.
On the right hand side in a split screen, you will find my
videos guiding you step by step throughout the project.
But... what will be the outcome of this project in this project? In this
project, you will programmatically prompt an OpenAI model using
the OpenAI API, prompt engineering and the temperature
parameter.
You will use OpenAI to enrich a database and generate text
that is descriptive of data objects.
So these are your three main learning objectives:
programmatically prompt OpenAI text models via API, enrich
data in a web application using OpenAI API, and manage two OpenAI
text generation parameters: temperature and tokens.
I have built a realistic project scenario.
You will take on the role of a full stack developer in a web
app startup called "MovieAI".
Your company's final product will allow users to enrich their
movie collection data
with the use of AI.
You will prompt OpenAI models using OpenAI API
with Python, and interact with JSON objects representing
each movie.
Prompting the AI model, you will enrich the data
of the user's movie collection and ask the AI to dynamically
generate each movie plot.
Let me give you a brief demonstration of the final outcome
of this project.
This is your web application with your user's movie collection:
by clicking the "show director", "show year" or "show genre" buttons
you will prompt the AI to generate an answer
to the question:
"Who is the director of this movie?" or "When was this movie
released?". By clicking the "generate plot button"
you will prompt programmatically the AI to write a plot
for this movie. We can reset the plot and generate it again.
Every time a new plot will be generated, a new piece of text
will be written by the AI following your prompt.
You will also learn two basic parameters to start fine tuning
the answer from the AI. Let's get ready to begin: on your
cloud desktop
you will find four folders.
The "Resource"s folder contains the PDF version of useful
resources which you will also find as reading items in your
Coursera course, as well as on your Chrome browser bookmarks
bar. Here you find the resources folder.
The "Sample project" folder contains the full code of the
completed project outcome
for your reference. To complete each mandatory task
with this guided project
you will use the "working folder". Throughout the project
you will have two optional practice activities,
and at the end of the project, an optional final cumulative
activity.
If you will choose to practice with these optional ungraded
activities, you will find the relevant material
in this "Practice activities" folder.
Excited and ready to work on this project?
Let's get started! In this first task
we're going to set up OpenAI API.
We'll create an OpenAI account and API key, set up
an environment variable storing your API key, and then
we'll call the API key from your code. To get started,
we'll need to create an OpeNAI account. Open a Chrome
browser window and visit openai.com. From the top right
hand corner, click "menu" and then "sign up", follow
the instructions on screen to create an account with your
email address.
Each new account will be allowed a $5 credit for API free
trial usage.
This will be more than enough to complete this project.
Pause the video and resume it when you have completed your
OpenAI account creation.
Once you're logged in with your OpenAI account, click "API".
On the top right hand corner, click on your account and then
click "manage account", click "usage".
Here you will see a report on your API free trial credit
usage, to see how much you have, you have used,
when does it expire
and what is the remaining credit. On the left hand side
click API keys. To use the OpenAI API
you will need to generate a key for your project.
Click "create new secret key",
give it an optional name, we'll call it  "guided project" and then
click "create secret key".
This will be the only time your generated API key will be
visible. Click the "copy" button.
We'll copy and save this key somewhere safe.
We'll save it in an environment
variable. Click "Done" and open Visual Studio Code from your
task bar. Visual Studio Code is the editor we will use
throughout this guided project. In the welcome tab, click "new
file" to create a new file. Choose "text file".
You can also create a file by clicking "file > new text file".
Once you have your file created, we'll save it right away.
Click "File", "Save as", save it in your working folder on your
desktop.
So click desktop, working folder, select the "save as type"
"- all files" and name the file .env
so the file will have no name,
it will be .env, and then click "save". We're going to store
the key in this file.
So type in "debug  true" and then 
OPENAI_API_KEY
So this will be your environment, variable, press CMD+V
or CTRL+V depending if you're using a Mac keyboard or a PC
keyboard to paste your copied API key and then CTRL+S
or CMD+S to save the file.
Now let's open our main Python file.
So click "file", "open file" and then open the "app.py" file
from within the working folder, and then click open. Click
open and open the file in visual studio.
So here you can see already the skeleton of this Python file.
I have created a sample flask app to work with the OpenAI
API. So we will work with the API within a web application
using Flask, which is a Python web framework.
You won't need to know much about flask,
we're only using it as a server and web application for OpenAI
API to work with.
I will explain how the app is built. In the app.py file,
the main Python file, at the moment, we simply have
the skeleton of our Flask app.
We have all the library and modules needed for the Flask app
to work, the core of the app and an index page, index.html,
template to be rendered as the main page of the app.
Now, we want to add the API key.
So we're going to add "import OS" to call for the environment
variable from the operating system.
We also want to use the OpenAI API,
so we're going to import openai, I'm going to use dotenv
to work with the environment variable.
So we're also going to add from dotenv import load_dotenv
to load the environment variable.
Now we're going to use this module, we have a load_dotenv
and we're going to let OpenAI know which is our API
key. So we'll have openai and we'll pass API_key
and this will be os.getenv and we'll call for the variable
which is OPENAI_API_KEY.
This is the environment variable we have created in the .env
file. It's useful to store the API key in an environment
variable so that it doesn't get exposed into your code.
So if your project is ever made public, you won't expose your
API key.
And then we're going to press CTRL+S or CMD+S
if you're using a Mac keyboard to save the file.
Let's briefly review what we have achieved in this task.
We have set up OpenAI API, as key takeaways: creating an OpenAI
free account will give you access to OpenAI API; to use
OpenAI API you'll
need to create an API key; you can create different
keys to use for different projects;
you can revoke and delete each API key from your OpenAI
account dashboard; to increase security, especially in your
public projects, store the API key in an environment variable.
In the next task,
we're going to experiment with the API playground
to understand a few key concepts of how the model works
and how will we programmatically prompt it.
See you in the next task.
