# Twitter-users-biography-based-classifier

This project is about classifying Twitter users in 10 pre-defined classes based on their textual biography.
To extract the biography for the users I used the  API. The only initial requirement to run this API is a key and a column with the users' SenderScreenName information (their unique name on twitter)

To build the training set I downloaded some pre defined lists of hundreds of twitter users belonging to each specific class considered by the classifier.
To avoid noisy calls given by the limited amount of data and the high number of classes, I developed n binary classifiers (n = # of classes), instead of building a single multiclassifier.

The final results were above the average standards for industrial classification problems in terms of f1-score and accuracy
