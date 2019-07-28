
## Questions of Model and Feature Selection ##


QUESTION: HOW DO YOU TRADE-OFF BETWEEN BIAS AND VARIANCE?

ANSWER:

        High bias signifies that the model isn't able to identify certain features
        even if a very large dataset is provided for training, this signifies that
        model underfits, and we would try to increase the complexiety of the model,
        upto a level so that, it is able to improve itself, if larger training
        dataset is provided.
        But with the increasing complexiety of the model, the variance also starts,
        so, considering a highly complex model, the model will overfit.

        So, in order to find perfect trade-off, we should try with a low complexiety
        model, and gradually increase the complexiety and check it's performance
        on the validation set at each iteration. After a certain complexiety, the
        bias will be significantly low, and model would be able to generalize well
        on validation set.


QUESTION: WHAT ARE THE DIFFERENT ATTRIBUTES THAT CAN BE SELECTED BY MODEL SELECTION
          METHODS?
ANSWER: 

        Choice of different Machine Learning approach, for eg: SVMs, Logistic
        regression, etc - or chosing between different hyperparameters or sets of
        the same machine learning approach, -e.g deciding the complexiety fo the
        model, through deciding the polynomial degrees for linear regression.

QUESTION: WHY DO WE NEED VALIDATION SET?
ANSWER: 
        
        Validation is basically used to tune hyperparameters - you don't want to
        tune them on the training set because that can result in overfitting. nor
        do you want to tune them on test set, because than as we tuned it on test
        set, so we don't have any other dataset for checking the performance of the
        model, because the model had already seen all the data.

        That is why we tune our hyperparameters on a dataset different from both
        training and test dataset. We train our model on training dataset, we tune
        it's hyperparameters by checking it's performance with validation dataset.
        And finally check the performance of model on Test Dataset.

QUESTION: DESCRIBE DIFFERENT CROSS VALIDATION TECHNIQUES?
ANSWER: 
        
        Following are the various types of Cross Validation Techniques:

        a) K-Fold CROSS VALIDATION:
        We divide the whole dataset into k different subgroups. Now at each iteration
        the data of k-1 subgroups are used for training the model, and the remaining
        one subgroup is used as a validation set. This allows the model not to suffer
        from the underfitting due to less data (as in Holdout Validation). The error
        score is computed by averaging over all k iterations.

        b) STRATIFIED K-FOLD CROSS VALIDATION:
        It is a slight variation of the K-Fold Cross validation, in which we
        make each of the k-subgroups a representative of the whole dataset, by
        ensuring that the proportion of the positive and negative samples, are same
        in each subgroup as in the whole training dataset.

        The above two cross validation techniques are non-exhaustive cross validation
        techniques i.e only a selection combination of training and validation set
        are considered.

        c) LEAVE-P-OUT CROSS VALIDATION:
        In this technique, out of n data points, n-p are used for training, and
        p are used for validation, untill all the combinations are considered.
        Then the error score is computed by averaging over all possible combinations.
        This is an exhaustive cross validation technique.

To understand more: https://towardsdatascience.com/cross-validation-in-machine-learning-72924a69872f

QUESTION: WHAT IS HOLD-OUT CROSS VALIDATION? What are the advantages and disadvantages?
ANSWER: 
        
        HOLD-OUT CROSS VALIDATION is a validation technique, where a part of the
        dataset is separated (holded out) from it, and is used for tuning the hyperparameters.

        ADVANTAGES: It is better than traditional validation techniques.
        DISADVANTAGES: This technique can still produce model with high variance, because
        the evaluation highly depends on which data is in validation set, and which
        is in training set. We should ensure that both the datasets are a good representative,
        of the whole dataset.

QUESTION: WHAT IS K-FOLD CROSS VALIDATION? ADVANTAGES AND DISADVANTAGES?
ANSWER: 
        
        For definition look into above question.
        ADVANTAGES: Unlike, Hold-out cross validation, K-Fold cross validation,
        uses each data point in both training as well as validation, hence the
        evaluation process will not suffer from underfitting, due to lack of training
        data.
        DISADVANTAGES: It is a non-exhaustive technique.

QUESTION: WHAT IS LEAVE-ONE-OUT CROSS VALIDATION? ADVANTAGES AND DISADVANTAGES.
ANSWER: 
        
        DEFINITION is mentioned in one of the above questions.
        ADVANTAGES: It is an exhastive technique, which take all the possible
        combinations of dataset into account.
        DISADVANTAGES:

To understand better: https://www.analyticsvidhya.com/blog/2016/12/introduction-to-feature-selection-methods-with-an-example-or-how-to-select-the-right-variables/

QUESTION: WHY IS FEATURE SELECTION REQUIRED?
ANSWER: 
        
        Feature selection is one of the trivial part of building a machine learning
        model. Generally the data collected from a source consists of many unnecessary
        variables which aren't useful for out problem statement.
        Also, some of the variables may be correlated to each other, and the one doesn't
        add much information if first one is already added in our model, so these
        variables without adding any information, just increasing the computations.
        Also, irrelevant and partially relevant features can negatively impact the
        model performance.
        Hence, it is necessary to get right number of variables, and right features
        selected for an efficient and accurate model.


QUESTION: WHAT IS FORWARD FEATURE SELECTION METHOD? ADVANTAGES AND DISADVANTAGES.
ANSWER: 
        
        Forward feature selection is a wrapper method for feature selection, where we
        start with no features and add the features in the model one by one, untill
        the performance doesn't stops improving. The feature added is the one which
        best improves the performance.

        ADVANTAGES: It helps in identifing the correlated features, and avoid there
        incorporation in the model.
        DISADVANTAGES: The major disadvantage of any of the techniques using wrapper
        method is that, it uses a lot of computational resources and is a time
        consuming process.

QUESTION: WHAT IS BACKWARD FEATURE SELECTION METHOD? ADVANTAGES AND DISADVANTAGES.
ANSWER: 
        
        It is the opposite of forward feature selection method. We start from all
        the features and removes the least significant feature at each iteration
        which improves the performance of the model. We repeat this untill no further
        improvement is possible.

        ADVANTAGES: The backward feature selection ensures better optimiality of
        larger subsets than the forward feature selection because, the forward
        feature selection stops when the model performance stops improving, and
        hence, the subset of features selected may be not the optimal one,
        because later combinations weren't tried.

        DISADVANTAGES: The backward feature selection is computationally more
        expensive than forward if we consider stopping the iterations when no further
        improvements are achieved.

To Understand Better: http://clopinet.com/isabelle/Projects/ETH/Questions_lecture_8.html

QUESTION: WHAT IS FILTER FEATURE SELECTION METHOD AND DESCRIBE TWO OF THEM?
ANSWER: 
        
        Filter methods are independent of any machine learning algorithms, it basically
        finds some statistical relation between the response variable and the feature,
        and accordingly decide the importance of a particular feature.
        Some of the filter methods are:
        a) Pearson's Correlation.
        b) LDA: Linear Discriminant analysis.
        c) ANOVA: Analysis of Variance.
        d) Chi-Square Test.

QUESTION: WHAT IS MUTUAL INFORMATION AND KL DIVERGENCE?
ANSWER: 
        
        a) Mutual Information: The mutual information between two random variables
           is a measure of the mutual dependence between the two variables. More
           specifically, it quantifies the "amount of information" obtained about
           one random variable observing the other.
        b) KL-divergence:

To understand better: https://en.wikipedia.org/wiki/Mutual_information
