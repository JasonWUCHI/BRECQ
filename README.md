# BRECQ
Referencing Pytorch implementation of BRECQ, ICLR 2021

```latex
@article{li2021brecq,
  title={BRECQ: Pushing the Limit of Post-Training Quantization by Block Reconstruction},
  author={Li, Yuhang and Gong, Ruihao and Tan, Xu and Yang, Yang and Hu, Peng and Zhang, Qi and Yu, Fengwei and Wang, Wei and Gu, Shi},
  journal={arXiv preprint arXiv:2102.05426},
  year={2021}
}
```

# Links to Colab
1. Round-to-Nearest and FP32 Model
- https://colab.research.google.com/drive/1jRHirxZRaufpJAj1dixfo-bvWBYB-L7i?usp=sharing
2. AdaRound
- https://colab.research.google.com/drive/1sEcnR6QacAFfKGHcYFNk5xiDowkSKzrw?usp=sharing
3. Weight for the mnist diffusion model and other quantized model
- https://drive.google.com/drive/folders/1_WGoVt-QsN9bSZw-dgwq0qzHt8bIwx4s?usp=drive_link

# Progress
1. Finish Implementing FID Score
2. Finish implementing INT4, INT5, INT8

# Problem Observed
1. Not sure why but INT4 has lower FID than the FP32 model... probably MNIST is too easy?

# Experiments TODO
1. Try other more challenging dataset such as Cifar10
2. The activation distribution change-over-time chart
5. Qualitative Result comparison
6. Split the diffusion process to N chunks, and quantize the model in different chunks separately.

| Precision | FID | Inception Score | Elapsed time (s) to generate 100 images |
| ---------- | --- | --------------- | -------------------------------|
| FP32 | 423.80 | 3.2058 | 8.7629 |
| INT8 (AdaRound) | 321.39 | 2.8715 | - |
| INT8 (Q-Diffusion with AdaRound) | - | 3.1133 | - |
| INT4 (Round to nearest) | 414.58 | 3.2058 | 6.6632 |


