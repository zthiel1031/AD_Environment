In virtual box, click on the `New` icon at the top.

![](Images/2023-03-05-16-14-05.png)

For the name create something easy, in this case I'll use `Client`. Make sure the type is set to `Microsoft Windows` and the version is `Windows 10 (64-Bit)` then click next

![](Images/2023-03-06-22-25-23.png)

Next we will select how much RAM our machine will have. We can set our machine to have 2gb of Ram, however we can always change this later if needed. After doing so we can click continue through the rest of the prompts

![](Images/2023-03-06-22-26-30.png)


After creating the virtual machine we need to set a few different settings. With our new Client machine selected click on the `Settings` at the top of the page.

![](Images/2023-03-06-22-27-38.png)

On the settings page, select `System` then the `Processor` tab.
If you have multiple CPU cores on your system you can give it more than one, which will speed up some of the processes. However, it is not necessary. I set mine to 4 CPUs for this lab

![](Images/2023-03-06-22-28-20.png)

On the settings page, select `Network` and make sure adapter 1 is set to `Internal Network` and it should automatically generate the same internal network name we set for our domain controller.

![](Images/2023-03-06-22-29-04.png)

We are finally ready to launch our machine however it does not have an Operating system installed. Double click on the machine and you will see a dialoge box asking for a start up disk. You can click the folder to add your windows 10 iso that was downloaded. Then click start.

![](Images/2023-03-05-16-41-27.png)

Once the machine loads, proceed with a normal windows installation. During the setup it will as you to add a product key and you can say `I don't have a product key`

![](Images/2023-03-06-22-33-41.png)

When select an operating system. Make sure that you use anything other than WIndows 10 Home as you will not be able to join the domain. For ours we will select `Windows 10 Pro`. 

![](Images/2023-03-06-22-34-25.png)

