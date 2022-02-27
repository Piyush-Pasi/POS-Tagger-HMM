# Implementing POS Tagging using HMM and Viterbi algorithm

**Platform** : Python Jupyter, Google Colab or VS Code.  
VS Code (version 1.59.0) was used to run the code. 

## Common libraries used in Bigram and Trigram based implementations
nltk (version 3.2.5)  
IPython (version 7.26.0)  
numpy (version 1.19.5)  
pandas (version 1.1.5)  
pickle (version 4.0)  
regex (version 2019.12.20)  
seaborn (version 0.11.1)  
sklearn (version 0.24.2)  
matplotlib (version 3.2.2)  

### Additional library used in bigram based implementation
ipywidgets (version 7.6.3)

## Running the code
### Running HMM_Viterbi_Bigram_Model.ipynb
The section "Train function" contains the function to train the model given the training data.  

The "Prediction function" section contains the function which tests the model using the generated transmission and emission probabilities.  

The POS_tag_assign() function assigns tags according to the model and returns the predicted tags.  

**Run all the cells** to generate the confusion matrix, overall metrics and per POS tag metrics of the model.

### Running HMM_Viterbi_Trigram_Model.ipynb
###### Note:
Skip train_test_split if custom train,test sets are used  
If you are using your custom train and test set make sure data type is same: train_set , test_set : List[ List[ tuple(word,tag) ] ]  

To train call: HMM_Viterbi_Train(train_set)  
Train Function returns Emission and Transition Probability tables which are arguments for testing and prediction

To test call: HMM_Viterbi_Test(test_set, transitionProbTable, emissionProbTable) # transitionProbTable, emissionProbTable are output from train function  

For custom sentence testing : Run cells in Section "Custom Sentence Testing"  

###### Caution:  
Testing for large no. of sentences is slow for Trigram assumption  
Run all cells for functions to be defined, Note and Cautions are mentioned in the Notebook as well  

## References
https://www.mygreatlearning.com/blog/pos-tagging/  

https://github.com/zachguo/HMM-Trigram-Tagger/blob/edb3351e2f0a58ea6bcfacbadb7167624ab1637b/HMM.py#L53  

https://github.com/parthasm/Viterbi-Bigram-HMM-Parts-Of-Speech-Tagger/blob/0dde0677d7bad5caeb5055a4a924635249d301a6/Viterbi_POS_Universal.py  

http://csci572.com/papers/SpeechLanguageProc.pdf  

https://nlp.stanford.edu/~wcmac/papers/20050421-smoothing-tutorial.pdf  

https://stathwang.github.io/part-of-speech-tagging-with-trigram-hidden-markov-models-and-the-viterbi-algorithm.html  

https://web.stanford.edu/~jurafsky/slp3/3.pdf  

https://www.isip.piconepress.com/courses/msstate/ece_8463/lectures/2004_fall/lecture_33/lecture_33.pdf  

https://www.kaggle.com/deepanshusinha/hmms-and-viterbi-algorithm-for-pos-tagging  

https://medium.com/data-science-in-your-pocket/pos-tagging-using-hidden-markov-models-hmm-viterbi-algorithm-in-nlp-mathematics-explained-d43ca89347c4  

https://medium.com/hackernoon/building-a-bigram-hidden-markov-model-for-part-of-speech-tagging-1b784a87ab2c  
