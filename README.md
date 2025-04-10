# MarioGAN-LSI
This project implements the experiments for the paper *[Illuminating Mario Scenes in the Latent Space of a Generative Adversarial Network](https://arxiv.org/abs/2007.05674)*. Our project implements a method for Latent Space Illumination (LSI) which explores the latent space of generative adversarial network via modern quality diversity algorithms (MAP-Elites, ME (Iso+LineDD), CMA-ME). The project is derived from the *[MarioGAN](https://github.com/TheHedgeify/DagstuhlGAN)* project. We use a newer version of the *[Mario-AI-Framework](https://github.com/amidos2006/Mario-AI-Framework)* that allows for a richer definition of game tiles. 

# Training the GAN
The GAN that generates Mario levels can be run by the following command in the GANTrain folder:

```
python3 GANTraining.py --cuda
```

However, training the GAN is unnecessary as we include a *[pretrained model](https://github.com/icaros-usc/MarioGAN-LSI/blob/master/GANTrain/samples/netG_epoch_4999_7684.pth)* in the repo.

# Running LSI Experiments
Experiments can be run with the command:
```
python3 search/run_search.py -w 1 -c search/config/experiment/experiment.tml
```

The w parameter specifies a worker id which specifies which trial to run from a given experiment file. This allows for parallel execution of all trials on a high-performance cluster.
