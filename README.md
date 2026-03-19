# Ex.No.6 Development of Python Code Compatible with Multiple AI Tools

## Aim:

Write and implement Python code that integrates with multiple AI tools to automate the task of interacting with APIs, comparing outputs, and generating actionable insights with Multiple AI Tools.

## Explanation:

Develop a python code that integrates multiple AI tool by interacting with their APIs. Compare outputs from different APIs. Analyze the response and the Output.

The aim is to understand how to request help from AI tools for tasks like writing Python code, integrating with APIs, comparing outputs, and generating actionable insights.

## Code for Positive Review:
```python

from nltk.sentiment import SentimentIntensityAnalyzer 
import nltk 
nltk.download('vader_lexicon') 

generated_text = "This smartphone offers outstanding battery life and an intelligent AI camera 
that captures stunning photos." 
print("Generated Review:\n") 
print(generated_text) 

sia = SentimentIntensityAnalyzer() 
sentiment = sia.polarity_scores(generated_text) 
print("\nSentiment Analysis:") 
print(sentiment) 

if sentiment['compound'] > 0: 
  print("\nInsight: The review is positive and suitable for marketing promotion.") 
else: 
  print("\nInsight: The review tone is neutral or negative.")
```
## Output:

<img width="782" height="166" alt="image" src="https://github.com/user-attachments/assets/5edffa52-9948-4beb-98e0-c1eb2c8232d4" />

## Code for Negative Review:
```python

from nltk.sentiment import SentimentIntensityAnalyzer
import nltk

nltk.download('vader_lexicon')


generated_text = "This smartphone has very bad battery life and a poor AI camera that takes blurry photos."

print("Generated Review:\n")
print(generated_text)


sia = SentimentIntensityAnalyzer()
sentiment = sia.polarity_scores(generated_text)

print("\nSentiment Analysis:")
print(sentiment)

if sentiment['compound'] > 0:
    print("\nInsight: The review is positive and suitable for marketing promotion.")
else:
    print("\nInsight: The review tone is neutral or negative.")
```
## Output:

<img width="858" height="188" alt="image" src="https://github.com/user-attachments/assets/dde04341-057f-4a9e-87b4-2295bf9283a0" />

## Result
The sentiment of the given reviews was successfully analyzed using the VADER sentiment analyzer:
- The positive review produced a high positive compound score (> 0), indicating favorable sentiment.
- The negative review produced a negative compound score (< 0), indicating unfavorable sentiment.

Thus, the system correctly classifies reviews based on their sentiment polarity.
