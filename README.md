# Depression-Analysis
The project could be run as a notebook using jupyter or google colab

Minimum System Requirements:
8GB RAM is preferred.
A CPU with the Advanced Vector Extensions (AVX) instruction set
Operating System:
Windows 10 and 11 (Intel/AMD 64-bit)
Linux (Intel/AMD 64-bit, kernel 3.10.0 or higher, glibc 2.17 or higher)

Link to the sources and datasets used:
https://drive.google.com/drive/folders/159VbfG9SYB_C6m_gT8dhekqbSN7AFY3v?usp=share_link

Contains 2 datasets, 1 with tweets that indicate depression and the other containing random tweets that do not necessarily indicate depression. 
The google news vectors file contains the pretrained vectors for word2vec model 

Due to the lack of publicly available dataset for depressive tweets, the essential dataset for this research was compiled by the web scraper TWINT, which used the keyword depression to collect all tweets from a given day.

The initial steps include preprocessing the data inorder to expand contractions, remove emojis,hashtags,@mentions, and stop words of NLP. After which Tokens are generated.

Word2Vec is used to group together similar words.

TF-IDF is used to find out the term frequency that depicts how important a word is in a document

Different models were trained
- A baseline model (SVC) that uses TF-IDF
- Naive bayes classifier
- SGD Classifier
- Logistic Regression Model
- LSTM

A CNN+LSTM model used gave an accuracy of 99.61% . In order to determine the optimal fit, various activation functions such as sigmoid, tanh, and softmax were utilised in the hidden layers. Given that logistic regression models provide good accuracy for binary classifications, the models' accuracy is compared to that of the LRM, and the model with the highest accuracy is ultimately picked. The ReLU function, which is implemented by the majority of CNNs in their activation layer, has been applied to all models. The various models explore the various optimizers and loss functions before concluding on the top model with an accuracy of 99.61%.
Though the baseline model gave us the same results as the LSTM, the best model is chosen as the latter as it does further weight updation and error reduction using optimizers
