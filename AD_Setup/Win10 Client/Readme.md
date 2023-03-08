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

Finally we need to attach our Client to the domain. To do so we will use the advanced renamee feature through our system's about page. To access this right-click on the `Start` icon and select `System`

![](Images/2023-03-07-20-02-04.png)

Scroll down to the bottom of the window and select `Rename this PC (Advanced)`

![](Images/2023-03-07-20-03-18.png)

The system properties window will appear and you will click on the box that says `Change` to add the computer to the domain and change it's name.

Make sure you select the bubble that says `Domain` and add it to `mydomain.com` and rename the computer.

![](Images/2023-03-07-20-06-50.png)

You will then be required to enter a username and password to allow the computer to join the domain. For us we will use the admin account we created.

![](Images/2023-03-07-20-07-40.png)

After clicking `Ok` it will take a minute and you will see a welcome to the domain screen and it will ask you to restart the system.

Upon restarting the computer will attempt to log in a the local user. Select `Other User` iin the bottom left of the screen and you will see that it now says we are signing in to the domain of `MYDOMAIN`. Pick any random user that was created and sign in as them to verify the accounts were created successfully.

![](Images/2023-03-07-20-13-13.png)
