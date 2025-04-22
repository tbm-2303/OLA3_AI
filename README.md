# OLA3_AI
## cph-tm246@cphbusiness.dk - Timothy Busk Mortensen 
---

## 1. Defne each of the 4 T's of Prompt Engineering

- Traits:
Traits are short instructions on how you want the LLM to engage with you. I would consider "role" and "audience" as the most basic traits. Some LLM has build in support for defining these. In gpt we can set the audience in "who are you" under "customize gtp". Examples could be: Giving a role to the LLM such as a teacher or student. Giving the LLM clues about the intended audience can also help. For example one could instruct the LLM to tailor the content to a middle school student, a highschool student or a college student. Traits are broader then just Role and Audience, and can sometimes overlap with the other t's. For example, in GPT the user can give traits about "tone", and "format"(be chatty, answer in only list format). 

- Tasks:
This is where we formulate what we want the LLM to achieve. The central part will usually take the form of a specific "action" such as (summarize, write, analyse, translate, order). There are a few different rules and guidelines on how to formulate the tasks in different scenarios. I will go over a handfull of the most important ones i the following:
    - Simplicity + experiment: Keeping the prompt simple and experimenting with different variants is a good way to get getting started. If the task at hand is big, it can be a good idea to break it into smaller sub-tasks. It can sometimes be easier to formulate each sub-task, using all the appropriate rules and guidelines, instead of trying to apply them to a very big and complex task.
    - Specificity: Try to keep instructions specific and unambigious. Try to avoid loose and imprecise terms. They should be detailed and descriptive enough for the LLM to understand the task and its details, but not so much that unimportant or redundant details are included.
    - Examples: Providing examples can sometimes be helpful when trying to formulate a prompt. Sometimes it can even be shorter and easier to provide an example instead of trying to explain it. The LLM can pick up on patterns in the examples and it also helps with format, tone and style in the outcome. 

- Tone:
This controls the style and formality of the output. Examples could be: "Use a formal and academic language and tone." You can also use famous people as reference for specific lingustic styles. For example: "Write a poem in the style of David Attenborough. 

- Targets:
Who is the targeted audience for the output. In GPT we can customize this value manually before prompting. Under "customize gtp" there is a form named "what do you do?". Provide the nessecary details about the audience and the LLM will use these context clues to tailor the outcome to that audience. Some of the details might already be described in tone intructions or as traits. Providing additional context clues about the audience can help the guide the model the right direction. One could include extra information about the audience and what the outcome is used for. 

It is important to keep in mind that all LLM's are not created the same way. Terms might have different names and some concepts might be lacking or missing in some models. For more help on more model specific prompt engineering, one should go the official model documentation. 



Terms:

- zero-shot: Simple prompt with no examples. Large LLM's are trained on ALOT of data and can handle alot of tasks without any examples. 
- few-shot: When the task at hand is more complex, providing examples of desired outputs can help the LLM recognize the pattern. Few-shot prompting also has its limitations. The LLM will still miss the pattern in some cases, specially if the task is about reasoning. In these cases, the task might need to be broken down into smaller chunks. 
- Chain-of-Thought (CoT) Prompting: This is close to few-shot prompting but with some extra added reasoning in the examples. Instead of just providing the outcome, the reasoning behind the outcome is also included. Providing instructions like "Think step by step" in the reasoning chain, combined with 1 or 2 example reasoning chains, could make the LLM pick up on the pattern automatically.