# Building a Better Brain 
Module 20 Challenge

## Overview of Project
The purpose of this project was to showcase the ability to build, train, compile/run, and optimize a Neural Network using Keras DeepLearning. There are some major sections but ultimately it was the same as any machine learning challenge: most of the heavy lifting was done in the pre-processing step, while the hardest part of the actual modeling was waiting for it to finish.

## Results

We set out on this challenge to answer 6 questions posed by the Project. They will be answered in sequential order, with image support for the majority.

<img width="558" alt="1" src="https://user-images.githubusercontent.com/116296092/227808609-c30ef18a-bab7-4b66-9484-06bc691612eb.png">

For the first two: Which variables are considered targets, and which are considered features? These are fairly easy to answer, as we want to know whether a loan's Status is active (approved) or not, and that will be based on the remainder of the application and the information contained within application_df. Those variables are the features, while approval (status) is the target.

IMAGE

Data that is not considered to be a target or a feature would this case be the Employer Identification Number (EIN) and the Name of the company being considered. Neither of these has any bearing on the application status or whether they were approved, and so their columns were dropped at the beginning of the process to not provide extra noise, potentially confusing the model.

IMAGE

In this model, per the screenshot of the "finished" nn.summary(), I used 80 neurons in the first layer, and 30 in the second. This allowed me to match the output of nn.summary() to the challenge checkpoint in the walkthrough. This also provided the model with a terrifying degree of accuracy out of the gate, which will be discussed.

IMAGE

I was able to acheive and severely surpass the targeted accuracy rating of 75%. According to the module, the pre code is allegedly less than that, which is where deliverable 3 would have come into play. Perhaps surprisingly, the model came up with a 99.98% accuracy rating on the data fed to it, with an initial loss metric of 2%. This is acceptable for nearly any application I might be using it for in the class, and certainly for many applications outside of it for predictive purposes. Steps were not taken to increase performance, as overfitting is already a concern. Further optimization would hurt the model.

## Analysis and Challenges

Overall, the deep learning model was a successful excersize in prediction of data. It was able to minimize its loss over the epochs it was trained on, and was able to fit almost perfectly (but not too much so that it was a 100% rate and overfit) in the first instantiation. Further runs would better refine it, as it continues to learn. Other models may be used for this task however, and one that would be far simpler to parse and set up in the first place would be a RandomForest model. As many categories as there are, and defined along hard lines as a yes or no approval, a RandomForest model would be able to accurately predict (though with potentially less accuracy) the same results, while also being easier to read and far less resource/time intensive to complete its prediction compared to the Keras net. RF's also require far less knowledge to adapt and replicate, unlike a Deep learning model that would require weight checkpoints and an h5 file export/import to be tested or used by another operator elsewhere.