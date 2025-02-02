Installation on GNU/Linux
=========================

## Install via Conda

Use conda or bioconda to install OpenMS.

```{tab} openms
openms contains OpenMS C++ Tools.
```

```{tab} libopenms
libopenms is the C++ library required for the OpenMS C++ Tools to work.
```

```{tab} pyopenms
pyopenms is the python package that allows to use algorithms from libopenms in Python.
```

```{tab} openms-thirdparty
openms-thirdparty are external tools that are wrapped in OpenMS with adapters. This is required to use the adapters in
the openms package.
```

1. Follow the instructions to [install conda](https://docs.conda.io/projects/conda/en/latest/user-guide/install/linux.html).
2. Install OpenMS using conda:
   `conda install -c openms openms`
3. Other OpenMS packages can be installed using:
   ```
   conda install -c openms pyopenms
   conda install -c openms openms-thirdparty
   conda install -c openms libopenms
   ```

To install using bioconda:

```
conda install -c bioconda openms
conda install -c bioconda libopenms
conda install -c bioconda openms-thirdparty
```

## Install via Debian package

For Debian-based Linux users, it is suggested to  use the [deb-package](https://abibuilder.informatik.uni-tuebingen.de/archive/openms/OpenMSInstaller/release/latest/) provided. It is most easily installed with **[gdebi](https://launchpad.net/gdebi)**
which automatically resolves the dependencies available in the PPA Repositories.

```bash
sudo apt-get install gdebi
sudo gdebi /PATH/TO/OpenMS.deb
```
If you encounter errors with unavailable packages, troubleshoot using the following steps.

1. Qt5 (or one of its packages, e.g. `qt5xbase`) is missing.
   It might be because your Debian is too old to have a recent enough version in its official repositories. It is
   suggested to use the same packages that are used while building (make sure to adapt the Qt version and your
   Debian/Ubuntu version, here Xenial):
   ```bash
   sudo add-apt-repository ppa:beineri/opt-qt59-xenial
   sudo apt-get update
   ```
   Run the installation again.
2. ICU with its `libicu` is missing.
   You can find the missing version on [pkgs.org](https://pkgs.org) and install it with `gdebi`, too. You can have
   multiple versions of ICU installed.
3. Error while executing a tool
   To ensure the tool functionality, make sure you add the `OPENMS_DATA_PATH` variable to your environment as follow
   `export OPENMS_DATA_PATH=/usr/share/OpenMS`
4. Thirdparty installation of Qt5 in 1
   Make sure you source the provided environment file using:
   `source /opt/qt59/bin/qt59-env.sh`

   Executables for THIRDPARTY applications can be found in:
   `/usr/share/OpenMS/THIRDPARTY`
5. Add the folders in your `PATH` for a convenient use of the adapters.

## Install via package managers

Packaged versions of **OpenMS** are provided for Fedora, OpenSUSE, Debian, and Ubuntu. You can find them to download
[here](https://pkgs.org/download/openms). For other GNU/Linux distributions or to obtain the most recent version of the
library, installation should be done via building from the source code.

```{important}
These packages are not directly maintained by the OpenMS team and they can not be guaranteed to have the
same behaviour as when building it from source code. Also, their availability and version is subject to change and
support might be limited (due to unforeseen or untested behaviour). It is suggested not to install them parallel to our
Debian package.
```

```{note}
Some thirdparty software used via adapter tools in OpenMS might also require an installed JavaVM.
```

## Run via a (Bio)Docker image

Make sure you have [Docker installed](https://docs.docker.com/engine/install/).

Our Docker support is constantly updated. Images can be obtained via [ghcr.io](https://ghcr.io).

```{tab}

[openms-executables](https://ghcr.io/openms/openms-executables:latest)

```

```{tab}

[openms-library](https://ghcr.io/openms/openms-library:latest)

```

Or via [BioContainers Registeries](https://biocontainers.pro/registry).

1. [BioContainers libopenms](https://biocontainers.pro/tools/libopenms)
2. [BioContainers openms](https://biocontainers.pro/tools/openms)
3. [BioContainers openms-thirdparty](https://biocontainers.pro/tools/openms-thirdparty)
4. [BioContainers pyOpenMS](https://biocontainers.pro/tools/pyopenms)

Docker images can be pulled via or one of the following commands:

```
docker pull biocontainers/openms
docker pull biocontainers/libopenms
docker pull biocontainers/openms-thirdparty
docker pull biocontainers/pyopenms
```

Dockerfiles to build different kind of images (corresponding to build instructions, e.g. on ArchLinux) can be found on
GitHub in [OpenMS/dockerfiles](https://github.com/OpenMS/dockerfiles) repository.

## Build OpenMS from source

To build OpenMS from source, follow the build instructions for [Linux](https://abibuilder.informatik.uni-tuebingen.de/archive/openms/Documentation/release/latest/html/install_linux.html).
