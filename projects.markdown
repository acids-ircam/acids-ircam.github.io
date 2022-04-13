---
layout: page
title: Projects 
permalink: /projects/
---


Here, we detail a list of all usable projects created by ACIDS and their quick description, along with indications for availability in MaxMsp, PureData, Max4Live, VST and porting to embedded platforms (Raspberry Pi and Jetson Nano). All of the projects here are resolutely open-source under a CC-BY-NC-SA 4.0 licence. We first give a quick overview of all the projects and then provide more detailed information.

## Overview

<h4>Neurorack</h4> [![Full repository](https://img.shields.io/badge/Github-neurorack-7DA416.svg?style=flat-square&logo=Github)](https://github.com/ninon-io/Impact-Synth-Hardware) 
[![Published in ArXiV](https://img.shields.io/badge/Paper-1907.00971-167DA4.svg?style=flat-square&logo=arXiv)](https://arxiv.org/abs/1907.00971)
[![Video on YouTube](https://img.shields.io/badge/Video-Max4Live-7DA416.svg?style=flat-square&logo=Youtube)](https://www.youtube.com/watch?v=64VpQenCHVs)
            
Embedded deep audio synthesis in Eurorack format

**RAVE** 

[![Full repository](https://img.shields.io/badge/Github-rave-7DA416.svg?style=flat-square&logo=GitHub)](https://github.com/acids-ircam/ddsp_pytorch) 
[![Published in ArXiV](https://img.shields.io/badge/Paper-2111.05011-167DA4.svg?style=flat-square&logo=arXiv)](https://arxiv.org/abs/2111.05011)
[![Video on YouTube](https://img.shields.io/badge/Video-None-7D1616.svg?style=flat-square&logo=Youtube)]()

Real-time Audio Variational auto-Encoder

#### FlowSynth: Universal audio synthesizer control

[![Full repository](https://img.shields.io/badge/Github-flow_synth-7DA416.svg?style=flat-square&logo=Github)](https://github.com/acids-ircam/flow_synthesizer) 
[![Published in ArXiV](https://img.shields.io/badge/Paper-1907.00971-167DA4.svg?style=flat-square&logo=arXiv)](https://arxiv.org/abs/1907.00971)
[![Video on YouTube](https://img.shields.io/badge/Video-Max4Live-7DA416.svg?style=flat-square&logo=Youtube)](https://www.youtube.com/watch?v=UufQwUitBIw)

#### DDSP: Differentiable Digital Signal Processing 

[![Full repository](https://img.shields.io/badge/Github-ddsp_pytorch-7DA416.svg?style=flat-square&logo=GitHub)](https://github.com/acids-ircam/ddsp_pytorch) 
[![Published in ArXiV](https://img.shields.io/badge/Paper-2001.04643-167DA4.svg?style=flat-square&logo=arXiv)](https://arxiv.org/abs/2001.04643) 
[![Video on YouTube](https://img.shields.io/badge/Video-PureData-7DA416.svg?style=flat-square&logo=Youtube)](https://www.youtube.com/watch?v=_U6Bn-1FDHc&ab_channel=AntoineCaillon)

#### VSChaos: 

[![Full repository](https://img.shields.io/badge/Gitlab-vschaos-7DA416.svg?style=flat-square&logo=Gitlab)](https://forge-2.ircam.fr/chemla/vschaos) 
[![Published in ArXiV](https://img.shields.io/badge/Paper-None-7D1616.svg?style=flat-square&logo=arXiv)]()
[![Video on YouTube](https://img.shields.io/badge/Video-None-7D1616.svg?style=flat-square&logo=Youtube)]()

#### WaVAE: Waveform Variational Auto-Encoder

[![Full repository](https://img.shields.io/badge/Github-wavae-7DA416.svg?style=flat-square&logo=Github)](https://github.com/acids-ircam/wavae) 
[![Published in ArXiV](https://img.shields.io/badge/Paper-None-7D1616.svg?style=flat-square&logo=arXiv)]()
[![Video on YouTube](https://img.shields.io/badge/Video-PureData-7DA416.svg?style=flat-square&logo=Youtube)](https://www.youtube.com/watch?v=Q3Ejm_ll6KU)


## Details

<h4 align="center">
  <a href="#categories">Categories</a> •
  <a href="#projects">Projects</a> •
  <a href="#acknowledgements">Acknowledgements</a> •
  <a href="#license">License</a>
</h4>

---

## Categories

Our different projects fall into four major categories
- *Generation* includes all model that allow to synthesize signal, based on different paradigms.
- *Control* are models which aim to learn high-level control over other generative mechanisms.
- *Hardware* are specific projects to use our models in embedded hardware platforms and synthesizers.
- *Others* mostly regroup past (discontinued) projects, notably on symbolic notation.

## Projects

### Generation

This category includes all model that allow to synthesize signal, based on different paradigms.


---

#### RAVE: Real-time Audio Variational auto-Encoder
[![Full repository](https://img.shields.io/badge/Github-rave-7DA416.svg?style=flat-square&logo=GitHub)](https://github.com/acids-ircam/ddsp_pytorch) 
[![Published in ArXiV](https://img.shields.io/badge/Paper-2111.05011-167DA4.svg?style=flat-square&logo=arXiv)](https://arxiv.org/abs/2111.05011)
[![Video on YouTube](https://img.shields.io/badge/Video-None-7D1616.svg?style=flat-square&logo=Youtube)]()

**Available plugins** 
[![Full repository](https://img.shields.io/badge/MaxMsp-_-7DA416.svg?style=flat-square&logo=Apple)]()
[![Full repository](https://img.shields.io/badge/MaxMsp-_-7DA416.svg?style=flat-square&logo=Windows)]()
[![Full repository](https://img.shields.io/badge/PureData-_-7DA416.svg?style=flat-square&logo=Linux)]()

**Friend summary.** RAVE is a signal generator, which is both high-quality (48kHz generation) and blazingly-fast (25x realtime on CPU). Compared to previous (DDSP) approaches, we can generate any type of sounds (polyphonic, noises), and we can also greatly reduce the number of control dimensions. The drawback is that the dimensions themselves are not necessarily understandable. Therefore, we can use it for timbre transfer train another (prior) model to generate audio automatically.

**Scientific summary.** RAVE is a variational autoencoder for fast and high-quality neural audio synthesis. The RAVE model allows both fast and high-quality audio waveform synthesis, by using a novel two-stage training procedure, namely representation learning and adversarial fine-tuning. Using a post-training analysis of the latent space allows a direct control between the reconstruction fidelity and the representation compactness. By leveraging a multi-band decomposition of the raw waveform, we show that our model is the first able to generate 48kHz audio signals, while simultaneously running 20 times faster than real-time on a standard laptop CPU. We evaluate synthesis quality using both quantitative and qualitative subjective experiments and show the superiority of our approach compared to existing models. Finally, we present applications of our model for timbre transfer and signal compression. All of our source code and audio examples are publicly available

**Works best for** *timbre transfer to any sound* and *prior (self-sufficient) generation*

---

#### DDSP: Differentiable Digital Signal Processing 
[![Full repository](https://img.shields.io/badge/Github-ddsp_pytorch-7DA416.svg?style=flat-square&logo=GitHub)](https://github.com/acids-ircam/ddsp_pytorch) 
[![Published in ArXiV](https://img.shields.io/badge/Paper-2001.04643-167DA4.svg?style=flat-square&logo=arXiv)](https://arxiv.org/abs/2001.04643) 
[![Video on YouTube](https://img.shields.io/badge/Video-PureData-7DA416.svg?style=flat-square&logo=Youtube)](https://www.youtube.com/watch?v=_U6Bn-1FDHc&ab_channel=AntoineCaillon)

**Available plugins** 
[![Full repository](https://img.shields.io/badge/PureData-_-7DA416.svg?style=flat-square&logo=Apple)]()
[![Full repository](https://img.shields.io/badge/PureData-_-7DA416.svg?style=flat-square&logo=Linux)]()

**Friend summary.** The [DDSP model](https://github.com/magenta/ddsp) mixes DSP with deep learning. The cool thing is that it is lightweight and controls understandable synthesis blocks (harmonic synth and filtered noise). Also, the control signals are known descriptors (f0 and loudness). But this seriously limits the type of signal that can be modeled (monophonic and harmonic). Also the control descriptors must have good expressivity, otherwise the synthesized sound is a bit crappy. This implementation can be exported to a torchscript model, ready to be used inside a realtime environment (see [this video](https://www.youtube.com/watch?v=_U6Bn-1FDHc)).

**Scientific summary.** Differentiable Digital Signal Processing (DDSP) library, which enables direct integration of classic signal processing elements with deep learning methods. Focusing on audio synthesis, we achieve high-fidelity generation without the need for large autoregressive models or adversarial losses, demonstrating that DDSP enables utilizing strong inductive biases without losing the expressive power of neural networks. Further, we show that combining interpretable modules permits manipulation of each separate model component, with applications such as independent control of pitch and loudness, realistic extrapolation to pitches not seen during training, blind dereverberation of room acoustics, transfer of extracted room acoustics to new environments, and transformation of timbre between disparate sources. In short, DDSP enables an interpretable and modular approach to generative modeling, without sacrificing the benefits of deep learning.

**Works best for** *timbre transfer to monophonic instruments*

---

#### VSChaos: 

[![Full repository](https://img.shields.io/badge/Gitlab-vschaos-7DA416.svg?style=flat-square&logo=Gitlab)](https://forge-2.ircam.fr/chemla/vschaos) 
[![Published in ArXiV](https://img.shields.io/badge/Paper-None-7D1616.svg?style=flat-square&logo=arXiv)]()
[![Video on YouTube](https://img.shields.io/badge/Video-None-7D1616.svg?style=flat-square&logo=Youtube)]()

**Available plugins** 
[![Full repository](https://img.shields.io/badge/MaxMsp-_-7DA416.svg?style=flat-square&logo=Apple)]()

**Friend summary.** VSChaos is an open-source Python library for variational neural audio synthesis. This library, based on pytorch, allows high-level functions for creating, training, and using many variants of variational auto-encoding. It provides easy data loading, with a unified dataset architecture, with methods specifically targeting audio data handling (spectral transforms, raw waveform slicing, transformations). There is also a modular definition of variational auto-encoders and generative adversarial networks, allowing to define custom hybridations. This facilitates the easy definition for model conditioning and semi-supervised methods, algebraic losses, allowing to define custom training criteria. It is available as a set of Max patches for real-time / offline generation.

**Works best for** *experimental harmonic synthesis*

---

#### WaVAE: Waveform Variational Auto-Encoder

[![Full repository](https://img.shields.io/badge/Github-wavae-7DA416.svg?style=flat-square&logo=Github)](https://github.com/acids-ircam/wavae) 
[![Published in ArXiV](https://img.shields.io/badge/Paper-None-7D1616.svg?style=flat-square&logo=arXiv)]()
[![Video on YouTube](https://img.shields.io/badge/Video-PureData-7DA416.svg?style=flat-square&logo=Youtube)](https://www.youtube.com/watch?v=Q3Ejm_ll6KU)

**Available plugins** 
[![Full repository](https://img.shields.io/badge/PureData-_-7DA416.svg?style=flat-square&logo=Linux)]()

**Friend summary.** Despite its name, its not a waveform based VAE, but a melspec one with a melGAN decoder. There is also an adversarial regularization on the latent space in order to extract the loudness from it. You can even use it on your dataset, and train the whole thing in maybe 2-4 days on a single GPU. This model has realtime generation and a highly-compressed and expressive latent representation.

---

#### Generative timbre spaces

[![Full repository](https://img.shields.io/badge/Github-timbre-7DA416.svg?style=flat-square&logo=GitHub)](https://github.com/acids-ircam/variational-timbre) 
[![Published in ArXiV](https://img.shields.io/badge/Paper-1805.08501-167DA4.svg?style=flat-square&logo=arXiv)](https://arxiv.org/abs/1805.08501)
[![Video on YouTube](https://img.shields.io/badge/Video-None-7D1616.svg?style=flat-square&logo=Youtube)]()

**Friend summary.** This project aims to construct generative timbre spaces, this mixes deep audio synthesis and perceptual studies. The audio rendering was not up to current standards, but the perceptual inference works very well.

**Scientific summary.** We show that Variational Auto-Encoders (VAE) can alleviate all of these limitations by constructing generative timbre spaces. To do so, we adapt VAEs to learn an audio latent space, while using perceptual ratings from timbre studies to regularize the organization of this space. The resulting space allows us to analyze novel instruments, while being able to synthesize audio from any point of this space. We introduce a specific regularization allowing to enforce any given similarity distances onto these spaces. We show that the resulting space provide almost similar distance relationships as timbre spaces. We evaluate several spectral transforms and show that the Non-Stationary Gabor Transform (NSGT) provides the highest correlation to timbre spaces and the best quality of synthesis. Furthermore, we show that these spaces can generalize to novel instruments and can generate any path between instruments to understand their timbre relationships. As these spaces are continuous, we study how audio descriptors behave along the latent dimensions. We show that even though descriptors have an overall non-linear topology, they follow a locally smooth evolution. Based on this, we introduce a method for descriptor-based synthesis and show that we can control the descriptors of an instrument while keeping its timbre structure.

**Works best for** *understanding timbre*

---



### Control

---

#### FlowSynth: Universal audio synthesizer control

[![Full repository](https://img.shields.io/badge/Github-flow_synth-7DA416.svg?style=flat-square&logo=Github)](https://github.com/acids-ircam/flow_synthesizer) 
[![Published in ArXiV](https://img.shields.io/badge/Paper-1907.00971-167DA4.svg?style=flat-square&logo=arXiv)](https://arxiv.org/abs/1907.00971)
[![Video on YouTube](https://img.shields.io/badge/Video-Max4Live-7DA416.svg?style=flat-square&logo=Youtube)](https://www.youtube.com/watch?v=UufQwUitBIw)

**Available plugins** 
[![Full repository](https://img.shields.io/badge/Max4Live-_-7DA416.svg?style=flat-square&logo=Apple)]()
[![Full repository](https://img.shields.io/badge/MaxMsp-_-7DA416.svg?style=flat-square&logo=Apple)]()

**Scientific summary.** Sound synthesizers are pervasive in music and they now even entirely define new music genres. However, their complexity and sets of parameters renders them difficult to master. We created an innovative generative probabilistic model that learns an invertible mapping between a continuous auditory latent space of a synthesizer audio capabilities and the space of its parameters. We approach this task using variational auto-encoders and normalizing flows Using this new learning model, we can learn the principal macro-controls of a synthesizer, allowing to travel across its organized manifold of sounds, performing parameter inference from audio to control the synthesizer with our voice, and even address semantic dimension learning where we find how the controls fit to given semantic concepts, all within a single model. Our model can be used in creative applications and its real-time implementation in Ableton Live.

**Works best for** *finding synth parameters from audio*, *automatic macro-controls*, *quick exploration of synths*, 

---



### Hardware

---

#### Neurorack: Embedded deep audio synthesis in Eurorack format

[![Full repository](https://img.shields.io/badge/Github-neurorack-7DA416.svg?style=flat-square&logo=Github)](https://github.com/ninon-io/Impact-Synth-Hardware) 
[![Published in ArXiV](https://img.shields.io/badge/Paper-1907.00971-167DA4.svg?style=flat-square&logo=arXiv)](https://arxiv.org/abs/1907.00971)
[![Video on YouTube](https://img.shields.io/badge/Video-Max4Live-7DA416.svg?style=flat-square&logo=Youtube)](https://www.youtube.com/watch?v=64VpQenCHVs)

**Scientific summary.** This project documents the Neurorack, which is a deep AI-based synthesizer based on the Jetson Nano development kit in a EuroRack format. The following diagram briefly explains the overall structure of the module and the relations between the hardware and software (green) components. The hardware part features 4 CV and 2 Gates (along with a screen, rotary and button for handling the menus), which all communicate with specific Python libraries. Note that the behavior of these controls (and the module itself) is highly dependent on the type of deep model embedded. For this first version of the Neurorack, we implemented a descriptor-based impact sounds generator.

## Acknowledgements


## Copyright and license

Code and documentation copyright 2012-2022 by all members of ACIDS. Code released under the [CC-BY-NC-SA 4.0 licence](https://creativecommons.org/licenses/by-nc-sa/4.0/).
