Welcome back.
In the previous task, we've been experimenting with key
concepts of OpenAI API, to test and understand how the OpenAI
model works.
In this task,
we're going to prompt programmatically OpenAI to generate
a response through a simple Python script to prompt the OpenAI
model through the OpenAI API.
Let's go back to Visual Studio Code.
We're going to create a new file,
so we'll click "file", "new file" and this time we're going
to select a "Python file", then we're going to save it,
so we'll click "file> save as" and we'll save it right away
calling it prompt.py and we'll save it in the working folder.
Then click save.
We're going to write a Python script that we can execute, we can run
it through the command prompt, so that we'll programmatically
prompt the OpenAI API model.
Let's see how to build such a file.
First, we're going to import OS so that we can retrieve
the API key from the environment variable.
Then we're going to add OpenAI,
so we'll import openai  so that we can use the API, then
from the dotenv ibrary, we're going to import the load_dotenv
method so that we can retrieve the API key
from the environment variable.
We'll run the, um we'll insert the function load_dotenv
and then we're going to pass to openai the API key
retrieving it from the environment variable.
So we're going to getenv, and we'll get it from the
environment variable
OPENAI_API_KEY
So this way we have passed the API key to OpenAI so that we
can use it to prompt programmatically the model.
Now we're going to create an object, a response object using
the openai.completion.Create method from the OpenAI API.
So this will create the completion to a prompt and we need
to pass a few parameters,
two of them are mandatory:
what model do we want to use and what is the actual prompt.
So we're going to start with model and we use the text davinci.
So text-davinci-003, we'll insert
the parameters comma separated,
so we're going to add the prompt now.
So we'll write in "prompt=" and we're going to write,
"write the plot of the movie Close Encounters of the third
kind". And we're going to limit the response by saying "in no
more than 100 words" just like we did on the playground.
So comma again and we're going to add another parameter.
So model and prompt are the two mandatory parameters.
There's a few parameters that the API will use that have
a default value.
So in this guided project, we're going to use only
"temperature" as we have seen already in the playground,
to modulate the response. The default value is 1,
so we're going to use the default value for now. The other
parameter we're going to use is max_tokens.
So this will establish what is the maximum number of tokens
that we can use between the prompt and the response.
We're going to use
the often-used value of 256 for now. In your Chrome browser,
in the resources bookmarks folder, you'll find the resource
that explains the tokens and how do they work,
what are they and how to count them.
This will explain how a token is a minimum unit of the API
and it's more or less four characters in the English language.
It will give you additional context and information,
and there's even a tokenizer tool that can anticipate more
or less how many
tokens would you need for your prompt and response?
Remember that the number of tokens is divided
between the prompt and the response,
so if you need 100 tokens for the length of the prompt
and another 100 tokens for the length of the response,
the maximum tokens should be 200, as we'll be using
100 to write the prompt and 100 to get the response.
Now we're going to add one last line so that we can print
in our terminal or command prompt window, the response.
So we have print (response),
but as the response is constructed with an array of different
choices, it can be one or more, so that the AI model
will choose a few different responses, will create a few
different responses to choose from,
so we're going to call for the index zero in choices,
so we can get the first choice.
And in this case, it's the only choice.
And then we use "text.strip" so that we can take the text
from within the choices array. Great!
Now, we can save with CTRL+S or CMD+S depending
if you're using a PC or Mac keyboard and we can run
this script in the command prompt.
So we'll open the command prompt from the task bar
at the bottom of your screen, of your cloud desktop screen,
we're going to reach the "desktop" folder and the "working
folder" you can use tab to complete.
And here in the working folder, we're going to run the script
Python prompt.py, we hit enter and after a few seconds,
we'll receive the response from the AI model,
and as you can see, it has generated the plot of the movie
"Close Encounters of the third kind" and it's printed on screen.
Let's use a little bit of prompt engineering.
What we have done here is a "zero shot prompt".
So we have created a prompt and we simply asked the AI model
to generate the plot of the movie and it returns the
generated plot.
What if we want to provide a few examples for the AI
to understand how do we want this plot to be written:
that is called a "few shots" as opposed to "zero shots"
that we have now. Pause the video and take a moment to read
the response and see how it is constructed.
The movie follows the story of the protagonist Roy Neary
and he continues describing the movie. Resume the video when
you're ready.
So back to visual studio, I have edited the prompt, adding
a couple of examples with specific mentions
of one of the characters of the movie, Claude Lacombe, and his
team of scientists trying to make contact with aliens. Feel
free to pause the video to read the prompt fully and then
resume when you're ready.
I have changed also max tokens so that we accommodate
for the longer prompt now.
So I have increased the number of max tokens used by my
response generation, and then back on the command prompt,
let's see what the result of this prompt editing was.
The prompt has generated a new plot, a new response,
and this time, there's a specific mention of Claude Lacombe and
his team of scientists.
While in a number of different response generations,
I have tried earlier, there was never a mention
of this character and his mission to make contact with aliens
for the first time.
So providing a couple of examples has already changed
the way the AI model is structuring the response.
So this is the difference between a zero shot and a few shots
approach. Calibrating the prompt and the examples
will change the responses the way you need.
Great. Now that we have created our first
programmatic prompt,
let's quickly review what we have covered in this task.
So our key takeaways: import openai module to use the OpenAI
API in Python; use the openai completion create function
to generate the response; pass the mandatory model and prompt
parameters; optional parameters will receive a default value
if not otherwise specified by your request;
the API request will generate a response.choices array
with alternative responses to the submitted the prompt;
a zero-shot approach will simply prompt the model;
a few-shot approach will provide examples to guide
the response. In the next task,
we're going to have an optional ungraded practice activity.
Feel free to take this recommended practice,
otherwise you can move on to the following instructional task.
See you there!
