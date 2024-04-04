# Prompting strategies

## Write clear instructions

These models cannot read your mind. 
If outputs are too long, ask for brief replies.
If outputs are too simple, ask for expert-level writing.
If you dislike the format, demonstrate the format you'd like to see.
The less the model has to guess at what you want, the more likely it is you will get it.

- Include details in your prompt to get more relevant answers
- Ask the model to adopt a persona
- Use delimiters to clearly indicate distinct parts of the input
- Provide examples
- Specify the desired length of the output

## Provide reference text

Language models can confidently invent fake answers, especially when asked about esoteric topics or for citations and URLs. In the same way that a sheet of notes can help a student do better on a test, providing reference text to these models can help in answering with fewer fabrications.

- Instruct the model to answer using a reference text
- Instruct the model to answer with citations from a reference text

## Split complex tasks

Just as it is good practice in software engineering to decompose a complex system into a set of modular components, the same is true of tasks submitted to a language model. Complex tasks tend to have higher error rates than simpler tasks. Furthermore, complex tasks can often be re-defined as a workflow of simpler tasks in which the outputs of earlier tasks are used to construct inputs to later tasks.

- Use intent classifications to identify the most relevant instructions for a user query
- For dialogue applications that require very long conversations, summarize or filter previous dialogue
- Summarize long documents piecewise and construct a full summary recursively

## Give the model time to 'think'

If asked to multiply 17 by 28, you might not know it instantly, but can still work it out over time. Similarly, models make more reasoning errors when trying to answer right away, rather than taking time to work out an answer. Asking for a 'chain of thought' before an answer can help the model reason its way toward correct answer more reliably.

- Instruct the model to work out its own solution before rushing to a conclusion
- Use inner monologue or a sequence of queries to hide the model's reasoning process
- Ask the model if it missed anything on previous passes

## Use external tools

Compensate for the weaknesses of the model by feeding it the outputs of other tools. For example, a text retrieval systems can tell the model about relevant documents. A visual modelling tool can provide detailed cause-effect relationships that might not be explicit in a natural language statement. A code execution interpreter can help the model do math and run code. If a task can be done more reliably or efficiently by a tool rather than by a language model, offload it to get the best of both. 

- Use embeddings-based search to implement efficient knowledge retrieval
- Use diverse visual representations and notations to clarify complex situations and problems that cannot easily be expressed in natural language
- Use code execution to perform more accurate calculations or call external APIs
- Give the model access to specific functions

## Test changes systematically

Improving performance is easier if you can measure it. In some cases a modification to a prompt will achieve better performance on a few isolated examples but lead to worse overall performance on a more comprehensive set of examples. Therefore to be sure that a change is net positive to performance it may be necessary to define a comprehensive test suite (also known as an 'eval').

- Evaluate model outputs with reference to gold-standard answers

