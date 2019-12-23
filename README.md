# Spam_classifier
A binary classifier which classifies a given document as a spam or non-spam.


Let’s consider a straightforward document classification problem: deciding whether or not an e-mail is spam.
We’ll use a bag-of-words model, which means that we’ll represent a document in terms of just an unordered
"bag" of words instead of modeling anything about the grammatical structure of the document. If, for
example, there are 100,000 words in the English language, then a document can be represented as a 100,000-
dimensional vector, where the entries in the vector corresponds to a binary value 1 if the word appears
in the document and 0 otherwise. Of course, most vectors will be sparse (most entries are zero).

We have implemeted a Naive Bayes classifier for this problem. For a given document D, we’ll need to evaluate
P(S = 1| w1,w2..,wn), the posterior probability that a document is spam given the features (words) in
that document. The Naive Bayes assumption, which says that for any 'i' not equal 'j', w_i is independent from
w_j given S. (It may be more convenient to evaluate the likelihood (or "odds"), and
compare that to a threshold to decide if a document is spam or non-spam.)

A dataset of known spam and known non-spam emails is already made, and
split into a training set and a testing set. Our program accepts command line arguments like this:

./spam.py training-directory testing-directory output-file

The training-directory contains two subdirectories called spam and notspam, containing
email files that can be used to estimate the needed probabilities of the model. The testing-directory contains
test emails, one per file; our program outputs a output-file in a format like this:

00393.85c9cd10122736d443e69db6fce3ad3f spam
01064.50715ffeb13446500895836b77fcee09 notspam

and so on, where the first part of each line is a filename and the second is predicted class (spam or notspam).



The data files are compressed for faster upload/download.

Use the command "tar -xzf data.tar.gz" on Linux to extract the files or WinRar on Windows.

First few paragraphs, explaining the background were taken from a coding assignment by Prof David Crandall from his course B551.