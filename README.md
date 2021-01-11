# Q-A-system-benchmarking-using-word-embeddings-
The main purpose is to find the top 3 and top 5 matched paragraphs from the corpus data for every question. Through this project the motive is to extract data from the SQuAD dataset and then pre-processing it to make it ready for vectorization. We have used the Fasttext model for vectorization because it takes into account the internal structure of words while learning word representations.

This project is implemented on two models- pretrained and self trained. In each model, we have taken data from SQuAD dataset and have considered those questions which are not inference based. The data is converted to dataframe. The questions and texts are then converted using our model and stored in the list.
For each question, we will iterate over all paragraph vectors and will check whether the correct paragraph is matched with our top 3 and top 5 predicted similar paragraphs. The accuracy of the model will be returned. We will again find the accuracy but after removing the stopwords in both questions and paragaraphs.
To further increase the accuracy, we will modify the cosine similarity formula to find the similarity between the question and a sentence in a paragraph. Therefore, instead of considering the whole paragraph, we will only consider the most similar sentence as the cosine similarity value of that question with that paragraph. 
At last, we will print the top 5 most similar paragraphs from the original set of paragraphs for the given question.

In the case of self-trained model, the parameters in it are chosen in such a way to get the best accuracy possible.
