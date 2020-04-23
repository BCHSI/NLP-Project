# UC Berkeley MEng Capstone Project

This project, combined with cTAKES (we assume that you have used cTAKES and have some basic understanding of how it works), is used for enable precision medicine and improving the working efficiency for medical NLP researchers. To summarize briefly, it's consist of three parts. 

#### 1.UserInterface
The first one is in the UserInterface Folder, which builds User Interface to display output of cTAKES added with some additional features: The comprehensive distribution of confidence score of the whole medical data, in which you can click on each datapoint to access more detailed information about that datapoint. Also in the main webpage, you can see the output of cTAKES in a organized way and a corresponding confidence score of that concept. When you click on the concept, all the reference sentence from original text from medical records where the medical concepts are extracted will appear on the page. By clicking on any of them, the user will be able to label the data as right or wrong in terms of the output of cTAKES.

#### 2.NLP Metrics
One important component of our project is the calculation of NLP metrics, the second one is the mechanism behind the calculation of NLP metrics, including BLEU Score, Cosine Similarity, Jaccard Similarity, Levenshtein Similarity, Elmo Score.

#### 3.Machine Learning Models
As mentioned in the UserInterface part, one of the ultimate goals is to display the confidence score to the users. Using the NLP metrics data calculated for each concept as X, the user labeld data as label y, we were able to train several machine learning models to predict the confidence score for each concept. These models include Logistic Regression, SGD Classifier, KNN Classifer as well as Random Forest, among which random forest has the best performance and we incorporate this machine learning model into our user interface for the confidence score prediction.

The way it works is that we calculated NLP metrics including BLUE Score, Cosine Similarity, Elmo, Jaccard Similarity, Levenshtein Similarity from the output of cTAKES as X for machine learning, and we label 1000 data manually as y. After the machine learning model has been trained, when there are new data, the model will predict the confidence score of new data based on the calculated NLP metrics of that datapoint. Afterwards, all the information will be displayed in the user interface and the user can keep continuing labeling the data for machine learning to improve system reliability so that there's a active learning and prediction loop.

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.

### Prerequisites

What things you need to install the software and how to install them

```
Give examples
```

### Installing

A step by step series of examples that tell you how to get a development env running

Say what the step will be

```
Give the example
```

And repeat

```
until finished
```

End with an example of getting some data out of the system or using it for a little demo

## Running the tests

Explain how to run the automated tests for this system

### Break down into end to end tests

Explain what these tests test and why

```
Give an example
```

### And coding style tests

Explain what these tests test and why

```
Give an example
```

## Deployment

Add additional notes about how to deploy this on a live system

## Built With

* [Dropwizard](http://www.dropwizard.io/1.0.2/docs/) - The web framework used
* [Maven](https://maven.apache.org/) - Dependency Management
* [ROME](https://rometools.github.io/rome/) - Used to generate RSS Feeds

## Contributing

Please read [CONTRIBUTING.md](https://gist.github.com/PurpleBooth/b24679402957c63ec426) for details on our code of conduct, and the process for submitting pull requests to us.

## Versioning

We use [SemVer](http://semver.org/) for versioning. For the versions available, see the [tags on this repository](https://github.com/your/project/tags). 

## Authors

* **Billie Thompson** - *Initial work* - [PurpleBooth](https://github.com/PurpleBooth)

See also the list of [contributors](https://github.com/your/project/contributors) who participated in this project.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

* Hat tip to anyone whose code was used
* Inspiration
* etc

# UC Berkeley MEng Capstone Project: UCSF NLP UI for Apache cTAKES

Welcome to the UI Github.
You can find our preliminary python code in jupyter notebooks in the "Notebooks" directory.
These notebooks give information on the Word2Vec model training and the confidence score model training.

I am currently working on making this project installable to make it easier to deal with.
Until then, you can simply clone the repository, unzip the best_cosine_model file in the flaskr/cosine_similarity_model directory, and then run the flask application in a python GUI (e.g. Pycharm or Microsoft Visual Studio).

You must also install all the necessary packages and dependencies manually currently.

Please note that the performance of the UI may be slightly slow currently, as we are using advanced NLP pipelines to calculate the "confidence scores".

Thanks for trying this out!
The UCSF NLP Team.
