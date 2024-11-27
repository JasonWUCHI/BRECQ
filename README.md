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

#Links to Colab
1. Round-to-Nearest and FP32 Model
- https://colab.research.google.com/drive/1jRHirxZRaufpJAj1dixfo-bvWBYB-L7i?usp=sharing
2. AdaRound
- https://colab.research.google.com/drive/1sEcnR6QacAFfKGHcYFNk5xiDowkSKzrw?usp=sharing

#Experiments TODO
1. Try other more challenging dataset such as Cifar10
2. The activation distribution change-over-time chart
3. Check how to quantize to other degree such as INT4, INT5, INT8. Currently we have the code for INT8.
4. The FID Score of different quantization method
5. Qualitative Result comparison
6. Split the diffusion process to N chunks, and quantize the model in different chunks separately.