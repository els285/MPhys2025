# New CSF Instructions

CSF is the computing cluster I use for training models on GPUs.
You need to use a terminal for this and `ssh` in e.g.
```
ssh <username>@csf3.itservices.manchester.ac.uk
```
where you will then be prompted for your password and will have to do two-factor authentication.

You can also access CSF through the `Remote-SSH` extension to VSCode (although you may have to fiddle with the parameters of the `Remote-SSH` extension).

## GPU on CSF

Main instructions for GPUs on CSF3 [here](https://ri.itservices.manchester.ac.uk/csf3/batch-slurm/gpu-jobs-slurm/)


To get an interactive GPU job, do:
```
srun --partition=gpuL --gpus=2 --ntasks=4 --time=1-0 --pty bash
```

Submitting a batch job:
```
sbatch <submit_script>
```

Checking job
```
squeue
```

Connecting to a running job 

Example submission script:
```
#!/bin/bash --login
#SBATCH -p gpuL               # v100 GPUs
#SBATCH -G 1                  # 1 GPU
#SBATCH -t 1-0                # Wallclock limit (1-0 is 1 day, 4-0 is the max permitted)
#SBATCH -n 1                  # One Slurm task
#SBATCH -c 8                  # 8 CPU cores available to the host code.
                              # Can use up to 12 CPUs with an A100 GPU.
                              # Can use up to 12 CPUs with an L40s GPU.

# Latest version of CUDA
module purge
module load libs/cuda

echo "Job is using $SLURM_GPUS GPU(s) with ID(s) $CUDA_VISIBLE_DEVICES and $SLURM_CPUS_PER_TASK CPU core(s)"

# This example uses OpenMP for multi-core host code - tell OpenMP how many CPU cores to use.
export OMP_NUM_THREADS=$SLURM_CPUS_PER_TASK

conda activate nu2flow_enve

python scripts/train.py
h = i
```