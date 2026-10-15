# AI-EDGE REU: ML Experiments

Experiments from the AI-EDGE Summer REU at Ohio State (Summer 2026), using PyTorch in Google Colab.

## Projects

| Project | What I did | Result |
|---|---|---|
| [CNN hyperparameters](cnn_hyperparameters.ipynb) | Trained CNNs on Fashion-MNIST across 3 learning rates and 3 network sizes | Best: 91.66% validation accuracy (lr 0.01); worst: 80.57% (lr 0.0001). Learning rate mattered more than network size. |
| [Vision Transformer](vit_fashion_mnist.ipynb) | Adapted a ViT to Fashion-MNIST and trained it with AdamW for 20 epochs | 85.36% test accuracy, below the CNN baseline |
| [VAE experiments](vae_experiments.md) | Changed latent size, beta, and learning rate one at a time | Latent size 2 to 10 cut reconstruction error ~35% |

## Notes

- **CNN notebook:** data loading is from a program-provided starter; I extended it with three size variants and an experiment loop.
- **ViT notebook:** uses the ViT implementation from [ml-tutorials-suite](https://github.com/williamqwu/ml-tutorials-suite). My work was adapting it to Fashion-MNIST (input size, channels), training it, and comparing against the CNN.
- **ViT vs. CNN:** the two used different optimizers and epoch counts, so this is a rough comparison, not a controlled one.
- **Evaluation:** the course notebooks evaluate on the test set (labeled "validation"), with no separate held-out validation split.
