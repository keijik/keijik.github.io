# How to train your model to write the code you want!

Have you seen AI models that can generate code for you?  Well, if you haven't, you're going to see them more soon thanks to models like [OpenAI](https://openai.com)'s [Codex models](https://openai.com/).  This article will show how to get models like Codex to generate code you want using a technique called [Prompt Engineering](https://en.wikipedia.org/wiki/Prompt_engineering).

Prompt engineering is the practice of using *prompts* to get the output you want.  A prompt is a sequence of text like a sentence or a block of code.  The practice of using prompts to elicit output originates with *people*.  Just as you can prompt people with things like a topic for writing an essay, amazingly you can use prompts to elicit an AI model to generate target output based on a task that you have in mind.

![Prompt Completion](/images/01-prompt-completion-01.png)

The output to a prompt is called a *completion*.  It's just another name for the output to a prompt.  An example task might be to write a Python program to add two numbers.  If you write out the task as a Python comment like so:
```Python
# Write a function that adds two numbers and returns the result.
```
And give it that comment as a prompt to Codex, it will generate the code for you like this:
```Python
def add(a, b):
    return a + b
```

The easiest way to get started with OpenAI Codex is to use the OpenAI Playground, which is available for free for new users.  This picture shows the Playground after Codex has generated the completion for the prompt in the comment.

![OpenAI Playground](/images/01-openai-add-two-numbers.png)

I highly recommend that you review OpenAI's [best practices](https://beta.openai.com/docs/guides/code/best-practices) on how to best use Codex and become familiar with the OpenAI Playground.

Codex is also available as part of the VS Code editor in a feature called [GitHub Copilot](https://copilot.github.com).  I wrote this article in VS Code and as I wrote the above Python example, Copilot automatically used Codex to suggest the code.  Below is a screenshot of Copilot in action.  The grey text including the Python function defintion is Copilot's suggested completion.  Note that it even suggests the close quote for the Markdown code section.

![Copilot completion example](/images/01-copilot-add-two-numbers.png)

So how can you add the power of Codex in your applications?  An example like the above is simple and easy for Codex to generate.  For custom applications, you may need to craft the prompt to better describe your problem.  This includes giving Codex examples to help tell it what you are looking for.  This is called *prompt engineering*.  The rest of this article shows you examples and techniques in prompt engineering to help you get the code you want.  

## Guiding the Model with Examples
Prompts are the input sequences given to an AI model, which generates the output word by word.  There are some excellent references on how these AI models work such as [Jay Alammar's GPT-3 guide]().  For a given model, the exact sequence of text that you provide to the model in the prompt influences all of the subsequent output.

Let's say that you tell Codex "I want to add two numbers".  We saw above an example of the output that it generates.  Suppose that you prefer a slightly different style of Python code.  You like to name your arguments differently like this:

![Function example](/images/03-context-example-basic-copilot-context.png)

It turns out that if you give Codex a longer prompt including the above, then it will work hard to match its output to the way you like.  Notice that it uses a shorter function name, and names the arguments exactly as with the example you gave.

![Basic prompt engineering](/images/03-context-example-basic-copilot-result.png)

Now you know that you can influence how the model outputs by the way you craft the prompt to the model.  This is what prompt engineering is.



