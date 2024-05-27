# Challenge 4: Orchestrate the set up with Prompt Flow

Prompt flow is a development tool designed to streamline the entire development cycle of AI applications powered by Large Language Models (LLMs).  In the past challenges, you’ve been working on the Playground to try out some simple orchestrations of what a chatbot could look like, adjusting only parameters, the system message and the data sources . However, the complexity of your use requires some additional work. Your use case requires more than one data connections to be intertwined in just one use case, and each of them needs to be handled in a customized way. Let’s go ahead and start this journey using Prompt Flow!
## Description

You will have more than one way to solve this problem. As so, it is important that you discuss as a team where each part of the information available should be considered as an input and as an output and where. 


### Step #1: Understand and design the solution: 

In this first step, your Coach will be your ally in guiding you to a good solution. You are going to decide which tool will constitute your solution. You can choose from LLMs, Prompts, Python functions, Content Safety, Embeddings, etc. Each “node” that you will choose, will be connected to the others, starting from an “input” from the user and an “output” which is the response from the chat. For each node, you will also have inputs and outputs (e.g you receive the customer ID [input] and retrieve from the search index the information on this specific user [output]).

**Suggestion**: You can try to use tools such as Microsoft Whiteboard or a simple PowerPoint slide to help you orchestrate and organize your thoughts about the solution

### Step #2: Implement the Solution
In this step, your coach will not only be your ally but also a team member. Some of the tools you might be using, can be more difficult to handle than others, and for the most difficult ones, your coach will help you implement it. Nevertheless, it’s important that you try to find the way forward in the simpler solution and, above all, remember that every team member should be on the same page.


## Sucess Criteria

To complete this challenge successfully, you must:
1.	Explain the connections inside the Azure AI Studio
2.	Adapt the system message(s)
3.	Add the customer context as a crucial part of your solution
4.	Explain the role of variants in the solution 
5.	Explain the reasoning behind your solution
6.	Test your solution with some fixed prompts and respective customers ID:


| CustomerID     | Prompt    | Answer     |
|--------------|--------------|--------------|
| 2 | How can I set up the tent? |  |
| 9 | My jacket is ruined. Can I still return it?  |  |
|  10 | What is the color of the pants I bought |  |

## Learning Resources
Use the following resources to help you create your solution:
* https://learn.microsoft.com/en-us/azure/ai-studio/how-to/prompt-flow
* https://learn.microsoft.com/en-us/azure/ai-studio/how-to/create-manage-runtime
* https://learn.microsoft.com/en-us/azure/ai-studio/how-to/flow-develop
* https://learn.microsoft.com/en-us/azure/ai-studio/how-to/prompt-flow-tools/embedding-tool
* https://learn.microsoft.com/en-us/azure/ai-studio/how-to/flow-tune-prompts-using-variants
* https://learn.microsoft.com/en-us/azure/ai-studio/how-to/prompt-flow-tools/prompt-tool
* https://learn.microsoft.com/en-us/azure/ai-studio/how-to/prompt-flow-tools/llm-tool
* https://learn.microsoft.com/en-us/azure/ai-studio/how-to/prompt-flow-tools/python-tool
* https://github.com/microsoft/promptflow
* https://learn.microsoft.com/en-us/training/modules/get-started-prompt-flow-ai-studio/6-exercise

## Tip
The "Validate and parse input" button will be your best friend
