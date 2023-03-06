Now that we have our machine running, and the network set up, we can look to installing Active Directory domain services.

---

From the server manager dashboard click `Add roles and features`

![](Images/2023-03-05-21-04-26.png)

On the wizard screen, click `Next` three times until you get to the server roles. Make sure to click the box that says `Active Directory Domain Services.` Then click `Next` through the rest of the prompts.

![](Images/2023-03-05-21-08-54.png)

Once the iinstall is finished you will see a warning symbol with the flag at the top of the window. The warning says we enabled AD Domain services but there is no domain created. To do so click on `Promote this server to a domain controller`

![](Images/2023-03-05-21-14-41.png)

On the deployment configuration screen make sure to click `Add a new forest` and give your root domain a name. In this example we will use my domain.com.

![](Images/2023-03-05-21-18-48.png)

On the next page you will need to put in a password for the Directory Services Restore Mode so feel free to use whatever password you like and hit next. You can then push `Next` through the rest of the prompts and push `Install` when you come to it.

Once the install finishes it will automatically restart the machine. 

Notice upon restart, our username has changed to `MYDOMAIN\Administrator`

Instead of using the built in admin account we will create our own which we can do by going to `Start`, `Windows Administrative Tools`, then `Active Directory Users and Computers`.

![](Images/2023-03-05-21-37-09.png)

Once users and computers loads we see our domain listed on the left side of the window. Let's create a new Organizational Unit (OU) to put our admin account in. We can do so by right-clicking our domain, going to `New` and then to `Organizational Unit`

![](Images/2023-03-05-21-40-10.png)

We named our OU _ADMINS and now we can create a new user for that OU by right-clicking our newly created OU, going to `New` and then to `User` We can then fill out our information using the `a-` to denote this is an admin account.

![](Images/2023-03-05-21-43-46.png)

On the following screen you can create a password and uncheck the box that says `User must change password at next logon`

![](Images/2023-03-05-21-45-58.png)

This will create the account, however it will not add it to the OU by default. We can ad it by right-clicking on our user and selecting `Properties` Then select the `Members Of` tab and hit `Add`. On the next window we can type `Domain Admins` and click the `check name` button. If the object name underlines that means it is good to go. If the group isn't listed it will bring up another window asking to verify name and remove the typos from the list.

![](Images/2023-03-05-21-52-23.png)

You can then sign out, and upon doing CTRL+ALT+DEL you can select other user in the bottom left of the screen. For the username you'll use whatever you set it to. For me it was a-zthiel, and log in with the password for the account.