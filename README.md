# Coursera Tiktok Dataset Analysis

RandomForestClassifier is an ensemble learning method that builds multiple decision trees during training and merges them for better prediction stability and accuracy. It reduces overfitting by averaging the results of various trees, each trained on a subset of the data.

XGBClassifier is an advanced gradient-boosting algorithm that builds decision trees sequentially. Each new tree improves upon the accuracy of the classifier by correcting the errors of the previous trees.

Both classifiers were applied to the dataset (not included in repository) and were trained to predict whether or not a video was a 'claim' or an 'opinion'. The variables in the dataset are shown below:

- \# (int64)
- claim_status (object)
- video_id (int64)
- video_duration_sec (int64)
- video_transcription_text (object)
- verified_status (object)
- author_ban_status (object)
- video_view_count (float64)
- video_like_count (float64)
- video_share_count (float64)
- video_download_count (float64)
- video_comment_count (float64)
- new variable: transcription_len (int64)

"video_transcription_text" was cut from the analysis completely due to my lack of expereince in string vectorization in Python. "claim_status" was the target variable, so that was also cut from the dataset. Verified status was a variable with 3 states, so it was normalized. A new variable, transcription_len, was also used, and it was the number of characters in video_transcription_text.