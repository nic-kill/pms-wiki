# NAS Software Comparison

This page serves as an opinionated comparison between the main players in the Home NAS space.

## Proxmox

!!! quote
    Proxmox VE is a complete open-source platform for enterprise virtualization. With the built-in web interface you can easily manage VMs and containers, software-defined storage and networking, high-availability clustering, and multiple out-of-the-box tools on a single solution.
  
While not technically a NAS software, Proxmox has become my go to home server OS of choice due to its flexibility and that it ships ZFS natively. For more details, see [Proxmox](../tech-stack/proxmox.md).

## unRAID

!!! quote
    Unraid OS allows sophisticated media aficionados, gamers, and other intensive data-users to have ultimate control over their data, media, applications, and desktops, using just about any combination of hardware.

[UnRAID ](https://unraid.net/) is perhaps the obvious alternative to PMS and indeed it does serve this niche incredibly well. The project has a long track record of supporting the product and has a [community](https://unraid.net/community) around it that is truly second to none.

However, unRAID is not open-source. It is also a paid product - there is nothing inherently wrong with people charging money for software they support. Like with Apple products you are paying for someone else to make decisions for you and unRAID has a very opinionated way of doing things.

## OpenMediaVault

!!! quote
    openmediavault is the next generation network attached storage (NAS) solution based on Debian Linux. It contains services like SSH, (S)FTP, SMB/CIFS, DAAP media server, RSync, BitTorrent client and many more. Thanks to the modular design of the framework it can be enhanced via plugins.

[openmediavault](https://www.openmediavault.org/) is open-source, based around Debian and has been regularly updated for years. It is capable of providing every feature that PMS does *and* provides a webUI. The project does a lot of things right and is a notable contender in this comparison and is for the most part the work of one developer, votdev. Incredible stuff.

<p align="center">
<img alt="omv-github" src="../../images/omv-github.png">
</p>

That said, for a GUI to be worth learning it has to be meaningfully better than the alternative by reducing complexity or being eye-candy. Unfortunately, OMV fails on both fronts. Sadly the UI looks dated and each time I've tried to use the project over the years I've come away frustrated by the extra complexity it adds. 

<p align="center">
<img alt="omv-ui" src="../../images/omv-ui.png">
</p>

This pervasive frustration was also the case as a new user. Something that could be configured in a few lines of a config file required navigating a UI and doing a whole lot of clicking. As a more experienced administrator these days I have embraced automation via [Ansible](../concepts/infraascode.md#ansible) and can rebuild a server in 15 minutes from scratch. Managing a server entirely via the CLI might seem intimidating at first but it's really the way to go. Yes, even via mobile using JuiceSSH on Android or blink on iOS - see [remote access](../remote-access/index.md).

OpenMediaVault is just Linux underneath though which is a good thing. This means it runs docker, supports ZFS (via DKMS), SnapRAID and MergerFS too. 

*[PMS]: Perfect Media Server
*[webUI]: Web User Interface (GUI)