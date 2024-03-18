# Sequencing-and-bioinformatics-training-KEMRI-2024
## Installation of Miniconda
### Step 1 Download Miniconda installer
```
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh .
```
### Step 2. Install Miniconda
```
bash miniconda-installer.sh
```

Follow the instructions shown on the screen. 
Next, you will be shown this option below.
```
Miniconda3 will now be installed into this location:
/root/miniconda3

  - Press ENTER to confirm the location
  - Press CTRL-C to abort the installation
  - Or specify a different location below
```

Just press ENTER and continue.

Once the installation is finished, you will be prompted to start Miniconda or not.

### Step 3. Configure Miniconda

```
Do you wish the installer to initialize Miniconda3
by running conda init? [yes|no]
[no] >>>
```

Type ‘yes’, then hit ENTER. You should see this as an output.


```
no change     /root/miniconda3/condabin/conda
no change     /root/miniconda3/bin/conda
no change     /root/miniconda3/bin/conda-env
no change     /root/miniconda3/bin/activate
no change     /root/miniconda3/bin/deactivate
no change     /root/miniconda3/etc/profile.d/conda.sh
no change     /root/miniconda3/etc/fish/conf.d/conda.fish
no change     /root/miniconda3/shell/condabin/Conda.psm1
no change     /root/miniconda3/shell/condabin/conda-hook.ps1
no change     /root/miniconda3/lib/python3.11/site-packages/xontrib/conda.xsh
no change     /root/miniconda3/etc/profile.d/conda.csh
modified      /root/.bashrc

==> For changes to take effect, close and re-open your current shell. <==

If you'd prefer that conda's base environment not be activated on startup, 
   set the auto_activate_base parameter to false: 

conda config --set auto_activate_base false

Thank you for installing Miniconda3!
```
