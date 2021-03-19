### Overview

For this project, two different subreddit APIs will be used to create binary classification models to classify which subreddit a given post came from. We seek to identifies features that most improve the accuracy of the models and limitations the models may have.
---
### Process

- Gather and prepare your data using the `requests` library.
- Create and compare models. (Naive Bayes, Logistic, KNN)
- Record the summary of the results you found.

### My Analysis

1. The model that predicts most accurately is a MultinomialNB model with TfidVectorizor. (Our product model)
2. It has roughly 92% accuracy.
3. It is a little overfitting (to be expected from regression models).
4. It is not overwhelmed with FN or FP (can be intrepretted as a good model)
5. The model predicts that these are the unique words for Smite category: god, conquest, tiamat, item, tp (Teleport), jungle
6. And for Heroes of the Storm category:  hero, talent, aram, blizzard, qm (Quick Match), sl (Storm League)
    
### Limitaions

1. Any discussion that are seldom to occur are likely to be predicted into the wrong category.
2. Short texts have higher chances of being predicted incorrectly
3. Model is sensitive to spelling errors.

### Conclusion

After creating the best model, which has high accuracy and low bias on False predictions, we can conclude that Smite reddit users are most interested in god, conquest, tiamat, item, tp (Teleport), and jungle. In the other hand, Heroes of the storm are most interested in hero, talent, aram, blizzard, qm (Quick Match), and sl (Storm League)
