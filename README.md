# WDSProject

<h1>Windows Deployment Services Imaging Project</h1>

<h2>Description</h2>
I used a Windows 10 Enterprise virtual machine to create an image for workstations in the domain to boot from. I created and formatted another partition using disk management in order to allow the image to be stored. After installing the applications, I ran Sysprep to allow the image to be deployed to other computers. 
<br/><br/>
I booted the virtual machine into winPE and copied the image to the partition that I created using the dism command within command prompt. Then I added a USB drive to the virtual machine to store the install.wim file. In order to store the file, I had to reformat the USB drive as exFAT because the maximum file size of FAT32 was insufficient for the install.wim file. Then I used the AnyBurn application to edit the original Windows 10 iso file from Microsoft by adding the new install.wim file to the Windows 10 iso.
<br/><br/>
I added the edited Windows iso into the Windows Server 2019 and mounted the iso to access the install.wim and boot.wim files. Then I installed Windows Deployment Services onto the Server by navigating to Server manager and add roles and features where I added the Windows Deployment services role. Then I opened Windows Deployment Services within Administrative Tools and right-clicked the server and clicked on configure server. Then I clicked the option to integrate with Active Directory, I unchecked the options for proxy DHCP server and I clicked on respond to known and unknown clients for the PXE boot option. Once Windows Deployment Services was configured I expanded the server in the Windows Deployment Services tool and right-clicked on boot images and clicked on add boot image. Then I added the boot.wim file from the mounted Windows iso file. I followed the same steps for the install images but I added the install.wim file from the mounted iso file. Then I booted the workstation virtual machine from the network card and the customized image I had created was deployed successfully to the workstation on the domain.

<br />


<h2>Technologies Used</h2>

- <b>Windows 10</b>
- <b>Sysprep</b>
- <b>VirtualBox</b>
- <b>WinPE</b>
- <b>AnyBurn</b>
- <b>Windows Deployment Services</b>
- <b>PXE</b>


