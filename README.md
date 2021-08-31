# urban-soud-classification
Classification of the UrbanSound8K using CNN.

I have tried to classify the various sounds that are frequently heard in residential areas.
The UrbanSound8K dataset has been chosen.

This dataset contains 8732 labeled sound excerpts (<=4s) of urban sounds from 10 classes: air_conditioner, car_horn, children_playing, dog_bark, drilling, enginge_idling, gun_shot, jackhammer, siren, and street_music. The classes are drawn from the urban sound taxonomy. For a detailed description of the dataset and how it was compiled please refer to our paper.
All excerpts are taken from field recordings uploaded to www.freesound.org. 

I have built spectrograms for all the audio clips using a windowing function that is applied to each clip, then the Short-Term Fourier Transform (STFT) is computed on each frame, finally the power spectrum and filter banks are computed. 

This will be done using libraries like Librosa.

Model optimizer: We have used RMSprop.
RMSprop is a gradient based optimization technique. This normalization balances the step size (momentum), decreasing the step for large gradients to avoid exploding, and increasing the step for small gradients to avoid vanishing.

Loss function: Categorical cross entropy loss is used.
 It compares the predicted label and true label and calcCNN model:
I have used 4 convolution layers with maxpooling in between each layers.
Then it is flattened.
Finally comes the 2 Dense layers (relu and Softmax).ulates the loss.

I have successfully classified the dataset audio into 10 classes with an accuracy of 83% without considering salience(foreground/background).
The model can predict whether the source of sound is in the background or foreground with an accuracy of 74.58 %.
I have created some audio files which contain multiple sounds classes from the dataset and were able to find out what sounds were present in it.
