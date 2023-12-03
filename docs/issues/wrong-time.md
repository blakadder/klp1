---
comments: true
title: Wrong system time & date
description: Fix wrong time and/or date that's showing in history, logs and console
---

SSH to the IP address of KLP1. 

Login with username **root** and password **makerbase**.

Run command `sudo dpkg-reconfigure tzdata` and select your timezone.

Time zone should now be set correctly, now you need to enable time syncing.

Run `sudo apt-get install chrony -y`.

This will uninstall ntp and install chrony, a service used to sync time.s

Run `timedatectl` to check if the time and date are now properly synced.

```shell
mks@mkspi:~$ timedatectl
               Local time: Fri 2023-11-17 21:56:55 CET
           Universal time: Fri 2023-11-17 20:56:55 UTC
                 RTC time: Fri 2023-11-17 20:56:54
                Time zone: Europe/Zagreb (CET, +0100)
System clock synchronized: yes
              NTP service: inactive
          RTC in local TZ: no
```
