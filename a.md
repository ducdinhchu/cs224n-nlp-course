Welcome back.
In the previous task, we have learned how to programmatically
prompt the OpenAI model using the API.
This is an optional and ungraded practice activity.
The goal is really just to check your understanding.
In this practice activity, you will demonstrate your ability
to prompt OpenAI text models via Python and OpenAI API.
Create a new Python script and write an OpenAI request,
choosing the text-davinci-003 model, create the prompt
of your choice,
for example "list the main cast of the movie Batman by Tim
Burton", be specific and offer examples when applicable
to improve the quality of the response.
Here's a few things to note: import OpenAI module to use
the OpenAI API,
the only mandatory parameters are model and prompt.
Use prompt engineering techniques to generate better
responses.
And remember to use your API key from your environment
variable. As a pro tip, be descriptive and specific in your
prompt.
Provide examples to clarify what type of response you want
to generate.
So use the zero shot versus a few shot approach, and clearly
separate the instructions from the content in your prompt.
So when you're providing examples, use quotation marks
to clearly separate the two.
My advice for you is not to edit your previously created
prompt.py file, but to write from scratch a new script just
to practice, feel free to pause the video, start your
practice now and you can reference back to this slide whenever
you need.
When you resume the video, we're going to review the practice
activity together.
Let's review the practice together.
You can compare your result with mine.
If you have used the example provided in the slide, maybe
you have used this prompt:" list the main cast of the movie
Batman by Tim Burton".
So I have created a prompt-practice.py file,
I have imported os, openai and load_dotenv from dotend, I have used
load_dotenv to assign to OpenAI API key the environment variable taken
from the operating system, the environment variable, storing
my API key.
Then I have generated a response using openai.completion.create
I have chosen the text Davinci model
and I have written a prompt "list the main cast of the movie
Batman by Tim Burton", temperature is set as default
1 and max tokens, I have increased the value to 1000 as I
can't really predict how long the response from the model
will be.
And then I print the response, using the zero index in choices.
I'm going to move to command prompt and run this file.
And here is the response from the model.
So with this prompt, I have received a numbered list
with the actor and character, with the 10 main characters,
the main members of the cast, instead of using a zero shot
approach, I'm going to use a few-shot approach now and going
back to my script, I'm going to edit the prompt. In my
practice,
I went above and beyond.
I have clearly marked the two examples.
So I have created a multi line variable for the prompt using
the three quotation marks.
We have the "list the main cast of the movie Batman by Tim
Burton".
Here is two examples of how to generate each item in the list.
Example one, Jack Nicholson, the Joker with a brief
description of the character and then example two Michael
Keaton, Batman and a brief description of the character.
I'm going to save and see how the list generation
will change based on the example that I have now provided.
So I'm going to run again prompt-practice.py and see how the AI
model response will change.
Now, I have received a new list.
It's no longer a numbered list.
It's following my examples and it's creating the list
with the actor and the character and a brief description.
Feel free to read through the response, pausing the video
and resume it when you're done.
Congratulations on your practice.
In the next task, we're going to data enrich the movie
collection of the user with OpenAI using what
we have learned so far.
See you there!
