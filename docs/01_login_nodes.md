# Login Nodes
Login nodes serve as the "front door" to the system; they provide a safe environment for preparing jobs, moving files, loading software, and submitting work to the scheduler. They are not intended for heavy computation, so it's important to use them only for lightweight tasks. Most HPC systems provide two main ways to access a login node:

1. **Web Browser Access**

Some clusters have browser-based online portals or web clients where you can log in using your HPC credentials. These portals often present you with tools like JupyterLab/Notebook, RStudio, or graphical file managers. Many also provide a browser-based terminal for command-line work.
    
* **Advantages:**

    * No need to install special software on your local machine.

    * Works from any device with an internet connection.

    * Often includes access to virtual desktops or virtual machines for running GUI-based applications.

* **Limitations:**

    * Performance can be slower compared to a direct SSH connection.

    * Features may be limited to what the web interface provides.

2. **Secure Shell (SSH)**

This is the most common method for connecting to HPCs. If you are unfamiliar with SSH, we recommend you to take a few minutes to read through [this lesson](https://hsf-training.github.io/hsf-training-ssh-webpage/01-introduction/index.html). It is also possible to use SSH with an integrated development environment (IDE), such as Visual Studio Code, Spyder, or Jupyter.

* **Advantages:**

    * Generally faster and more responsive than web-based portals.

    * Widely supported across all operating systems.

* **Limitations:**

    * Requires some familiarity with the command line.

    * Needs an SSH client installed and configured on your local machine.

    * May require extra setup (SSH keys, firewall rules) before first use.

## After Connecting
Regardless of how you log in, you will start on a login node. From there, you can:

* Navigate the file system and manage your project data.

* Edit and prepare job scripts.

* Load necessary software modules.

* Submit jobs to compute nodes through the scheduler.

>Tip: Avoid running resource-intensive computations directly on login nodes. These are shared by all users, and heavy use can affect system performance.