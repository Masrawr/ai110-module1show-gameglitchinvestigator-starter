# 💭 Reflection: Game Glitch Investigator

Answer each question in 3 to 5 sentences. Be specific and honest about what actually happened while you worked. This is about your process, not trying to sound perfect.

## 1. What was broken when you started?

- What did the game look like the first time you ran it?
- List at least two concrete bugs you noticed at the start  
  (for example: "the hints were backwards").

  1.The game prompted to enter a score between 1-100, but it accepted out of range numeric inputs.(non-numeral input was not tested)
  2.The game prompted "Press Enter" for submitting your guess but it resulted in nothing.
  3.The correct guess was "65" but game gave false hints and prompted to "Go Lower".
  4.The game was incorrect about what the user guessed as well.
  5."New Game" button does not perform it's function.

**Bug Reproduction Log**

Document at least 3 bugs you found. Add rows as needed.

| Input | Expected Behavior | Actual Behavior | Console Output / Error |
|-------|-------------------|-----------------|------------------------|
|  101  |   Out of Range        Game accepts           None
|  -5   |   Out of Range        Game accepts      "Your score:-35"
|   27  |  higher or lower     Hint: Go lower     "Correct guess: 65"

---

## 2. How did you use AI as a teammate?

- Which AI tools did you use on this project (for example: ChatGPT, Gemini, Copilot)?
  
  I used Claude in this project.

- Give one example of an AI suggestion that was correct (including what the AI suggested and how you verified the result).

  The AI helped point to the lines where the error was being caused and exactly what part of the code was incorrect. For example the out of range being accepted bug, the AI showed that there was no check for out of range exceptions and I asked it to make the simple correction to check for out of range exception.

- Give one example of an AI suggestion that was incorrect or misleading (including what the AI suggested and how you verified the result).

  I think I was specific with my instructions to the AI therefore it did not make incorrect changes or misleading comments.

---

## 3. Debugging and testing your fixes

- How did you decide whether a bug was really fixed?

  I ran the game and tested specific out of range input values and verified the game did not accept it and also output a out of range message. 

- Describe at least one test you ran (manual or using pytest)  
  and what it showed you about your code.

  I ran both. Pytest confirmed all test cases were passed, and manual test within the game itself also verified out of range input values were not accepted. 

- Did AI help you design or understand any tests? How?

  AI only helped me understand why the "pytest" command was causing erros. It corrected me to run "python3 -m pytest" instead, which was correct and terminal showed all tests were passed.

---

## 4. What did you learn about Streamlit and state?

- How would you explain Streamlit "reruns" and session state to a friend who has never used Streamlit?

  

---

## 5. Looking ahead: your developer habits

- What is one habit or strategy from this project that you want to reuse in future labs or projects?
  - This could be a testing habit, a prompting strategy, or a way you used Git.
- What is one thing you would do differently next time you work with AI on a coding task?
- In one or two sentences, describe how this project changed the way you think about AI generated code.
