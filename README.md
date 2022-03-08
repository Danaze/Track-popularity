### Predicting the popularity of a spotify track
#### Dependencies
To run the notebook, the following python packages are required:<br />
   &nbsp;&nbsp;&nbsp; numpy <br />
   &nbsp;&nbsp;&nbsp;     matplotlib <br />
   &nbsp;&nbsp;&nbsp;     pandas <br />
   &nbsp;&nbsp;&nbsp;    keras<br />
   &nbsp;&nbsp;&nbsp;     sklearn <br />
   &nbsp;&nbsp;&nbsp;     seaborn <br />
This notebook goes through data preparation, anlysis and modelling to answer the following questions: <br />
The dataset can be downloaded from [here](https://www.kaggle.com/ektanegi/spotifydata-19212020)

##### &nbsp;&nbsp;&nbsp; 1. What are the features that influence spotify track popularity?
##### &nbsp;&nbsp;&nbsp; 2. How those features are distributed ?
##### &nbsp;&nbsp;&nbsp; 3. Based on 1 and 2, building a ML model for prediction.

In the notebook, the questions are analysed step-by-step to arrive at data-driven conclusions.
### Summary of Findings - Data exploration:
1. Features such as energy, year and valence has high variability <br />
2. Features such as liveness, danceability, tempo and loudness has relatively lower variablility and concentrated in some ranges. <br />
(distributions.PNG "Distribution of the features")
### Correlation
1. danceability and valence has high correlation <br />
2. loudness has high correlation with energy <br />
3. accousticness has negative correlation with energy, loudness, popularity and year <br />
4. popularity is highly positively correlated with year. Also loudness and energy seem to have strong correlation with popularity <br />

![alt text](corr.PNG "Correlation Matrix")
### Prediction
1. The deep learning model performance is very close to RF model performance.
2. The deep learning model shows no / only minor improvement (interms of validation data) after about 100 epochs. In this particular problem, the RF model can be the better option since it is computationaly less expensive and less prone to overfitting than the deep learing approach.
![alt text](dl.PNG "Training and validation metrics for the deep learning model")

### Acknowledgement
&nbsp;&nbsp; [1]. Spotify web API documentation, link [here](https://developer.spotify.com/documentation/web-api/reference/#/operations/get-track). <br />
&nbsp;&nbsp; [2]. Kaggle data set, link [here](https://www.kaggle.com/ektanegi/spotifydata-19212020). <br />
### Medium blog post summarizing the results is available [here]()