The repository is organized as follows:

- **Data**: input data used in the practical sessions:

- **Notebooks**: Python codes and Jupyter Notebooks used in the practical sessions. More specifically,

   - **VisualOptimization**: Gradient-based optimization of a 2D cost function with visualization of model trajectories.
   - **BasicPytorch**: Introduction to PyTorch, Linear and Logistic Regression.
   - **LearningFunction**: A practical look at the Universal Approximation Theorem and its implications for learning functions with NNs.
   - **MixtureDensityNetwork**: Mixture Density Networks for multi-modal probabilistic predictions
   - **WellLogFaciesPrediction**: Well Log facies prediction based on Force2020 Challange
   - **EventDetection**: Seismic event detection with Recurrent NNs
   - **SaltNet**: U-Net Salt Segmentation based on TGS Kaggle Challange
   - **EikonalPINN**: Physics-informed NN solution of Eikonal equation

- **Wandb**: Example usage of [Wandb](https://wandb.ai/site) with Logistic Regression for efficient ML experimentation

## Environment

To ensure reproducibility of the results, we have provided a `environment.yml` file. Ensure to have installed Anaconda or Miniconda on your computer. If you are not familiar with it, we suggesting using the [KAUST Miniconda Install recipe](https://github.com/kaust-rccl/ibex-miniconda-install). This has been tested both on macOS and Unix operative systems.

After that simply run:
```
./install_env.sh
```
It will take some time, if at the end you see the work `Done!` on your terminal you are ready to go!

Later in the course, it may be useful to have access to a workstation with GPU capabilities (it will speed up your training time).
A modified version of the environment and installation files for GPU-powered environment are also provided here.

Finally, if you do not have access to a GPU directly, you could use the [KAUST Ibex](https://www.hpc.kaust.edu.sa/ibex). To install the GPU environment follow the following steps:
```
ssh ${USER}@glogin.ibex.kaust.edu.sa
salloc --time=01:00:00 --gres=gpu:v100:1 
srun --pty bash
./install_env-gpu.sh
```

A sample SLURM file is provided
`jupyter_notebook_ibex.slurm` that allows setting up a Jupyter notebook with GPU capabilities.
