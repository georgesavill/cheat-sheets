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

To change user's password:
```
sudo passwd [username]
```
