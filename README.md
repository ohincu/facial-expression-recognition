# Facial Expression Recognition 

Facial Expression Recognition (FER) is a computer vision task that aims at detecting a human's emotions.   
This project focuses on recognizing three primary facial expressions: anger, happiness, and sadness, through a CNN model.

## Data
The dataset comprises of 48x48 pixel grayscale facial emages labeled by emotion/facial expression.  
The emotions present in this dataset are put into 7 categories: angry, disgust, fear, happy, sad, surprise, neutral.  
The data is already split into training, validation and test data in the dataset.

You can find the dataset via https://kaggle.com/competitions/challenges-in-representation-learning-facial-expression-recognition-challenge.
originally curated by "Dumitru, Ian Goodfellow, Will Cukierski, Yoshua Bengio. (2013). Challenges in Representation Learning: Facial Expression Recognition Challenge. Kaggle."

## Packages used  
* Data Manipulation: pandas, numpy
* Data Visualization: matplotlib, scikitplot
* ML: scikit-learn, tensorflow, keras

## Methodolody
The CNN model is trained using Keras, has 3 convolution layers followed by two fully connected layers and finally an output layer.  
Once developed, the model is saved in a JSON file for easy access and reuse.

## Challenges
**Training data**  
The data consists of images where the face expression cannot be instinctively be identified even by a human, e.g. a neutral from a sad expression. Also, some images that are labeled as "sad" could be easily be labeled as "neutral".
Some facial expressions are subtle, making it difficult even for humans to distinguish between them, such as differentiating neutral from sad expressions. Additionally, some "sad" images could easily be labeled as "neutral." While the emotional data is generally balanced, the "disgust" emotion is underrepresented, accounting for less than 5% of the dataset.

**Data quality**  
The data is in low-resolution, and that poses a big challenge as facial expressions hinge on subtle features throughout the face, including the eyes, mouth, nose, cheeks, and more.  
Imperfect lighting and varying angles in the images further complicate the recognition process.

## Results & Future work
The model achieved a peak accuracy of approximately 76%. It's important to note that the focus was on three emotions only.  
Expanding the model to include all seven emotions would likely result in a drop in accuracy.

Improvements could be made with better labeling, higher-resolution training data, and improved lighting conditions.  
However, one has to remember that certain emotions, e.g. "disgust," can even be hardly identified by humans.   

![Alt text](accuracy.png)

![Alt text](loss.png)

### Ethical Considerations
It's essential to stress that the collection and monitoring of facial data must be carried out ethically and with consent. 
Neglecting this can lead to privacy and security concerns, potentially exposing individuals to misuse of their data by 
malicious third parties. 
