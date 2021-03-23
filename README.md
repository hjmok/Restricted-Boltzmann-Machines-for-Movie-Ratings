# Restricted-Boltzmann-Machines-for-Movie-Ratings

For this project, a Restricted Boltzmann Machine model predicts whether a user will like or dislike a movie. 


## Dataset and Library
PyTorch was the main module used for this model.

The dataset consisted of 1 million rows of movie ratings from 6040 users across 3952 films. A rating of 1 or 2 is considered disliked and 3 or more is considered liked.
Please find the dataset from Grouplens and select the 'MovieLens 1M Dataset':
https://grouplens.org/datasets/movielens/

## Restricted Boltzmann Machines Overview
Restricuted Boltzmann Machine (RBM) is an unsupervised learning algorithm, resulting in no outputs and no back propagation. This means RBMs only have visible and hidden nodes. RBMs use Contrastive Divergence to update the weights of nodes by having the every visible node that is connected to every hidden node updating each other. The RBM is constantly updating the values between the visible and hidden nodes until convergence, meaning the values no longer change. 

RBMs are good algorithms to use for recommender systems. This is because the hidden nodes learn to extract key features about the inputs when learning. Using this project as an example, the RBM would get whether a user liked or disliked the movies as the inputs. Then the hidden layer would try to understand why each user liked certain movies, having each hidden node group common traits among the films such as the genre, certain actors/directors, etc. This way, once the hidden layer establish nodes for the key features, it can then use said nodes to recommend further films to specific users.

For more details, please read the following paper by Asja Fischer and Christian Igel, as well as the implementation on Github:

http://cms.dm.uba.ar/academico/materias/1ercuat2018/probabilidades_y_estadistica_C/5a89b5075af5cbef5becaf419457cdd77cc9.pdf

## Results
After 20 epochs, the training and test losses achieved were 0.228 and 0.204 respectively. This means that the RBM model was able to predict whether a user liked or disliked a new movie roughly 4/5 times.

For the resulting image, please visit: https://hjmok.github.io/josephmok_portfolio/#/RBM
