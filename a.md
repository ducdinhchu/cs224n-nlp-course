Welcome back.
In the previous task, we've been setting up the OpenAI API,
creating the OpenAI account and an API key, setting up
an environment variable, storing the API key and then
calling the variable in the Python code.
In this task, we're going to experiment with the key concepts
of OpenAI. We're going to explore how the large language
model works and how the temperature parameter influences
prompt responses.
We'll do so using the  OpenAI API Playground. On your cloud
desktop, open a Chrome browser window and from "Resources"
select the OpenAI playground. Make sure you're logged
in with your OpenAI account as this will use some of your
free trial credits for OpenAI API.
On the right hand side from the mode dropdown menu, select
"complete" OpenAI has different text generative models such
as Ada, Curie or DaVinci, and different chat models such as GPT
3.5 and GPT 4.
We're going to use the DaVinci model as the latest text
generation model, as opposed to a chat model.
All of these OpenAI models are LLMs or Large Language
Models.
So how does a large language model work? To understand it,
let's start with a simple prompt.
We'll type in "write the plot of the movie the Goonies"
and to limit the response, let's say "in 100 words" and then
click "submit". The playground will send an API request
through your account and generate a response.
The minimum API usage unit is called "token", an OpenAI token
roughly represents three or four characters.
So to generate one average English language word, you will
probably be using between one and two tokens. From the right hand
side menu, scroll down to the bottom and select "full
spectrum" from the "show probabilities" dropdown menu, then
click the "regenerate" button to send the prompt again
and generate a new response.
This time, the response will be color coded, depending
on the probability of each chosen word.
This will help us understand how an LLM or large language
model works.
The model, trained with a very large data set, makes a decision
for each sequence of characters, evaluating the probability
that each sequence has to follow the previous sequence.
With the playground
full spectrum visualization, by clicking on each word,
we'll be able to see the list of top alternatives
and the relevant probability calculation. In green, you
will see the instances in which a very high probability
option has been chosen.
For example, "group" has the top probability of 98.19%
In yellow and red,
the mid and bottom probability options, for example, "living"
the top option here was "from" but "living" was a bottom
option or "treasures" where the top probability option was
"labyrinth".
There are different parameters to change the way the response
is generated and how the model operates
a choice between different options.
We will consider only one parameter in this project:
temperature.
The default value of temperature is 1.
Let's try to increase it to 2
and let's see what will happen.
We click the "regenerate" button, send the prompt again
and generate a new response.
As you can see, this is fairly nonsensical: Mcode junior high
group really doesn't have anything to do with the Goonies
and doesn't really much make any sense.
We even have some sequence of characters such as "SgmuIl" that are
completely nonsense. As you notice with the color coding,
pretty much all of the options of this response have a red
color. So the model has been choosing always the bottom
probability options.
What will happen instead if we decrease the temperature
and we bring it close to zero. We'll regenerate the response.
and you'll notice that most of the responses are green
or green-yellow.
So the model has been choosing the highest probability
options. Let's try regenerating again.
It's almost the same response.
So decreasing, the temperature will bring the probabilistic
model close to "almost deterministic".
You will almost have always the same response
every time you prompt the model. The higher the temperature,
the wilder the model will be in producing the response,
generating many nonsensical phrases.
This is very helpful to get a clear understanding of how
the model works.
and what does it really mean to generate text with OpenAI,
so that we'll know how to use the temperature parameter
when we want to calibrate our response.
Let's briefly review what we have learned in this task:
you can use the API playground to test the API,
before you write your code;
a large language model generates responses based
on the probability each character sequence has to follow
the previous one;
each token (the minimum billable character sequence generated
by the API) is generally made of 3-4 characters;
temperature is the parameter used to calibrate
how largely probabilistic or close to deterministic
the model's response must be. In the next task
we will start writing a simple Python script to prompt
programmatically OpenAI through the API and generate
a response.
See you there!
