[author]:        <> (William Quinn)
[last modified]: <> (2020-10-12)
[revision]:      <> (1)

# How do I connect to a VDI session?

Technical Operations provides a VDI infrastructure that can be accessed by faculty and staff who are unable to utilize the VPN infrastructure in place. There are two primary methods for connecting to our VDI infrastructure - via the VMware Horizon Client and via the VMware Horizon HTML Access (web access).

Technical Operations recommends using the VMware Horizon Client. To download the VMware Horizon Client, [click here if you're running Windows](https://my.vmware.com/en/web/vmware/downloads/details?downloadGroup=CART21FQ2_WIN_800&productId=1027&rPId=52667) or [click here if you're running Mac](https://my.vmware.com/en/web/vmware/downloads/details?downloadGroup=CART21FQ2_MAC_800&productId=1027&rPId=52668).

!!! Info

     If you're unable to install the VMware Horizon Client, feel free to click on VMware Horizon HTML Access and continue with the rest of the guide.

## Installing the VMware Horizon Client

Double-click on the VMware Horizon Client download to begin the installation of the VMware Horizon Client.

### Mac

![](./img/UxviDKPEQvEASjd2ZBwhER1BTEqAaViTeA.png =512x)

To install the VMware Horizon Client on a Mac, simply drag the VMware Horizon Client icon into your Applications folder. From there, you can find the application in Launchpad.

### Windows

![](./img/ALCv1rl78V8Md4O4WnA7uSRuQZDZ7uJ1zA.png =512x)

To install the VMware Horizon Client on Windows, double-click the installer file. From there, click on the **Agree & Install **button. Once completed, you can find the application in the start menu. 

## Connecting to the VDI Session via the Client

Open the VMware Horizon Client on your computer.

![](./img/_qjK5v2y2UMALmZ_ktlP9maXUr5CbpyT9g.png =512x)

The following window should appear. Type in  in the Connection Server box and check the **Always connect at launch** button, then click on **Connect**.

![](./img/iKa-2nRbGYT4pb7AyLJ8DaUcPX9rFN_oXw.png =512x)

A login box should now appear. To login to the VMware Horizon server, use your username and password that you'd use for your computer, then click on Login.

!!! Warning

     Please do not use your email address as the username as it will not allow you to log in.

You should immediately connect to a VDI session. From here, you'll want to use Remote Desktop to log into your assigned work machine.

## Connecting to a VDI Session via Web Browser

To connect to a VDI session to access Motlow State resources, head over to <https://view.mscc.edu>.

![](./img/Ecv2516A2Ja43sGjNs5pGlS-VVddqTnIJg.png =512x)

You should see a screen similar to the one above. You'll have two options for connecting to the VMware Horizon system, the VMware Horizon Client and the VMware Horizon HTML Access (web-based). From here, click on the **VMware Horizion HTML Access** on the right-side of the screen.

![](./img/6IBlt9xiLYFUrLVNPV6O7bOgNM7TLMFgmg.png =512x)

You should now see the login screen. To login to the VMware Horizon server, use your username and password that you'd use for your computer, then click on **Login**.

!!! Warning

     Please do not use your email address as the username as it will not allow you to log in.

![](./img/ycEPjWBQLSLWmkPy0hJnBY_U5VuSOu8NaQ.png =512x)

You should now see the following screen. Click on **Faculty Desktop** and you'll be logged into a VDI session. From here, you'll want to use Remote Desktop to log into your assigned work machine.

After connecting using a VDI session, the next thing most employees need is to connect to their desktop machine via Remote Desktop or RDP.

Double-click on the Remote Desktop Connection icon on your desktop, or press the _Start_ button and type in _Remote Desktop Connection_ and press **Enter** on your keyboard.

![](./img/C-vpFjtVFtsNvvl1e783xc7wGK29ie0rdA.png =512x)

The Remote Desktop Connection window will appear. In the Computer field, type in the name of your computer, then click on **Connect**.

![](./img/eKHdMcC9tNm4JdcEEBk7wDobSws76lVoQw.png =512x)

A Windows Security dialog box will appear. Input the following information:

  + **Username:** MOTLOW\username  

For example, if your username is RLocke, you would type in MOTLOW\RLocke

  + **Password:** Your Motlow State password
  + _Optionally_, you may check the box to _Remember me_.

![](./img/9i5BvZj8RivxCJUA5V6kpbcGbTHhAAJWHA.png =512x)

Click on **OK**. You may see a warning window pop up that states _The identity of the remote computer cannot be verified. Do you want to connect anyway?_. Click on **Yes** and optionally check the box that states _Don't ask me again for connections to this computer_.

If everything authenticates successfully, you'll be connected to your desktop machine using Remote Desktop. To close out of Remote Desktop, move your mouse to the top-middle of your screen to show a blue connection bar and press the **X** button.
