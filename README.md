# Generative Models

This is juyoung-hong's repository of generative models.

# Getting Started

## Environment

Set Environment using one of below commands.

```bash
# pip
pip install -r requirements.txt

# conda
conda env create --file environment.yaml
```

## WorkFlow

1. Modify config file (experiment/*.yaml)
2. Train
```bash
python3 src/train/train_VAE.py experiment=mnist_VAE.yaml
```
3. Monitoring
```bash
tensorboard --logdir=logs/train/runs
```
4. Inference
```bash
python3 src/inference/inference_VAE.py -o=result -d=cuda -ckpt logs/train/runs/2023-11-03_12-37-21/ckpt/model/epoch_29.pth
```

## Model Zoo

|Model Type|Docs|
|:---:|:---:|
|AE|[Auto Encoder](docs/AutoEncoder.md)|
|VAE|[Variational Auto Encoder](docs/VariationalAutoEncoder.md)|
|GAN|[Generative Adversarial Networks](docs/GAN.md)|
|cGAN|[Conditional Generative Adversarial Networks](docs/cGAN.md)|
|DCGAN|[Deep Convolutional Generative Adversarial Networks](docs/DCGAN.md)|
|ACGAN|[Auxiliary Classifier Generative Adversarial Networks](docs/ACGAN.md)|
|WGAN|[Wasserstein Generative Adversarial Networks](docs/WGAN.md)|
|WGAN-GP|[Wasserstein Generative Adversarial Networks - Gradient Penalty](docs/WGAN-GP.md)|
|CycleGAN|[Cycle Consistent Adversarial Networks](docs/CycleGAN.md)|

# References

- [lightning-hydra-template](https://github.com/ashleve/lightning-hydra-template)
- [Generative Deep Learning](https://www.oreilly.com/library/view/generative-deep-learning/9781492041931/)
- [modulabs youtube](https://www.youtube.com/watch?v=vZdEGcLU_8U)
