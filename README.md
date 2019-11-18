# Docker installation

Docker is a virtual machine that makes software installations easier


## System requirements for Docker for mac

* Mac hardware must be a 2010 or newer model, with Intel’s hardware support for memory management unit (MMU) virtualization, including Extended Page Tables (EPT) and Unrestricted Mode. You can check to see if your machine has this support by running the following command in a terminal: sysctl kern.hv_support

* macOS El Capitan 10.11 and newer macOS releases are supported. At a minimum, Docker for Mac requires macOS Yosemite 10.10.3 or newer, with the caveat that going forward 10.10.x is a use-at-your-own risk proposition.

* Starting with Docker for Mac Stable release 1.13, and concurrent Edge releases, we no longer address issues specific to macOS Yosemite 10.10. In future releases, Docker for Mac could stop working on macOS Yosemite 10.10 due to the deprecated status of this macOS version. We recommend upgrading to the latest version of macOS.

* At least 4GB of RAM

* VirtualBox prior to version 4.3.30 must NOT be installed (it is incompatible with Docker for Mac). If you have a newer version of VirtualBox installed, it’s fine.


## Installation
* Make an account on [Docker Hub](https://hub.docker.com/)
* For MacOS click install to install the docker installer.
* Double-click **Docker.dmg** to open the installer, then drag Moby the whale to the Applications folder.
* You are prompted to authorize Docker.app with your system password after you launch it. Privileged access is needed to install networking components and links to the Docker apps. The whale in the top status bar indicates that Docker is running, and accessible from a terminal.
* If you just installed the app, you also get a success message with suggested next steps and a link to this documentation. Click the whale (whale
menu) in the status bar to dismiss this popup.



## Test it out in your terminal
```bash
docker run hello-world
```

## System requirements for Docker for Windows

* To run Docker, your machine must have a 64-bit operating system running Windows 7 or higher. Additionally, you must make sure that virtualization is enabled on your machine. 

* Docker for Windows requires Microsoft Hyper-V to run. The Docker for Windows installer enables Hyper-V for you, if needed, and restart your machine. After Hyper-V is enabled, VirtualBox no longer works, but any VirtualBox VM images remain. VirtualBox VMs created with docker-machine (including the default one typically created during Toolbox install) no longer start. These VMs cannot be used side-by-side with Docker for Windows. However, you can still use docker-machine to manage remote VMs.
* Virtualization must be enabled. Typically, virtualization is enabled by default. This is different from having Hyper-V enabled. For more detail see Virtualization must be enabled in Troubleshooting.
* The current version of Docker for Windows runs on 64bit Windows 10 Pro, Enterprise and Education (1607 Anniversary Update, Build 14393 or later).
Containers and images created with Docker for Windows are shared between all user accounts on machines where it is installed. This is because all Windows accounts use the same VM to build and run containers.
* Nested virtualization scenarios, such as running Docker for Windows on a VMWare or Parallels instance, might work, but come with no guarantees. For more information, see Running Docker for Windows in nested virtualization scenarios
What the Docker for Windows install includes: The installation provides Docker Engine, Docker CLI client, Docker Compose, Docker Machine, and Kitematic.
* If you have Windows 10 Pro edition or Enterprise with Hyper-V enabled you can install Docker Desktop for Windows
* If you have Windows other than Pro and Enterprise you can use Docker Toolbox which uses Oracle Virtual Box

## Installation Docker Desktop for Windows 10 Pro and Enterprise

* Make an account on [Docker Hub](https://hub.docker.com/)
* Download [Docker Desktop](https://www.docker.com/products/docker-desktop)
* After installation clone this repository

```bash
git clone https://github.com/docker/doodle.git
```
* A Docker image is a private filesystem, just for your container. It provides all the files and code your container will need. Running the docker build command creates a Docker image using the Dockerfile. This built image is in your machine's local Docker image registry.

```bash
cd doodle\cheers2019 ; 
docker build -t [username]/cheers2019 .
```
* Run the container

```bash
docker run -it --rm [username]/cheers2019
```
* Share the image to Docker Hub

```bash
docker login ; 
docker push [username]/cheers2019
```

## Installation Docker Toolbox for Windows 10 Home

* To run Docker, your machine must have a 64-bit operating system running Windows 7 or higher. Additionally, you must make sure that virtualization is enabled on your machine.
* Install the Docker Toolbox in [ToolBox Releases](https://github.com/docker/toolbox/releases) and install the latest version
* Follow the installer wizard. Uncheck Virtualbox if you have already installed it
* Click on Docker QuickStart Terminal
* Now you will see bash open with the $ sign
* Test Docker out with this command

```bash
docker run hello-world
```


