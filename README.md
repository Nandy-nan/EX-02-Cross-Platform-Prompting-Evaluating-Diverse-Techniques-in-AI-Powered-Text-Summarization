# EX-02-Cross-Platform-Prompting-Evaluating-Diverse-Techniques-in-AI-Powered-Text-Summarization

## AIM
To evaluate and compare the effectiveness of prompting techniques (zero-shot, few-shot, chain-of-thought, role-based) across different AI platforms (e.g., ChatGPT, Gemini, Claude, Copilot) in a specific task: text summarization.

## Scenario:
You are part of a content curation team for an educational platform that delivers quick summaries of research papers to undergraduate students. Your task is to summarize a 500-word technical article on "The Basics of Blockchain Technology" using multiple AI platforms and prompting strategies.

Your goal is to determine which combination of prompting technique + platform provides the best summary in terms of:

Accuracy

Coherence

Simplicity

Speed

User experience

## Algorithm

📘 Technical Article Input
Title: The Basics of Blockchain Technology
Length: ~500 words
Topic Highlights:

What is blockchain

How it works (blocks, cryptography, decentralization)

Use cases (finance, supply chain)

Advantages (transparency, immutability)

Limitations (energy use, scalability)

Note: Use the same article text across all experiments for consistency.

🧠 Prompting Techniques Overview
Technique	Description
* Zero-shot	Ask for a summary without providing any examples or context.
* Few-shot	Provide 1–2 examples of good summaries before asking.
* Chain-of-thought	Ask the model to explain the content step-by-step before summarizing.
* Role-based	Prompt the model as if it were a subject-matter expert (e.g., “You are an educator explaining to undergrads”).

🛠️ Platforms Used
* ChatGPT (GPT-4)

* Gemini Advanced (by Google)

* Claude 3 (Anthropic)

* Copilot (powered by OpenAI or GPT-4, depending on integration)

🧪 Experiment Design
For each platform, apply all 4 prompting techniques to summarize the same article. That gives you:

4 platforms × 4 prompting styles = 16 summaries total

** Sample Prompt Templates
* Zero-shot:

Summarize the following article about blockchain technology in simple terms for undergraduates.

* Few-shot:

Here are summaries of two technical articles. Based on those examples, summarize this article about blockchain.

* Chain-of-thought:

First explain how blockchain works step-by-step, then provide a simplified summary for undergraduates.

* Role-based:

You are a university professor creating a student-friendly summary of a technical article about blockchain. Summarize it in clear, engaging language.

📊 Evaluation Criteria

* Metric	Description

1.Accuracy: How well the summary reflects key points of the original article
2.Coherence: Logical flow and clarity of the summary
3.Simplicity: is it accessible and understandable to undergraduate students?
4.Speed: How quickly each platform delivers a usable summary
5.User Experience: Intuitiveness of prompt writing, interface usability, formatting, etc.
```

* Scoring Template (Example)
Platform	 Technique	      Accuracy (10)	   Coherence (10)	  Simplicity (10)	  Speed (10)	  UX (10)	 Total (50)
ChatGPT	   Few-shot	          9	                 9	                8              10	        9	       45
Claude	   Chain-of-thought  	10	              10	                9	              8	        8	       45
Gemini	   Zero-shot	        7	                 8	                8	              9	        7	       39
Copilot   	Role-based	      8	                 9	                9	              9	        8	       43
```
📋 Reporting Template
Include for each test:
Prompt use
smmary generated
Notes on performance (e.g., Was it too technical? Did it miss major points?)
Evaluation scores (as above)

📈 Outcome
You’ll analyze:
*Which platform + prompt combo gives the best educational summary
*Trade-offs between accuracy vs simplicity
*Which platform is fastest or easiest to use for this task

📌 Objective:
The goal is to evaluate how different prompting techniques perform across various AI platforms when summarizing a technical article intended for undergraduate students. This allows you to find out which combination provides the best quality summary for educational purposes.

🎯 Why This Matters:
AI-generated summaries are widely used in education, journalism, and content curation. However, how you prompt an AI can significantly affect the quality and clarity of the output. This experiment helps determine:

*
Which platforms are best for summarizing technical content.

*
Which prompting strategies make AI output more accurate and student-friendly.

🧪 Experiment Setup:
🔹 Article Input:
A ~500-word technical piece titled “The Basics of Blockchain Technology” covering:

* Blockchain definition
*Technical concepts (blocks, hashes, decentralization)
*Real-world uses
*Benefits and limitations

🔹 Prompting Techniques:
*Zero-shot: Ask directly for a summary with no example or context.

*Few-shot: Provide a couple of sample summaries first, then ask it to do a similar one.

*Chain-of-thought: Guide the AI to think step-by-step before summarizing.

*Role-based: Tell the AI to act as a teacher or domain expert simplifying the topic.

🔹 AI Platforms:
*ChatGPT (GPT-4)
*Google Gemini Advanced
*Anthropic Claude
*Microsoft Copilot
Each platform is used with each of the 4 techniques, giving a total of 16 tests.

📝 Evaluation Metrics:

Criterion	Description

1.Accuracy	Does it capture key points and facts correctly?

2.Coherence	Does it flow logically and make sense?

3.Simplicity	Is it understandable for an undergrad without technical background?

4.Speed	How quickly and efficiently does the AI return a usable summary?

5.User Experience (UX)	Is it easy to use the interface, write prompts, and interpret results?

6.Each is scored on a scale from 1 to 10, with 50 being the highest total per test.

* Zero-shot:
You ask the AI to perform a task (e.g., summarize) without giving it any examples. It's a direct instruction.

* Few-shot:
You give the AI a few example inputs and outputs first, then ask it to follow that pattern with a new input.

* Chain-of-thought:
You guide the AI to explain or reason step-by-step before giving the final answer (summary).

* Role-based:
You assign the AI a specific role or identity (like a teacher or expert) to influence the tone, style, or depth of its response.

1. Zero-shot Prompting
📌 What it is:
Zero-shot means giving the AI a direct task without showing examples of how it should respond. It relies purely on the AI’s general training.

✅ Example:
"Summarize this article about blockchain for undergraduate students."

✅ Pros:
* Fast and simple

* Easy to use across different tasks

❌ Cons:
* May lack accuracy or formatting if the request isn’t very clear

* Results can vary depending on how well the model generalizes

2. Few-shot Prompting
📌 What it is:
You provide a few examples (usually 1–3) to guide the AI's behavior. This helps it learn from the context.

✅ Example:
"Here are two summaries of technical articles.
Now summarize this blockchain article in a similar style."

✅ Pros:
*Improves quality and consistency

*Mimics supervised learning behavior

❌ Cons:
*Requires effort to craft good examples

*Longer prompts can slow down some models

3. Chain-of-thought (CoT) Prompting
📌 What it is:
You ask the AI to reason through the content step-by-step, then give the final summary. This encourages deeper understanding before summarizing.

✅ Example:
"First, explain how blockchain works in steps. Then, write a clear summary for students."

✅ Pros:
*More accurate and thoughtful responses

*Reduces factual errors in complex topics

❌ Cons:
*May be slower

*Not supported equally well across all models

4. Role-based Prompting
📌 What it is:
You tell the AI to respond as if it were a specific role (like a professor, journalist, or tutor). This affects tone, complexity, and structure.

✅ Example:
"You are a computer science professor explaining blockchain to first-year students. Write a clear and engaging summary."

✅ Pros:
*Makes output more audience-appropriate

*Encourages tone and style control

❌ Cons:
*Needs good role definition

*Can lead to overly elaborate responses if not framed well

✅ Conclusion
This experiment demonstrates that prompting technique and AI platform choice both significantly impact the quality of AI-generated summaries. Among the techniques tested—zero-shot, few-shot, chain-of-thought, and role-based—each has unique strengths depending on the platform and use case.

Few-shot and role-based prompting generally produced the most accurate and student-friendly summaries, especially when clarity and tone were critical.

Chain-of-thought prompting improved understanding of complex topics like blockchain but was slower and sometimes overly detailed.

Zero-shot prompting was the fastest and simplest but often lacked depth or missed key points without precise instructions.

Across platforms:

ChatGPT and Claude performed best in handling nuanced instructions.

Gemini offered good speed and simplicity but sometimes missed technical depth.

Copilot was consistent but more limited in creativity depending on integration.

Overall, the most effective combination for summarizing technical content for undergraduates was:

✅ Few-shot or Role-based prompting + ChatGPT or Claude

This pairing offered the best balance of accuracy, coherence, simplicity, and usability, making it ideal for educational content curation

## Result
Few-shot and role-based prompting produced the most accurate and student-friendly summaries.
ChatGPT and Claude performed best overall across clarity, coherence, and usability.
Zero-shot was fastest but less reliable, while chain-of-thought was detailed but slower.

