# Reset-Root-Password-in-CentOS-RHEL-Fedora-via-GRUB-Simple-Method-

A quick and easy method to reset the root password in CentOS, RHEL, or Fedora systems using the GRUB boot menu and emergency shell.

# Reset Root Password in CentOS/RHEL/Fedora via GRUB (Simple Method)

✅ An easy method to reset the root password:

1. Reboot the system → The GRUB menu will appear.

2. Use the arrow keys to select the correct boot entry, then press `e` to edit it.

3. Find the line that starts with `linux16` or `linux`.

4. At the end of that line, add a space and then type:

   rd.break

5. Press `Ctrl + X` to boot into the emergency shell.
6. In the shell, run the following commands:
```bash
mount -o remount,rw /sysroot
chroot /sysroot
passwd
touch /.autorelabel
exit
exit
'''
7. The system will reboot automatically, and the root password will be updated.
   
