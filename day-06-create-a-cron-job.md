# Day 06 - Create a Cron Job
The Nautilus system admins team has prepared scripts to automate several day-to-day tasks. They want them to be deployed on all app servers in Stratos DC on a set schedule. Before that they need to test similar functionality with a sample cron job. Therefore, perform the steps below:

- a. Install cronie package on all Nautilus app servers and start crond service.
- b. Add a cron */5 * * * * echo hello > /tmp/cron_text for root user.

## What I Did
- Commands practiced:
  - `dnf install cronie`
  - `sudo su -e`
  - `crontab -e`
  - `sudo systemctl start crond`

## What I Learned
- How to become a root: `sudo su -` This ensures you’re editing root’s config, not your own.
 - `crontab -e` is in vi; u can insert by pressing 'i';'Esc'; ; :wq (save and exit)
 - dont forget to start the application after installing
- a quick way without editing in vi is `echo "*/5 * * * * echo hello > /tmp/cron_text" | crontab -`

## Challenges / Questions
- What is a Cronie?:
- Cronie is a Linux utility that runs scheduled tasks (cron jobs); It’s basically the cron daemon that comes with many modern Linux distributions, especially Fedora, CentOS, and RHEL.
Purpose: Automates repetitive tasks (like backups, cleanup scripts, or reports) by running them at fixed times, dates, or intervals.

- How to start an application/chronie e.g?
- `sudo systemctl start crond`
### Overall
- `sudo systemctl start <service_name>`
- `sudo systemctl enable <service_name>`
- `sudo systemctl status <service_name>`

