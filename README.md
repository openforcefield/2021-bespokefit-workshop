# 2021-bespokefit-workshop

Materials for the 2021 OpenFF Bespokefit workshop.

## Installation and getting started

#### 1. Clone the repository:

```
git clone https://github.com/openforcefield/2021-bespokefit-workshop.git
cd 2021-bespokefit-workshop
```

#### 2. Install and activate the conda environment:

```
conda env create -f env.yml
conda activate 2021-bespokefit-workshop
```

#### 3. Start up the jupyter notebook with:

```
jupyter notebook workshop.ipynb
```

### Using a remote environment

If you performed the installation instructions above on a remote host accessible via SSH,
you can connect to the Jupyter notebook server through an SSH tunnel.

Among the notebook server output from the instructions above, you should see a line like:

```
[I 17:17:45.169 NotebookApp] http://localhost:<port>/?token=<token-content>
```

You will need this for the below instructions.

1. Open a terminal on your local host, and run the following, noting `<port>` from the server output above:

```
ssh -N -L 8801:localhost:<port> <remote-host>
```

2. In a web browser on your local host, enter the following in the URL bar

```
localhost:8801
```

3. Copy the token from the terminal running the server.
   It should be among the output like that given above, where `<token-content>` is shown.
   Enter this into the prompt for the token to access the notebook.


### Alternative way to download workshop materials

If you are unable to run `git clone` on your machine, you can instead click on the green `Code` button on the front page of this repository and download its contents as a zip file.

### Alternative way to install required software

If you are unable to run the `conda env create` command above, you can download a "single-file installer" that will deploy a conda installation with all the workshop software into your userspace. The single file installers are in the "Assets" section of the [latest release](https://github.com/openforcefield/2021-benchmarking-workshop/releases) of this repository. This single file installer is installed as follows (this is shown for Bash on Mac, the filenames/source commands will be slightly different on csh/Linux)

```
bash openff-benchmark-2021.08.04.0-py37-MacOSX-x86_64.sh -b -p ./miniconda3
source miniconda3/etc/profile.d/conda.sh 
conda activate
```
