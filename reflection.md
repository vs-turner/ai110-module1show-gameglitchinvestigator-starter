# 💭 Reflection: Game Glitch Investigator

Answer each question in 3 to 5 sentences. Be specific and honest about what actually happened while you worked. This is about your process, not trying to sound perfect.

## 1. What was broken when you started?

- What did the game look like the first time you ran it?
- List at least two concrete bugs you noticed at the start  
  (for example: "the hints were backwards").

The hints were almost always wrong. They did not seem to be random but tended to point in the wrong direction. The only time the result was correct was when user guessed the exact number.

## 2. How did you use AI as a teammate?

- Which AI tools did you use on this project (for example: ChatGPT, Gemini, Copilot)?
- Give one example of an AI suggestion that was correct (including what the AI suggested and how you verified the result).
- Give one example of an AI suggestion that was incorrect or misleading (including what the AI suggested and how you verified the result).

I used Copilot to locate the bug in app.py. it correctly identified that the comparison operator in check_guess was flipped. It suggested changing the condition from guess > secret to guess < secret for the "Too High" branch. I verified this by running the pytest test it generated

## 3. Debugging and testing your fixes

- How did you decide whether a bug was really fixed?
- Describe at least one test you ran (manual or using pytest)  
  and what it showed you about your code.
- Did AI help you design or understand any tests? How?

I ran the pytest test that Copilot generated to confirm the logic was correct in isolation. Then I played several rounds of the game.

## 4. What did you learn about Streamlit and state?

- How would you explain Streamlit "reruns" and session state to a friend who has never used Streamlit?

Every time you click a button or type something in a Streamlit app, the entire Python script runs again from the top. so if you want to keep track of the player's score or the secret number across multiple guesses, you have to put it there. If you don't, the score resets to zero every single time the player clicks a button, 

## 5. Looking ahead: your developer habits

- What is one habit or strategy from this project that you want to reuse in future labs or projects?
  - This could be a testing habit, a prompting strategy, or a way you used Git.
- What is one thing you would do differently next time you work with AI on a coding task?
- In one or two sentences, describe how this project changed the way you think about AI generated code.

I've never used git this much before, it is reassuring to have Ai help with the syntax.
