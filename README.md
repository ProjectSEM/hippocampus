## hippocampus

This repo hosts the hippocampus model file described in this paper: 

[Complementary learning systems within the hippocampus: a neural network modeling approach to reconciling episodic memory with statistical learning](http://rstb.royalsocietypublishing.org/content/372/1711/20160049.long) by Anna C. Schapiro, Nicholas B. Turk-Browne, Matthew M. Botvinick, Kenneth A. Norman


First of all, you need to clone this repo. If you don’t use github, just click “clone or download” (the green button on the upper right), then click “Download ZIP”. And if you unzip it, you should get a folder called `\hippocampus`. The model file is `\hippocampus\src\Schapiro_etal_hippocampus_model_exercise.proj`


Now we need to get emergent 7.0.1. A huge thanks to [Daniel Greenidge](https://github.com/cdgreenidge), who made a virtual machine image that contains Emergent 7.0.1! A detailed explanation of the installation process is described below, modified from [Daniel’s documentation](https://github.com/cdgreenidge/emergent7-vm). 


**1.** Install VirtualBox to run the virtual machine image [here](https://www.virtualbox.org/wiki/Downloads). Made sure you install the version that corresponds to your OS (mac, windows or linux). 

Alternatively, if you use homebrew, you can install VirtualBox by running the following command in the terminal: 
```
brew cask install virtualbox
```

then restart the terminal and run:
```
virtualbox
```

**2.** Download the virtual machine image created by Daniel 
[here](https://drive.google.com/a/princeton.edu/uc?export=download&confirm=o7kD&id=0B2p760tyzIMANnIwVUFsNUxHbVE)

**3.** Import the virtual machine image file (`emergent7vm.ova`) into VirtualBox. From the VirtualBox home screen,
select *File* > *Import Appliance*. Choose the virtual machine image (`emergent7vm.ova`) and accept the default options. The virtual box interface should look like the following: 

<img src="https://github.com/ProjectSEM/hippocampus/blob/master/readme_sup/virtualbox_interface.png" width="600" />


**4.** Start the VM by double-clicking “emergent7vm” on the VirtualBox home screen. 

**5.** Add a shared folder between the VM and your machine, so the VM can access the hippocampus model file.

With the VM running,
click *Devices* > *Shared Folders* > *Shared Folder Settings*. Click the small
plus sign to add a shared folder. Make sure to check the "Auto mount" and "Make
permanent" checkboxes. Once you've added the shared folder, reboot the VM (lower right corner). 

Now the vm interface should look like this: 
<img src="https://github.com/ProjectSEM/hippocampus/blob/master/readme_sup/vm_interface.png" width="600" />


**ps: if the screen is locked, the default password is `ubuntu`**

**6.** After it restarts, click the “emergent” icon on the desktop, then click *File* > *Open Project*. You should see the shared folder under “places”, it should be called `\sf_hippocampus` (assuming you didn’t change the folder name when you clone the repo). Click `\sf_hippocampus` > `\src` > `Schapiro_etal_hippocampus_model_exercise.proj`. 


**7.** To train the model, click `Batch_Init` and then `Batch_Run`. To test the model, click `Test_init` and then `Test_Run`. The activation values of the model will be saved automatically. Because the folder is shared between the virtual machine and the host, you can access the saved activation files from your machine. 
 
<img src="https://github.com/ProjectSEM/hippocampus/blob/master/readme_sup/emergent7_interface.png" width="800" />


**Homework!?**

Here’s an [assignment](https://docs.google.com/document/d/1n0sTdKeWUKJWlshFZMXMaoSFVoGVXyKTdMGYw9JXYJU/edit) based on this model, take a look if you are interested! 
