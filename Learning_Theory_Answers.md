##  QUESTIONS ON LEARNING THEORY ##

QUESTION 1: DESCRIBE BIAS AND VARIANCE WITH EXAMPLES. (**)
ANSWER: 
        BIAS: Bias of the model is expected generalization error even if we were
              to fit in a very large-training set because there will be some patterns
              in the data that model can't capture due to lack of complexiety.

        VARIANCE: We would say that a model has a high variance, if it produces,
                  very low training eroor but a high generalization error because
                  of underfitting.

        To describe a set of values of a particular variable, let us say we define
        a polynomial function, so as we increase the degree of polynomial to fit
        the training data, the variance of the model increases while the bias
        decreases. While in lower degrees, bias is large but variance (complexiety)
        is very low.

        So, while selecting a model we should select the best possible Bias-VARIANCE
        trade-off, for ensuring a better quality model.

        SUMMARY: HIGH BIAS: --------> UNDERFITTING.
                 HIGH VARIANCE: ----> OVERFITTING.

Link: To understand better. (https://www.bmc.com/blogs/bias-variance-machine-learning)

QUESTION 2: WHAT IS EMPIRICAL RISK MINIMIZATION?
ANSWER: In a general setting, We want to minimize the true risk associated with
        our model, that it's predictions will deviate from the ground truth.
        But, since we don't know the true family of functions, or the true joint probability
        distribution which the data follows, it is not possible to calculate
        true expected risk in practical applications, so instead we calculate an
        empirical risk on the training dataset on our assumed hypothesis functions,
        and try to learn it's parameters by minimizing the empirical risk. This learning
        procedure is known as Empirical Risk Minimization.

Link: To understand better. (https://en.wikipedia.org/wiki/Empirical_risk_minimization)

QUESTION 3: WHAT IS UNION BOUND AND HOEFFDING'S INEQUALITY?
ANSWER:

QUESTION 4: WRITE THE FORMULA FOR TRAINING ERROR AND GENERALIZATION ERROR.
POINT OUT THE DIFFERENCES.
ANSWER: TRAINING ERROR: The error on the training dataset, i.e the dataset available
                        to the model while training, is known as training error.
                        In case of a classifier f(x).

                        Formula: E_train = sum(error(f(xi),yi))/n
                        where
                        (xi,yi): belongs to the training dataset.
                        error(): is sum function which is high if f(xi) and yi are
                        very dissimilar.

        GENERALIZATION ERROR: The error on the unseen or test data produced by the
                              model, is known as generalized error. Since, we want
                              our model to perform well on the unseen data, our major
                              target is to reduce the generalization error.

Generally, E_generalization is greater than E_train.

Link: To understand better. (https://www.youtube.com/watch?v=Xeo6LGcsxkg)

QUESTION 5: STATE THE UNIFORM CONVERGENCE THEOREM AND DERIVE IT.
