# WDSProject

<h1>Windows Deployment Services Imaging Project</h1>

<h2>Description</h2>
I used a Windows 10 Enterprise virtual machine to create an image for workstations in the domain to boot from. I created and formatted another partition using disk management in order to allow the image to be stored. After installing the applications, I ran Sysprep to allow the image to be deployed to other computers. 
<br />
I booted the virtual machine into winPE and copied the image to the partition that I created using the dism command within command prompt. Then I added a USB drive to the virtual machine to store the install.wim file. In order to store the file, I had to reformat the USB drive as exFAT because the maximum file size of FAT32 was insufficient for the install.wim file.

<br />


<h2>Technologies Used</h2>

- <b>Windows 10</b>
- <b>Sysprep</b>
- <b>VirtualBox</b>
- <b>WinPE</b>
- <b>AnyBurn</b>
- <b>Windows Deployment Services</b>
- <b>PXE</b>


<h2>Project walk-through:</h2>
