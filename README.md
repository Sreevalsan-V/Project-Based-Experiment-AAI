## NAME: SREEVALSAN V
## 212223240158
## 16/05/2024
## OBJECTIVE:
TO PERFORM SENTIMENTAL ANALYSIS ON THE FACEBOOK DATA AND COLLECT THE POSITIVE FEEDBACK FROM THE DATA.
## PROGRAM:
```
import nltk
from nltk.sentiment import SentimentIntensityAnalyzer

# Download NLTK resources
nltk.download('vader_lexicon')

# Load the sentiment analyzer
sia = SentimentIntensityAnalyzer()

# Example Facebook data
facebook_data = [
    "I love the new feature! It's amazing.",
    "The service was terrible. I'm very disappointed.",
    "Great job on the update!",
    "The product quality is poor. I won't be buying again.",
    "It's okay, nothing special.",
    "I'm not sure how I feel about the new changes.",
]

# Perform sentiment analysis and filter for positive feedback
positive_feedback = []

for message in facebook_data:
    sentiment_score = sia.polarity_scores(message)['compound']
    if sentiment_score > 0:  # Positive sentiment
        positive_feedback.append(message)

# Print the positive feedback
print("Positive Feedback:")
for feedback in positive_feedback:
    print(feedback)


```
## OUTPUT:
![image](https://github.com/Sreevalsan-V/Project-Based-Experiment-AAI/assets/152585309/b709cd20-fe91-4881-8153-47ee0b796713)

