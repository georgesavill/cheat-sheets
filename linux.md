# Linux cheat sheet

## Check file/directory sizes

To check where disk space is being used by the machine:
```
sudo du -cha --max-depth=1 / | grep -E "M|G"
```
Will give an output like:
```
75M     /boot
661M    /var
810M    /usr
5.2M    /run
607M    /lib
541M    /snap
2.0G    /swap.img
15M     /bin
150G    /hdd0
16M     /sbin
5.7M    /etc
```

---

To check file sizes within the current directory:
```
du -ha
```
---

To recursively copy files, maintaining permissions, in "archive" mode, showing transfer speed and progress per file:
```
rsync -ahr --progress [source] [destination]
```

See [here](https://www.computerhope.com/unix/rsync.htm) for more info on rsync.

---

To add a new user:
```
sudo adduser [username]
```

To change user's password:
```
sudo passwd [username]
```

To add a group to a user:
```
sudo usermod -a -G [group] [user]
```

---

To remove the sudo password prompt for a user:

```
sudo visudo
```

and add the following line:
```
george ALL=(ALL) NOPASSWD: ALL
```

---

To add a shorthand alias for shell commands:

```
alias update="sudo apt update"
```

---

Clone a drive:
```
sudo dd if=/dev/sda of=/dev/sdb bs=100M conv=notrunc status=progress
```

---

Create a shortcut:
```
ln -s [target of shortcut] [name/path of shortcut]
```