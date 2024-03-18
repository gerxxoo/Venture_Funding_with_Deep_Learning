# Venture_Funding_with_Deep_Learning

BACKGROUND
You work as a risk management associate at Alphabet Soup, a venture capital firm. Alphabet Soup’s business team receives many funding applications from startups every day. This team has asked you to help them create a model that predicts whether applicants will be successful if funded by Alphabet Soup.

The business team has given you a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. With your knowledge of machine learning and neural networks, you decide to use the features in the provided dataset to create a binary classifier model that will predict whether an applicant will become a successful business. The CSV file contains a variety of information about these businesses, including whether or not they ultimately became successful.


PROJECT
The project is broken into three major segments. Segment one requires the preparation of the data. A csv containing features of 34,000 companies is provided. The companies' EIN and name is irrelevant to the final decision, so those are dropped. I then take the categorical features and assign them a variable. I encode the categorical features using OneHotEncoder and create a new data frame with the new encoded data. After, I take the numerical features and concatenate them to the encoded categorical ones to create a data frame with all numerical values. Finally, I separate my y variable (whether the company is successful) from the X variables (all other features). At this point the data is prepared.

The second segment invloves the creation of a nueral network model. I begin by setting the number of input features equal to the number of columns in my X variables data frame. Neural network models involve plenty of trial and error, so I decide to assign 58 nodes to the first layer and 29 to the second. I just took the initial amount of inputs (116) and kept dividnig by two. I create my Sequential model instance and begin adding the layers to the model. I compile the data using binary_crossentropy for loss and, adam as the optimizer, and accuracy as the metric I am searching for. I then fit the model using 50 epochs and making sure the data is shuffled after each epoch. Now the model is ready.

The final segment only requires making some changes to the original model to create two new updated versions. All I changed on the first update is the amount of nodes in the layers. The first layer has 50 nodes and the second has 25. The second update also has a change of nodes, but also has a third layer added. The layers have 75, 50, and 25 nodes, respectively. The results of each model are interesting. Much to my surprise, the original model performs the best with a loss of .6023 and an accracy of .7265. The first updated model has a loss of .6495 and an accuracy of .7285. The second updated model has a loss of .6417 and an accuracy of .7293. The accuracy is essentially equal across the three models. It is a small advantage in loss where the orginal model takes the lead. 


CODE SOURCE
The code was fully sourced from classwork assignments. 


TECHNOLOGIES
This project requires the use of pandas, pathlib, tensorflow, and sklearn. Dense and Sequential were imported from tensorflow. OneHotEncoder, StandardScaler, and train_test_split were imported from sklearn.The project was developed using Python on a Visual Studio Code. 