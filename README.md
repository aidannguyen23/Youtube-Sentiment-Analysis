# YouTube Sentiment Analysis

## Overview

# YouTube Sentiment Analysis

This Python project utilizes PyTorch, transformers, and Google's YouTube Data API v3 to perform sentiment analysis on comments from a specified YouTube video, using the [DistilBERT model fine-tuned for multilingual sentiment analysis](https://huggingface.co/lxyuan/distilbert-base-multilingual-cased-sentiments-student). The sentiment distribution is presented through a pie chart visualization.


**I ran three youtube music videos through the program:**
1. Kanye West - Bound 2 : https://www.youtube.com/watch?v=BBAtAM7vtgc&ab_channel=KanyeWestVEVO
2. TWICE "FANCY" M/V : https://www.youtube.com/watch?v=kOHB85vDuow&ab_channel=JYPEntertainment
3. Spongebob Campfire Song :  https://www.youtube.com/watch?v=_9yhDpVUK3Q&ab_channel=superpielover100

**And obtained the following results:**

![image](https://github.com/aidannguyen23/Youtube-Sentiment-Analysis/assets/34725584/b1bc3278-7671-43ed-9296-339565bc71c5)

## Usage <a name="usage"></a>

1. Obtain a YouTube Data API key from the [Google Developers Console](https://console.developers.google.com/). Replace `DEVELOPER_KEY` in the `get_youtube_comments_df` function with your API key.

2. Run the Python script `analyze_sentiment.py` after specifying the target video ID:
    ```bash
    python analyze_sentiment.py
    ```

## Dependencies <a name="dependencies"></a>

- `torch`
- `transformers`
- `pandas`
- `numpy`
- `googleapiclient`
- `nltk`
- `matplotlib`

## Example <a name="example"></a>

Here's an example of how to use the code:

```python
# Set the target YouTube video ID
video_id = "_9yhDpVUK3Q"

# Fetch comments data
df = get_youtube_comments_df(video_id, max_results=100)

# Preprocess comments
# ... (cleaning and sentiment analysis steps)

# Visualize sentiment distribution
# ... (pie chart generation)
```
## Limitations:

1. Limited Sample Size due to YouTube API Restrictions
The YouTube Data API restricts the retrieval of comments to a maximum of 100 per request. Consequently, the project's sample size might be limited, potentially affecting the representativeness of the sentiment analysis. To mitigate this, consider strategies such as collecting comments from multiple API requests or focusing on videos with higher comment activity.

2. Model Reliability
Occasionally, the sentiment analysis model may fail to accurately predict sentiments for certain comments. As with any machine learning model, the predictions are based on the data it was trained on and might not generalize perfectly to all comment types or languages. Users should be aware that inaccuracies or misclassifications may occur, impacting the overall analysis.

Users can improve the analysis by aggregating results from multiple videos or refining the model with more diverse and extensive training data for enhanced performance across various comment types and languages.
