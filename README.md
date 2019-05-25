# Topic-Modelling
How to select the hyperparameters in topic models is the most crucial part of any topic modeling task.

For example, the alpha parameter controls the convergence of document-topic distribution. A small alpha gives 
a strong weight to the most influential topic for the document, meaning the model will more likely to consider the document 
is composed of a small number of topics, and vice versa. A rule of thumb given by Griffiths & Steyvers(2004) is to use 50/k, 
where k is the number of topics.

Another example is beta (or delta in Gibbs Sampling code), which controls the convergence of the word distribution under 
each topic. Similar to alpha, when a small beta (delta) is given, the model will most likely to choose a common word from the 
topic, leading to several peaks in the topic-word distribution. As beta grows bigger, dramatic peaks will start dissappearing, 
and the model will be more “flat”. The rule of thumb is to set beta (delta) equal to 0.1.

While the above mentioned parameteres have a general strategy for selection, how to determine the cut-off point for top words
and the number of topics is not covered. There is not really one best metric for these, and may depend on the task at hand. 
For example, if the user wishes to get a big picture of the corpus by topic modeling, the user should use a small number of 
topics to avoid information overloading, but oftentimes autonomous methods lead to a higher number of topics.

In this project, I explored two tasks:

1. How many top words should be picked from the topics:
   Cut-off point
2. How many topics should be used:
   Perplexity
   Extrinsic Method
   Intrinsic Method
   Document clustering
