# How to Analyze Sound by Quantum-Fourier-Transformation and turn it into a Music-Fractal-Film
Classical Fourier transformation is a widely used and well established technique. Some examples for this are analyzing solid state material by X-ray crystallography, digital signal processing, or encoding digital signals for internet communication.

### Why doing it on a Quantum Computer?

Quantum Fourier Analysis is analogous to the classical Fourier transformation, by making use of quantum parallelism. With this we get an exponential speedup. Unfortunately, this directly does not make signal processing faster due to its specific quantum nature [1].  
However, many Quantum Algorithms are relying essentially on Quantum Fourier Transformation (QFT) like e.g., factorization large numbers by Shor’s algorithm [5].
In this Blog we will used QFT to analyze an example piece of music. In doing so, 
we want to outline how QFT works in principle. Finally we will link this to arty quantum-images and with this create a film with music and the respective synchronous Quantum analysis.

### What is sound?

<img src="https://github.com/TMuehge/The-Sound-of-Quantum/blob/main/artwork/quantum-sketch1.png?raw=true" alt="Employee data" title="Employee Data title">

Physically sound is a mechanical longitudinal or compression air wave. The air particles are coupled between each other which means that they are somehow connected via elastic springs causing air particles moving back and forward. This coupling is the reason, why introduced motion by for instance a loudspeaker propagates as a wave. The ear together with the brain is decomposing the airwave into the set of frequencies and is performing a biological Fourier analysis. The composition of different frequencies over time can be noise, speech or if done right music.
