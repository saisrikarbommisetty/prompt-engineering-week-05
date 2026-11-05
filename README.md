# Week 05 – Zero-shot vs Few-shot Sentiment Classification

## 1. Aim

To understand and compare zero-shot and few-shot prompting techniques by performing sentiment classification on product reviews using a Large Language Model.

## 2. Objectives

- Understand zero-shot prompting.
- Understand few-shot prompting.
- Compare classification using prompts with and without examples.
- Perform sentiment analysis on product reviews.
- Classify reviews into positive, negative, and neutral categories.
- Evaluate classification performance using predefined sentiment labels.
- Calculate and compare the accuracy of both prompting techniques.

## 3. Technologies Used

- **Programming Language:** Python
- **LLM Provider:** Google Gemini
- **Python SDK:** google-genai
- **Environment Management:** python-dotenv
- **Model:** gemini-3.6-flash

## 4. Experiment Description

This experiment demonstrates the difference between zero-shot and few-shot prompting through sentiment classification of five product reviews.

The program uses a predefined collection of reviews, each associated with an actual sentiment label.

### Zero-shot Prompting

Zero-shot prompting asks the model to classify a review without providing any classification examples.

The model is instructed to identify the sentiment as one of the following:

- Positive
- Negative
- Neutral

### Few-shot Prompting

Few-shot prompting provides sample input-output examples to guide the model's classification.

The experiment uses the following examples:

- "Best phone ever!" → positive
- "The camera is terrible." → negative
- "The phone works as expected." → neutral

The model then classifies the given review using these examples.

## 5. Dataset

The experiment uses five predefined product reviews:

| Product Review | Actual Sentiment |
|---|---|
| The battery life is amazing! | Positive |
| It works, nothing special. | Neutral |
| The camera quality is terrible. | Negative |
| I really love the display and performance. | Positive |
| The phone is okay, but nothing impressive. | Neutral |

## 6. Implementation Steps

1. Import the required Python libraries.
2. Load environment variables using python-dotenv.
3. Initialize the Google Gemini API client.
4. Select the Gemini model.
5. Define five product reviews with actual sentiment labels.
6. Create separate result lists for zero-shot and few-shot classifications.
7. Construct a prompt containing zero-shot and few-shot instructions.
8. Send the prompt to the Gemini model for each review.
9. Extract and display the generated classifications.
10. Store the predicted sentiment labels.
11. Compare predictions with actual sentiment labels.
12. Calculate the accuracy of both methods.
13. Display the comparison summary and conclusion.

## 7. Installation

Install the required dependencies:

```bash
pip install -r requirements.txt
```

## 8. API Configuration

Create a `.env` file in the Week-05 project directory.

Add your Google Gemini API key:

```env
GEMINI_API_KEY=your-api-key-here
```

The program loads the environment variable using:

```python
load_dotenv()
```

The Gemini client is initialized using the retrieved API key.

Never upload your actual API key to GitHub.

## 9. Execution

Run the Python program:

```bash
python experiment5.py
```

The program processes all five reviews and displays their actual labels, predicted sentiments, and final accuracy comparison.

## 10. Expected Output

The console displays:

- Product reviews.
- Actual sentiment labels.
- Zero-shot classifications.
- Few-shot classifications.
- Zero-shot accuracy.
- Few-shot accuracy.
- Final comparison and conclusion.

The accuracy is calculated using the number of correctly classified reviews out of five.

## 11. Accuracy Calculation

The experiment calculates accuracy using:

**Accuracy = (Correct Predictions / Total Reviews) × 100**

For five product reviews:

**Accuracy = (Correct Predictions / 5) × 100**

The program compares the number of correct predictions for both prompting techniques.

## 12. Analysis

Zero-shot prompting relies on the model's existing knowledge and the instructions provided without classification examples.

Few-shot prompting provides sample classifications that help guide the model toward the expected sentiment categories.

The experiment compares the classification results to understand whether providing examples improves sentiment prediction accuracy for the selected reviews.

## 13. Result

Successfully implemented a sentiment classification experiment using Python and the Google Gemini API. Compared zero-shot and few-shot prompting techniques on five product reviews and evaluated their classification performance using predefined sentiment labels.

## 14. Conclusion

This experiment demonstrates how providing examples within a prompt can guide a Large Language Model toward the desired classification format. It also provides practical experience in sentiment analysis, prompt design, prediction evaluation, and accuracy comparison.

## 15. Project Structure

```text
Week-05/
│
├── experiment5.py
├── requirements.txt
├── README.md
└── outputs/
    └── execution screenshots
```