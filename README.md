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
Source Material Preparation: Select a 500-word technical article, "The Basics of Blockchain Technology," to be used as the single, consistent input for all tests. A control summary will be manually written to serve as a benchmark for accuracy.

Platform Setup: Access and normalize settings (if possible) across the four target platforms: ChatGPT, Gemini, Claude, and Copilot.

Prompt Technique Formulation: Design four distinct prompts for the same article, one for each technique:

Zero-Shot: A simple, direct command.

Prompt: "Summarize the following text:"

Role-Based (Persona): Uses the specific persona from the scenario.

Prompt: "You are part of a content curation team for an educational platform. Your task is to summarize the following 500-word technical article on 'The Basics of Blockchain Technology' for undergraduate students. Your goal is to be accurate, coherent, and simple."

Chain-of-Thought (CoT): Asks the model to reason first, then summarize.

Prompt: "Read the following article. First, identify the 3-5 main concepts. Second, explain what each concept means in one sentence. Finally, combine these explanations into a single, simple summary for a student."

Few-Shot: Provides one example of a good summary before giving the real task.

Prompt: "Here is an example of how to summarize a technical text for a student:

Original: 'Cloud computing is an on-demand delivery model for IT resources over the Internet with pay-as-you-go pricing. Instead of buying, owning, and maintaining physical data centers and servers, organizations can access technology services, such as computing power, storage, and databases, from a cloud provider. This involves IaaS (Infrastructure-as-a-Service), PaaS (Platform-as-a-Service), and SaaS (Software-as-a-Service).'

Summary: 'Cloud computing lets you rent computing services, like storage or processing power, over the internet instead of owning your own expensive hardware. This pay-as-you-go model helps companies save money and easily scale as needed.'

Now, using the same simple and clear style, summarize this article on Blockchain:"

Execution and Data Collection: Run each of the 4 prompts on all 4 platforms, for a total of 16 tests. For each test, record the following:

The generated summary (Output).

Speed: Time from prompt submission to full response generation (in seconds).

User Experience (UX): Qualitative note (e.g., "Easy," "Required re-prompting," "Formatted poorly").

Comparative Analysis (Evaluation): Create a rubric to score each of the 16 summaries from 1-5 on the three key criteria:

Accuracy: Does the summary correctly represent the article's main points without errors?

Coherence: Does the summary flow logically and read as a single piece of text?

Simplicity: Is the language free of jargon and understandable to an undergraduate with no prior knowledge?

## Result

The experiment confirmed that the prompting technique had a more significant impact on summary quality than the choice of AI platform.

The Role-Based (Persona) prompt was the clear winner. It consistently produced the best balance of Accuracy, Coherence, and Simplicity by directly addressing the scenario's goal and audience (undergraduate students).

Zero-Shot prompts were fast but often too technical, failing on Simplicity.

Chain-of-Thought improved Accuracy but sometimes harmed Coherence, producing lists instead of paragraphs.

Few-Shot prompts yielded good results but at a high cost to User Experience and Speed due to the setup required.

All four platforms proved capable, with minor differences in rephrasing. The conclusion is that the Role-Based prompt is the optimal strategy for this task, as it provides the necessary context for any of the tested platforms to succeed


