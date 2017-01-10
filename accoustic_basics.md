# Acoustic imaging (basics) 

The pdf version of this document can be download ['here'](./acoustic_imaging_src/acoustic.pdf).

In this section, we will explain some basis of the acoustic theory to understand the propagation of acoustic waves and the echographic process.

Propagation of acoustic waves
=============================

In this section, we will define the different types of acoustic waves and some basic equations and properties of the propagation of acoustic waves.

Wave types
----------

An acoustic wave is a perturbation of the local state without displacement of the global state. Acoustic waves are periodic, their spatial periodicity is given by the wavelength *λ*. Consider a medium at rest such as on Fig. 1, where the particles are represented by the dots. Such a periodic structure represent a metal for example. When an acoustic wave propagate in this medium, the particles will have a local displacement.

 ![Medium at rest.<span data-label="fig:at_rest"></span>]

 *Figure 1: medium at rest.*

There is two types of acoustic waves, the longitudinal waves (Fig. 2) also named P waves and the transverse waves (Fig. 3) also named SH or SV waves. The longitudinal waves are compressional waves, the direction of the displacement of the particles is the same than the direction of propagation of the wave. The transverse waves are shear waves, the direction of displacement is then perpendicular to the direction of propagation of the wave. In a fluid, such as the water, only longitudinal waves can propagate. In the human body, the shear modulus is very small, it can be considered as a fluid, and so only longitudinal waves will be generated.

 ![Longitudinal wave.<span data-label="fig:Pwave"></span>]
 *Figure 2: longitudinal wave.*

  [Medium at rest.<span data-label="fig:at_rest"></span>]: ./acoustic_imaging_src/image/at_rest.png "fig:"
  [Longitudinal wave.<span data-label="fig:Pwave"></span>]: ./acoustic_imaging_src/image/Pwave.png "fig:"

 ![Shear wave.<span data-label="fig:Swave"></span>]

 *Figure 3: shear wave.*

In the rest of the document, we will only consider longitudinal waves.

  [Shear wave.<span data-label="fig:Swave"></span>]: image/Swave.png "fig:"

Mathematical formulation
------------------------

In acoustic, a fluid medium is describe by two mecanical parameters: the mass density *ρ* and the bulk modulus *κ*. The bulk modulus relate the change of volume of a medium to the isostatic pressure apply on it. The velocity of the acoustic wave *c* is:
$$c=\\sqrt{\\dfrac{\\kappa}{\\rho}},
 \\label{eq:speed of sound}$$
 for example, for the water we have: *ρ* = 1000 kg.m<sup>−3</sup>, *κ* = 2.19 MPa and *c* = 1480 m.s<sup>−1</sup>.

The mathematical formulation is obtained by solving the Helmholtz equation, for exemple, the acoustic pressure *p*(*x*,*t*) can be expressed as:
$$p\\left(x,t\\right)=\\left(A^{+}\\e^{\\im kx}+A^{-}\\e^{-\\im kx}\\right)\\e^{-\\im 
\\omega t},
 \\label{eq:math 1D formulation}$$
 $A^{+}\\e^{\\im kx}$ is a wave of amplitude *A*<sup>+</sup>, propagating toward the positive *x*, $A^{-}\\e^{-\\im kx}$ is a wave of amplitude *A*<sup>−</sup>, propagating toward the negative *x*. $k=\\dfrac{\\omega}{c}$ is the wavenumber, *ω* = 2*π**f* the angular pulsation and *f* the frequency.

When we make an echographic image, we are intresting only on the intensity of the wave:
$$I=\\dfrac{1}{2}\\Re\\left\[p\\left(x,t\\right)v^{\*}\\left(x,t\\right)\\right\],
 \\label{eq:acoustic intensity}$$
 where *v*(*x*,*t*) is the velocity of the particle, and *x*<sup>\*</sup> represent the complex conjugate of *x*. It can be shown with the Euler’s equation that the intensity is directly proportional to the square modulus of the pressure.

Refraction and diffusion of acoustic waves
------------------------------------------

When an acoustic wave passes from a medium (0) to a second medium (1), a part of the wave is reflected an the over part is transmitted through the interface. When the interface is flat in the point of view of the wave, we have refraction (it is a quasi one dimensional problem, because the wave is reflected on only one direction of the space). When the wave sees the curvature of the interface, the wave is scattered on all the directions of the space, we talk then about diffusion.

### Refraction of a wave

 ![Refraction of a wave.<span data-label="fig:refraction"></span>]

*Figure 4: refracation of a wave.*

We consider an incident wave $\\phi\_{\\inc}$ normal to an interface, the reflected $\\phi\_{R}=R\\phi\_{\\inc}$ and the transmitted $\\phi\_{T}=T\\phi\_{\\inc}$ waves are also normal to the interface (Fig. 4). *R* and *T* represent respectively the reflexion and transmission coefficient. By solving this problem, we show that:
$$R=\\dfrac{Z\_2-Z\_1}{Z\_2+Z\_1},
 \\label{eq:reflection coefficient}$$
 where *Z*<sub>*i*</sub> = *ρ*<sub>*i*</sub>*c*<sub>*i*</sub> is the acoustic impedance of the medium *i*.

  [Refraction of a wave.<span data-label="fig:refraction"></span>]: image/refraction "fig:"

If we consider, for example the reflection of a wave at an interface between water (*ρ*<sub>0</sub> = 1000 kg.m<sup>−3</sup>, *c*<sub>0</sub> = 1480 m.s<sup>−1</sup>) and a muscle (*ρ*<sub>1</sub> = 1070 kg.m<sup>−3</sup>, *c*<sub>1</sub> = 1590 m.s<sup>−1</sup>), the reflection coefficient is equal to 69.10<sup>−3</sup>, so only 7% of the pressure is reflected. If we know consider an interface between water and bone (*ρ*<sub>1</sub> = 2175 kg.m<sup>−3</sup>, *c*<sub>1</sub> = 4000 m.s<sup>−1</sup>), then nearly 70% of the incident wave is reflected. The echos due to bones are much more higher than the ones due to the muscles.

### Scattering of a wave

Even if an object is very small in front of a wave, it always scattered the wave (Fig. 5). It is much more complicated to determine the scattered wave than the reflected wave such as in sec. .

 ![Scattering of a wave.<span data-label="fig:diffusion"></span>]

*Figure 5: scattering of a wave.*

The diffused wave goes in every direction of the space, it lead that its amplitude decreases with the distance from the object.

  [Scattering of a wave.<span data-label="fig:diffusion"></span>]: image/diffusion "fig:"

Attenuative media
-----------------

The human body is an attenuative media, this mean that the amplitude of a wave propagating in such medium decreases along its direction of propagation. Mathematically, the propagation of waves in this kind of medium is written as:
$$p\\left(x,t\\right)=\\left(A^{+}\\e^{\\im kx}\\e^{-\\alpha x}+A^{-}\\e^{-\\im 
kx}\\e^{\\alpha x}\\right)\\e^{-\\im 
\\omega t}.
 \\label{eq:math 1D absobing formulation}$$
 The difference between the propagation of a wave between a non-attenuative and an attenuative medium is present on Fig. . So when we do acoustic imaging in the human body, we must gradually amplify the received signal if we want to convert correctly the analogical signal into a digital signal, because if the amplitude of the signal is smaller than the precision of the ADC, we can’t measure it (see appendix ). Classically, we do Time Gain Compensation (TGC) on the receive signal in order to keep a convenient amplitude of the received signal. An example of this kind of treatment is presented on Fig. , it’s apply to the attenuated signal on the right side of Fig. .

 ![Acoustic pressure of a wave propagating in a non-attenuative (left) and attenuative (right) medium.<span data-label="fig:attenuative medium"></span>]

*Figure 6: acoustic pressure of a wave propagating in a non-attenuative (left) and attenuative (right) medium.*

 ![Example of TGC applied on the attenuated signal (right side of Fig. .<span data-label="fig:tgc example"></span>]

* Figure 7: Example of TGC applied on the attenuated signal (right side of Fig. 6.*

  [Acoustic pressure of a wave propagating in a non-attenuative (left) and attenuative (right) medium.<span data-label="fig:attenuative medium"></span>]: image/attenuative_medium "fig:"
  [Example of TGC applied on the attenuated signal (right side of Fig. .<span data-label="fig:tgc example"></span>]: image/tgc_example "fig:"

Transducer
==========

A transducer is an acoustic sensor, it convert electric power to mechanical power and conversely. So if you apply an electric signal on it, it will generate acoustic wave (like a speaker), and if an acoustic wave deform it, it generate an electrical signal (like a microphone).

In order to have a correct radial precision in acoustic imaging, the acoustic wave must be focused on one point. This can be done by two kind of technologies: focussed transducer and transducers array.

Focussed transducer
-------------------

 ![Acoustic wave focalisation (red) by a focussed transducer.<span data-label="fig:transducer scheme"></span>]

* Figure 8: acoustic wave focalisation (red) by a focussed transducer.

This kind of transducer have a spherical shape, so the emitted acoustic wave naturally focalised at the center of the sphere (Fig. ). The area of the focal spot is an ellipse, the value of *l* and *L* can be approximate by:

  [Acoustic wave focalisation (red) by a focussed transducer.<span data-label="fig:transducer scheme"></span>]: image/transducer_scheme "fig:"


$$l=\\dfrac{\\lambda R}{2r},
 \\label{eq:l value}$$

*L* = 15(1−0.01*θ*)*l*.

More *θ* is high, more the ellipse is small. When we do acoustic imaging, we want *l* to be as small as possible to increase the radial precision. Moreover we want *L* to be high, because the echo of an object outside of this ellipse will be too small to be measured. So we have to make a compromise between *l* and *L*.

At the nearfield (it depend on *λ* and *r*) of the transducer, the acoustic pressure is to chaotic so we can’t do acoustic imaging in the nearfield of this kind of transducer.

Transducers array
-----------------

On a transducers array, generally, the size of each transducer is small compare to the wavelength, so they emit spherical waves. If all the transducers emit a wave at the same time, the array will emit a plan wave. If you apply a right delay between the emission of each transducer it is possible to generate a focussed acoustic wave (Fig. ). This delay can be simply calculated, indeed, by knowing the distance between each transducer, you just have to determine a delay that consist on having all the wave generated by each transducer arriving exactly at the same on a given point of the space. By doing this the waves interfere coherently near this point (high pressure) and incoherently everywhere else (low pressure).

 <img src="image/transducers_array" title="fig:" alt="Acoustic wave focalisation with an array of transducers." style="width:30.0%" />

With a transducers array, it is possible to focalise at different points at the same time, so acoustic imaging can be faster with this and it don’t need a motor to image a plane. However they are much more expensive than a simple focussed transducer and the electronic is much more complicated to drive a transducers array.

Signal Processing
=================

In this section we introduce the Fast Fourier Transform (FFT) and present a basic signal processing to improve an echographic signal.

Fast Fourier Transform
----------------------

The Fourier Transform is a transformation that express a function of a given dimension as a function of another dimension. Classically, a time dependent signal is expressed as a function of the frequencies. In acoustic we also apply Fourier transform to a space signal, so the transform is a function of the wavelength. The Fourier Transform *S* of a real signal *s* is complex and ℜ(*S*) is an even function and ℑ(*S*) is odd.

The FFT is an algorithm that calculate the Fourier Transform of a signal very fast, the number of point of the signal must be a power of 2. The FFT of a signal is a periodic function with a periodicity equal to the frequency sampling of the initial signal. Classically, the FFT algorithm return the Fourier Transform for the positive frequencies. Due to the periodicity of the FFT, the second half of the signal is the negative frequency part.

Consider a time signal sample at frequency *f*<sub>*e*</sub> = 640 MHz composed of N=1024 points (Fig. ). If you keep only the positive frequencies, the frequency vector corresponding to the FFT go from 0 to $f\_e\\dfrac{N-1}{N}$. On octave its given by linspace(0,fe\*(N-1)/N,N). The FFT of the time signal keeping the positive frequencies is presented on Fig. .

If one want to filter the signal, it is more convenient to consider the negative frequencies, because if you want to filter the a signal between x and y MHz, you must put to 0 all frequencies except the points between x and y MHz and also the points between -x and -y MHz. In this case, the frequency vector is given by linspace(-fe/2\*(N-1)/Nfe/2,N) and you must put the second half of the FFT signal at the beginning. To do that you must create a new vector of the same size than the FFT signal, and doing fox example: S2(1:N/2-1)=S(N/2+2:end) and S2(N/2:end)=S(1:N/2+1). Then you obtain the signal presented on Fig. .

The real and imaginary part of the FFT presented on Figs.  and are divided by their maximum amplitude to have readable graphics.

If one want to know the central frequency of a transducer, you must take the modulus of the FFT of an echo of the transducer. The central frequency is the frequency where the modulus has the higher value.

 ![Example of a time signal.<span data-label="fig:time signal"></span>]

 ![FFT of the signal presented on Fig.  keeping the positive frequencies. On blue real part and green imaginary part.<span data-label="fig:positive frequencies"></span>]

 ![FFT of the signal presented on Fig.  with the negative frequencies. On blue real part and green imaginary part.<span data-label="fig:negative frequencies"></span>]

  [Example of a time signal.<span data-label="fig:time signal"></span>]: image/time_signalb "fig:"
  [FFT of the signal presented on Fig.  keeping the positive frequencies. On blue real part and green imaginary part.<span data-label="fig:positive frequencies"></span>]: image/positive_frequenciesb "fig:"
  [FFT of the signal presented on Fig.  with the negative frequencies. On blue real part and green imaginary part.<span data-label="fig:negative frequencies"></span>]: image/negative_frequenciesb "fig:"

Hilbert transform
-----------------

The Hilbert transform is useful for signal processing in echographic imaging, because with this transformation we can access to the envelop of a given signal. The Hilbert transform can be determine easily with the FFT. Indeed, if you calculate the FFT of a signal and put all the negative frequencies to 0 and do an IFFT (Inverse Fast Fourier Transform), then you have the Hilbert transform of the signal. By doing this to the signal presented in Fig. , we obtain the transform signal presented on Fig. .

 ![Hilbert transform of the signal presented on Fig. . Blue real part, green imaginary part and red modulus.<span data-label="fig:hilbert transform"></span>]

  [Hilbert transform of the signal presented on Fig. . Blue real part, green imaginary part and red modulus.<span data-label="fig:hilbert transform"></span>]: image/hilbert_transformb "fig:"

Basic echographic signal processing
-----------------------------------

The most basic signal processing for echographic imaging is to filter the signal and extract the envelop of the filtered signal. So you make a FFT of the signal measured by the transducer and you filter ± 2 MHz around the central frequency of the transducer for example, lets say between 5.5 and 9.5 MHz for a transducer centered at 7.5 MHz. You can keep the positive frequency, so you put all frequency smaller than 5.5 and higher than 9.5 MHz to 0. By doing this you apply a square window on the signal, you can also apply an Hamming, Hanning or Blackmann window. The negative frequency are also put to 0 with this method so if you make an IFFT, you apply a Hilbert transform to the filtered signal. By taking the modulus so we access to the envelop of the filtered signal.

Now we have to define the pixels of the image. For example we can say that a pixel as the same length that the wavelength *λ* of the acoustic wave, $\\lambda=\\dfrac{c}{f}$ (*c* = 1500 m.s**<sup>−1</sup>). The time *t* needed to travelled a distance *d* is $t=\\dfrac{2d}{c}$ (2 because the wave travelled back and forth) so if *d* = *λ* then *t* = 26.7*μ*s. At 640 MHz, it correspond to 171 time points. The value of pixel is then define by integrated the signal on 171 points. An echographic image show the value of the acoustic power in dB, so to obtain this you just have to plot 20log(*s*). Where *s* is the envelop of the filtered signal integrated on the adequate number of time points.

ADC
===

In this appendix, we make a quick introduction to Analogical Digital Converter. This component is one of the most important in an echographic probe, so it is necessary to understand how does it work.

As its name suggest, an ADC convert the algebrical value of the tension of a signal to a digital signal. To remember, a digital signal is a binary signal, the 0 correspond to 0 V, the low value and 1 correspond to high value (5 V for example). In a computer or smartphone, all the treatment are made in the digital form, so it is necessary to convert the analogical signal measured on the transducer to a digital signal. An ADC is characterized by its sampling rate expressed in sampling per second (Sps) and its precision *n*. The sampling rate define the number of time it convert a signal per second. The precision define on how many bites the digital number is written, so the ADC sample the signal on 2<sup>*n*</sup> values.

An ADC is supply with a given continuous current *V*<sub>cc</sub>. So the ADC sampling of the analogical are 2<sup>*n*</sup> value equally space between −*V*<sub>cc</sub> (or 0V) and +*V*<sub>cc</sub>. The precision *p* of the ADC is then:
$$p=\\dfrac{2V\_{\\text{cc}}}{2^n-1}.
 \\label{eq:precision adc}$$

So if we have *V*<sub>cc</sub> = 5 V on a 8 bites ADC (*n* = 8), then the precision is then 39.2 mV. Now consider than the output *k* of the ADC is an unsigned integer (this mean that the output is 0 to 255) then the voltage *V*<sub>m</sub> of the analogical signal is:
*V*<sub>m</sub> = −*V*<sub>cc</sub> + *k**p*,
 so if *k* = 23 then the analogical signal is -4.1 V high.

