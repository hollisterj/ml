## Chapter 1 Exercises

1. How would you define Machine Learning?
   - Machine Learning is the field of study that gives computers the ability to learn without being explicitly programmed to do so. Machine learning algorithms learn and adjust by evaluating data.
1. Can you name four types of problems where it shines?
   - Problems for which existing solutions require a lot of fine-tuning or long lists of rules. The existing solutions can be a pain to maintain when new data necessitates new rules. Ex. An effective spam filter that adapts to new patterns in spam.
   - Problems that are too complicated for traditional approaches or have no known algorithm. Ex. Speech recognition, recognizing hand-written characters.
   - Problems involving fluctuating environments as machine learning algorithms can adapt to changes.
   - Problems where patterns aren't easily recognizable by humans. Machine learning can detect and inform on correlations and trends.
1. What is a labeled training set?
    - A training set where the correct solution (label) is saved with each data element.
1. What are the two most common supervised tasks?
    - A supervised learning task is one where the training set also includes the label (solution). The two most common supervised tasks are:
      - Classification. Assigning a class to data elements.
      - Regression. Predicting a target value by evaluating predictors.
1. Can you name four common unsupervised tasks?
    - Unsupervised tasks do not have labels assigned to the training data.
      - Clustering. Group the data by learned correlations.
      - Anomaly detection and novelty detection. Detecting when data does not fit within learned bounds. Ex. outlier detection.
      - Visualization and dimensionality reduction. Visualization tasks arrange complex data into visual representations to help the analyze the data. Dimensionality reduction. Simplifying the data without losing too much information. For example combining two features that are highly correlated.
      - Association rule learning. TODO add explanation.
1. What type of Machine Learning algorithm would you use to allow a robot to walk in various unknown terrains?
    - First, you need to evaluate the terrain in order to adjust the style of step to take. Regression could be used sequentially to predict the target position of the next step.
    - Reinforcement learning could also be used to evaluate the environment and select the appropriate walking style.
1. What type of algorithm would you use to segment your customers into multiple groups?
    - Clustering would be effective to segment customers into groups by similar features.
1. Would you frame the problem of spam detection as a supervised learning problem or an unsupervised learning problem?
    - Spam detection would need to be a supervised learning problem. I don't think unsupervised learning would be effective at detecting spam vs. ham.
1. What is an online learning system?
    - A system that uses tests sets sequentially in order to adapt. Online learning is incremental learning.
1. What is out-of-core learning?
    - Algorithms that operate on data sets that are too large to fit into a particular machines memory. Chunks of data are processed sequentially to stay within memory capacity.
1. What type of learning algorithm relies on similarity measure to make prediction?
    - Instance based learning. The algorithm assigns a similarity weight to new data based on test data and classifies it accordingly.
1. What is the difference between a model parameter and a learning algorithm hyperparameter?
    - A learning algorithm hyperparameter is a parameter of the learning algorithm and not of the model. One hyperparameter is regularization which reduces the risk of overfitting. Once the hyperparameter is set, it is used to evaluate the training set as well as the operational data.
1. What do model-based learning algorithms search for? What is the most common strategy they use to succeed? How do they make predictions?
    - Model based learning algorithms search for the best data-fitting equation most commonly by minimizing the cost function. The algorithm makes a prediction by evaluating the data-fitting equation given the data.
1. Can you name four of the main challenges in Machine Learning?
    - The four main challenges in Machine Learning are:
      - Insufficient quantity of training data. ML algorithms need thousands of examples for simple problems and millions for complex problems.
      - Nonrepresentative training data. Poor performance occurs because the training data did not comprehensively represent the real data.
      - Poor quality data. Errors in the test data, outliers and noise will reduce model performance.
      - Irrelevant features. The features in the training data are not effective in determining the desired solution.
1. If your model performs great on the training data but generalizes poorly to new instances, what is happening? Can you name three possible solutions?
    - The model is overfitting the data. Three possible solutions are:
     - Holdout validation. Separate a validation set from the training set. Train the model on the training set (minus the validation set) and then select the model that performs best on the validation set.
     - Perform cross-validation. Use many small validation sets to select the model parameters that work best over all the small validation sets.
      - Use a train-dev set. The train-dev set is held out from the training data. If the model works well on the train-dev set, then the model is not overfitting the data. If it is not, then the data in the train-dev set is significantly different than the training set data. There is a data mismatch.
1. What is a test set, and why would you want to use it?
  - The test set is used to evaluate the performance of the model tuned on the training set. Without validation of the model how would you be confident in deployment?
1. What is the purpose of a validation set?
   - The validation set is used to evaluate performance of the models being developed. It provides feedback on what set of model parameters worked well and which ones did not.
1. What is a train-dev set, when do you need it, and how do you use it?
  - A train-dev set is a set-aside of "real" data. It should be used when there could be a significant difference between the training set and "real" data. A model that is performing well on the test set can also be used to evaluate the train-dev set. Whether the model performs well or not on the train-dev set is indicative of overfitting or data mismatch.
1. What can go wrong if you tune hyperparameter using the test set?
  - Risk of overfitting the data and poor performance once the model is deployed.
