# Prof. Dong LSTM

## The project aim at predicting CA1 neuron activities by feeding RNN model CA1 and CA3 inputs before t steps. It is anticipated that proper sturcutre and loss function of RNN should be able to attain state-of-the-art performance since in learns the basis functions rather than using hand-crafted ones in MIMO model previously used in Prof. Song's lab.

The branch *master* is not the lastest version of the code. It is the first preliminary test.

## LSTM Example
**generate_sine_wave.py** and **train.py** is the demonstrates how to use 2 layer LSTM models to predict the input sine wave in the next 100 future steps after training.  

## Read Spike data from Matlab data structure
**read_data.py** reads the data.m and converts Coordinate list (COO) to sparse matrix as numpy array, then save data as .pickle

## Train model
**train_.py** is the main file defining the networks, optimization, loss functions, and prints loss. It lacks proper criteria to evaluate accurary of predictions

The branch *test* is the more up-to-date version of the scripts to predict spikes

## Modify the sampling rate of data
**bin_timesteps.py** enables one to change the sampling rate of the raw data from the default 1 millisecond to multiple milliseconds. The training difficulty will be reduced sinece the sparseness usually results in poor loss functions/ training signals.

## Raster plot
**raster.py** allows one to plot the raster plot of the data. It allows one to observe the sparsity of the data intuitively.

## Network Sturcture
**RNN.py** The network class is defined here.

**main.py** The main code for the training and validation. Run this script to start. Now you are able to resume training from the checkpoints. It not only prints loss but also accuracy.
	Some works to do : arguments parser to enable command-line instruction. 



