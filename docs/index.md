# Introduction: What is High Performance Computing?
High Performance Computing (HPC) refers to the practice of using many computer processors simultaneously to solve problems that would take too long, or be outright impossible, on a single, standard computer. In other words, it is the science of *supercomputing*. HPC systems allow researchers, engineers, and analysts to run massive simulations, process huge datasets, and perform advanced modeling that drives discoveries in fields such as climate science, astrophysics, genomics, materials engineering, and artificial intelligence.

At its core, an HPC system is made up of a group of interconnected computers, known collectively as a **cluster**. Each individual computer within the cluster is called a **node**. A node contains its own processors, memory, storage, and networking hardware, along with an operating system (OS) that enables it to run software and communicate with other nodes.

The way these nodes work together is key to HPC performance. By dividing a large problem into smaller parts and processing them in parallel across multiple nodes, the system can achieve results thousands or millions of times faster than a single machine. This approach is known as **parallel computing** and is a defining feature of HPC.

In most HPC environments, computing resources are categorized into **login nodes** and **compute nodes**:

* **Login nodes:**

     * These are entry points to the cluster. Users typically connect to login nodes using Secure Shell (SSH) from their personal or work computer. These nodes are not designed to handle heavy computational tasks; instead serving as a workspace for preparing to send tasks to other sections of the cluster. On login nodes, you can typically create and edit scripts, move and organize files, load necessary software modules, and submit jobs to the system's scheduler. There are usually only a few login nodes, and they can be shared by many users at once.

* **Compute nodes:**

    * These are the stars of an HPC system. Compute nodes are where the actual intensive computations or simulations are run. They typically are much more powerful than a standard desktop, often equipped with multiple CPUs (central processing units), large amounts of memory, and sometimes specialized hardware like GPUs (graphics processing units). Users do not log in to compute nodes directly, instead they request an **interactive session** from a login node to run commands in real time, or they submit jobs to a **batch queue** managed by a scheduler such as Slurm or HTCondor.

This separation of roles ensures that login nodes remain responsive for all users while compute nodes are fully dedicated to processing workloads. By scaling up to hundreds or thousands of compute nodes, an HPC system can tackle computations at speeds measured in trillions of operations per second - well beyond what a typical computer could achieve.

In this lesson, we're going to go over how to access login nodes, how to queue batch jobs, and how to find help if you run into issues. If this is your first time reading technical documentation, we recommend you to take a few minutes to go through our [lesson on understanding technical documentation](https://det-lab.github.io/reading-documentation/) before continuing. 

---

[Click here](01_login_nodes.md) to continue to the next section where we will explain how to access login nodes.