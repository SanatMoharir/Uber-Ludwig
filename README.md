# Uber-Ludwig
All the ML projects done using the uber's LUDWIG

What is Ludwig ?

Ludwig is a toolbox built on top of TensorFlow that allows to train and test deep learning models without the need to write code.


For All instructions about the installation you can refer: https://uber.github.io/ludwig/getting_started/  


All Examples of the commands and input files will be passed to ludwig

Model Definition: {input_features: [{name: content, type: text}], output_features: [{name: airline_sentiment, type: category}]}


Ludwig Train: ludwig train --data_csv ./Tweets.csv --model_definition "{input_features: [{name: content, type: text}], output_features: [{name: airline_sentiment, type: category}]}"


Ludwig Visualize: ludwig visualize --visualization learning_curves --training_statistics ./Tweets.json


Ludwig Predict: ludwig predict --data_csv path/to/data.csv --model_path /path/to/model


Ludwig Visualize: ludwig visualize --visualization compare_performance --test_statistics path/to/test_statistics_model_1.json path/to/test_statistics_model_2.json


Available datatypes in Ludwig:

    binary
    numerical
    category
    set
    bag
    sequence
    text
    timeseries
    image
