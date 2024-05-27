# GMI

<div align="center">
<img src="https://img.shields.io/badge/pytorch-black?style=flat&logo=PyTorch&logoColor=#EE4C2C"/>
<img src="https://img.shields.io/badge/python-black?style=flat&logo=Python&logoColor=#3776AB"/>  
</div>

GAN을 활용한 Image Classfication Model Inversion Attack
# Description

### Start. 
Model Inversion Attack에 GAN을 적용하면 해당 작업을 수행할 수 있지 않을까라는 생각

### Search.
GAN을 활용한 Model Inversion Attack의 경우 많은 연구가 이루어져 있지는 않았지만, 하나의 논문을 발견할 수 있었음.

### Make a copy of search
해당 연구 내용을 바탕으로, 해당 모델을 따라서 구현하고, 실행시켜 그 효과를 검증해보기 위해 노력함.

### Hardship
해당 내용을 따라하던 도중, 전체 dataset의 구조와 학습 방식을 알 수 없었기에, 문제점을 마주침

### Development
1-wasserstein distane라는 개념을 도중 알게 되었고, 이를 이용하면 Image Classification Model의 출력을 GAN의 Discriminator의 출력과 맞춰 손실을 계산할 수 있지 않을까 생각함.

### Conclusion
결론적으로, 공격 대상이 될 모델의 영향을 받은 인공지능이, 그렇지 않은 인공지능보다 생성해낸 이미지와 공격 대상 모델의 학습 데이터와 코사인 유사도의 최댓값이 높았고, 이는 GAN이 원본 데이터의 값을 재현해낼 수 있다는 바를 시사함.

### Limit
하지만, MNIST의 데이터 특성상 학습 이미지의 다양성이 너무나 부족했고, 인공지능이 학습하는 과정에서 항상 같은 값을 출력해낼 수는 없다는 점에서, 완벽하게 GMI의 가능성을 제시했다고 보기는 어려움.

# Refrence

Zhang, Yuheng, et al. "The secret revealer: Generative model-inversion attacks against deep neural networks." Proceedings of the IEEE/CVF conference on computer vision and pattern recognition. 2020.
