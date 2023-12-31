# YouTube Sentiment Analysis

## Overview

This repository contains Python code for sentiment analysis on YouTube comments using PyTorch, transformers library, and Google's YouTube Data API v3. The project aims to analyze sentiments expressed in comments on a specific YouTube video and visualize the sentiment distribution through a pie chart. 

I ran three youtube music videos through the program:
1. Kanye West - Bound 2 : https://www.youtube.com/watch?v=BBAtAM7vtgc&ab_channel=KanyeWestVEVO
2. TWICE "FANCY" M/V : https://www.youtube.com/watch?v=kOHB85vDuow&ab_channel=JYPEntertainment
3. Spongebob Campfire Song :  https://www.youtube.com/watch?v=_9yhDpVUK3Q&ab_channel=superpielover100

And obtained the following results:
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
