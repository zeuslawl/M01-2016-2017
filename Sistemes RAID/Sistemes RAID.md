# Sistemes RAID

#### 1. Resum de sistemes RAID fent servir una taula com la vista a classe.

| Niveles |Número Min | N Máx discos fallados| Capacidad | Read | Write | 
| ------- | --------- | -------------------- | --------- | ---- | ----- |
| Raid 0 | 2 | 0 | 100% | EXCELENTE | EXCELENTE |
| Raid 1 | 2(Máx)| 1 | 50% | V.GOOD | GOOD |
| Raid 5 | 3 | 1 | 67% ~ 94% | V. GOOD | GOOD |
| Raid 6 | 4 | 2 | 50% -- 88% | GOOD | GOOD |
| Raid 10 | 4 | 1/ Mirror | 50% | V.GOOD | GOOD |  


#### 2. Descripció de la metodologia utilitzada a classe per a fer proves amb màquines virtuals.

- Crear 3 discos con la memoria que quieras. ( en mi caso 200 MB) /dev/vdc  /dev/vdd /dev/vde
- Instalamos mdadm
- Creamos el Raid ( mdadm --create nombre --level=1 --raid-devices=2 /dev/vda /dev/vdd )
- Para saber el estado del raid ( cat /proc/mdstat )
- Crear sistema ficheros ( mkfs.ext4 /dev/md0 )
- Para montarlo ( mount /dev/md0/mnt )
- ¿Donde esta montado? ( df -h )
- Crear img ( dd if=/dev/zero of=test.img bs=4k count=1000 )
- Para que el sistema recargue los discos. ( partprobe )
- mdadm --detail /dev/md0
- Para borrar el raid ( mdadm /dev/md0 --remove /dev/vdc )


#### 3. Comandes i descripció de les mateixes per tal de crear un sistema RAID1

mdadm --create nombre --level=1 --raid-devices=2 /dev/vda /dev/vdd

#### 4. Comandes i descripció de les mateixes per tal de crear un sistema RAID5

mdadm --create nombre --level=5 --raid-devices=3 /dev/vda /dev/vdd /dev/vdb

#### 5. Comandes i descripció de les mateixes per tal de crear un sistema RAID6

mdadm --create nombre --level=6 --raid-devices=4 /dev/vda /dev/vdd /dev/vdb /dev/vdc

#### 6. Comandes i descripció de les mateixes per tal de crear un sistema RAID10

mdadm --create nombre --level=10 --raid-devices=4 /dev/vda /dev/vdb /dev/vdc /dev/vdd


