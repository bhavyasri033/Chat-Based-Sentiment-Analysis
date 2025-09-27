#  Chat-Based Sentiment Analysis  

---

##  Overview  
This project focuses on building a **chat-based sentiment analysis system** capable of classifying user messages into **Positive, Negative, or Neutral** categories.  
It applies **Natural Language Processing (NLP)** techniques, **TF-IDF vectorization**, and a **Naive Bayes classifier** to analyze text data, including handling **emojis** for richer sentiment understanding.  

The project includes both **model training** and an **interactive chat-based interface**, where users can input text and receive real-time sentiment predictions.  

---

##  Features  
- 📝 Text preprocessing (tokenization, stopword removal, emoji handling, normalization)  
- 😀 Conversion of emojis to text for accurate sentiment interpretation  
- 🔤 **TF-IDF vectorization** to extract meaningful features from text  
- 🤖 **Naive Bayes classifier** for sentiment prediction  
- 📊 Model evaluation using accuracy, classification report, confusion matrix, and ROC curve  
- 💬 Real-time **interactive chat interface** for testing custom inputs  

---

## 📂 Dataset  
- The dataset used contains text messages labeled as **Positive, Negative, or Neutral**.  
- Preprocessing steps included:  
  - Converting emojis to text  
  - Removing punctuation, stopwords, and duplicates  
  - Normalizing text to lowercase  
- Dataset format:
| TEXT                         | REACTION |
| ---------------------------- | -------- |
| I love this project! 😊      | positive |
| This is terrible 😡          | negative |
| Okay, I will check it later. | neutral  |


---

##  Methodology  
1. **Data Cleaning**  
 - Removed duplicates and null values  
 - Standardized sentiment labels  

2. **Text Preprocessing**  
 - Emoji conversion → `emoji.demojize()`  
 - Lowercasing, punctuation removal  
 - Stopword removal (`nltk.stopwords`)  
 - Tokenization  

3. **Feature Extraction**  
 - Used **TF-IDF Vectorizer** with bi-grams and max 5000 features  

4. **Model Training**  
 - Applied **Naive Bayes Classifier** (MultinomialNB)  
 - Split dataset: **80% training / 20% testing**  

5. **Evaluation**  
 - Accuracy Score  
 - Classification Report (Precision, Recall, F1-score)  
 - Confusion Matrix visualization  
 - ROC Curve for multi-class performance  

6. **Interactive Testing**  
 - Implemented chat-based interface for real-time predictions  

---

##  Results  
- ✅ Model achieved strong performance in sentiment classification  
- ✅ Balanced results across **Positive, Negative, Neutral** classes  
- 📈 Evaluation metrics:  
- **Accuracy**: ~85-90% (depending on dataset size and quality)  
- High **Precision and Recall** for positive/negative classes  
- 📊 Visualizations included:  
- Sentiment distribution plot  
- Confusion Matrix  
- ROC Curve for multi-class classification  

---

##  Conclusion  
This project demonstrates how **NLP + Machine Learning** can be applied to sentiment analysis in chat systems.  
The Naive Bayes model combined with TF-IDF proved to be **efficient, interpretable, and fast**, making it suitable for real-time applications.  
Handling **emojis** added significant improvements to sentiment detection in casual, chat-like messages.  

---

## Future Scope  
- 🌐 **Web deployment** using Flask/FastAPI for real-world usage  
- 📱 Integration into **chatbots** for customer support and social media monitoring  
- 🤯 Experimentation with **deep learning models (LSTMs, BERT, Transformers)**  
- 📈 Expand dataset with **multi-domain and multilingual data**  
- 🔔 Sentiment-aware **recommendation systems** for personalized interactions  

---

##  Tech Stack  
- **Language**: Python  
- **Libraries**:  
- Data: `pandas`, `numpy`  
- NLP: `nltk`, `emoji`, `re`, `string`  
- ML: `scikit-learn`  
- Visualization: `matplotlib`, `seaborn`  

---

##  Usage  
```bash
# Clone repo
git clone https://github.com/your-username/chat-sentiment-analysis.git
cd chat-sentiment-analysis

# Install dependencies
pip install -r requirements.txt

# Run the script
python sentiment_analysis_(project).py

