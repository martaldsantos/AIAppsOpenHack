# Challenge 5- Evaluate the chat performance

Now that we have created our LLM flow to be able to get information from the customer and what the customer is looking for, we will now evaluate our chat performance. This will be done for two main reasons:
1.	Ensuring we have the right connection to our datasources
2.	Ensuring that the system message has all the desired information to run this evaluations

In case neither or one of the options above is not to your desired liking, we should re-evaluate our solution and our flow.

## Description

We will use built-in metrics evaluations to our model. To do this, we will use a previously created set of data that will be imputed to the model. You can find this .jsonl file in this folder with the format evaldata.jsonl.

If you wish to find more metrics, be sure to have a look at the [curated and custom metrics offered by the AI Studio](https://learn.microsoft.com/en-us/azure/ai-studio/concepts/evaluation-metrics-built-in?tabs=warning)

### Measures 


| Metrics        | Description                                                                                                             | Required Input                               | Score Value                       |
|----------------|-------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|-----------------------------------|
| Groundedness   | Measures how grounded the model's predicted answers are in the input source. Even if LLM’s responses are true, if not verifiable against source, then is ungrounded. | question, answer, context (no ground truth) | 1 to 5, with 1 being the worst and 5 being the best. |
| GPT Similarity | Measures similarity between user-provided ground truth answers and the model predicted answer using GPT Model.           | question, answer, ground truth (context not needed) | 1 to 5, with 1 being the worst and 5 being the best. |
| Relevance      | Measures how relevant the model's predicted answers are to the questions asked.                                          | question, answer, context (no ground truth) | 1 to 5, with 1 being the worst and 5 being the best. |
| Coherence      | Measures the quality of all sentences in a model's predicted answer and how they fit together naturally.                 | question, answer (no ground truth or context) | 1 to 5, with 1 being the worst and 5 being the best. |
| F1 Score       | Measures the ratio of the number of shared words between the model generation and the ground truth answers.              | question, ground truth answer, generated answer | Float [0-1]                       |
| Fluency        | Measures the grammatical proficiency of a generative AI's predicted answer.                                             | question, generated answer                   | Integer [1-5]: where 1 is bad and 5 is good |

## Sucess Criteria

To complete this challenge successfully, you must:
* Create an evaluation from your prompt flow
* Correctly identify the metrics needed to our use case (and with the data you have available)
* Correctly identify the parameters needed for each one of the metrics.
* Wait for the evaluation to succeed on the evaluation tab
  
*Be sure to enable the "Show batch runs" option*

![image](https://github.com/martaldsantos/AIAppsOpenHack/assets/44229401/ea23a9c6-3123-4369-9c14-62e5d3890069)
* Save and analyze the results from each one of the metrics.


## Learning Resources
Use the following resources to help you create your solution:

* https://learn.microsoft.com/en-us/azure/ai-studio/how-to/evaluate-generative-ai-app?pivots=ai-studio
* https://learn.microsoft.com/en-us/azure/machine-learning/prompt-flow/how-to-bulk-test-evaluate-flow?view=azureml-api-2
* https://learn.microsoft.com/en-us/azure/ai-studio/how-to/generate-data-qa
* https://learn.microsoft.com/en-us/azure/ai-studio/how-to/evaluate-flow-results


## Tips
Sometimes not all the documentation refers to what we want and need. Please find the right documentation on the requirements specified in the introduction section of this challenge.

Sometimes the chat history can and should be empty

You have the option to use a chat with or without context, as you also have two solutions in this repo. Please understand the difference and choose accordingly
 
