Welcome back.
In the previous task, we have been programmatically prompting
an OpenAI model, writing a Python script using OpenAI API,
and if you have chosen to complete the optional practice
activity, you have further practice programmatic
prompting, generating a list of a movie cast members using
the zero shot and few shot approaches.
In this task, we are going to start applying programmatic
prompting to our web app using OpenAI data to enrich
the movie collection.
This guided project will give you skills to incorporate OpenAI
in your apps for a variety of objectives.
In this task,
we will take information from a JSON object containing
the movie details, and use such information to prompt OpenAI
for key movie info such as director, year of release
and movie genre.
Go back to visual studio, close all tabs, click "file > open
folder",
select working folder from your desktop and click "select
folder".
You don't need to save your word space configuration as
a file. Prompt.py and prompt-practice.py come from our
previous task and optional practice.
Everything else makes up the flask web app, double click
app.py to open it
and let's briefly review the app.
The templates folder contains the web UI template index.html,
the static folder contains the JavaScript and CSS used
by the app.
Double click the script.js in the JS folder to open it.
In this guided project scenario,
you are at an early stage development of the web app
with a simple UI written in HTML, CSS and Javascript.
Within the javascript,
we used Jquery to manipulate the interface and to communicate
with the flask server's
Rest API to pass on some details needed to build the OpenAI
API request in the Python script and later use its response.
Let's review the JavaScript file.
While in the production environment, you may have a database,
at this stage
we have saved the user's movie collection information
in an array of JSON objects within the JavaScript.
In the second array of JSON objects, we have stored
the details needed for each API request to the server, button-path
defines the Jquery path to the button that when clicked
will generate each request.
The output div path defines the div where the response
obtained by OpenAI will be written, and url defines the URL
to which the request should be sent.
This URL will be mapped into a Python flask endpoint.
An endpoint is essentially an indicator of what logical unit
of Python code should be executed when a certain URL
is visited on the server.
In the JavaScript, we also have three functions: addMoviesHTML
will generate the web page by adding a row
for each movie stored in the user's movie collection to index
html, taking the details from the movies
JSON. The getData function will build the Ajax server
request that we will use to interact with our server's
API. The OpenAI API request will be created by the Python
script with the code contained by the relevant endpoint.
The add Events function sets up listeners for click events
defining what will happen when each button is clicked.
For example, when a button such as  "show director"
is clicked, the getData function is executed
with the relevant request data for the button
with the "director" class, sending a request to the server
which is then mapped into the relevant endpoint in the Python
script.
The Python endpoint fires the OpenAI I API request
and the response of the OpenAI request is finally returned
to our JavaScript and written within the output div.
Now that we have a good idea of how the app works,
let's go back to the app.py file.
Let's create an endpoint for the director request.
So we're going to use the app get decorator and we're going
to add the URL that we have specified for the request,
api/get/director
So we're creating a route to an endpoint so that the
request is generated for the OpenAI API,
when this URL is reached. We're going to add the cross
origin as we're taking details from JSON
so we need to use the CORS policy, and we're going to add
a function, "get director" to build the OpenAI API request.
First, we need to get the parameters coming from the request
that we have sent to the server.
So we're going to use reuest.args we're going to have args equal
request.args so this way we're taking the arguments,
we're taking the details coming from the request
that we have sent to the server containing the details
of the movie coming from our JSON file.
We'll define "movie title" and it will be args.get "movie title" so
that we take from the parameters specifically the movie title.
Now that we have defined movie title, taken from the request
parameters, we can start to write in a programmatic prompt
to OpenAI API and we're going to store the prompt
in a variable so that we can prepare it beforehand,
and we will later use it into the OpenAI API request.
So we say prompt = "give me the director of the movie"
and we separate the instructions from content
so we use quotation marks and then we'll add a string
placeholder taking the movie title from the parameters sent
through the server request,
so this is coming from the JSON. "Give me the director
of the movie {movie_title} and will be very specific
with the prompt engineering,
so it will say "give me just the full name with spaces
in between where applicable but no other words, characters,
symbols or punctuation".
So we want to data enrich the movie collection, we want a straight
answer just the name of the director,
so we're being very specific with the prompting and then
we'll use the format function to establish what to assign
to this string placeholder,
so we'll say "movie_title=movie_title" so that we're taking
the parameter from the request arguments
and now we can build the response object just like we did
in the previous tasks.
So we'll have response equal and we use the OpenAI
completion create method to create a response.
We need to pass on the mandatory parameter model
and we're going to use again the text-davinci-003 model
and we're going to pass on the prompt which we have prepared
beforehand.
So "prompt" will be equal to the prompt variable
that we have created, and we're going to pass on a standard
temperature of 1 for now.
And we use max_tokens setting it at 64 as we need a short
answer, the other parameters that are not mandatory, they
will be set by default at the API defaults
and we're going to return the response.
So we're going to take the choices at index position
zero and text strip so that we can return the response
from this prompt. Pause the video and try creating the other
endpoints:  one for the year and one for the movie genre
and resume the video when you're done so that we can review
it together.
Let's review it together.
Creating the other two endpoints will be almost identical
to creating the director one.
We're going to have a new decorator with the URL
api/get/year and we'll define a function get_year where we
change the prompt to "give me the year of release of the movie
movie, just the year,
no other words"
And then we'll create the third endpoint with the URL
api/get/genre
we create and define a function
get_genre with the "give me the genre of the movie and just
the genre with spaces in between where applicable".
So we edit the prompt here as well.
But the three endpoints will be almost identical to one
another.
Feel free to pause the video to review the code and resume
when you're ready.
Make sure you save the code by pressing CTRL+S or CMD+S
on your keyboard,
depending if you're using PC or Mac, then open the command
prompt, locate the "desktop > working folder" and then type in
"flask run".
This will start your Flask application and the local server.
You can type in this address into your browser to see the app
in action.
And then by clicking "show director, "show year" or "show genre" you can
see the result of your OpenAI API requests.
After the test, you can go back to command prompt, press
CTRL + C to stop the server and then exit.
Let's review the key takeaways of this task.
In this task we have been data enriching the movie collection
prompting OpenAI with JSON data. Use your data to prompt
the model, passing JSON properties to the prompt parameter of
the openai.Completion.create
API request; clearly separate the instructions from the
passed content
For example, what is the director of the movie?
Placing the movie title in quotation marks and be specific in
your prompt to generate clear and concise responses.
For example, only specify the full name of the director.
Do not add any other information. In the next task
We're going to have an optional ungraded practice activity
which is recommended for your practice.
Otherwise you can continue to the following task, where we will
start generating a plot programmatically.
See you there.
