# Optical Character Recognition

Digit and letter recognition neural networks using MNIST and EMNIST datasets. Vanilla, convolutional and convolutional-LSTM networks were used for clasifying individual characters and words from artificially created images from the combined EMNIST letter images.

## Prerequisites

 - Libraries: __TensorFlow, matplotlib, tkinter, pickle, opencv, PyQT5, pandas__
 - Data: MNIST and EMNIST binary datasets (found in the data folder)
 
 
## Structure of the project

 - demo_gui: 
 	- interfata.py is the main script that opens a GUI in which you can draw digits
	- save them and use the convolutional architecture to get the prediction of that character
 	- you can also save them to train an aditional network with those images
	
 - character_recognition_models:
 	- cuvinte:
		- word_generator: extracts approximately 2000 most commonly used words in english
		- generate_clean: generates images and labels for the words extracted and saves them as binaries
	- sources:
		- model.py: main model function. Inherits Data class for functionalities on data sets. Train or load models
		- new_conv_rnn_singleChr.py: generates binaries of noised out images for later use (it can be used with generate_clean later on, to append some other artificially created data
	- LSTM:
		- lstm.py: conv-lstm model with all aditional required functionalities. Can create word-images and labels, append them and train a conv-lstm architecture
