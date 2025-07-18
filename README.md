Project Summary: Chatbot using NLP and Cosine Similarity
This project demonstrates the development of a simple rule-based chatbot using Python and fundamental Natural Language Processing (NLP) techniques. The chatbot is designed to generate responses based on a pre-defined dataset of dialogues.

🔧 Key Components:

1. Dataset Understanding & Preprocessing
A dialogues dataset is used as the chatbot's knowledge base.

Each dialogue line is analyzed for sentiment and cleaned using text normalization techniques:

Lowercasing

Removing punctuation

Stopword removal

Lemmatization

2. Feature Extraction & Matching
The cleaned dialogues are vectorized using TF-IDF (Term Frequency-Inverse Document Frequency) to represent text numerically.

Cosine Similarity is computed between the user’s query and all dataset lines to find the most relevant response.

If the similarity score is above a threshold, the chatbot returns the closest match.

3. Sentiment Analysis
Sentiment is computed (likely using a library like TextBlob or VADER) for each example.

This helps in understanding the emotional tone of conversations and can be used to tailor responses in future improvements.

4. Error Handling
If the user's input has low similarity to any known dialogue (i.e., it's an irrelevant or unknown question), the bot responds with a fallback message like:

“I'm sorry, I don't understand your question.”

5. Chatbot Function
A reusable Python function is developed to handle:

Input cleaning

Vectorization

Similarity matching

Sentiment feedback

Response generation

