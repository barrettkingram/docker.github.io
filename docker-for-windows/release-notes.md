---
description: Change log / release notes per stable release
keywords: Docker Desktop for Windows, stable, release notes
redirect_from:
- /winkit/release-notes/
title: Docker Desktop for Windows Stable Release notes
toc_min: 1
toc_max: 2
---

Here are the main improvements and issues per stable release, starting with the
current release. The documentation is always updated for each release.

For system requirements, see
[What to know before you install](install.md#what-to-know-before-you-install).

Release notes for _stable_ releases are listed below, [_edge_ release
notes](edge-release-notes) are also available. (Following the Docker Engine - Community release model,
'beta' releases are called 'edge' releases.)  You can learn about both kinds of
releases, and download stable and edge product installers at [Download Docker
for Windows](install.md#download-docker-for-windows).

## Stable Releases of 2019

## Docker Desktop Community 2.1.0.4
2019-10-21

> [Download](https://hub.docker.com/?overlay=onboarding)
>
> You must sign in to Docker Hub to download Docker Desktop.

Docker Desktop 2.1.0.4 contains a Kubernetes upgrade. Note that your local Kubernetes cluster will be reset after installing this version.

### Upgrades

- [Docker 19.03.4](https://github.com/docker/docker-ce/releases/tag/v19.03.4)
- [Kubernetes 1.14.7](https://github.com/kubernetes/kubernetes/releases/tag/v1.14.7)
- [Go 1.12.10](https://github.com/golang/go/issues?q=milestone%3AGo1.12.10+label%3ACherryPickApproved)
- [Kitematic 0.17.9](https://github.com/docker/kitematic/releases/tag/v0.17.9)

### New

Docker Desktop now enables you to sign into Docker Hub using two-factor authentication. For more information, see [Two-factor authentication](index/#docker-hub).

## Docker Desktop Community 2.1.0.3
2019-09-16

[Download](https://download.docker.com/win/stable/38240/Docker%20Desktop%20Installer.exe)

### Upgrades

- [Kitematic 0.17.8](https://github.com/docker/kitematic/releases/tag/v0.17.8)

## Docker Desktop Community 2.1.0.2
2019-09-04

[Download](https://download.docker.com/win/stable/37877/Docker%20Desktop%20Installer.exe)

Docker Desktop 2.1.0.2 contains a Kubernetes upgrade. Your local Kubernetes cluster will be reset after installing this version.

### Upgrades

- [Docker 19.03.2](https://github.com/docker/docker-ce/releases/tag/v19.03.2)
- [Kubernetes 1.14.6](https://github.com/kubernetes/kubernetes/releases/tag/v1.14.6)
- [Go 1.12.9](https://github.com/golang/go/issues?q=milestone%3AGo1.12.9+label%3ACherryPickApproved)
- [Docker Machine 0.16.2](https://github.com/docker/machine/releases/tag/v0.16.2)

## Docker Desktop Community 2.1.0.1
2019-08-08

[Download](https://download.docker.com/win/stable/37199/Docker%20Desktop%20Installer.exe)

  Note that you must sign in and create a Docker ID in order to download Docker Desktop.

### Upgrades

* [Docker 19.03.1](https://github.com/docker/docker-ce/releases/tag/v19.03.1)
* [Docker Compose 1.24.1](https://github.com/docker/compose/releases/tag/1.24.1)
* [Kubernetes 1.14.3](https://github.com/kubernetes/kubernetes/releases/tag/v1.14.3)
* [Compose on Kubernetes 0.4.23](https://github.com/docker/compose-on-kubernetes/releases/tag/v0.4.23)
* [Docker Machine 0.16.1](https://github.com/docker/machine/releases/tag/v0.16.1)
* [linuxkit v0.7](https://github.com/linuxkit/linuxkit/releases/tag/v0.7)
* Linux Kernel 4.9.184
* [Kitematic 0.17.6](https://github.com/docker/kitematic/releases/tag/v0.17.6)
* [Qemu 4.0.0](https://github.com/docker/binfmt) for cross compiling for ARM
* [Alpine 3.10](https://alpinelinux.org/posts/Alpine-3.10.0-released.html)
* [Docker Credential Helpers 0.6.3](https://github.com/docker/docker-credential-helpers/releases/tag/v0.6.3)

### New

* Selecting the ‘Experimental features’ checkbox in the Daemon, **Settings** menu turns on experimental features for Docker daemon and Docker CLI.
* Docker Desktop now checks for stored credentials at startup before attempting to mount any shared drives. This prompts users to reenter the credentials if they are invalid.

### Experimental

> Experimental features provide early access to future product functionality. These features are intended for testing and feedback only as they may change between releases without warning or can be removed entirely from a future release. Experimental features must not be used in production environments. Docker does not offer support for experimental features.

Docker Desktop Community 2.1.0.0 contains the following experimental features:

* Docker App: Docker App is a CLI plugin that helps configure, share, and install applications. For more information, see [Working with Docker App](/app/working-with-app/).
* Docker Buildx: Docker Buildx is a CLI plugin for extended build capabilities with BuildKit. For more information, see [Working with Docker Buildx](/buildx/working-with-buildx/).

### Bug fixes and minor changes

* Fixed PowerShell script signing issue that caused `AuthorizationManager check failed` errors on machines with strict group policies on PowerShell script signing. [docker/for-win#4376](https://github.com/docker/for-win/issues/4376)
* Fixed an issue where users were unable to start Docker Desktop after upgrading to version 2.1.0.0. [docker/for-win#4390](https://github.com/docker/for-win/issues/4390)
* Fixed an issue where attempts to upgrade Docker Desktop to version 2.1.0.0 sometimes failed with the error `value cannot be null`. [docker/for-win#4343](https://github.com/docker/for-win/issues/4343)
* Fixed an issue that caused the installer to hang when upgrading Docker Desktop to version 2.1.0.0. [docker/for-win#4387](https://github.com/docker/for-win/issues/4387)
* Improved the error messages displayed during VM lifecycle operations. [docker/for-win#4348](https://github.com/docker/for-win/issues/4348)
* Docker Desktop now supports a configurable user timeout for VMs on slower machines. [docker/for-win#4393](https://github.com/docker/for-win/issues/4393)
* Restricted the `cluster-admin` role on local Kubernetes cluster to `kube-system` namespace.
* Reduced the VM startup time. swap is not created every time a virtual machine boots.
* Fixed a bug which caused Windows to crash when a user cancels switching the version using Windows User Account Control (UAC) settings.
* Fixed an issue where Docker Desktop restarts when a user logs out of Windows and logs back in, which results in retaining the exported ports on containers.
* Fixed Kubernetes installation with VPNkit subnet.
* Fixed a bug where the process output was not redirected to stdout when gathering diagnostics on Windows, which sometimes resulted in a crash.
* Fixed race condition where Kubernetes sometimes fails to start after the app is restarted.
* The system tray icon now opens the Docker Desktop menu with left and right mouse button.
* When displaying the crash report window, Docker Desktop does not send a bugsnag crash report unless the user needs the report to upload diagnostics.
* Docker Desktop has removed the ability to log in using email address as a username as the Docker command line does not support this.
* For Linux containers on Windows (LCOW), the host must run Windows 10 Professional or Windows 10 Enterprise version 1809 or later.
* The **Send usage statistics** checkbox is selected by default in Docker Desktop for Windows Community. This option cannot be modified.
* Docker Desktop has added a new dialog box during startup which allows users to retry mounting a shared drive or remove it from the shared drives list after a failed attempt.
* Fixed the Kubernetes Delete operation of persistent volume claims on Windows.
* Docker Desktop now truncates UDP DNS responses which are over 512 bytes in size.
* Fixed a bug where Docker was not added to PATH after installation in some cases.
* Fixed port 8080 that was used on localhost when starting Kubernetes.
* Renamed the product from **Docker for Windows** to **Docker Desktop**.
* Fixed the **Create issue** link in the Diagnostics window.
* Fixed a bug related to service log collection in diagnostics.
* Docker Desktop now gathers `/etc/hosts` to help with diagnostics.
* Added the missing daemon options in Docker Engine 18.09.
* When two services have a common exposed port, Docker Desktop exposes the available ports for the second service.
* Fixed the UI lock when changing the Kubernetes state.

### Docker Community Edition 2.0.0.3 2019-02-15

[Download](https://download.docker.com/win/stable/31259/Docker%20for%20Windows%20Installer.exe)

* Upgrades
  - [Docker 18.09.2](https://github.com/docker/docker-ce/releases/tag/v18.09.2), fixes [CVE-2019-5736](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2019-5736)

* Bug fix
  - Fix crash in system tray menu when the Hub login fails or Air gap mode

### Docker Community Edition 2.0.0.2 2019-01-16

[Download](https://download.docker.com/win/stable/30215/Docker%20for%20Windows%20Installer.exe)

* Upgrades
  - [Docker 18.09.1](https://github.com/docker/docker-ce/releases/tag/v18.09.1)
  - [Docker Machine 0.16.1](https://github.com/docker/machine/releases/tag/v0.16.1)
  - [Kubernetes 1.10.11](https://github.com/kubernetes/kubernetes/blob/master/CHANGELOG-1.10.md#v11011), fixes [CVE-2018-1002105](https://github.com/kubernetes/kubernetes/issues/71411)
  - [Kitematic 0.17.6](https://github.com/docker/kitematic/releases/tag/v0.17.6)
  - Golang 1.10.6, fixes CVEs: [CVE-2018-16875](https://www.cvedetails.com/cve/CVE-2018-16875), [CVE-2018-16873](https://www.cvedetails.com/cve/CVE-2018-16873) and [CVE-2018-16874](https://www.cvedetails.com/cve/CVE-2018-16874)
  - Windows 14393 is marked as deprecated ; it will not be supported anymore in the next major stable release (2.1.0.0 and further)

* Bug fixes and minor changes
  - Rename Docker for Windows to Docker Desktop
  - Add 18.09 missing daemon options

## Stable Releases of 2018

### Docker Community Edition 2.0.0.0-win81 2018-12-07

[Download](https://download.docker.com/win/stable/29211/Docker%20for%20Windows%20Installer.exe)

* Upgrades
  - [Docker compose 1.23.2](https://github.com/docker/compose/releases/tag/1.23.2)

* Bug fixes and minor changes
  - Compose: Fixed a bug where build context URLs would fail to build on Windows. Fixes [docker/for-win#2918](https://github.com/docker/for-win/issues/2918)

### Docker Community Edition 2.0.0.0-win78 2018-11-19

[Download](https://download.docker.com/win/stable/28905/Docker%20for%20Windows%20Installer.exe)

* Upgrades
  - [Docker 18.09.0](https://github.com/docker/docker-ce-packaging/releases/tag/v18.09.0)
  - [Docker compose 1.23.1](https://github.com/docker/compose/releases/tag/1.23.1)
  - [Docker Machine 0.16.0](https://github.com/docker/machine/releases/tag/v0.16.0)
  - [Kitematic 0.17.5](https://github.com/docker/kitematic/releases/tag/v0.17.5)
  - Linux Kernel 4.9.125

* New
  - New version scheme

* Deprecation
  - Removed support of AUFS

* Bug fixes and minor changes
  - Windows Containers: Fix group daemon option settings. Fixes [docker/for-win#2647](https://github.com/docker/for-win/issues/2647)
  - Windows Containers: Better host.docker.internal resolution, don't rewrite it if not modified. From [docker/for-win#1976](https://github.com/docker/for-win/issues/1976)
  - Do not try to update samba share mounts when using Windows Containers
  - Improved dns update too verbose in logs
  - VPNKit: Improved scalability of port forwarding.
  - VPNKit: Limit the size of the UDP NAT table. This ensures port forwarding and regular TCP traffic continue even when running very chatty UDP protocols.
  - LCOW does not need --platform flag on multi-arch images any more
  - Disk size can now be ajusted from 32GiB to drive space.
  - Fix dns update too verbose in logs
  - Fix panic in diagnose

### Docker Community Edition 18.06.1-ce-win73 2018-08-29

[Download](https://download.docker.com/win/stable/19507/Docker%20for%20Windows%20Installer.exe)

* Upgrades
  - [Docker 18.06.1-ce](https://github.com/docker/docker-ce/releases/tag/v18.06.1-ce)

* Bug fixes and minor changes
  - Fix bug in VM activity detection, preventing Docker Desktop from starting. Fixes [docker/for-win#2404](https://github.com/docker/for-win/issues/2404)
  - Fix bug in detection when Windows service is not running, and propose to restart the service.
  - Fix local DNS failing to resolve inside containers. Fixes [docker/for-win#2301](https://github.com/docker/for-win/issues/2301), [docker/for-win#2304](https://github.com/docker/for-win/issues/2304)
  - Fix Kubernetes status display after reset to factory default
  - Fix bug where `host.docker.internal` is not resolved in some cases. Fixes [docker/for-win#2402](https://github.com/docker/for-win/issues/2402)
  - Use a 1MB vhdx blocksize instead of the default 32MB. See [docker/for-win#244](https://github.com/docker/for-win/issues/244). Also see [Microsoft Best Practices for running Linux on Hyper-V](https://docs.microsoft.com/en-us/windows-server/virtualization/hyper-v/best-practices-for-running-linux-on-hyper-v)
  - Fix diagnostics in specific cases when the Windows service is not started.
  - Changed the samba default file permission to avoid an issue with too open rights. Fixes [docker/for-win#2170](https://github.com/docker/for-win/issues/2170)
  - On RS5 insider, fixed wrong detection of missing feature "Containers" requiring you to install the feature and then reboot.

### Docker Community Edition 18.06.0-ce-win72 2018-07-26

[Download](https://download.docker.com/win/stable/19098/Docker%20for%20Windows%20Installer.exe)

* New
  - Renewed signing certificate. The installer may show a Windows Defender popup until the renewed certificate is whitelisted. Click "More info" to view the app is published by "Docker Inc" and run it.

* Bug fixes and minor changes
  - Fix bug in automatic feature enabling if "Hyper-V" and "Containers" Windows features are not enabled already when starting Docker Desktop.

### Docker Community Edition 18.06.0-ce-win70 2018-07-25

[Download](https://download.docker.com/win/stable/19075/Docker%20for%20Windows%20Installer.exe)

* Upgrades
  - [Docker 18.06.0-ce](https://github.com/docker/docker-ce/releases/tag/v18.06.0-ce)
  - [Docker Machine 0.15.0](https://github.com/docker/machine/releases/tag/v0.15.0)
  - [Docker compose 1.22.0](https://github.com/docker/compose/releases/tag/1.22.0)
  - [LinuxKit v0.4](https://github.com/linuxkit/linuxkit/releases/tag/v0.4)
  - Linux Kernel 4.9.93 with CEPH, DRBD, RBD, MPLS_ROUTING and MPLS_IPTUNNEL enabled

* New
  - Kubernetes Support. You can now run a single-node Kubernetes cluster from the "Kubernetes" Pane in Docker for Windows settings and use kubectl commands as well as Docker commands. See https://docs.docker.com/docker-for-windows/kubernetes/

* Bug fixes and minor changes
  - AUFS storage driver is deprecated in Docker Desktop and AUFS support will be removed in the next major release. You can continue with AUFS in Docker Desktop 18.06.x, but you will need to reset the disk image (in Settings > Reset menu) before updating to the next major update. You can check documentation to [save images](https://docs.docker.com/engine/reference/commandline/save/#examples) and [backup volumes](https://docs.docker.com/storage/volumes/#backup-restore-or-migrate-data-volumes)
  - Fix bug which would in some cases cause virtual machine logs to be written to RAM rather than disk, and the virtual machine to hang.
  - Fix security issue with named pipe connection to docker service.
  - Fix VPNKit memory leak. Fixes [docker/for-win#2087](https://github.com/docker/for-win/issues/2087), [moby/vpnkit#371](https://github.com/moby/vpnkit/issues/371)
  - Fix restart issue when using Windows fast startup on latest 1709 Windows updates. Fixes [docker/for-win#1741](https://github.com/docker/for-win/issues/1741), [docker/for-win#1741](https://github.com/docker/for-win/issues/1741)
  - DNS name `host.docker.internal` can be used for host resolution from Windows Containers.  Fixes [docker/for-win#1976](https://github.com/docker/for-win/issues/1976)
  - Fix broken link in diagnostics window.
  - Added log rotation for docker-ce logs inside the virtual machine.
  - Changed smb permission to avoid issue when trying to manipulate files with different users in containers. Fixes [docker/for-win#2170](https://github.com/docker/for-win/issues/2170)

### Docker Community Edition 18.03.1-ce-win65 2018-04-30

[Download](https://download.docker.com/win/stable/17513/Docker%20for%20Windows%20Installer.exe)

* Upgrades
  - [Docker 18.03.1-ce](https://github.com/docker/docker-ce/releases/tag/v18.03.1-ce)
  - [Docker compose 1.21.1](https://github.com/docker/compose/releases/tag/1.21.1)
  - [Notary 0.6.1](https://github.com/docker/notary/releases/tag/v0.6.1)

* Bug fixes and minor changes
  - Fix startup failure when the HOME environment variable is already defined (typically started from the command line). Fixes [docker/for-win#1880](https://github.com/docker/for-win/issues/1880)
  - Fix startup failure due to incompatibility with other programs (like Razer Synapse 3). Fixes [docker/for-win#1723](https://github.com/docker/for-win/issues/1723)

### Docker Community Edition 18.03.1-ce-win64 2018-04-26

[Download](https://download.docker.com/win/stable/17438/Docker%20for%20Windows%20Installer.exe)

* Upgrades
  - [Docker 18.03.1-ce](https://github.com/docker/docker-ce/releases/tag/v18.03.1-ce)
  - [Docker compose 1.21.0](https://github.com/docker/compose/releases/tag/1.21.0)
  - [Notary 0.6.1](https://github.com/docker/notary/releases/tag/v0.6.1)

* Bug fixes and minor changes
  - Fix startup failure when the HOME environment variable is already defined (typically started from the command line). Fixes [docker/for-win#1880](https://github.com/docker/for-win/issues/1880)
  - Fix startup failure due to incompatibility with other programs (like Razer Synapse 3). Fixes [docker/for-win#1723](https://github.com/docker/for-win/issues/1723)

### Docker Community Edition 18.03.0-ce-win59 2018-03-26

[Download](https://download.docker.com/win/stable/16762/Docker%20for%20Windows%20Installer.exe)

* Upgrades
  - [Docker 18.03.0-ce](https://github.com/docker/docker-ce/releases/tag/v18.03.0-ce)
  - [Docker Machine 0.14.0](https://github.com/docker/machine/releases/tag/v0.14.0)
  - [Docker compose 1.20.1](https://github.com/docker/compose/releases/tag/1.20.1)
  - [Notary 0.6.0](https://github.com/docker/notary/releases/tag/v0.6.0)
  - Linux Kernel 4.9.87
  - AUFS 20180312

* New
  - Virtual machine disk size can be changed in settings. Fixes [docker/for-win#105](https://github.com/docker/for-win/issues/105)
  - Virtual machine swap size can be changed in settings.
  - New menu item to restart Docker.
  - Support NFS Volume sharing. See [docker/for-win#1700](https://github.com/docker/for-win/issues/1700)
  - Allow to activate Windows Containers during installation (avoid virtual machine disk creation and virtual machine boot when working only on Windows containers). See [docker/for-win#217](https://github.com/docker/for-win/issues/217).
  - Experimental feature: LCOW containers can now be run next to Windows containers (on Windows RS3 build 16299 and later). Use `--platform=linux` in Windows container mode to run Linux Containers On Windows. Note that LCOW is experimental; it requires the daemon `experimental` option.

* Bug fixes and minor changes
  - Fix Windows Containers port forwarding on Windows 10 build 16299 post KB4074588. Fixes [docker/for-win#1707](https://github.com/docker/for-win/issues/1707), [docker/for-win#1737](https://github.com/docker/for-win/issues/1737)
  - Fix daemon not starting properly when setting TLS-related options.
  - DNS name `host.docker.internal` shoud be used for host resolution from containers. Older aliases (still valid) are deprecated in favor of this one. (See https://tools.ietf.org/html/draft-west-let-localhost-be-localhost-06).
  - Fix for the HTTP/S transparent proxy when using "localhost" names (for example, `host.docker.internal`). Fixes [docker/for-win#1130](https://github.com/docker/for-win/issues/1130)
  - Fix Linuxkit start on Windows RS4 Insider. Fixes [docker/for-win#1458](https://github.com/docker/for-win/issues/1458), [docker/for-win#1514](https://github.com/docker/for-win/issues/1514), [docker/for-win#1640](https://github.com/docker/for-win/issues/1640)
  - Fix risk of privilege escalation. (https://www.tenable.com/sc-report-templates/microsoft-windows-unquoted-service-path-vulnerability)
  - All users present in the docker-users group are now able to use Docker. Fixes [docker/for-win#1732](https://github.com/docker/for-win/issues/1732)
  - Migration of Docker Toolbox images is not proposed in Docker For Windows installer (still possible to [migrate Toolbox images manually](https://docs.docker.com/docker-for-windows/docker-toolbox/) ).
  - Better cleanup for Windows containers and images on reset/uninstall. Fixes [docker/for-win#1580](https://github.com/docker/for-win/issues/1580), [docker/for-win#1544](https://github.com/docker/for-win/issues/1544), [docker/for-win#191](https://github.com/docker/for-win/issues/191)
  - Desktop icon creation is optional in installer; do not recreate Desktop icon on upgrade (effective on next upgrade). Fixes [docker/for-win#246](https://github.com/docker/for-win/issues/246), [docker/for-win#925](https://github.com/docker/for-win/issues/925), [docker/for-win#1551](https://github.com/docker/for-win/issues/1551)

### Docker Community Edition 17.12.0-ce-win47 2018-01-12

[Download](https://download.docker.com/win/stable/15139/Docker%20for%20Windows%20Installer.exe)

* Bug fixes and minor changes
  - Fix linuxkit port-forwarder sometimes not being able to start. Fixes [docker/for-win#1506](https://github.com/docker/for-win/issues/1506)
  - Fix certificate management when connecting to a private registry. Fixes [docker/for-win#1512](https://github.com/docker/for-win/issues/1512)
  - Fix Mount compatibility when mounting drives with `-v //c/...`, now mounted in /host_mnt/c in the linuxkit virtual machine. Fixes [docker/for-win#1509](https://github.com/docker/for-win/issues/1509), [docker/for-win#1516](https://github.com/docker/for-win/issues/1516), [docker/for-win#1497](https://github.com/docker/for-win/issues/1497)
  - Fix icon displaying edge. Fixes [docker/for-win#1508](https://github.com/docker/for-win/issues/1508)

### Docker Community Edition 17.12.0-ce-win46 2018-01-09

[Download](https://download.docker.com/win/stable/15048/Docker%20for%20Windows%20Installer.exe)

* Upgrades
  - [Docker 17.12.0-ce](https://github.com/docker/docker-ce/releases/tag/v17.12.0-ce)
  - [Docker compose 1.18.0](https://github.com/docker/compose/releases/tag/1.18.0)
  - [Docker Machine 0.13.0](https://github.com/docker/machine/releases/tag/v0.13.0)
  - Linux Kernel 4.9.60

* New
  - Virtual machine entirely built with linuxkit
  - Add localhost port forwarder for Windows (thanks @simonferquel). Use Microsoft localhost port forwarder when it is available (insider build RS4).

* Bug fixes and minor changes
  - Display various component versions in About box.
  - Fix vpnkit issue when username has spaces. See [docker/for-win#1429](https://github.com/docker/for-win/issues/1429)
  - Diagnostic improvements to get VM logs before VM shutdown.
  - Fix installer check for not supported Windows `CoreCountrySpecific` Edition.
  - Fix a class of startup failures where the database fails to start. See [docker/for-win#498](https://github.com/docker/for-win/issues/498)
  - Links in update changelog now open the default browser instead of IE. (fixes [docker/for-win#1311](https://github.com/docker/for-win/issues/1311))

## Stable Releases of 2017

### Docker Community Edition 17.09.1-ce-win42 2017-12-11

[Download](https://download.docker.com/win/stable/14687/Docker%20for%20Windows%20Installer.exe)

* Upgrades
  - [Docker 17.09.1-ce](https://github.com/docker/docker-ce/releases/tag/v17.09.1-ce)
  - [Docker compose 1.17.1](https://github.com/docker/compose/releases/tag/1.17.1)
  - [Docker Machine 0.13.0](https://github.com/docker/machine/releases/tag/v0.13.0)

* Bug fixes and minor changes
  - Fix bug during Windows fast-startup process. Fixes [for-win/#953](https://github.com/docker/for-win/issues/953)
  - Fix uninstaller issue (in some specific cases dockerd process was not killed properly)
  - Fix Net Promoter Score Gui bug. Fixes [for-win/#1277](https://github.com/docker/for-win/issues/1277)
  - Fix `docker.for.win.localhost` not working in proxy settings. Fixes [for-win/#1130](https://github.com/docker/for-win/issues/1130)
  - Increased timeout for virtual machine boot startup to 2 minutes.


### Docker Community Edition 17.09.0-ce-win33 2017-10-06

[Download](https://download.docker.com/win/stable/13620/Docker%20for%20Windows%20Installer.exe)

* Bug fixes
  - Fix Docker For Windows unable to start in some cases: removed use of libgmp sometimes causing the vpnkit process to die.

### Docker Community Edition 17.09.0-ce-win32 2017-10-02

[Download](https://download.docker.com/win/stable/13529/Docker%20for%20Windows%20Installer.exe)

* Upgrades
  - [Docker 17.09.0-ce](https://github.com/docker/docker-ce/releases/tag/v17.09.0-ce)
  - [Docker Compose 1.16.1](https://github.com/docker/compose/releases/tag/1.16.1)
  - [Docker Machine 0.12.2](https://github.com/docker/machine/releases/tag/v0.12.2)
  - [Docker Credential Helpers 0.6.0](https://github.com/docker/docker-credential-helpers/releases/tag/v0.6.0)
  - Linux Kernel 4.9.49
  - AUFS 20170911

* New
  - Windows Docker daemon is now started as service for better lifecycle management
  - Store Linux daemon configuration in ~\.docker\daemon.json instead of settings file
  - Store Windows daemon configuration in C:\ProgramData\Docker\config\daemon.json instead of settings file
  - VPNKit: add support for ping!
  - VPNKit: add slirp/port-max-idle-timeout to allow the timeout to be adjusted or even disabled
  - VPNKit: bridge mode is default everywhere now
  - Add `Skip This Version` button in update window

* Security fixes
  - VPNKit: security fix to reduce the risk of DNS cache poisoning attack (reported by Hannes Mehnert https://hannes.nqsb.io/)

* Bug fixes and minor changes
  - Kernel: Enable TASK_XACCT and TASK_IO_ACCOUNTING
  - Rotate logs in the virtual machine more often (docker/for-win#244)
  - Reset to default stops all engines and removes settings including all daemon.json files
  - Better backend service checks (related to https://github.com/docker/for-win/issues/953)
  - Fix auto updates checkbox, no need to restart the application
  - Fix check for updates menu when auto updates was disable
  - VPNKit: do not block startup when ICMP permission is denied. (Fixes docker/for-win#1036, docker/for-win#1035, docker/for-win#1040)
  - VPNKit: change protocol to support error messages reported back from the server
  - VPNKit: fix a bug which causes a socket to leak if the corresponding TCP connection is idle
    for more than 5 minutes (related to [docker/for-mac#1374](https://github.com/docker/for-mac/issues/1374))
  - VPNKit: improve the logging around the UNIX domain socket connections
  - VPNKit: automatically trim whitespace from int or bool database keys
  - Do not move credentials into the credential store at startup

### Docker Community Edition 17.06.2-ce-win27 2017-09-06

[Download](https://download.docker.com/win/stable/13194/Docker%20for%20Windows%20Installer.exe)

* Upgrades
  - [Docker 17.06.2-ce](https://github.com/docker/docker-ce/releases/tag/v17.06.2-ce)
  - [Docker Machine 0.12.2](https://github.com/docker/machine/releases/tag/v0.12.2)

### Docker Community Edition 17.06.1-ce-rc1-win24 2017-08-24

[Download](https://download.docker.com/win/stable/13025/Docker%20for%20Windows%20Installer.exe)

**Upgrades**

- [Docker 17.06.1-ce-rc1](https://github.com/docker/docker-ce/releases/tag/v17.06.1-ce-rc1)
- Linux Kernel 4.9.36
- AUFS 20170703

**Bug fixes and minor**

- Fix locked container id file (Fixes [docker/for-win#818](https://github.com/docker/for-win/issues/818))
- Avoid expanding variables in PATH env variable (Fixes [docker/for-win#859](https://github.com/docker/for-win/issues/859))

### Docker Community Edition 17.06.0-ce-win18 2017-06-28

[Download](https://download.docker.com/win/stable/12627/Docker%20for%20Windows%20Installer.exe)

**Upgrades**

- [Docker 17.06.0-ce](https://github.com/docker/docker-ce/releases/tag/v17.06.0-ce)
- [Docker Credential Helpers 0.5.2](https://github.com/docker/docker-credential-helpers/releases/tag/v0.5.2)
- [Docker Machine 0.12.0](https://github.com/docker/machine/releases/tag/v0.12.0)
- [Docker compose 1.14.0](https://github.com/docker/compose/releases/tag/1.14.0)
- Linux Kernel 4.9.31

**New**

- Windows Server 2016 support
- Windows 10586 is marked as deprecated; it is not supported going forward in stable releases
- Integration with Docker Cloud, with the ability to control remote Swarms from the local command line interface (CLI) and view your repositories
- Unified login between the Docker CLI and Docker Hub, Docker Cloud.
- Sharing a drive can be done on demand, the first time a mount is requested
- Add an experimental DNS name for the host: docker.for.win.localhost
- Support for client (i.e. "login") certificates for authenticating registry access (fixes [docker/for-win#569](https://github.com/docker/for-win/issues/569))
- New installer experience

**Bug fixes and minor changes**

- Fixed group access check for users logged in with Active Directory (fixes [docker/for-win#785](https://github.com/docker/for-win/issues/785))
- Checked environment variables and add some warnings in logs if they can cause docker to fail
- Many processes that were running in admin mode now run within the user identity
- Cloud federation command lines now open in the user home directory
- Named pipes are now created with more constrained security descriptors to improve security
- Security fix: Users must be part of the specific group "docker-users" to run Docker for Windows
- Reset to default / uninstall also reset Docker cli settings and logout user from Docker Cloud and registries
- Detected a bitlocker policy preventing windows containers to work
- Fixed an issue on filesharing when explicitly disabled on vmswitch interface
- Fixed virtual machine not starting when the machine had a very long name
- Fixed a bug where Windows daemon.json file was not written (fixes [docker/for-win#670](https://github.com/docker/for-win/issues/670))
- Added patches to the kernel to fix VMBus crash
- Named pipe client connection should not trigger dead locks on `docker run` with data in stdin any more
- Buffered data should be treated correctly when docker client requests are upgraded to raw streams

### Docker Community Edition 17.03.1-ce-win12  2017-05-12

[Download](https://download.docker.com/win/stable/12058/Docker%20for%20Windows%20Installer.exe)

**Upgrades**

- Security fix for CVE-2017-7308

### Docker Community Edition 17.03.0, 2017-03-02

[Download](https://download.docker.com/win/stable/10743/Docker%20for%20Windows%20Installer.exe)

**New**

- Renamed to Docker Community Edition
- Integration with Docker Cloud: control remote Swarms from the local CLI and view your repositories. This feature is going to be rolled out to all users
progressively

**Upgrades**

- [Docker 17.03.0-ce](https://github.com/docker/docker/releases/tag/v17.03.0-ce)
- [Docker Compose 1.11.2](https://github.com/docker/compose/releases/tag/1.11.2)
- [Docker Machine 0.10.0](https://github.com/docker/machine/releases/tag/v0.10.0)
- Linux kernel 4.9.12

**Bug fixes and minor changes**

- Matched Hyper-V Integration Services by ID, not name
- Don't consume 100% CPU when the service is stopped
- Log the diagnostic id when uploading
- Improved firewall handling: stop listing the rules since it can take a lot of time
- Don't rollback to the previous engine when the desired engine fails to start
- Don't use port 4222 inside the Linux virtual machine
- Fixed startup error of ObjectNotFound in Set-VMFirmware
- Added detailed logs when firewall is configured
- Added a link to the Experimental Features documentation
- Fixed the copyright in the About dialog
- VPNKit: fix unmarshalling of DNS packets containing pointers to pointers to labels
- VPNKit: set the Recursion Available bit on DNS responses from the cache
- VPNKit: Avoid diagnostics to capture too much data
- VPNKit: fix a source of occasional packet loss (truncation) on the virtual ethernet link
- Fixed negotiation of TimeSync protocol version (through kernel update)

### Docker for Windows 1.13.1, 2017-02-09

[Download](https://download.docker.com/win/stable/1.13.1.10072/InstallDocker.msi)

**Upgrades**

- [Docker 1.13.1](https://github.com/docker/docker/releases/tag/v1.13.1)
- [Docker Compose 1.11.1](https://github.com/docker/compose/releases/tag/1.11.1)
- Linux kernel 4.9.8

**Bug fixes and minor changes**

- Add link to experimental features
- New 1.13 cancellable operations should now be properly handled by the Docker for desktop
- Various typos fixes
- Fix in Hyper-V VM setup (should fix `ObjectNotFound` errors)

### Docker for Windows 1.13.0, 2017-01-19

[Download](https://download.docker.com/win/stable/1.13.0.9795/InstallDocker.msi)

**Upgrades**

- [Docker 1.13.0](https://github.com/docker/docker/releases/tag/v1.13.0)
- [Docker Compose 1.10](https://github.com/docker/compose/releases/tag/1.10.0)
- [Docker Machine 0.9.0](https://github.com/docker/machine/releases/tag/v0.9.0)
- [Notary 0.4.3](https://github.com/docker/notary/releases/tag/v0.4.3)
- Linux kernel 4.9.4

**New**

- Windows containers
- Improved UI for Daemon.json editing
- VHDX file containing images and non-host mounted volumes can be moved
  (using "advanced" tab in the UI)
- Support for arm, aarch64, ppc64le architectures using qemu
- TRIM support for disk (shrinks virtual disk)
- Virtual machine's time synchronization is forced after the host wakes from sleep mode
- Docker Experimental mode can be toggled

**Bug fixes and minor changes**

- Improved Proxy UI
- Improvements to Logging and Diagnostics
- About Box is now copy/paste enabled
- Improvements in drive sharing code
- Optimized boot process
- Trend Micro Office Scan made the API proxy think no drive was shared
- Show a link to the virtualization documentation
- Always remove the disk on factory reset
- VPNKit: Improved diagnostics
- VPNKit: Forwarded UDP datagrams have correct source port numbers
- VPNKit: If one request fails, allow other concurrent requests to succeed.
  For example this allows IPv4 servers to work even if IPv6 is broken.
- VPNKit: Fix bug which could cause the connection tracking to
  underestimate the number of active connections
- VPNKit: add a local cache of DNS responses

## Stable Releases of 2016

### Docker for Windows 1.12.5, 2016-12-20

[Download](https://download.docker.com/win/stable/1.12.5.9503/InstallDocker.msi)

**Upgrades**

- Docker 1.12.5
- Docker Compose 1.9.0

### Skipped Docker for Windows 1.12.4

We did not distribute a 1.12.4 stable release

### Docker for Windows 1.12.3, 2016-11-09

[Download](https://download.docker.com/win/stable/1.12.3.8488/InstallDocker.msi)

**New**

- Restore the virtual machine's configuration after user changes

- Detect firewall configurations that might block file sharing

- Send more GUI usage statistics to help us improve the product

- The path to HyperV disks is not hardcoded anymore, making the Toolbox import work with non-standard paths

- Verify that all HyperV features are enabled

- Added Moby console to the logs

- Save the current engine with the other settings

- Notary version 0.4.2 installed

- Reworked the File Sharing dialog and underlying mechanism
  - Pre-fill username
  - Faster and more reliable feedback when the user/password is not valid
  - Better support for domain users
  - Error message in Logs when File Sharing failed for other reasons

**Upgrades**

- Docker 1.12.3
- Linux Kernel 4.4.27
- Docker Machine 0.8.2
- Docker Compose 1.8.1
- aufs 20160912

**Bug fixes and minor changes**

**General**

- Added the settings to the diagnostics

- Made sure we didn't use an older Nlog library from the GAC

- Fixed a password escaping regression

- Supports writing large values to the database, specially for trusted CAs

- Preserves the Powershell stacktraces

- Writes OS and Application versions at the top of each log file

- Don't recreate the virtual machine if only the DNS server is set

- The uninstaller now kills the service if it failed to stop it properly

- Improved debug information

**Networking**

- VpnKit is now restarted if it stops

- VpnKit: impose a connection limit to avoid exhausting file descriptors

- VpnKit: handle UDP datagrams larger than 2035 bytes

- VpnKit: reduce the number of file descriptors consumed by DNS

**File sharing**


- Faster mount/unmount of shared drives

- Added a timeout to mounting/unmounting a shared drive

**Hyper-V**

- Make sure invalid "DockerNat" switches are not used

**Moby**

- Increase default ulimit for memlock (fixes [https://github.com/docker/for-mac/issues/801](https://github.com/docker/for-mac/issues/801))

### Docker for Windows 1.12.1, 2016-09-16

[Download](https://download.docker.com/win/stable/1.12.1.7135/InstallDocker.msi)

>**Important Note**:
>
> The auto-update function in Beta 21 cannot install this update. To install the latest beta manually if you are still on Beta 21, download the installer here:

> [https://download.docker.com/win/beta/InstallDocker.msi](https://download.docker.com/win/beta/InstallDocker.msi)

> This problem is fixed as of Beta 23 for subsequent auto-updates.

**New**

* To support trusted registry transparently, all trusted CAs (root or intermediate) on the Windows host are automatically copied to Moby

* `Reset Credentials` also unshares the shared drives

* Logs are now rotated every day

* Support multiple DNS servers

* Added `mfsymlinks` SMB option to support symlinks on bind mounted folder

* Added `nobrl` SMB option to support `sqlite` on bind mounted folders

* Detect outdated versions of Kitematic

**Upgrades**

* Docker 1.12.1
* Docker machine 0.8.1
* Linux kernel 4.4.20
* aufs 20160905

**Bug fixes and minor changes**

**General**

* Uploading a diagnostic now shows a proper status message in the Settings

* Docker stops asking to import from the Toolbox after an upgrade

* Docker can now import from the Toolbox just after HyperV is activated

* Added more debug information to the diagnostics

* Sending anonymous statistics doesn't hang anymore when Mixpanel is not available

* Support newlines in release notes

* Improve the error message when the Docker daemon is not responding

* The configuration database is now stored in memory

* Preserve the stacktrace of PowerShell errors

* Display service stacktrace in error windows

**Networking**

* Improve name servers discovery
* VpnKit supports search domains
* VpnKit is now compiled with OCaml 4.03 rather than 4.02.3

**File sharing**

* Set `cifs` version to 3.02

* VnpKit: reduce the number of sockets used by UDP NAT, reduce the probability

* `slirp`: reduce the number of sockets used by UDP NAT, reduce the probability that NAT rules time out earlier than expected

* Fixed password handling for host file system sharing

**Hyper-V**

* Automatically disable lingering net adapters that prevent Docker from starting or using the network

* Automatically delete duplicated MobyLinuxVMs on a `reset to factory defaults`

* Improved the HyperV detection and activation mechanism

**Moby**

* Fixed Moby Diagnostics and Update Kernel

* Use default `sysfs` settings, transparent huge pages disabled

* `Cgroup` mount to support `systemd` in containers

**Known issues**

* Docker automatically disables lingering net adapters. The only way to remove them is manually using `devmgmt.msc` as documented in [Remove stale network adapters](troubleshoot.md#4-remove-stale-network-adapters) under [Networking issues](troubleshoot.md#networking-issues) in Troubleshooting.

### Docker for Windows 1.12.0, 2016-07-28

[Download](https://download.docker.com/win/stable/1.12.0.5968/InstallDocker.msi)

* First stable release

**Components**

* Docker 1.12.0
* Docker Machine 0.8.0
* Docker Compose 1.8.0
