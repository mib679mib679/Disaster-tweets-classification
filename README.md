This is an attempt on classify a series of tweets into two classes - disaster-related or not related.<br />
I performed preprocessing to clean the text to help enhance the model performance. This process included correcting some typos, removing non-english characters, special characters, digits, emojis, URLs, punctuations, aiming to make the data as clean as possible. 
However, removing urls might have negetively impacted the model performance as many URLs appeared in disaster-related tweets.
To compensate the lack of data, I used a low-level data augmentation technique, where words were randomly replaced to artificially generate more training data.
I trained a transformer model to classify the tweets and acheived 78% accuracy, which I believe represents almost the maximum predictability with this data. 
A similar project on kaggle used BERT and acheived 82% accuracy but still didn't acheived perfect predictions.

Several thoughts on how to further improve the results:
1. Fixing all the typos might help improve predictions, though this is very time-consuming and generally not recommended.
2. In this project I ignored the keyword column, which might be useful for improving predictions.
3. Implementing a more advanced data-augmentation technique could involve replacing each keyword with a synonym to enhance the model.
4. t-SNE could be used to generate data visualisations to examine whether there is text data overlap or not, which might explain why some data is difficult to predict accurately.

