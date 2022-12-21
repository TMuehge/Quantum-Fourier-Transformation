# How to Analyze Sound by Quantum-Fourier-Transformation and turn it into a Music-Fractal-Film
Classical Fourier transformation is a widely used and well established technique. Some examples for this are analyzing solid state material by X-ray crystallography, digital signal processing, or encoding digital signals for internet communication.

### Why doing it on a Quantum Computer?

Quantum Fourier Analysis is analogous to the classical Fourier transformation, by making use of quantum parallelism. With this we get an exponential speedup. Unfortunately, this directly does not make signal processing faster due to its specific quantum nature [1].  
However, many Quantum Algorithms are relying essentially on Quantum Fourier Transformation (QFT) like e.g., factorization large numbers by Shor’s algorithm [5].
In this Blog we will used QFT to analyze an example piece of music. In doing so, 
we want to outline how QFT works in principle. Finally we will link this to arty quantum-images and with this create a film with music and the respective synchronous Quantum analysis.

### What is sound?
<img src="https://github.com/TMuehge/Quantum-Fourier-Transformation/blob/main/artwork/sound1aa.png?raw=true" alt="sound1aa" title="sound1aa">
Physically sound is a mechanical longitudinal or compression air wave. The air particles are coupled between each other which means that they are somehow connected via elastic springs causing air particles moving back and forward. This coupling is the reason, why introduced motion by for instance a loudspeaker propagates as a wave. The ear together with the brain is decomposing the airwave into the set of frequencies and is performing a biological Fourier analysis. The composition of different frequencies over time can be noise, speech or if done right music.

### What is QFT?
<img src="https://github.com/TMuehge/Quantum-Fourier-Transformation/blob/main/artwork/sound2.png?raw=true" alt="sound2" title="sound2">
Fourier transformation is a mathematical technique that turns a time dependent function into it’s frequencies. 
In the above picture you see on the left side a time representation of a sound made by a guitar. On the right side you see the calculated Fourier transform of the sound example showing all the related frequencies and their amplitudes.
So, how to do the same thing on a Quantum Computer?

### Quantum Fourier Transformation:
QFT is an analogue to classical Discrete Fourier transformation. In classical Discrete Fourier Transformation (DFT) you basically take an arbitrary time dependent wave like you see on the left side of the above picture. The amplitude of this wave for a given time interval is defined by a set of numbers x_i. N defines the sampling rate of this wave for a given time interval.
In other words, the wave in the time dependent space can be defined by a vector x where x_i in {0, N-1}. 
If we want to transform x into the frequency space we calculate a new vector y with y_k ; k in {0, N-1} and each element of y is calculated by a sum of discrete sin and cos waves:
<img src="https://github.com/TMuehge/Quantum-Fourier-Transformation/blob/main/artwork/dft.png?raw=true" alt="sound2" title="sound2">
Quantum Fourier Transformation is almost the same. We take an orthonormal basis |0> … |N-1> and perform a transformation into the Fourier basis. 

<img src="https://github.com/TMuehge/Quantum-Fourier-Transformation/blob/main/artwork/qft.png?raw=true" alt="sound2" title="sound2">
N = 2 for 1 qubit <br />
N = 4 for 2 qubits <br />
N = 8 for 3 qubits <br />
N= 2^n (n = number of qubits) <br />

This means, that we can in principle perform an exponential number of sampling defined by the qubit count. This seems to be an exponential speedup! <br />
Unfortunately, it is not possible get the QFT coefficients out of the superposition as they are destroyed by a measurement.
The result come from multiple repetition of the measurement and the corresponding statistics as you will see in the below program example.


