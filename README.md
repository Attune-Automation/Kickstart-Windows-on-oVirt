



[![Docs](https://img.shields.io/badge/docs-latest-brightgreen.svg)](http://doc.servertribe.com)
[![Discord](https://img.shields.io/discord/844971127703994369)](http://discord.servertribe.com)
[![Docs](https://img.shields.io/badge/videos-watch-brightgreen.svg)](https://www.youtube.com/@servertribe)
[![Generic badge](https://img.shields.io/badge/download-latest-brightgreen.svg)](https://www.servertribe.com/community-edition/)

# Kickstart WinPE oVirt






# Attune

[Attune](https://www.servertribe.com/)
automates and orchestrates processes to streamline deployments, scaling,
migrations, and management of your systems. The Attune platform is building a
community of sharable automated and orchestrated processes.

You can leverage the publicly available orchestrated blueprints to increase
your productivity, and accelerate the delivery of your projects. You can
open-source your own work and improve existing community orchestrated projects.

## Get Started with Attune, Download NOW!

The **Attune Community Edition** can be
[downloaded](https://www.servertribe.com/comunity-edition/)
for free from our
[ServerTribe website](https://www.servertribe.com/comunity-edition/).
You can learn more about Attune through
[ServerTribe's YouTube Channel](https://www.youtube.com/@servertribe).







# Clone this Project

To clone this project into your own instance of Attune, follow the
[Clone a GIT Project How To Instructions](https://servertribe-attune.readthedocs.io/en/latest/howto/design_workspace/clone_project.html).




## Blueprints

This Project contains the following Blueprints.



### Attune v4 Setup WinPE Support


### Attune v4 SWPE Install C wimlib


### Attune v4 SWPES Setup Samba


### Blueprints For Kickstart WinPE oVirt


### Check oVirt Drivers Installed - Group


### Deploy Win10 ISO For WinPE


### Deploy Win 2016 ISO For WinPE


### Deploy Win 2019 ISO For WinPE


### KS oVirt Boot WinPE Recreate Virtual Machine


### LIN WinPE Kickstart BIOS Win 2019+oVirt with wimmountrw


### LIN WinPE Kickstart UEFI Win 2019+oVirt with wimmountrw


### Setup Attune ovirt-imageio


### WinPE Kickstart Win10+oVirt


### WinPE Kickstart Win2016+oVirt


### WinPE Kickstart Win2019+oVirt





## Parameters


| Name | Type | Script Reference | Comment |
| ---- | ---- | ---------------- | ------- |
| Attune OS Build Server | Linux/Unix Node | `attuneosbuildserver` | This variable is used in the "Kickstart" build procedures, so the "Attune Server" can be used to build Attune servers. |
| Attune Server | Linux/Unix Node | `attuneserver` |  |
| Drivers Drop Directory | Text | `driversdropdirectory` | Put any extra drivers you want used by WinPE and the Windows installer here.<br><br>This can contain subfolders.<br><br>These are the "*.inf" files.<br><br>WinPE's startnet.cmd will recursively search for the "*.inf" files to install.<br><br>autounattend.xml will do the same.<br><br>This folder path relative to "{ksAttuneBaseDir}/build-{targetServer.fqn}".<br><br>Example: Setting this as "drop_in_drivers" will mean the drivers drop in directory will be at "{ksAttuneBaseDir}/build-{targetServer.fqn}/drop_in_drivers".<br><br>If "drop_in_drivers" exists, it's contents will be copied to "Drivers" folder.<br><br>If "drop_in_drivers" does not exist, it is ignored.<br><br>The contents of the Drivers folder will eventually seen at "X:\attune_drivers" by WinPE and the Windows installer. |
| Kickstarted Node | Basic Node | `kickstartednode` |  |
| Kickstarted Windows Node | Windows Node | `kickstartedwindowsnode` |  |
| Kickstart Organisation Name | Text | `kickstartorganisationname` |  |
| KS VMWare: Attune Base Dir | Text | `ksvmwareattunebasedir` |  |
| KS: Windows Interface Alias | Text | `kswindowsinterfacealias` | oVirt Deployments = "Ethernet"<br>ESXi Deployments = "Ethernet0"<br><br>This is the "InternetAlias" of the interface shown when you run "get-netipaddress" from powershell on the machine. |
| Linux: Attune User | Linux/Unix Credential | `linuxattuneuser` |  |
| Linux: Root User | Linux/Unix Credential | `linuxrootuser` |  |
| oVirt: Bios Type | Text | `ovirtbiostype` | Valid Values are (they must be in all capitals):<br>1. CLUSTER_DEFAULT - Use the cluster-wide default.<br>2. I440FX_SEA_BIOS - i440fx chipset with SeaBIOS.<br>3. Q35_OVMF - q35 chipset with OVMF (UEFI) BIOS.<br>4. Q35_SEA_BIOS - q35 chipset with SeaBIOS.<br>5. Q35_SECURE_BOOT- q35 chipset with OVMF (UEFI) BIOS with SecureBoot enabled.<br><br>https://ovirt.github.io/ovirt-engine-api-model/4.5/#types/bios_type |
| oVirt: Cluster Name | Text | `ovirtclustername` |  |
| oVirt: CPU Count | Text | `ovirtcpucount` |  |
| oVirt: Datacenter Name | Text | `ovirtdatacentername` |  |
| oVirt: Disk Interface | Text | `ovirtdiskinterface` | SATA or IDE required for Windows<br>VIRTIO_SCSI for windows after driver install<br>VIRTIO for Linux |
| oVirt: Disk Storage Name | Text | `ovirtdiskstoragename` |  |
| oVirt: Engine API User | Basic Credential | `ovirtengineapiuser` |  |
| oVirt: Engine Server | Basic Node | `ovirtengineserver` |  |
| oVirt: Memory Size | Text | `ovirtmemorysize` |  |
| oVirt: Network Name | Text | `ovirtnetworkname` |  |
| oVirt: NIC Interface | Text | `ovirtnicinterface` | E1000 for Windows<br>VIRTIO for Linux |
| oVirt: TimeZone | Text | `ovirttimezone` |  |
| Samba Windows Directory | Text | `sambawindowsdirectory` | The extracted Windows Directory on the Samba server that we want to run setup.exe from. |
| Target Server | Basic Node | `targetserver` |  |
| Target Server: Lin | Linux/Unix Node | `targetserverlin` | The target server is a generic placeholder, usually used for the server a script will run on.<br>For example, the server being built if the procedure is building a server. |
| Target Subnet | Network IPv4 Subnet | `targetsubnet` |  |
| Windows: Administrator | Windows Credential | `windowsadministrator` | The windows administrator user |
| WinPE Samba Server | Linux/Unix Node | `winpesambaserver` |  |




## Files

| Name | Type | Comment |
| ---- | ---- | ------- |
| oVirt Guest Drivers | Version Controlled Files | from c:\program files\virtio-win |
| WIN10 Enterprise ISO | Large Archives |  |
| WinPE 2019 ISO | Large Archives |  |
| WinPE ISO for Windows 10 oVirt | Large Archives |  |
| WinPE startnet.cmd | Version Controlled Files |  |
| WIN Raw Win2016 ISO | Large Archives | https://www.microsoft.com/en-us/evalcenter/download-windows-server-2016 |
| WIN Raw Win2019 ISO | Large Archives |  |
| WIN Win10 Unattended Config oVirt with Drivers | Version Controlled Files |  |
| WIN Win2019 Unattended Config with Drivers | Version Controlled Files |  |






# Contribute to this Project

**The collective power of a community of talented individuals working in
concert delivers not only more ideas, but quicker development and
troubleshooting when issues arise.**

If you’d like to contribute and help improve these projects, please fork our
repository, commit your changes in Attune, push you changes, and create a
pull request.

<img src="https://www.servertribe.com/wp-content/uploads/2023/02/Attune-pull-request-01.png" alt="pull request"/>

---

Please feel free to raise any issues or questions you have.

<img src="https://www.servertribe.com/wp-content/uploads/2023/02/Attune-get-help-02.png" alt="create an issue"/>


---

**Thank you**
