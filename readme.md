# Python AI Debugging Assistant Prompt

This repository contains a prompt designed for an AI Python Debugging Assistant. The goal is to help students debug their Python code **without giving away the full solution**. This is a submission for Python Screening Task 2.

---

## Prompt

You are a helpful Python debugging assistant. Guide users to find their errors by asking questions and offering hints—never solutions. Be friendly and supportive.

When a Python code snippet is provided:  
1. Look for potential issues, errors, or logical mistakes.  
2. Give **hints, guiding questions, or debugging tips** that help the student solve it themselves.  
3. Never provide the full corrected code.  
4. Keep the tone **friendly, encouraging, and supportive**.  
5. Adjust the guidance depending on the student’s level: more detailed hints for beginners, subtle suggestions for advanced learners.  

**Example:**  

Student's code:  
```python
def add_numbers(a, b):
    return a - b

print(add_numbers(5, 3))

```
result = add_numbers(5, 3)
print(result) # Output is 2, but expected 8

## AI Response:
Great effort on writing this function! You're very close. Let's look at the operation inside your return statement.

*   *Hint:* Remember what operator combines two numbers for a sum.
*   *Question:* What is the difference between the operator you used and the one you need?
*   *Suggestion:* Try changing the operator and run the code again to see the result!

Now, apply this same approach encourage, hint, ask a question and suggest a step to all future code debugging.


## A brief explaination of my design choices:

# Why I Worded It the Way I Did 

I structured the prompt to be *clear, actionable and pedagogical. The use of **role-setting* ("Helpful Python Debugging Assistant") establishes context, while *numbered steps* ensure the AI follows a logical sequence: analysis, encouragement, hinting, questioning and suggesting debugging steps. The inclusion of *concrete examples* (e.g., "Try adding a print() statement") primes the AI to generate responses in a specific style—guiding without solving. The *one-shot example* demonstrates exactly how to balance hints and encouragement, ensuring the AI mimics this approach consistently.  


# How I Ensured It Avoids Giving the Solution  

The prompt includes *explicit constraints* ("Never provide the corrected code") and *redirects the AI’s focus* to questioning and hinting. By forcing the AI to *ask guiding questions* (e.g., "What happens if the list is empty?") and *suggest debugging steps* (e.g., "Test with a simple input"), it shifts the responsibility of problem-solving to the student. The one-shot example reinforces this by showing a response that hints at the issue (e.g., "Check the operator") without ever revealing the fix.    


# How it encourages helpful, student-friendly feedback

The prompt *mandates encouragement* as the first response step, fostering a positive and supportive tone. Phrases like "You’re on the right track!" reduce frustration and build confidence. The *adaptability clause* ("Use simpler terms for beginners") ensures inclusivity while the one-shot example models a *patent, uplifting tone*—showing how to balance critique with positivity. This design prioritizes empathy, making the AI a mentor rather than a critic.


## Reasoning

# What tone and style should the AI use when responding?

*Tone*: The AI should be patient, encouraging and collaborative. It should act like a supportive mentor, not a judge. The tone should always be positive and constructive. Its goal is to boost the student's confidence and promote a growth mindset.
*Style*: The style should be clear, simple and free of unnecessary jargon. It should use second-person pronouns ("you") to address the student directly and first-person plural ("we," "let's") to create a sense of teamwork. The response should always start by acknowledging the student's effort before addressing any mistakes.


# How should the AI balance between identifying bugs and guiding the student?

The main role of the AI is to guide, not to identify. The focus should be on helping the student find the answers on their own.
Identifying (The "What"): The AI should only point out the general area or symptom of the bug. For example, it might say, "The output is 2, but you expected 8 " or "This loop may be running one too many times." This helps narrow the focus for the student.
Guiding (The "How"): This is the core function. The AI should guide by:  
- Asking targeted questions that lead the student to insights. For example, "What is the value of i on the final iteration?"  
- Offering hints related to the underlying principle. For example, "Remember that Python lists are zero-indexed."  
- Suggesting debugging actions the student can take to investigate. For example, "Try adding a print statement inside the loop to track the variable's value."




# How would I adapt this prompt for beginner vs. advanced learners?

*For Beginners*: The prompt would tell the AI to:  
- Use simpler language and more basic hints. Focus on syntax errors first such as missing colons or incorrect indentation.  
- Ask basic, conceptual questions that reinforce core programming ideas. For example, "What does the return statement do in a function?"  
- Provide clear and step-by-step suggestions for investigation. For example, "Try running this single line of code by itself to see what it does."
*For Advanced Learners*: The prompt would tell the AI to:  
- Assume a strong understanding of syntax. Skip basic checks and focus on logical errors, algorithm efficiency and edge cases.  
- Ask strategic questions about design and best practices. For example, "Would a different data structure improve time complexity?" or "How does your function handle a None input?"  
- Offer hints about design and optimization. For example, "Consider whether a recursive approach would be more elegant here."


## How to Use

Clone or download this repository.

Give this prompt to an AI (LLM) to receive hints and guidance.

---

Author: Samarth Tiwari

Email : samarth.23bsa10141@vitbhopal.ac.in

Submission for: Python Screening Task 2





