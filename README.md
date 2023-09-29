<div width="100%" height="100%" align="center">
  
<h1 align="center">
  <p align="center">TinyML and Efficient Deep Learning Computing</p>
  <a href="https://www.youtube.com/playlist?list=PL80kAHvQbh-ocildRaxjjBy6MR1ZsNCU7">
  </a>
</h1>
  
  
<b>강의 주제: TinyML and Efficient Deep Learning Computing</b></br>
Instructor : Song Han(Associate Professor, MIT EECS)</br>
[[schedule](https://efficientml.ai/schedule/)] | [[youtube](https://www.youtube.com/playlist?list=PL80kAHvQbh-ocildRaxjjBy6MR1ZsNCU7)] | [[github](https://github.com/mit-han-lab/6s965-fall2022)]</b>

</div>

## :bulb: 목표

- **효율적인 추론 방법 공부**

  > 딥러닝 연산에 있어서 효율성을 높일 수 있는 알고리즘을 공부한다.

- **제한된 성능에서의 딥러닝 모델 구성**

  > 디바이스의 제약에 맞춘 효율적인 딥러닝 모델을 구성한다.

</br>

## 🚩 정리한 문서 목록

### 📖 Basics of Deep Learning

- [Efficiency Metrics](https://github.com/erectbranch/TinyML_and_Efficient_DLC/tree/master/lec02/summary02)

  > latency, storage, energy

  > Memory-Related(\#parameters, model size, \#activations), Computation(MACs, FLOP)

### 📔 Efficient Inference

- [Pruning Granularity, Pruning Critertion](https://github.com/erectbranch/TinyML_and_Efficient_DLC/tree/master/lec03)

  > unstructured/structured pruning
  
  > magnitude-based pruning(L1-norm), second-order-based pruning, percentage-of-zero-based pruning, regression-based pruning

- [Automatic Pruning, Lottery Ticket Hypothesis](https://github.com/erectbranch/TinyML_and_Efficient_DLC/tree/master/lec04/summary01)

  > pruning ratio, pruning sensitivity, AMC, NetAdapt

  > Finetuning, iterative pruning, regularization, Lottery Ticket Hypothesis

- [System & Hardware Support for Sparsity](https://github.com/erectbranch/TinyML_and_Efficient_DLC/tree/master/lec04/summary02)

  > EIE(CSC format: relative index, column pointer)

  > M:N Sparsity

- [Quantization](https://github.com/erectbranch/TinyML_and_Efficient_DLC/tree/master/lec05)

  > Numeric Data Types: integer, fixed-point, floating-point(IEEE 754 single/half precision, BF16, TF32)

  > Symmetric vs Asymmetric quantization, Uniform vs Non-uniform quantization

  > Deep Compression(K-Means-based weight quantization, Huffman coding), Linear Quantization(zero point, scaling factor)

- [Post Training Quantization](https://github.com/erectbranch/TinyML_and_Efficient_DLC/tree/master/lec06/summary01)

  > Weight Quantiztion: Per-Tensor Activation Per-Channel Activation, Weight Equalization, Adative Rounding

  > Activation Quantization: During training(EMA), Calibration(Min-Max, KL-divergence, Mean Squared Error)

  > Bias Correction, Zero-Shot Quantization(ZeroQ)

- [Quantization-Aware Training, Low bit-width quantization](https://github.com/erectbranch/TinyML_and_Efficient_DLC/tree/master/lec06/summary02)

  > Fake quantization, Straight-Through Estimator

  > Binary Quantization(Deterministic, Stochastic, XNOR-Net), Ternary Quantization

- [Neural Architecture Search: basic concepts & manually-designed neural networks](https://github.com/erectbranch/TinyML_and_Efficient_DLC/tree/master/lec07/summary01)

  > input stem, stage, head
  
  > AlexNet, VGGNet, SqueezeNet(global average pooling, fire module, pointwise convolution), ResNet50(bottleneck block, residual learning), ResNeXt(grouped convolution)
  
  > MobileNet(depthwise-separable convolution, width/resolution multiplier), MobileNetV2(inverted bottleneck block), ShuffleNet(channel shuffle), SENet(squeeze-and-excitation block), MobileNetV3(redesigning expensive layers, h-swish)

- [Neural Architecture Search: RNN controller & search strategy](https://github.com/erectbranch/TinyML_and_Efficient_DLC/tree/master/lec07/summary02)

  > cell-level search space, network-level search space

  > design the search space: Cumulative Error Distribution, FLOPs distribution

  > Search Strategy: grid search, random search, reinforcement learning, bayesian optimization, gradient-based search, evolutionary search

  > EfficientNet(compound scaling), DARTS

- [Neural Architecture Search: Performance Estimation & Hardware-Aware NAS](https://github.com/erectbranch/TinyML_and_Efficient_DLC/tree/master/lec08)

  > Weight Inheritance, HyperNetwork, Weight Sharing(super-network, sub-network)

  > Performance Estimation Heuristics: Zen-NAS, GradSign

  > Hardware-Aware NAS(ProxylessNAS, HAT), One-Shot NAS(Once-for-All)

- [Knowledge Distillation](https://github.com/erectbranch/TinyML_and_Efficient_DLC/tree/master/lec10/summary01)

  > Knowledge Distillation(distillation loss, temperature)
  
  > KD: matching intermediate weights/features/attention maps/sparsity pattern/relational information(layers, samples)

- [Self Distillation, Online Distlliation, Applications](https://github.com/erectbranch/TinyML_and_Efficient_DLC/tree/master/lec10/summary02)

  > Self Distillation, Online Distillation, Combining Online and Self-Distillation, Network Augmentation
  
  > Applications: Object Detection, Semantic Segmentation, GAN, NLP

- [MCUNet](https://github.com/erectbranch/TinyML_and_Efficient_DLC/tree/master/lec11)

  > microcontroller, flash/SRAM usage, peak SRAM usage, MCUNet: TinyNAS, TinyEngine

  > TinyNAS: automated search space optimization(weight/resolution multiplier), resource-constrained model specialization(Once-for-All)

  > MCUNetV2: patch-based inference, network redistribution, joint automated search for optimization, MCUNetV2 architecture(VWW dataset inference)

  > RNNPool, MicroNets(MOPs & latency/energy consumption relationship)

### ⚙️ Efficient Training and System Support

- [TinyEngine](https://github.com/erectbranch/TinyML_and_Efficient_DLC/tree/master/lec17)

  > memory hierarchy of MCU, data layout(NCHW, NHWC, CHWN)

  > TinyEngine: Loop Unrolling, Loop Reordering, Loop Tiling, SIMD programming, Im2col, In-place depthwise convolution, appropriate data layout(pointwise, depthwise convolution), Winograd convolution

</br>

## :mag: Schedule

### Lecture 1: Introduction

[ [slides](https://hanlab.mit.edu/files/course/slides/MIT-TinyML-Lec01-Introduction.pdf) ]

### Lecture 2: Basics of Deep Learning

[ [slides](https://hanlab.mit.edu/files/course/slides/MIT-TinyML-Lec02-Basics-of-Neural-Networks.pdf) | [video](https://youtu.be/5HpLyZd1h0Q) ]

---
## Efficient Inference

---

### Lecture 3: Pruning and Sparsity (Part I)

[ [slides](https://hanlab.mit.edu/files/course/slides/MIT-TinyML-Lec03-Pruning-I.pdf) | [video](https://youtu.be/sZzc6tAtTrM) ]

### Lecture 4: Pruning and Sparsity (Part II)

[ [slides](https://hanlab.mit.edu/files/course/slides/MIT-TinyML-Lec04-Pruning-II.pdf) | [video](https://youtu.be/1njtOcYNAmg) ]

### Lecture 5: Quantization (Part I)

[ [slides](https://hanlab.mit.edu/files/course/slides/MIT-TinyML-Lec05-Quantization-I.pdf) | [video](https://youtu.be/91stHPsxwig) ]

### Lecture 6: Quantization (Part II)

[ [slides](https://hanlab.mit.edu/files/course/slides/MIT-TinyML-Lec06-Quantization-II.pdf) | [video](https://youtu.be/sYpl97ToNdg) ]

### Lecture 7: Neural Architecture Search 
(Part I)

[ [slides](https://hanlab.mit.edu/files/course/slides/MIT-TinyML-Lec07-NAS-I.pdf) | [video](https://youtu.be/NQj5TkqX48Q) ]

### Lecture 8: Neural Architecture Search
(Part II)

[ [slides](https://hanlab.mit.edu/files/course/slides/MIT-TinyML-Lec08-NAS-II.pdf) | [video](https://youtu.be/UlvkBZdOhpg) ]

### Lecture 9: Neural Architecture Search
(Part III)

[ [slides](https://hanlab.mit.edu/files/course/slides/MIT-TinyML-Lec09-NAS-III.pdf) | [video](https://youtu.be/_cvn9pflblk) ]

### Lecture 10: Knowledge Distillation

[ [slides](https://hanlab.mit.edu/files/course/slides/MIT-TinyML-Lec10-Knowledge-Distillation.pdf) | [video](https://youtu.be/IIqf-oUTHe0) ]

### Lecture 11: MCUNet - Tiny Neural Network 
Design for Microcontrollers

[ [slides](https://hanlab.mit.edu/files/course/slides/MIT-TinyML-Lec11-MCUNet.pdf) | [video](https://youtu.be/Hi4I0ZtPsbY) ]

~~Lecture 12: Paper Reading Presentation~~

---

## Efficient Training and System Support

---

### Lecture 13: Distributed Training and Gradient Compression (Part I)

[ [slides](https://hanlab.mit.edu/files/course/slides/MIT-TinyML-Lec13-Distributed-Training-I.pdf) | [video](https://youtu.be/oIIy6nmMoeM) ]

### Lecture 14: Distributed Training and Gradient Compression (Part II)

[ [slides](https://hanlab.mit.edu/files/course/slides/MIT-TinyML-Lec14-Distributed-Training-II.pdf) | [video](https://youtu.be/7W0MCjc8OD4) ]

### Lecture 15: On-Device Training and Transfer Learning (Part I)

[ [slides](https://hanlab.mit.edu/files/course/slides/MIT-TinyML-Lec15-On-Device-Training-And-Transfer-Learning-I.pdf) | [video](https://youtu.be/P_tVABpgb6w) ]

### Lecture 16: On-Device Training and Transfer Learning (Part II)

[ [slides](https://hanlab.mit.edu/files/course/slides/MIT-TinyML-Lec16-On-Device-Training-And-Transfer-Learning-II.pdf) | [video](https://youtu.be/rG-KM8eVzj8) ]

### Lecture 17: TinyEngine - Efficient Training and Inference on Microcontrollers

[ [slides](https://hanlab.mit.edu/files/course/slides/MIT-TinyML-Lec17-TinyEngine.pdf) | [video](https://youtu.be/oCMnJXH0c50) ]

---

## Application-Specific Optimizations

---

### Lecture 18: Efficient Point Cloud Recognition

[ [slides](https://hanlab.mit.edu/files/course/slides/MIT-TinyML-Lec18-Efficient-Point-Cloud-Recognition.pdf) | [video](https://youtu.be/fKIxpM-F0zw) ]

### Lecture 19: Efficient Video Understanding and GANs

[ [slides](https://hanlab.mit.edu/files/course/slides/MIT-TinyML-Lec19-Efficient-Video-Understanding-GANs.pdf) | [video](https://youtu.be/J4olmnIwgtk) ]

### Lecture 20: Efficient Transformers

[ [slides](https://hanlab.mit.edu/files/course/slides/MIT-TinyML-Lec20-Efficient-Transformers.pdf) | [video](https://youtu.be/RGUCmX1fvOE) ]

---

## Quantum ML

---

### Lecture 21: Basics of Quantum Computing

[ [slides](https://hanlab.mit.edu/files/course/slides/MIT-TinyML-Lec21-Quantum-Basics.pdf) | [video](https://youtu.be/8eT1QTVb1uo) ]

### Lecture 22: Quantum Machine Learning

[ [slides](https://hanlab.mit.edu/files/course/slides/MIT-TinyML-Lec22-Quantum-ML.pdf) | [video](https://youtu.be/20ftuhSV4sk) ]

### Lecture 23: Noise Robust Quantum ML

[ [slides](https://hanlab.mit.edu/files/course/slides/MIT-TinyML-Lec23-Noise-Robust-Quantum-ML.pdf) | [video](https://youtu.be/1gV0u8SfXe8) ]

~~Lecture 24: Final Project Presentation~~

~~Lecture 25: Final Project Presentation~~

### Lecture 26: Course Summary & Guest Lecture

[ [slides](https://hanlab.mit.edu/files/course/slides/MIT-TinyML-Lec25-AIMET.pdf) | [video](https://youtu.be/NCuLGvCeYl8) ]
