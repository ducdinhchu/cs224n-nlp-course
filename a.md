Welcome to the third task in our guided project. In the previous task, we chatted with a ChatGPT model using the API key access. In this task, we will define the chatbot conversation function. So we will develop this function to manage and streamline the conversation flow between the user and the chatbot. Because as you know that we are building a chatbot. So we have to streamline the flow of conversation between the end user and the chatbot that we are building.

So the task objective is to design a conversation flow to handle the frequently asked questions and customer service scenarios. And we have to learn to create interactive functions using Python and to understand conversation management in chatbots in general and to enhance the user chatbot interaction experience.

So let's start and look at the conversation function.

As you can see here that first of all, we are defining the function. So we are defining the chatbot conversation function.

First of all, we initialize the conversation with an initial prompt.

And here note that there is always an initial or a basic or a starting prompt.

After this initial prompt, and continuously there should be an interaction between the user and the chatbot. And always when the user sends a prompt, the chatbot in return should reply back or provide a response to the end user until the user end the conversation.

So the input here is the user, we are getting here the user's input. Then the user will send the input and the prompt to the ChatGPT API and then receive a response from the ChatGPT model.

And note that here we are using the text 003 model. Unlike what we have seen in the previous task, the 002 model, as I mentioned, it's based on fine tuned supervised learning. But this advanced model is based on reinforcement learning with human feedback with minimal supervision. So this model is specifically designed to understand and generate natural language, text or instruction following tasks known as prompts.

Great, so we have also to set the temperature that we want to use.

And the temperature here is very important, the temperature ranges between 0 and 1. If the temperature approaches 0, means that I want the model to output a more focused or precise response. And if the temperature is approaching 1, means that I want the model to be more creative or generate more creative response or more random response.

Now, in our task, we will set the temperature to be 0.7, which is somehow a default temperature approaching creativity. Because we don't want the model to generate precise or focused output, why? Because want the model to be dynamic in responding back to the users. Because as you know that we are building a customer service chatbot. Now for the maximum tokens, the maximum tokens here. For this model that is trained with the human feedback we will use thousand 24 tokens, and this number is really enough for our task as maximum tokens. Now, as you see that we are extracting and displaying the ChatGPT's response. Because when the user sends the prompt, the user expects a response from the model then the prompt will be updated for the next iteration. So after the model replies back or responded back to the user, the user will send another message. So this is the updated prompt for the next iteration. So, whenever the user is sending the model and the model is responding back to the user. Means there is an iteration or an iterative process of prompting and getting a response from the prompts. Let's now execute this call and there are no errors or issues. The code is perfectly working, great. So that's it for this task, in the next task we will see how we can handle frequently asked questions, see you then.
