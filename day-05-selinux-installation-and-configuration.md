# Day 05 - Selinux Installation and Configuration
Following a security audit, the xFusionCorp Industries security team has opted to enhance application and server security with SELinux. To initiate testing, the following requirements have been established for App server 2 in the Stratos Datacen

Install the required SELinux packages.

Permanently disable SELinux for the time being; it will be re-enabled after necessary configuration changes.

No need to reboot the server, as a scheduled maintenance reboot is already planned for tonight.

Disregard the current status of SELinux via the command line; the final status after the reboot should be disabled.

## What I Did
- Commands practiced:
- `cat /etc/os-release`
- `dnf search selinux`
- `dnf install policycoreutils selinux-policy-targeted`
- `vi /etc/selinux/config`

## What I Learned
- dnf search selinux -> searches on CentOS distribution for Selinux
- nano is not alwyays installed on your system; vi or vim — usually installed by default on CentOS/RHEL systems.

## Challenges / Questions
- how do i know my linux ditribution?
- - `cat /etc/os-release`

- what are the different distributions? what are the commands to look for packages?

| Distribution             | Family        | Package Manager              | Search Packages Command                          | Install Packages Command                           |
| ------------------------ | ------------- | ---------------------------- | ------------------------------------------------ | -------------------------------------------------- |
| **CentOS, RHEL, Fedora** | Red Hat-based | `yum` (older), `dnf` (newer) | `yum search <package>` or `dnf search <package>` | `yum install <package>` or `dnf install <package>` |
| **Debian, Ubuntu**       | Debian-based  | `apt`                        | `apt search <package>`                           | `apt install <package>`                            |
| **SUSE, openSUSE**       | SUSE-based    | `zypper`                     | `zypper search <package>`                        | `zypper install <package>`                         |
| **Arch Linux**           | Independent   | `pacman`                     | `pacman -Ss <package>`                           | `pacman -S <package>`                              |

- how to use Vi or Vim?
-- Press i to enter insert mode
-- Make your changes
-- Press Esc to exit insert mode
-- Type :wq and hit Enter to save and quit
