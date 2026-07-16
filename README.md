# An-Elementary-Introduction-to-Lattice-Based-Cryptography

This is a deep dive into the theory of lattice-based cryptography with the intention of understanding the technical details of the state-of-the-art (NIST standardization candidate) signature scheme [Falcon](falconsign.info). The material is accessible to any undergraduate student who has taken one course in linear algebra and probability.

Note that the featured files have been compiled over a period of time. Occcassionally, there may be mismataches in notation or style. I intend to organize them into a single coherent exposition at some point. Meanwhile, I recommend reading them in the following order.

1. Read until section 2.1.2 in [Exposition – Fast Fourier Orthogonalization.pdf](https://github.com/pritamchandra/An-Elementary-Introduction-to-Lattice-Based-Cryptography/blob/1cfcd042f77e63bd3d591e39854babf63c7790b7/Exposition%20%E2%80%93%20Fast%20Fourier%20Orthogonalization.pdf) to be introduced to the `closest vector problem` and the `nearest plane` algorithm to solve it.

2. Move to [NTRUsign – overview.pdf](https://github.com/pritamchandra/An-Elementary-Introduction-to-Lattice-Based-Cryptography/blob/1cfcd042f77e63bd3d591e39854babf63c7790b7/NTRUsign%20%E2%80%93%20overview.pdf) to study one of the primary stepping stones on the road to Falcon.

3. Follow with [Tower Solver (Fast NTRU Key Generation).pdf](https://github.com/pritamchandra/An-Elementary-Introduction-to-Lattice-Based-Cryptography/blob/1cfcd042f77e63bd3d591e39854babf63c7790b7/Tower%20Solver%20(Fast%20NTRU%20Key%20Generation).pdf) where the `key generation` algorithm is made efficient. This algorithm features also in Falcon.

4. Change course to see an introduction `Fast Fourier Transform (FFT)` and how it is used to efficiently multiply polynomials in [Polynomial Multiplication using FFT.pdf](https://github.com/pritamchandra/An-Elementary-Introduction-to-Lattice-Based-Cryptography/blob/1cfcd042f77e63bd3d591e39854babf63c7790b7/Polynomial%20Multiplication%20using%20FFT.pdf).

5. Return to [Exposition – Fast Fourier Orthogonalization.pdf](https://github.com/pritamchandra/An-Elementary-Introduction-to-Lattice-Based-Cryptography/blob/1cfcd042f77e63bd3d591e39854babf63c7790b7/Exposition%20%E2%80%93%20Fast%20Fourier%20Orthogonalization.pdf) and read section 2.2 onwards. Here the ideas of `FFT` are used modify the `nearest plane` algorithm, which in turns makes the `signature generation` algorithm more efficient. The key component here is a fast method to orthgonalize special NTRU matrices in quasilinear time and compactly store them as an object called the `Falcon tree`.

6. Change course again to [Transcript Attacks on Deterministic Signature Schemes.pdf](https://github.com/pritamchandra/An-Elementary-Introduction-to-Lattice-Based-Cryptography/blob/1cfcd042f77e63bd3d591e39854babf63c7790b7/Transcript%20Attacks%20on%20Deterministic%20Signature%20Schemes.pdf) to note how a transcript of signatures can help break deterministic signature schemes like NTRUsign.

7. Move to [Randomized Nearest Plane by Klein.pdf](https://github.com/pritamchandra/An-Elementary-Introduction-to-Lattice-Based-Cryptography/blob/1cfcd042f77e63bd3d591e39854babf63c7790b7/Randomized%20Nearest%20Plane%20by%20Klein.pdf) to see how the `nearest plane` algorithm can be modified to a randomized version.

8. Proceed to [Introduction to Smoothing Parameter Bounds.pdf](https://github.com/pritamchandra/An-Elementary-Introduction-to-Lattice-Based-Cryptography/blob/1cfcd042f77e63bd3d591e39854babf63c7790b7/Introduction%20to%20Smoothing%20Parameter%20Bounds.pdf) for detailed dive into theory of dual lattices to establish bounds on the `smoothing parameter`, a quantity that is key for the security analysis of Falcon (or any other scheme in the [GPV](https://dl.acm.org/doi/10.1145/1374376.1374407) framework).
