After downloading and installing Virtual box and the extension pack, as well as all of the iso's needed for this lab. Open virtual box to create our domain controller.

# Create and Configure Domain Controller Machine

In virtual box, click on the `New` icon at the top.

![](Images/2023-03-05-16-14-05.png)

For the name create something easy, in this case I'll use `DC` for domain controller. Make sure the type is set to `Microsoft Windows` and the version is `Other Windows (64-Bit)` then click next

![](Images/2023-03-05-16-17-20.png)

Next we will select how much RAM our machine will have. We can set our machine to have 2gb of Ram, however we can always change this later if needed. After doing so we can click continue through the rest of the prompts

![](Images/2023-03-05-16-19-59.png)


After creating the virtual machine we need to set a few different settings. With our new DC machine selected click on the `Settings` at the top of the page.

![](Images/2023-03-05-16-22-38.png)

On the settings page, select `System` then the `Processor` tab.
If you have multiple CPU cores on your system you can give it more than one, which will speed up some of the processes. However, it is not necessary. I set mine to 4 CPUs for this lab

![](Images/2023-03-05-16-29-36.png)

Next we need to add another network interface card(NIC). To do so click the `Network` tab on the left. Looking back at our architecture diagram we can see on our domain controller we need two NICs one that will face the internet. This one is set by default in viirtual box as `Adapter 1` and is attached to `NAT`.

To create our internal NIC we need to click the `Adapter 2` tab. Check the `Enable Network Adapter` box and change `Attached to:` to Internal Network then click ok.

![](Images/2023-03-05-16-36-28.png)

We are finally ready to launch our machine however it does not have an Operating system installed. Double click on the machine and you will see a dialoge box asking for a start up disk. You can click the folder to add your windows server 2019 iso that was downloaded. Then click start.

![](Images/2023-03-05-16-41-27.png)

Once the machine loads, proceed with a normal windows installation. During the setup it will as you to select an operating system. Make sure that you use either of the `Desktop Experiences` doing so will give you a GUI to work wiith vs just a CMD line iinterface. 

After clickiing next and waiting for the install to complete, it will take several minutes where the server will restart and ask you to push any key to boot, please sit tight until it prompts you to create the admin user with a password. After that is done you should be able to log in to the machine with the credentials you set.

