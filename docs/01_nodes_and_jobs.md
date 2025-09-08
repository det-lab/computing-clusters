# Login Nodes
Login nodes are like the system's "front door", providing an environment to perform smaller, simple tasks, such as deleting, copying, or moving files, loading software, and preparing and submitting jobs to the scheduler. Login nodes in general have a much smaller share of the computing resources of a cluster, and they are also generally shared between all users. This means that trying to perform heavier computations runs not only the risk of failing or taking extended periods of times to complete, but can slow down the resource for everyone else attempting to use the cluster. It is vital then to remember to only use login nodes to submit jobs, not to try and run jobs from them.

Most HPC systems provide two main ways one can access a login node:

## 1. **Secure Shell (SSH)**

This is the most common method for connecting to HPCs. SSH allows for secure logins over unsecured networks by encrypting the data as it travels to and from both the user and server sides. If you are unfamiliar with SSH, we recommend you to take a few minutes to read through [this lesson](https://hsf-training.github.io/hsf-training-ssh-webpage/01-introduction/index.html). It is also possible to use SSH with an integrated development environment (IDE), such as Visual Studio Code, Spyder, or Jupyter.

* **Advantages:**

    * Generally faster and more responsive than web-based portals.

    * Widely supported across all operating systems.

* **Limitations:**

    * Requires some familiarity with the command line.

    * Needs an SSH client installed and configured on your local machine.

    * May require extra setup (SSH keys, firewall rules) before first use.

## 2. **Web Browser Access**

Some clusters have browser-based online portals or web clients where you can log in using your HPC credentials. These portals often present you with tools like JupyterLab/Notebook, RStudio, or graphical file managers. Many also provide a browser-based terminal for command-line work.
    
* **Advantages:**

    * No need to install special software on your local machine.

    * Works from any device with an internet connection.

    * Often includes access to virtual desktops or virtual machines for running GUI-based applications.

* **Limitations:**

    * Performance can be slower compared to a direct SSH connection.

    * Features may be limited to what the web interface provides.

## After Connecting
Regardless of how you log in, you will start on a login node. From there, you can:

* Navigate the file system and manage your project data, usually using either a virtual desktop or the command-line.

* Edit and prepare job scripts.

* Load necessary software modules.

* Submit jobs to compute nodes through the scheduler.

## Submitting Jobs

Depending on your computing cluster, you're likely to run into either Slurm (Simple Linux Utility for Resource Management) or HTCondor (High-Throughput Computing), which are able to run jobs either sequentially or in parallel. 

Using Slurm, each compute node/server has access to multiple **daemons**, such as **slurmd** which is similar to a remote shell and can wait for work, execute work, and return the job status before waiting for more work, **slurmdbd** (Slurm DataBase Daemon) which can record accounting information for multiple clusters in a single database, or **slurmrestd** (Slurm REST API Daemon) which can interact with Slurm through a REST API.

With HTCondor, after a user submits a job, the software allocates the task to available machines on the cluster and can automatically switch which machine it's using if necessary. This makes it especially useful for a job that needs to run several times with widely varying data sets. It can set a task for hundreds of machines at the same time and can pause or transfer some of the work between machines if other machines are needed for other jobs.

Then, depending on the cluster, there will likely be several options for you to begin running your jobs, such as interactively, in batch, or through a browser interface such as OnDemand.

Interactive sessions allow you to type commands and receive output back on-screen as commands complete.

Batch modes allows you to create a batch (or job) script which contains multiple commands to run, then the batch can be submitted to be ran by the compute servers as soon as resources are available.

# Compute Nodes