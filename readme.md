## Exercice 1
---

1. On ajoute un disque dur de 5 Go avec un provisionnement dynamique.
2. En utilisant ```lsblk``` on peut voir qu'il y a un sdb à 5Go.
3. ```fdisk /dev/sdb``` puis n pour créer une partition, +2G pour le nombre de giga, t pour modifier le type, puis w pour save.
4. Pour formater la partition on fait ```mkfs /dev/sdb1```
5. Car la partition n'est pas encore monté
6.  ```nano /etc/fstab```, puis ajouter ligne ```/dev/sdb1       /data ext4    defaults        0       0```
7.  ```mount /dev/sdb1 /data```

## Exercice 2
---

1. ```umount /dev/sdb1```
2. ```fdisk /dev/sdb```, d
3. ```pvcreate /dev/sdb```
4. ```vgcreate test /dev/sdb```
5. 
