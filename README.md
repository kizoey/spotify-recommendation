# spotify-recommendation
<p align="left">
  <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=Python&logoColor=white"/></a>&nbsp
  <img src="https://img.shields.io/badge/GoogleColab-F9AB00?style=flat-square&logo=GoogleColab&logoColor=white"/></a>&nbsp 
</p>
<b><i>Spotify recommendation</i></b> recommends spotify music according to your preference. The project is initiated by the curiosity of: Can music preferences be determined through numerical attributes rather than linguistic methods? We used <b><i>Spotify</i></b> open dataset including variables such as loudness, time_signature, liveness and more. We built a classification and recommendation system to classify music according to its taste and further recommend similar music to the user.<br>
The results of each classifier/recommendation model implemented are shown below.


<h2> major Contributions </h2>

- **Recommendation system** theory learning and practical experience
- Experience in learning and implementing various classification models
- Built **customized** dataset for recommendation
- Analysis and reasoning of the experiment results 

<h2> Directory </h2>

### _algorithms_
- **data_eda**: 데이터 EDA와 이에 맞는 전처리
- **classifier_models**: 분류 모델 학습
- **recommendation_models**: 추천 모델 학습
- **ensemble**: Classifier과 recommendation 모델 코드 모두 합치기


### _data_
- **spotify_data**: 잡코리아/링커리어에서 크롤링 후 전처리한 데이터 csv 파일


<h2> Results </h2>

<h3> Classifier </h3>

model | F1(%)
---- | ----
RandomForest (Randomized CV)|72.98
RandomForest (Grid Search CV)	|71.09
RandomForest	|72.03
XGBoost	|75.00
Voting(XGBoost + KNN + SVM +MLP)	|72.12
Voting(XGBoost + XGBoost)	|71.84
Lasso	|63.41
Ridge	|63.81
ElasticNet	|62.86
**CatBoost**	|**100.00**
ADABoost (Randomized CV)	|71.69
ADABoost (Grid Search CV)|	70.75
GDBoost (Randomized CV)	|70.81
GDBoost (Grid Search CV)|	70.24
Voting(ADABoost + GDBoost)	|72.30


<h3> Recommendation </h3>

model | baseline | RMSE
---- | ---- | ----
MF (SVD) | - | 0.7232
KNN_basic | user | 0.7712
KNN_basic | item | 0.7216
KNN_means|user|0.7568
KNN_means|item|0.7254
KNN_zscore|user|0.7571
KNN_zscore|item|0.7339
KNN_baseline|user|0.754
KNN_baseline|item|0.7317
Neural network|basic|0.7604
Neural network | without layers|0.7260
Neural network | without layers/nationality added|0.7250
Slopeone|-|0.7591
CoClustering|-|0.7479
**Hybrid**|-|**0.8117**
