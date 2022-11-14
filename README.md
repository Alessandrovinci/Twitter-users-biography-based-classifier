# Twitter-users-biography-based-classifier

This project is about classifying Twitter users in 10 pre-defined classes based on their textual biography.

To build the training set I downloaded some pre defined lists of ScreenNames belonging to hundreds of twitter users belonging to each specific class considered by the classifier. Given the ScreenNames, I extracted the biography of the users using the twitter Developers free API (https://developer.twitter.com/en/docs/twitter-api/users/lookup/api-reference/get-users). 

The only initial requirement to run this API is a developer key and a column with the users' SenderScreenName information (their unique name on twitter). 

After this step I had an initial database where each row had these information: SenderScreenName, Biography, label (10 classes in total)
To avoid noisy calls given by the limited amount of data and the high number of classes, I developed n binary classifiers (n = # of classes), instead of building a single multiclassifier.

Following a thorough model selection and tuning process, a Stochastic Gradient Descent with hinge loss was the best performing algorithm for almost all the classes.
The final results were above the average standards for industrial classification problems in terms of f1-score and accuracy.

Thank you for your attention.
Hope you enjoyed it :)

