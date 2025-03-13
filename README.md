## Artwork_classification
**This is the task project for GSoC 2025 application for the ArtExtract Project.**

In this project, wikiart data was used. To classify the artist, genre, and style of the picture, two
different kinds of convolutional neural networks were used which are **AlextNet model** and
**ResNet model**. To save time, I have used Res50 as the basic model and re-train the last 20
layers.
After training the two models, I used soft voting to stack the two models. In soft voting, each base
model gives a probability or confidence estimate for each category, which is then averaged or
weighted. The final prediction is the category with the highest average probability (or weighted
average probability).

The result shows that the models perform considerably well on the *_train.csv data. However, on the 
*_val.csv data, the model performs not so good. By the way, it can be found that the f-1 scores are 
high correlated with the scale of the training data. Thus, we may conclude that this is not caused 
by the model training problem but caused by the data preparations.
