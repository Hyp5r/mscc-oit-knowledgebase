[author]:        <> (William Quinn)
[last modified]: <> (2020-10-13)
[revision]:      <> (1)

# How do I perform a mail purge?

## Prerequisites

* **Discovery Management** role in Office 365
  + This role must be manually assigned in the Office 365 ECP.
* **Organization Management** role in Office 365
  + Tenant admins are automatically granted this role.
* [Exchange Online PowerShell Module](https://cmdletpswmodule.blob.core.windows.net/exopsmodule/Microsoft.Online.CSE.PSModule.Client.application)

## Performing a Compliance Search

Head over to <https://protection.office.com>, then click on *Search -> Content search* on the left side navigation bar.

![](./img/CB63_mXuFn5LJ8CPFd5plJPAJIHWUknLOA.png =512x)

A new window will appear. In the new window, click on the **New search** button near the top-left of the page.

![](./img/RKvzi9mWpPIMbf3GM1s5LtYuq1T_SmRIcg.png =512x)

In the search builder, you will have many options to choose from in searching for emails, OneDrive files, and more.

![](./img/eN14ZDJJ2ALJhVewvPVanFj_ED7jiO1VWw.png =512x)

Click on **Add conditions** to add new conditions to the search, including sender, recipients, time sent, and more. Under Locations, you can click on **All locations** to search all emails, OneDrive, and SharePoint sides. By clicking **Specific locations**, you can choose what locations you'd like to search.

Once everything is filled out, click on **Save & run**. You'll be prompted to type in the search's name and description before the search runs.

!!! Info

     Searches can take anywhere from a few minutes to several hours depending on criteria. You will need to periodically check the status of the search as you will not be alerted when the job is complete.

## Using PowerShell to Purge the Compliance Search

On a Windows Machine, install the Exchange Online PowerShell Module. You can then find it by searching the Start Menu for Microsoft Exchange.

![](./img/hH5rCvOpHr_lxWgdGSp8wwQ01sJZZMMwGA.png =512x)

After running the Exchange Online PowerShell Module, you'll be prompted with a PowerShell window with a note at the top.

![](./img/_Rzw795j3dSzerRyqEFEjFCBuGSMP1kCGg.png =512x)

To connect to the Security & Compliance center to look at compliance searches, type in the following command:

``` powershell
Connect-IPPSSession -UserPrincipalName <your email address>
```

An Okta login window will appear. Log into your account, and you'll be redirected back to the PowerShell window.

![](./img/BqijIqe5rZCwM69CuGUVtAbwVaPZGOMG6A.png =512x)

To look at a list of compliance searches, type in the following command:

``` powershell
Get-ComplianceSearch
```

This will list every compliance search in the system. Typically, the list is sorted from oldest to newest, but sometimes the list doesn't sort properly.

From here, you'll want to find the compliance search you ran earlier. 

!!! Info

    You may want to make the PowerShell window larger when running this command, otherwise you may not be able to see the third and fourth columns - those show the date the search completed and the current status of the search.

![](./img/x1bT1UaC-CxDmQg5iErLZwQNF1jB1y7AWA.png =512x)

Once you found your search and confirmed that it's completed, run the following command to purge all found emails from everyone's mailboxes:

``` powershell
New-ComplianceSearchAction -SearchName <your search name> -Purge -PurgeType SoftDelete
```

!!! Info

    You can switch out the `-PurgeType SoftDelete` command with `-PurgeType HardDelete` if needed. The difference between a `SoftDelete` and a `HardDelete` is whether or not the email itself can be recovered by a compliance search in the future. A `SoftDelete` will purge the email into a *Purged items* folder that a user cannot see, where a `HardDelete` will remove all instances of the email permanently.

This will prompt a confirmation with you to make sure this is what you want to run. Press **Y**, then press **Enter**.

Purging emails can take anywhere from several minutes to several hours, depending on volume of emails found and time of day.

*[ECP]: Exchange Control Panel
