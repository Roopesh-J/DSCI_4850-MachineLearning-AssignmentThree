# DSCI_4850-MachineLearning-AssignmentThree

For this assignment we essentially are running 3 SVM models each with their own kernel (linear,poly,rbf). We want to run this 3 different models across 3 folds that we manually create. Then we choose the best fold for each model and then the best model.

## Results for Fold 1:
![fold1](https://user-images.githubusercontent.com/92547312/228123059-ecb87db2-4e56-4a84-9c32-f00014649c74.jpeg)

#### Linear Classification Report and Analysis: 
                   precision    recall  f1-score   support

               0       0.64      0.67      0.65      2651
               1       0.66      0.62      0.64      2698
        accuracy                           0.65      5349
       macro avg       0.65      0.65      0.65      5349
    weighted avg       0.65      0.65      0.65      5349

From the classification report for the linear model, it seems that precision and recall are close for both classes. This means that the model identifies both classes almost equally well but doesn't do better on any specific class. 

From the graph of the liner model, we can see the training accuracy and validation accuracy converge. This means that the generalization error decreases with more samples and that our model is performing well, however we have to be careful about overfitting. The two accuracy lines cross over, indicating that the model slightly overfits. 

#### Poly Classification Report and Analysis: 
                   precision    recall  f1-score   support

               0       0.74      0.26      0.39      2651
               1       0.56      0.91      0.69      2698

        accuracy                           0.59      5349
       macro avg       0.65      0.59      0.54      5349
    weighted avg       0.65      0.59      0.54      5349

From the graph, it seems that the validation and training accuracy graphs do converge however they both cross over multiple times indicating a bad 'fit'. 

From the classification report, the precision for class 0 is much higher than it is for class 1 and the opposite is true for recall. This means that the model is better at indentifying class 1. 

#### Rbf Classification Report and Analysis: 
                    precision    recall  f1-score   support

               0       0.64      0.67      0.65      2651
               1       0.66      0.62      0.64      2698

        accuracy                           0.65      5349
       macro avg       0.65      0.65      0.65      5349
    weighted avg       0.65      0.65      0.65      5349

The RBF model graph is similar to the linear graph, it converges but overfits very slightly. 

The classification report for this model shows the f1-score for both classes to be close, this means that the model performance is balanced between precision and recall. Though this is misleading sicne the accuracy is .65, which is not very high.

### Results for Fold 2:
![fold2](https://user-images.githubusercontent.com/92547312/228123998-907fba04-6d86-4429-bdab-47663b5ed0af.jpeg)

#### Linear Classification Report and Analysis: 
                    precision    recall  f1-score   support

               0       0.65      0.67      0.66      2708
               1       0.65      0.64      0.64      2641

        accuracy                           0.65      5349
       macro avg       0.65      0.65      0.65      5349
    weighted avg       0.65      0.65      0.65      5349

From the graph of the liner model, we can see the training accuracy and validation accuracy converge nearly perfectly. The lines don't crossover but but do appear to be touching. This still indicates some level of overfitting. 

#### Poly Classification Report and Analysis: 
                   precision    recall  f1-score   support

               0       0.77      0.23      0.35      2708
               1       0.54      0.93      0.68      2641

        accuracy                           0.57      5349
       macro avg       0.65      0.58      0.52      5349
    weighted avg       0.65      0.57      0.51      5349

The model has higher precision but lower recall for class 0 and vice versa for class 1, indicating a possible difficulty in identifying class 0 and higher chance of false negatives for this class.

#### Rbf Classification Report and Analysis: 
                    precision    recall  f1-score   support

               0       0.65      0.66      0.66      2708
               1       0.65      0.64      0.64      2641

        accuracy                           0.65      5349
       macro avg       0.65      0.65      0.65      5349
    weighted avg       0.65      0.65      0.65      5349

Because the model has a similar precision and recall for both classes, this indicates a balanced performance. This means that the model isn't better on class or the other. 

### Results for Fold 3:
![fold2](https://user-images.githubusercontent.com/92547312/228123998-907fba04-6d86-4429-bdab-47663b5ed0af.jpeg)

#### Linear Classification Report and Analysis: 
                        precision    recall  f1-score   support

               0       0.64      0.67      0.65      2684
               1       0.65      0.62      0.64      2665

        accuracy                           0.65      5349
       macro avg       0.65      0.65      0.65      5349
    weighted avg       0.65      0.65      0.65      5349

For both classe the precision and recall are similar, with class 0 having slightly lower precision and higher recall compared to class 1. This means that the model performance similarly for both classes, but has a slightly better recall for class 0.

#### Poly Classification Report and Analysis: 
                   precision    recall  f1-score   support

               0       0.74      0.24      0.36      2684
               1       0.54      0.91      0.68      2665

        accuracy                           0.58      5349
       macro avg       0.64      0.58      0.52      5349
    weighted avg       0.64      0.58      0.52      5349   

The model has high precision but low recall for class 0, which means it has some difficulty identifying instances class 0 and there is a higher chance of false negatives for it. On the other hand, the model has a lower precision but higher recall for class 1.

#### Rbf Classification Report and Analysis: 
                        precision    recall  f1-score   support

               0       0.64      0.66      0.65      2684
               1       0.64      0.62      0.63      2665

        accuracy                           0.64      5349
       macro avg       0.64      0.64      0.64      5349
    weighted avg       0.64      0.64      0.64      5349

Looking at the graph for this model, it is very obvious that the model is overfitting. In fact, we see it starting to oscillate between overfitting and underfitting. This means that the model will flip between the two fits as more and more data comes in. While it will still converge it is not a good way to train a model.
