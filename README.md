# Machine-learning-lab
Simple API to serve a model forecasting Churn

This API is written in [Python] and it uses a number of open source projects to work properly:

* [Flask](https://flask.palletsprojects.com/) - Framework for provisioning of APIs
* [scikit-learn](https://scikit-learn.org/) - Machine learning library
* [xgboost](https://xgboost.ai/) - Another machine learning library
* [pickle](https://docs.python.org/3/library/pickle.html) - Library to saving and loading pretrained models

The notebook contains the preprocessing of the data and the different tested models. XGBoost is the best performer with around 86% of accuracy for this dataset.

### Local install
This API requires Python and the libraries in the file requirements.txt

1. Clone the repository
2. Run by executing the following command on the root directory of the project

```
python app.py
```

#### Testing the app

Send an explicit example to check the working:

```
curl --location --request GET 'http://localhost:3001/query?feats=465,France,Female,51,8,122522.32,1,0,0,181297.65'
```

If all is OK, you should get
```
{"response": [1]}
```

#### Acknowledgment

This is a [fork](https://github.com/platzi/laboratorio-machine-learning) of a little project proposed in a laboratory course on [Platzi](https://platzi.com), and this is my proposal of solution for this challenge.
