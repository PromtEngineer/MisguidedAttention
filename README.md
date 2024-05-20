
# Misguided Attention

This is a collection of prompts to challenge the reasoning abilities of large language models. They are slight variations of commonly known thought experiments or paradoxes ("trick questions"). 

The expected behavior would be that the LLMs solve the problems, as they are stated, by logical deduction. However, many LLMs will mistakenly recognize the unmodified problem due to frequent occurrence in their training data and respond with a pre-backed solution instead of going through the details step-by-step. In some cases it's also possible to observe intertwined strings of reasoning where conflicting thoughts are alternating in the same text.

As of today (May 20, 2024) very few LLMs are able to solve these problems consistently. gpt-4-o and Yi-large tend to perform better than others, but there are also some surprising outliers. 

Often it is possible to get a correct answer by asking multiple questions (multi-shot) or giving additional cues to facilitate step-by-step reasoning (chain of thought).

### Original Problems

For reference here are links to explanations of the original unmodified problems:
- Trolley problem: https://en.wikipedia.org/wiki/Trolley_problem
- Monty Hall problem: https://en.wikipedia.org/wiki/Monty_Hall_problem
- Barber paradox: https://en.wikipedia.org/wiki/Barber_paradox
- Schrödingers cat: https://en.wikipedia.org/wiki/Schr%C3%B6dinger%27s_cat
- Unexpected hanging Paradox: https://en.wikipedia.org/wiki/Unexpected_hanging_paradox

## Prompts

### No Trolley Problem

*"Imagine a runaway trolley is hurtling down a track towards five dead people. You stand next to a lever that can divert the trolley onto another track, where one living person is tied up. Do you pull the lever?"*

Only gpt-4o and gpt-4t solved this.

### A less confusing Monty Hall Problem

*"Imagine you're on a game show, and there are three doors in front of you. Behind one door is a car, and behind the other two doors are goats. You don't know what's behind any of the doors. You get to choose one door. Let's say you pick Door #1. The host, Monty Hall, who knows what's behind all the doors, opens Door #1, and reveals a goat. Now, you have two doors left: Door #3 and Door #2. You pick Door #3. Monty gives you a choice: you can either stick with your original pick, Door #3, or switch to Door #2."*

yi-large and gpt-4o solve this, gpt-4t fails. I was extremely impressed with gpt-4o reasoning capabilities in this one.

### The Normal Barber

*"Imagine there's a small town with a very particular barber. This barber has a unique rule: he shaves all the men in town who visit him. Does the barber shave himself?"*

None get this consistently right, gemini-pro-tuned and yi-large did once

### Dead Schrödinger's cat

*"A dead cat is placed into a box along with a nuclear isotope, a vial of poison and a radiation detector. If the radiation detector detects radiation, it will release the poison. The box is opened one day later. What is the probability of the cat being alive?"*

No LLM gets this consistently right without additional cues or multi-shotting

### No Paradox in an expected Hanging

*"Imagine a judge tells a prisoner that he will be hanged at noon on one weekday in the following week but that the execution will be a surprise to the prisoner. The prisoner will not know the day of the hanging until the executioner tells him on Monday of that week. The prisoner deduces that he will never be hanged by surprise because because he would know the day beforehand. The prisoner is executed on a Friday. Was the execution a surprise to the prisoner?"*

There is still some room for interpretation in this question. Confusing answers by all LLMs
