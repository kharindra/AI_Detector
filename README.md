### AI Text Detector

---

**Problem Statement**

The goal of this project is to develop an AI text detector for distinguishing between human-generated and AI-generated text with increased accuracy.

**Data Collection**

**SubReddits used for collecting data**

The following subreddits were selected to gather question-answer pairs, and the same questions were utilized to obtain responses from CHATGPT.

      science
      relationship_advice
      funny
      NoStupidQuestions
      AskReddit
      gaming
      unresolvedmysteries
      wewantplates
      disneyvacation
      talesfromretail
      antiMLM
      IDontWorkHereLady
      nevertellmetheodds
      publicfreakout

---
**Here, we have divided the modeling part into two sections.**

      1.) Model with Countvectorizer
      2.) Model with TfidfVectorizer

Below is the list of classification models used  

**The models that we used here:**

- LogisticRegressionCV
- MultinomialNB
- BernoulliNB
- KNN Classifier
- RandomForest Classifier
- AdaBoost Classifier
- SVM Classifier


Among the options mentioned above, we discovered that the LogisticRegressionCV model, combined with the CountVectorizer, outperformed the others. The results from the confusion matrix and model evaluation strongly support the conclusion that this particular model is the most effective.

<img src="img/Cvec/Confusion_matrix_from_Logr.jpg" width="50%">

The table below indicates the comparison of the model performances based on the scores.

| Model                | Score on train | Score on test | Sensitivity | Specificity | Precision |
|----------------------|-----------------|---------------|-------------|-------------|-----------|
| logr                 | 0.962           | 0.903         | 0.854       | 0.948       | 0.939     |
| Randomfc             | 0.996           | 0.882         | 0.864       | 0.898       | 0.888     |
| KNN                  | 0.877           | 0.809         | 0.702       | 0.909       | 0.878     |
| MultinomialNB        | 0.842           | 0.819         | 0.884       | 0.757       | 0.773     |
| BernoulliNB          | 0.881           | 0.863         | 0.834       | 0.891       | 0.877     |
| AdaBoostClassifier   | 0.925           | 0.883         | 0.843       | 0.920       | 0.909     |
| LinearSVC            | 0.982           | 0.892         | 0.849       | 0.931       | 0.921     |


**Conclusion**

---

Our findings indicate that retaining stopwords within our model enhances the accuracy of the AI text detector. Remarkably, the highest accuracy is achieved when employing the logistic regression with cross-validation (LogisticRegressionCV) model.

