# An analysis on using the features in the provided dataset to create a binary classifier that can predict whether applicants will be successful if funded by Alphabet Soup.

## Summary
The nonprofit foundation Alphabet Soup wants a tool that can help it select the applicants for funding with the best chance of success in their ventures. With your knowledge of machine learning and neural networks, you’ll use the features in the provided dataset to create a binary classifier that can predict whether applicants will be successful if funded by Alphabet Soup.

From Alphabet Soup’s business team, you have received a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. Within this dataset are a number of columns that capture metadata about each organization, such as:

EIN and NAME—Identification columns

APPLICATION_TYPE—Alphabet Soup application type

AFFILIATION—Affiliated sector of industry

CLASSIFICATION—Government organization classification

USE_CASE—Use case for funding

ORGANIZATION—Organization type

STATUS—Active status

INCOME_AMT—Income classification

SPECIAL_CONSIDERATIONS—Special considerations for application

ASK_AMT—Funding amount requested

IS_SUCCESSFUL—Was the money used effectively

## Data Processing
Target Variable = "IS_SUCCESSFUL" 
Features = "AFFILIATION", "CLASSIFICATION", "USE_CASE", "ORGANIZATION", "STATUS", "INCOME_AMT", "SPECIAL_CONSIDERATIONS", "ASK_AMT"
Deleted Variables = "EIN" and "NAME"

## Training and Evaluating the Model
### First Attempt
Used 2 hidden layers. Layer 1 was 80 nodes and layer 2 was 30 nodes with epochs of 100

<img width="652" alt="Screenshot 2023-04-06 at 9 26 57 AM" src="https://user-images.githubusercontent.com/106120403/230392357-79930432-e102-46a8-ad54-e94127f025c5.png">

This had an accuracy of 0.7310

### Second Attempt
Increased the number of hidden layers to 3. Layer 1 was 100 nodes, layer 2 was 70 nodes and layer 3 was 50 nodes with epochs of 100

<img width="652" alt="Screenshot 2023-04-06 at 9 30 30 AM" src="https://user-images.githubusercontent.com/106120403/230393215-bdc85a3f-e364-4f62-b1a6-bde9009cc7c9.png">

This had an accuracy of 0.7273 (i.e. the accuracy reduced)

### Third Attempt
Kept the same number of hidden layers from attempt 2 and changed the activation function used in the hidden layers from relu to sigmoid. Increased epochs to 150

<img width="652" alt="Screenshot 2023-04-06 at 9 40 27 AM" src="https://user-images.githubusercontent.com/106120403/230395648-051eaee1-4710-45c3-a3d7-3e81c14c8b64.png">

This had an accuracy of 0.7298 (i.e. the accuracy is less than attempt 1 but slightly higher than attempt 2)






