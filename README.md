# Modern-Language-Models
Assignment 5 (100 points)
This week, there are two tasks, one exploration and one synthesis. As usual, you'll be turning in both code and a PDF write-up.

Task 1: Exploration: Modern Language Models and Problematic Content (30 points)
As we briefly mentioned in Lecture 8 and as you'll learn about more in Reading Response 4, pre-trained language models are currently all the rage in the natural-language processing community. To be fair, they seem to do some cool things really well!

In this exploration task, sign up for a free OpenAI account so that you can use the OpenAI API Links to an external site.with the free credits you are given. Don't pay for extra credits, nor upgrade!

We want you to explore their API, such as the Completion API Links to an external site.. Using either the in-browser ``playground'' feature or by writing a script to make API calls, we want you to explore 10 facets of what this API does related to ethics, privacy, or the topics of this course. In some cases, you may find problematic behaviors, which would be very interesting to document. In other cases, you may find problematic behaviors accompanied by explicit content warnings (e.g., "Completion may contain sensitive content"); please document the cases where the content warning appears. In other cases, you might find that the API's response(s) don't seem to be problematic.

Write-up Question 1 (30 points, 3 each): Specifically, come up with ten questions to investigate (e.g., "Can I get the OpenAI API to reveal private information about Blase?" or "How does the API classify text about Chicago?"). For each, document three things:

What question are you investigating?
How did you investigate this question? Please record the specific queries (or examples thereof, if there are many) that you tried.
What did you find?
You don't need to submit any code for this task. However, if you scripted some interactions, please do submit that code to Canvas.

Task 2: Synthesis: Featurizing and Building an ML Model for Redacting AOL Search Data (70 points)
You'll recall that we discussed the AOL search data fiasco Links to an external site.in Lecture 2.

In this task, we want you to build a machine learning classifier that can be used to (attempt to) redact the seach data. This should be a binary classifier that assigns either the label redact'' ordo not redact'' to each token (word) in the search query column of the AOL search logs.

You can download just the readme and one of the 10 component files (227 MB). You definitely do not need to use all of this data. So that not everyone is dealing with the same data, if you're using a subset of the data, it'd be more interesting for us if you use the shuf command Links to an external site.to randomly permute the lines of the file. That said, you are also welcome to download the full logs (390 MB compressed, expands to 2.3 GB. In any case, do not further distribute these logs, try to look up or deanonymize the data subjects, or do anything else problematic with the data!

(28 points) The core part of what we want you to do for this task is feature engineering. Think about what features of the words might be good to feed into your model. Come up with, and implement, at least 8 features beyond the words themselves that you think will be useful in classifying whether a token should be redacted. At least 5 of these features should be non-trivial and involve either external data or external API calls. In contrast, we consider trivial features things like the length of the word or the part of speech.

Write-up Question 2 (4 points): Using bullet points, list the features you chose and briefly (at most one sentence!) explain why you chose each.

(10 points) By hand, label the redactions you would manually make for at least 100 queries. You should do this in machine-readable form for training your classifier. **Submit these manual redactions as part of your submission on Canvas.

(10 points) Train at least two different classifiers (in terms of architectures, like a logistic regression and an SVM model) for this task using your manual redactions. We realize that an alternative approach would involve just using those heuristics with a bunch of if-statements, but we want you to build a classifier.

Write-up Question 3 (10 points): Thinking back to Lecture 8, report the metrics you think are most important for these two classifiers and explain why you think those are the most important metrics for this task.

Write-up Question 4 (8 points): Briefly discuss what your classifier was able to redact successfully, as well as what it was not, on at least 100 lines (queries) of testing data (data other than what you redacted manually).
