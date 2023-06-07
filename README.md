



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

Clone this project into your own instance of Attune.

<img src="https://www.servertribe.com/wp-content/uploads/2023/02/Attune-clone-new-project-01.png" alt="clone a new project"/>

---

Paste the GIT repository URL into Attune and Select Clone.

<img src="https://www.servertribe.com/wp-content/uploads/2023/02/Attune-clone-new-project-02.png" alt="clone a new project"/>

---

**Now that this project is in your Attune instance you can begin creating
Jobs.**

Navigate to the Plan workspace and create a Job from a Blueprint in the
Project you cloned.

<img src="https://www.servertribe.com/wp-content/uploads/2023/02/Attune-plan-new-job-11.png" alt="plan a new job"/>

---

Configure the Parameters for the Job you created. Create the Values you're
missing in the next step.

<img src="https://www.servertribe.com/wp-content/uploads/2023/02/Attune-plan-new-job-12.png" alt="plan a new job"/>

---

Create the Values required to fill the Parameters for the Job.

<img src="https://www.servertribe.com/wp-content/uploads/2023/02/Attune-plan-new-job-13-1.png" alt="plan a new job"/>

---

Run your Job.

<img src="https://www.servertribe.com/wp-content/uploads/2023/02/Attune-run-job-01.png" alt="run your job"/>

---

**Congratulations, you’ve run a cloned project.**

If you need further assistance, please explore our help.

<img width=200 src="https://www.servertribe.com/wp-content/uploads/2023/02/Attune-get-help-01.png" alt="get help"/>




## Blueprints

This Project contains the following Blueprints.



### Attune v4 Setup WinPE Support


### Attune v4 SWPE Install C wimlib


### Attune v4 SWPES Setup Samba


### Blueprints For Kickstart WinPE oVirt


### Deploy Win10 ISO For WinPE


### Deploy Win 2016 ISO For WinPE


### Deploy Win 2019 ISO For WinPE


### KS oVirt Boot WinPE Recreate Virtual Machine


### Setup Attune ovirt-imageio


### WinPE Kickstart Win10+oVirt


### WinPE Kickstart Win2016+oVirt


### WinPE Kickstart Win2019+oVirt





## Parameters


| Name | Type | Script Reference | Comment |
| ---- | ---- | ---------------- | ------- |
| Attune OS Build Server | Linux/Unix Node | `attuneosbuildserver` | This variable is used in the "Kickstart" build procedures, so the "Attune Server" can be used to build Attune servers. |
| Attune Server | Linux/Unix Node | `attuneserver` | None |
| Kickstart Organisation Name | Text | `kickstartorganisationname` | None |
| KS VMWare: Attune Base Dir | Text | `ksvmwareattunebasedir` | None |
| KS: Windows Interface Alias | Text | `kswindowsinterfacealias` | oVirt Deployments = "Ethernet"
ESXi Deployments = "Ethernet0"

This is the "InternetAlias" of the interface shown when you run "get-netipaddress" from powershell on the machine. |
| Linux: Attune User | Linux/Unix Credential | `linuxattuneuser` | None |
| Linux: Root User | Linux/Unix Credential | `linuxrootuser` | None |
| oVirt: Bios Type | Text | `ovirtbiostype` | Valid Values are (they must be in all capitals):
1. CLUSTER_DEFAULT - Use the cluster-wide default.
2. I440FX_SEA_BIOS - i440fx chipset with SeaBIOS.
3. Q35_OVMF - q35 chipset with OVMF (UEFI) BIOS.
4. Q35_SEA_BIOS - q35 chipset with SeaBIOS.
5. Q35_SECURE_BOOT- q35 chipset with OVMF (UEFI) BIOS with SecureBoot enabled.

https://ovirt.github.io/ovirt-engine-api-model/4.5/#types/bios_type |
| oVirt: Cluster Name | Text | `ovirtclustername` | None |
| oVirt: CPU Count | Text | `ovirtcpucount` | None |
| oVirt: Disk Interface | Text | `ovirtdiskinterface` | SATA or IDE required for Windows
VIRTIO_SCSI for windows after driver install
VIRTIO for Linux |
| oVirt: Disk Storage Name | Text | `ovirtdiskstoragename` | None |
| oVirt: Engine API User | Basic Credential | `ovirtengineapiuser` | None |
| oVirt: Engine Server | Basic Node | `ovirtengineserver` | None |
| oVirt: Memory Size | Text | `ovirtmemorysize` | None |
| oVirt: Network Name | Text | `ovirtnetworkname` | None |
| oVirt: NIC Interface | Text | `ovirtnicinterface` | E1000 for Windows
VIRTIO for Linux |
| oVirt: TimeZone | Text | `ovirttimezone` | None |
| Samba Windows Directory | Text | `sambawindowsdirectory` | The extracted Windows Directory on the Samba server that we want to run setup.exe from. |
| Target Server | Basic Node | `targetserver` | None |
| Target Server: Lin | Linux/Unix Node | `targetserverlin` | The target server is a generic placeholder, usually used for the server a script will run on.
For example, the server being built if the procedure is building a server. |
| Target Subnet | Network IPv4 Subnet | `targetsubnet` | None |
| Windows: Administrator | Windows Credential | `windowsadministrator` | The windows administrator user |
| WinPE Samba Server | Linux/Unix Node | `winpesambaserver` | None |




## Files


| Name | Type | Comment |
| ---- | ---- | ------- |
| oVirt Guest Drivers | Version Controlled Files | from c:\program files\virtio-win |
| WIN10 Enterprise ISO | Large Archives | None |
| WinPE 2019 ISO | Large Archives | None |
| WinPE ISO for Windows 10 oVirt | Large Archives | None |
| WinPE startnet.cmd | Version Controlled Files | None |
| WIN Raw Win2016 ISO | Large Archives | https://www.microsoft.com/en-us/evalcenter/download-windows-server-2016 |
| WIN Raw Win2019 ISO | Large Archives | None |
| WIN Win10 Unattended Config oVirt with Drivers | Version Controlled Files | None |
| WIN Win2019 Unattended Config with Drivers | Version Controlled Files | None |






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
