# Microsoft Office 365 Course Notes

Notes and resources for Microsoft Office 365 official courses:

* [10997 - Office 365 Administration and Troubleshooting](https://www.microsoft.com/en-us/learning/course.aspx?cid=10997)

## Table of Contents

* [Setup](#setup)
* [References](#references)
* [Resources](#resources)

## Setup

Office 365 Account and Tenant Setup.

### Lab Environment

The instructor will inform you about the lab environment you will be using. Only complete the following section for online labs if you are using online labs. If you are using Hyper-V labs then skip the online labs section.

#### Online Labs

If using online labs follow these steps:

1. Go to [Learn On Demand](https://ddls.learnondemand.net/).
1. Click on `Register with Training Key`.
1. Enter the course training code provided by the instructor.

#### Hyper-V Labs

If using Hyper-V labs follow these steps:

1. To monitor the virtual machines using the shortcut on the Desktop launch `Hyper-V Manager`.
1. Open `PowerShell` using the icon on the Start Menu.
1. Type the following commands (use TAB autocomplete):

```powershell

# Only run these commands once each.

Get-VM | Remove-VMSnapshot
Get-VM | Set-VMProcessor -Count 2
Get-VM -Name *LON* | Set-VMMemory -StartupBytes 4GB
Get-VM | Checkpoint-VM
Get-VM | Where { $_.Name -match 'NAT|DC1' } | Start-VM

# Wait for the NAT and DC1 virtual machines to start.

Get-VM | Start-VM

```

Your lab environment is now ready for use.

User: `adatum\Administrator`

Pass: `Pa55w.rd`

### Courseware

1. Go to [Skillpipe](https://skillpipe.com/en-GB/).
1. Register or login with your account. If registering use a personal email address.
1. Select `Add a Course` and use the code given to you by the instructor.

### Email Address 📧

__Do not use your existing Microsoft accounts to work with the labs!__

1. Open [Outlook.com](https://outlook.live.com/owa/).
1. Create a new `outlook.com` account. Use your last name with the date eg: lastname20180618@outlook.com
1. Use this email address throughout the course.

### Office 365 Tenancy

The following steps will create a new trial Office 365 tenancy.

_Note: Use your mobile phone to prevent the need to supply a credit card._

1. Go to [Microsoft Office 365 Enterprise](https://products.office.com/en-au/business/office-365-enterprise-e3-business-software).
1. Click `Free trial`.
1. Using your new `outlook.com` email address, register for the free trial.

### Bookmarks

Bookmark the URLs in [References](#references) below.

## References

* [Office 365 Portal](https://portal.office.com/)
* [Office 365 Admin Portal](https://admin.microsoft.com/)
* [10997 GitHub Repository](https://github.com/MicrosoftLearning/10997-O365AdministrationandTroubleshooting)

## Resources

### Major Changes

* [Introducing a free version of Microsoft Teams](https://techcommunity.microsoft.com/t5/Microsoft-Teams-Blog/Introducing-a-free-version-of-Microsoft-Teams/ba-p/214592)
* [Skype for Business to Microsoft Teams upgrade](https://docs.microsoft.com/en-us/MicrosoftTeams/journey-skypeforbusiness-teams)



