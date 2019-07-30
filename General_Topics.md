## Curse of Dimensionality ##

QUESTION: DESCRIBE THE CURSE OF DIMENSIONALITY WITH EXAMPLES.
ANSWER: 

        The curse of dimensionality refers to the problem we face while the high
        dimensional spaces are used instead of the low dimensional spaces. As we 
        increase the number of features in our model, there is a requirement of 
        exponential increase in the required dataset size in order to maintain the data 
        density. 
        So, as we add more and more feature to our model, the training data becomes 
        sparser, and hence we end up overfitting on the training data. Hence, it's not
        always necessary that the model performance will increase by increasing number 
        of features, it goes up intially and then comes down again. 
        
TO UNDERSTAND BETTER: https://medium.com/diogo-menezes-borges/give-me-the-antidote-for-the-curse-of-dimensionality-b14bce4bf4d2

QUESTION: WHAT IS LOCAL CONSTANCY OR SMOOTHNESS PRIOR OR REGULARIZATION.
ANSWER:

        Local Constancy means, that a model's values should not change drastically if we make
        small changes in the input features. The function should be smooth. This is one of the
        most comman priors used in Simple Machine Learning Algorithms.  
        
        Example: K-means Clustering, the examples in the similar region are same. (extreme case)
        
TO UNDERSTAND BETTER: https://cedar.buffalo.edu/~srihari/CSE676/5.11%20MLBasics-Challenges.pdf


## Deep Learning Motivation ##

QUESTION: WHAT IS THE MATHEMATICAL MOTIVATION OF DEEP LEARNING AS OPPOSED TO STANDERD MACHINE LEARNING 
          TECHNIQUES?
