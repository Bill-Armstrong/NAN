# NAN: Noise-Attenuating Neuron:

## real-time machine learning that cares about the noise in data

The sofware here embodies an new idea for attenuating the noise in data (details below).

 This is a stage in project NANO (Noise-Attenuating Neuron Online). What remains to be done in project NANO is based on the idea that if samples are entered one by one into a training buffer, online as it were, the search for closest neighbors can be done in linear time in the size of the training buffer.  Instead of having a single training set as in NAN, we shall use a training buffer which is an integral part of the ALN. 
 
 The next stage will be putting thousands of NANO's together into a larger interconnected system to see what happens. Will it ultimately be a general learning system of unimaginable power? So as not to create too much undeserved hype, and at the same time keep the military people from seeking to exploit it, for now we are going to call this final stage "The Electric Chicken".

## Some details about noise-attenuation

For each sample in the data file a closest other sample in the file is found. A noise variance tool stores the difference of domain and function values. If the samples were at the same place in the domain, the variance of that difference of function values would have twice the noise variance at that place in the domain. However, the samples are not in the same place, and we don't know the slope of the ideal function between them.  So the idea is to store the differences of domain coordinates and the difference of domain values and wait until the ideal function is approximated ever better by linear pieces, as in an ALN, and to use the slope of the linear piece joining them to get a better estimate of noise variance.  If the training error of the linear piece is less than or equal to the noise variance, training is stopped locally, meaning the piece is not split. This gives us a superb way of avoiding over-training. This idea is used in both NAN and NANO.
