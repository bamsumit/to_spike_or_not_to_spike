# To Spike Or Not To Spike #

> _As engineers, we would be foolish
to ignore the lessons of a billion
years of evolution._
> _—Carver Mead, 1993_

## What are spikes? ##
Brain is the most interesting, yet enigmatic, thing for us humans.
It is a symbol of intelligence.
If we look into the underlying structure of the brain, it is a complicated interconnection of _neurons_.
Neurons are the fundamental entity in the brain, linked with each other via _synapse_.
The neurons can be of many different varieties, each tuned to perform a specific task.
However, there is one thing common between them.
They all process and emit _spike_ signal.
Barring very primitive organisms, spike is the currency of information exchange between neurons.

> __Spike__ or __Action Potential__ — A spike or an action potential is
a brief electric pulse in membrane potential, typically 1 to 2 ms in
duration and an amplitude of about 100 mv which roughly look alike
and is usually followed by a dip in membrane potential, that occurs in
regular or irregular intervals. The action potential is the elementary
unit of signal transmission.

[test](spikeInVivo.pdf)

Coming back to the question: what are spikes?
_Spikes_, also called _action potential_, are a sudden surge in the potential of a neuron.
When a spike occurs, there is an exchange of ions through the synapses.
The manner in which the _membrane potential_ rises and falls is usually different for various family of neurons, but very similar for an individual neuron.
Nevertheless, the following are true:

1. Spikes are momentary occurrences.
2. Spikes are sparse events.

When we look at a sequence of spikes, the subtle variation in the action potential dynamics is insignificant.
Instead, spikes are events in time which carry information between neurons.

[//]: # (For a machine learning researcher, it is a massively parallel interconnected entity of simple computational units.)
[//]: # (For a neuroscience researcher, it is a dynamic interaction of a neuron with its surrounding environment.)

## Why spike? ##
Why did nature choose spike as a means of signaling between neurons?
After all, the brain is the result of millions of years of evolutionary process.
One cannot answer it for sure. We can just guess!

One of the plausible explanations is to overcome the noisy environment in a biological system.
It is no surprise that the brain is a noisy environment.
After all, there are numerous dynamic interactions going on.
It needs an effective method of signaling to exchange information properly.
The solution: _speak less, but when you speak, make yourself loud and clear_.
To maintain a large signal to noise ratio, the amplitude of a signal needs to be much higher than the noise floor.
This is not a good strategy in terms of energy efficiency.
Especially considering the fact that 100 billion neurons in the brain consume few tens of watts of energy.
Signaling with spike allows a neuron to send a signal that is less likely to be corrupted by noise.
In addition, the sparsity of spikes means that the signaling mechanism is not energy hungry.

## Spiking Neuron ##
Simply stated, a _spiking neuron_ is the mathematical model of a biological neuron.
Obviously, there will be different degree of abstraction in the model.
As a bare minimum, a spiking neuron must take in incoming spikes as input and respond with its own spike event as the output.

In general, all spiking neurons are some abstracted version of the famous _Hodgkin-Huxley_ neuron model.
The common spiking neuron models are 
_Leaky Integrate and Fire (LIF)_ model,
_Izhikevich_ model,
_FitzHugh-Nagumo_<check spelling> model,
_Spike Response Model (SRM)_,
_Mihalas Niebur Neuron_ model
etc.

## Spiking Neural Network ##
A neural network where the computational unit is a spiking neuron is called Spiking Neural Network (SNN).
Instead of the commonly used non-linear activation function, 
the use of spiking neuron as the computational unit inherently introduces the notion of time in SNNs
since spikes are events in time.
Therefore an SNN is a continuous entity.
This property is in stark difference to the standard neural networks which lack the notion of time.
The inherent notion of time make SNNs suitable for temporal applications.

Think about how we recognize images.
We cannot simply identify the image from a momentary visual stimulus.
We have to look at the image for some time.
Our eyes look at different portions of the image,
in different orientations perhaps.
It is a continuous process.
In fact whatever we experience in life is an ongoing process.

An SNN is of equal importance to the field Machine Learning as well as Computational Neuroscience.
From a philosophical point of view, SNN is a key concept which holds the promise to fulfill the two main objectives of Neuromorphic Engineering (NE):
brain modeling and neuromorphic computing.
Brain modeling: for neuroscientists to understand the brain by modeling and simulating the activities of biological neurons;
and neuromorphic computing: for engineers to build brain-like machines by applying biological principles to computers.


## Current State of Spiking Neural Network ##
SNNs do bring added realism to artificial neural networks.
From a theoretical sense, they are proven to have higher computational capability than the standard neural networks.
In practice, however, we are far from realizing the increased computational power using SNNs.

One would think that we should be able to leverage the knowledge base for standard non-spiking neural networks
to unlock the potentials of SNNs.
However, we have a major roadblock in doing so.
Backpropagation method is the foundation of the success of non-spiking neural networks.
Unfortunately, we cannot port backpropagation technique for SNNs, 
at least it is not straightforward.

The state of SNN research is in its infancy.
It is a niche area of research adopted by a small community of neuromorphic computing and
researchers in the neuroscience community.
SNNs are suited for processing spike data from neuromorphic sensors such as silicon retina and silicon cochlea.
They are, by design, primed to process temporal data, not necessarily of neuromorphic nature.

Recently, there is a growing interest in neuromorphic hardware, such as Intel's Loihi, IBM's TrueNorth, SpiNNaker etc.
for extremely low power computing and large-scale networks.
Neuromorphic hardware makes use of spiking neurons on a physical substrate or their low-level computational architecture.
SNNs automatically align as the software to make use of them.
