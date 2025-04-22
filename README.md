# OLA3_AI
## cph-tm246@cphbusiness.dk - Timothy Busk Mortensen 
---

## 1. The 4 T's of Prompt Engineering

- Traits:
Traits are short instructions on how you want the LLM to engage with you. I would consider "role" and "audience" as the most basic traits. Some LLM has build in support for defining these. In gpt we can set the audience in "who are you" under "customize gtp". Examples could be: Giving a role to the LLM such as a teacher or student. Giving the LLM clues about the intended audience can also help. For example one could instruct the LLM to tailor the content to a middle school student, a highschool student or a college student. Traits are broader then just Role and Audience, and can sometimes overlap with the other t's. For example, in GPT the user can add traits about "tone", and "format"(be chatty, answer in list format). 
`Without it the LLM gives generic, sometimes bland answers`

- Tasks:
This is where we formulate what we want the LLM to achieve. The central part will usually take the form of a specific "action" such as (summarize, write, analyse, translate, order). There are a few different rules and guidelines on how to formulate the tasks in different scenarios. I will go over a handfull of the most important ones i the following:
    - Simplicity + experiment: Keeping the prompt simple and experimenting with different variants is a good way to get started. If the task at hand is big, it can be a good idea to break it into smaller sub-tasks. It can sometimes be easier to formulate each sub-task, using all the appropriate rules and guidelines, instead of trying to apply them to a very big and complex task.
    - Specificity: Try to keep instructions specific and unambigious. Try to avoid loose and imprecise terms. They should be detailed and descriptive enough for the LLM to understand the task and its details, but not so much that unimportant or redundant details are included.
    - Examples: Providing examples can sometimes be helpful when trying to formulate a prompt. Sometimes it can even be shorter and easier to provide an example instead of trying to explain it. The LLM can pick up on patterns in the examples and it also helps with format, tone and style in the outcome. 
`Without it the LLM gives off-topic, assumptive, and sometimes incorrect answers`


- Tone:
This controls the style and formality of the output. Examples could be: "Use a formal and academic language and tone." You can also use famous people as reference for specific lingustic styles. For example: "Write a poem using the speaking style of David Attenborough. 
`Without it the LLM gives inappropriate answers or use of words`


- Targets:
Who is the targeted audience for the output. In GPT we can customize this value manually before prompting. Under "customize gtp" there is a form named "what do you do?". Provide the nessecary details about the audience and the LLM will use these context clues to tailor the outcome to that audience. Some of the details might already be described in tone intructions or as traits. Providing additional context clues about the audience can help guide the model in the right direction. One could include extra information about the audience and what the outcome is used for to improve outcomes. In general context clues are very important.  
`Without it the explanation might be too technical (or too simple) for your audience`


It is important to keep in mind that all LLM's are not created the same way. Terms might have different names and some concepts might be lacking or missing in some models. For more help on model specific prompt engineering, one should go to the official model documentation. 

Example: 
A bad prompt is inprecise, lacking in context clues, vauge and has no clear goal or structure.
- Bad prompt: "Tell me about AI" 
- Good prompt: "You are a friendly computer science teacher. Explain what artificial intelligence is and how it is used today. Use a simple and enthusiastic tone, and write it for a curious high school student."



## Prompt engineering frameworks
Alot of different frameworks exists for prompt engineering.(RACE: Role, Action, Context, Expectation. APE: Action, Purpose, Expectation. COAST: Context, Objective, Actions, Scenario, Task. RICE: Role, Input, Context, Expectation) 

RICE; Role, Input, Context, Expectation.
Different frameworks work well with differens tasks. RICE is a scoring model that help prioritize elements. It uses 4 factors to score each stated element in accordance with a stated goal. RICE is good when u want alot of control over the structure or when the task include multiple steps. 

For example:

You are an expert Business Analyst. 

I have a blog on Gardening and I want to improve my Instagram reach. I am considering implementing the following changes, conduct a detailed RICE analysis(range 1-10, include RICE scores):

1. Post consistently: Regular posting keeps your audience engaged and increases visibility.
2. Use high-quality visuals: Eye-catching photos and videos grab attention.
3. Utilize Instagram Stories: They provide a more casual way to engage with your audience.
4. Host giveaways and contests: Encourage likes, comments, and shares for participation.
5. Collaborate with influencers: Partnering with influencers can expose your brand to new audiences.




GPT4o recognized this and outputs:

## 1. **Post Consistently**
- **Reach**: 8 – Regular posting increases visibility and potentially reaches your full audience base consistently.
- **Impact**: 8 – Builds engagement over time and boosts the algorithmic reach.
- **Confidence**: 9 – Proven strategy with strong industry data.
- **Effort**: 4 – Moderate effort to maintain a consistent schedule and content calendar.
- **✅ RICE Score**: `(8 × 8 × 9) / 4 = 144`

---

## 2. **Use High-Quality Visuals**
- **Reach**: 7 – Attractive visuals help capture attention, leading to more shares and saves.
- **Impact**: 9 – High visual quality is critical on a visual platform like Instagram.
- **Confidence**: 8 – Backed by clear best practices and performance data.
- **Effort**: 5 – Takes time/resources for photography or graphic design.
- **✅ RICE Score**: `(7 × 9 × 8) / 5 = 100.8`

---

## 3. **Utilize Instagram Stories**
- **Reach**: 6 – Stories reach the most engaged followers but may not bring new followers easily.
- **Impact**: 7 – Drives regular engagement and humanizes the brand.
- **Confidence**: 8 – Well-documented benefits.
- **Effort**: 3 – Relatively low effort with a phone and quick edits.
- **✅ RICE Score**: `(6 × 7 × 8) / 3 = 112`

---

## 4. **Host Giveaways and Contests**
- **Reach**: 9 – Can go viral with the right conditions.
- **Impact**: 8 – Strong short-term engagement boost.
- **Confidence**: 7 – Results can vary depending on execution.
- **Effort**: 6 – Requires planning, prize, rules, and follow-up.
- **✅ RICE Score**: `(9 × 8 × 7) / 6 = 84`

---

## 5. **Collaborate with Influencers**
- **Reach**: 10 – Direct access to new and relevant audiences.
- **Impact**: 8 – Can drive significant growth if aligned well.
- **Confidence**: 6 – Depends on influencer fit and authenticity.
- **Effort**: 7 – High effort in outreach, negotiation, and collaboration.
- **✅ RICE Score**: `(10 × 8 × 6) / 7 = 68.6`

---

## raw prompt:
Write a short poem about the ocean.


## raw response from mistral:
In the heart of the world, where sky and earth part,

Lies an unending canvas, an ocean's art.
A dance between tides, a rhythm undistorted,
Breathing life into tales that haven't started.

Whispers of secrets, hidden beneath its cloak,
Of sunken treasures and ships lost to rook.
Waves crash against shores, in melodies they croon,
A symphony of nature where mysteries bloom.

From coral reefs teeming with life so bright,
To the deepest abyss, bathed in endless night.
Where creatures dwell, as ancient as time,
In this liquid mirror, beauty sublime.

Oh, ocean vast, your depths unfathomable,
Your tales of change, eternal and mobile.
From distant shores to where sun meets sand,
You connect us all on our common land.

## using the four t's frameowrk

Trait: You are a creative and emotional poet.
Task: Write a short poem about the ocean.
Tone: Make it gentle, nostalgic, and calming.
Target: It is for someone going through a hard time, who needs something comforting and beautiful.

Prompt: You are a creative and emotional poet. Write a short poem about the ocean. Make it gentle, nostalgic, and calming. The poem is meant for someone going through a hard time, who needs something comforting and beautiful.

## prompt response:
In the quiet of twilight, where shadows softly merge,
I find you, lost in thoughts, my friend, I hear your fear.
The ocean's gentle whispers call to you today,
A calming lullaby, a balm for troubled sway.

Beneath the starry sky, it stretches wide and deep,
In its depths, secrets that time has kept.
Waves of compassion, crashing at your shore,
Carrying tales of love through life's untold lore.

Look out to sea, my friend, where moonlight takes flight,
See the silhouettes of dreams, basking in its light.
Feel the rhythmic pulse of tides that ebb and flow,
The world outside pauses as you softly grow.

The ocean is a testament, of life's endless grace,
Of the strength within us all to find our place.
Remember, my friend, in times of strife and stress,
The ocean's boundless beauty always beckons less.

So take comfort in its embrace, let sorrow ebb away,
For though storms come and go, love's eternal ballet.
Know that you are loved, in this world so wide and vast,
In the heart of the ocean, find your peace at last.


---


Terms/techniques:

- zero-shot: Simple prompt with no examples. Large LLM's are trained on ALOT of data and can handle alot of tasks without any examples. 
- few-shot: When the task at hand is more complex, providing examples of desired outputs can help the LLM recognize the pattern. Few-shot prompting also has its limitations. The LLM will still miss the pattern in some cases, specially if the task is about reasoning. In these cases, the task might need to be broken down into smaller chunks. 
- Chain-of-Thought (CoT) Prompting: This is close to few-shot prompting but with some extra added reasoning in the examples. Instead of just providing the outcome, the reasoning behind the outcome is also included. Providing instructions like "Think step by step" in the reasoning chain, combined with 1 or 2 example reasoning chains, could make the LLM pick up on the pattern automatically.