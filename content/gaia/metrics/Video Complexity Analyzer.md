
---
title: "Video Complexity Analyzer"
---

> [!quote] VCA 
> [VCA](https://vca.itec.aau.at/) is an open source video complexity analyzer. See the online documentation for instructions for building the source. The primary objective of VCA is to become the best spatial and temporal complexity predictor for every frame/ video segment/ video which aids in predicting encoding parameters for applications like online per-title encoding ([source](https://github.com/cd-athena/VCA)).



### DCT-based Energy Function
The energy function $H_{p,k}$ determines the block-wise texture of each frame, which is defined as:

> [!info] DCT-based Energy Function Equation
> $$H_{p,k} = \sum\limits_{i=0}^{w-1}\sum\limits_{j=0}^{w-1} e^{\left|\left(\frac{ij}{w^{2}}\right) -1 \right|} \left|DCT(i,j)\right|$$
> where $k$ is the block address in the $p^{th}$ frame, $w \times w$ pixels is the size of the block, and $DCT(i, j)$ is the $(i,j)^{th} DCT$ component when $i + j > 0$, else 0.


### Sum of Absolute Difference (SAD)

* *[Paper](https://dl.acm.org/doi/pdf/10.1145/3290408)

SAD is a block matching algorithm, where a frame is divided into non-overlapping blocks.

> [!info] SAD Equation
> $$SAD(i, j) = \sum\limits_{j=0}^{M-1}\sum\limits_{i=0}^{N-1} \left| C(k, t) - R(i + k, j + t) \right|$$
> 
> where $C(k, t)$ is the luminance value of the current frame and $R(i + k, j + t)$ is the luminance value of the reference frame.


In H.264 and HEVC, SAD is chosen because it uses fewer resources than other cost functions while also having low, and therefore acceptable distortion.


## Metrics of VCA

### Picture Order Count (POC)

### Spatial Complexity (E)

> [!info] Spatial Complexity Equation
> $$E = \sum_{k=0}^{C - 1} \frac{H_{p,k}}{C \cdot w^2}$$
> where $C$ represents the number of blocks per frame.



### Temporal Complexity (h)

> [!info] Temporal Complexity Equation
> $$h = \sum\limits_{k=0}^{C-1}\frac{SAD(H_{p,k}, H_{p-1, k})}{C \cdot w^2}$$



### Gradient of the Temporal Complexity (epsilon)

> [!info] Gradient of the Temporal Complexity Equation
>$$\epsilon = \frac{h_{p-1} - h_p}{h_{p-1}}$$

### Frame Brightness (L)

Frame Brightness denotes the average brightness of a frame.

> [!info] Frame Brightness Equation
> $$L = \sum\limits_{k=0}^{C-1} \sqrt{CB}_{0,k}$$
> 
> where $CB_{0, k}$ denotes the first index of the *coefficient buffer* of the k_{th} block.




### Average U Chroma Component (avgU)

### Average U Chroma Texture (energy U)

### Average V Chroma Component (avgV)

### Average V Chroma Texture (energyV)


