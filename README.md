# Making Predictions over Amazon Recommendation Dataset
- The link to the project: https://github.com/tiq015UCSD/Making_Predictions_over_Amazon_Recommendation_Dataset/blob/main/Tian_Qin_NLP.ipynb
## Scenario
Natural Language processing skills are very useful when conducting analysis ontext data. A typical use case would be extracting sentiment from customer
feedback on certain products. The feedback could be comments on the websites, conversation log with customer support .Eg. Amazon launched a newproduct
that can provide video of the their product on the Amazon page, if we need to gather some first hand user response (positive or negative) so as to make a
decision on whether to expand this feature or not, a NLP analysis on the comments below the video would be a good start.
## Process
1. Data Cleaning: 
    1) Stopwords removal: words like ‘the’, ‘a’, ‘me’.... could be removed, since theydon’t reflect any sentiment indication  
    2) Stemming: words will be transform to its stem, eg, tasty -> tasti, no specific meaning, just a protocal to process the text
    3) Punctuation removal: mostly, punctuation like, ‘,’, ‘.’, ‘?’, ‘!’ are all removed. However, currently some emoji symbols are also encoded as text in order toget abetter understanding of the sentiment. But, this is NOT required
    4) Upper/lower case
2. Feature Engineering
    - Python package:  
          from sklearn.feature_extraction.text import CountVectorizer  
          from sklearn.feature_extraction.text import TfidfVectorizer
    - Text to Vector
        1) unigram: one word is taken as an input
        2) Bigram: two words together are taken as one input
        3) TFIDF:  
https://towardsdatascience.com/tf-idf-for-document-ranking-from-scratch-in- python-on-real-world-dataset-796d339a4089#:~:text=TFIDF%20stands%20for%20%E2%80%9CTerm,Information%20Retrieval%20and%20Text%20Mining.
3. Model Building
    - Python package：
            from sklearn.linear_model import LogisticRegression  
            from sklearn.ensemble import RandomForestClassifier   
            from sklearn.model_selection import train_test_split   
    - Train / Test data split
4. Model evaluation
    - What metrics should you use to evaluate your model and how to interpret theresult?     
            Metrics:ROC,AUC, Precision,Recall,F1 etc

5. Feature Importance
