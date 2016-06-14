# Setting up Python2 and Python3 using Anaconda

### Miniconda2

- We only need python2 for scons. You can instead choose to install all of anaconda2 as well, if needed.
- Download miniconda 2.7 64-bit bash installer from conda.pydata.org/miniconda.html
- Change permissions on the downloaded script
```bash
chmod +x Miniconda2-latest-Linux-x86_64.sh
```

- Execute Miniconda2-latest-Linux-x86_64.sh 
   - Pick an install location, e.g, /home/agram/python/miniconda2
```bash
./Miniconda2-latest-Linux-x86_64.sh 
```
   
- Add "bin" directory to PATH (pre-pend it).
- Update the miniconda installation
```bash
conda update --all 
```
- Install scons
```bash
conda install scons
```


### Anaconda3

- Download anaconda 3.5 64-bit bash installer from www.continuum.io/downloads
- Changer permissions on the downloaded script
```bash
chmod +x Anaconda3-4.0.0-Linux-x86_64.sh
```
- Execute Anaconda3-4.0.0-Linux-x86_64.sh
   - Pick an install location, e.g, /home/agram/python/anaconda3
```bash
./Anaconda-3.4.0.0-Linux-x86_64.sh
```

- Add "bin" directory to PATH (make sure miniconda2 comes first and then anaconda3)
- Link conda from anaconda3 to conda3
```bash
ln -s /home/agram/python/anaconda3/bin/conda /home/agram/python/anaconda3/bin/conda3
```
-Add conda-forge to list of channels for the latest libraries
```bash
conda3 config --add channels conda-forge
```
- Update the anaconda installation
```bash
conda3 update --all
```

### Anaconda3 package management

```bash
conda3 remove --features mkl   (If conda uses mkl. This will get rid of annoying messages from mkl)
conda3 install krb5
conda3 install gdal
export GDAL_DATA="/home/agram/python/anaconda3/share"
conda3 install libgdal
conda3 install netcdf4
conda install -c omnia fftw3f=3.3.4
```