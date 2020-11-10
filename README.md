![Screenshot](docs/figures/DeepMoD_logo.png)

DeePyMoD is a modular framework for model discovery of PDEs and ODEs from noise data. The framework is comprised of four components, that can seperately be altered: i) A function approximator to construct a surrogate of the data, ii) a function to construct the library of features, iii) a sparse regression algorithm to select the active components from the feature library and iv) a constraint on the function approximator, based on the active components. 

![Screenshot](docs/figures/framework.png)

More information can be found in the following two papers: , [arXiv:2011.04336](https://arxiv.org/abs/2011.04336), [arXiv:1904.09406](http://arxiv.org/abs/1904.09406) and the full documentation is availeble on [phimal.github.io/DeePyMoD/](https://phimal.github.io/DeePyMoD/).

**What's the use case?** Classical Model Discovery methods struggle with elevated noise levels and sparse datasets due the low accuracy of numerical differentiation. DeepMoD can handle high noise and sparse datasets, making it well suited for model discovery on actual experimental data.

**What types of models can you discover?** DeepMoD can discover non-linear, multi-dimensional and/or coupled ODEs and PDEs. See our paper and the examples folder for a demonstration of each.

# Features

* **Many example notebooks** We have implemented a varyity of examples ranging from 2D Advection Diffusion, Burgers' equation to non-linear, higher order ODE's If you miss any example, don't hesitate to give us a heads-up.

* **Extendable** DeePyMoD is designed to be easily extendable and modifiable. You can simply plug in your own cost function, library or training regime.

* **Automatic library** The library and coefficient vectors are automatically constructed from the maximum order of polynomial and differentiation. If that doesn't cut it for your use case, it's easy to plug in your own library function.

* **Extensive logging** We provide a simple command line logger to see how training is going and an extensive custom Tensorboard logger.

* **Fast** Depending on the size of the data-set DeepMoD, running a model search with DeepMoD takes of the order of minutes/ tens of minutes on a standard CPU. Running the code on GPU's drastically improves performence. 

# How to install

To install DeePyMoD, simply run 

``` pip install .```

in the main directory. 