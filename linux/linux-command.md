## Sistemas Operativos.

El **software** (programa) se encarga de gestionar y usar el **hardware** (piezas). Interactua con la red de circuitos y componentes del ordenador.
**Ejemplos de Software**

- Windows
- Mac OS
- Linux

## Propiedades de Linux.

| Libre           | Su código fuente se puede usar, modificar y distribuir               |
| :-------------- | :------------------------------------------------------------------- |
| Multiusuario    | Varios usuarios pueden trabajar concurrentemente en la misma maquina |
| Multiplataforma | Instalable el multitud de dispositivos                               |
| Redes           | Permite acceso a recursos remotos y comunicaciones                   |
| Estabilidad     | Funciona correctamente meses, incluso años                           |
| Multitarea      | Se pueden realizar distintas tareas a la vez                         |

## Software libre.

**Libertades del software libre**

- Libertad de usar el programa.
- Estudiar cómo funciona el programa y modificarlo
- Libertad de distribuir copias del programa

## Qué es Linux?

Es un sistema operativo, formado por:

| Nucleo (Kernel)         | Interactua directamente con el hardware             | Gestion de memoria, control de acceso al ordenador y permisos |
| :---------------------- | :-------------------------------------------------- | :------------------------------------------------------------ |
| **Shell**               | **Intérprete de lenguaje de comandos**              | **Ejecuta los comandos**                                      |
| **Sistema de archivos** | **Unidad básica de organización de la información** | **Sin restricciones sobre nombre, extenciones, etc**          |

### Utilidad y aplicaciones.

- Edición y procesamiento del texto.
- Lenguajes y entornos de programación.
- Bases de datos.
- Hojas de cálculo.
- Navegación y edición web.
- etc.

## Distribuciones de Linux.

En el nucleo Linux incluye determinados programas para satisfacer las necesidades.

# Trying Out Commands

## who

```sh
bash-3.2$ who
katherine console  May 23 20:43
katherine ttys000  Jun  4 11:45
katherine ttys001  Jun  4 12:16
```

## finger

```sh
bash-3.2$ finger
Login    Name                 TTY  Idle  Login  Time   Office  Phone
katherine katherine            s00    10  Sat    11:45
katherine katherine            s00        Sat    12:16
katherine katherine           *con   11d  May 23 20:43
```

## whoami

```sh
bash-3.2$  whoami
katherine
```

## hostname

```sh
bash-3.2$ hostname
RKMBP2014.local
```

## passwd

```sh
bash-3.2$  passwd
Changing password for katherine.
Old Password:
New Password:
Retype New Password:

```

## exit

```sh
bash-3.2$  exit
Saving session...completed.
Deleting expired sessions...      39 completed.

[Process completed]

```

## /

(Directorio raíz)

```sh
bash-3.2$ cd /
bash-3.2$ ls
Applications	System		Volumes		cores		etc		opt		sbin		usr
Library		Users		bin		dev		home		private		tmp		var
```

## /home

(Contiene los directorios de los usuarios)

```sh
bash-3.2$ cd /home
bash-3.2$ ls
```

## /bin

(Ordenes usuales y utilidades)

```sh
bash-3.2$ cd /bin
bash-3.2$ ls
[		cp		dd		expr		launchctl	mkdir		pwd		sleep		test
bash		csh		df		hostname	link		mv		rm		stty		unlink
cat		dash		echo		kill		ln		pax		rmdir		sync		wait4path
chmod		date		ed		ksh		ls		ps		sh		tcsh		zsh
```

## /usr

Programas, librerias y fícheros de uso normal

```sh
bash-3.2$ cd /usr
bash-3.2$ ls
X11		X11R6		bin		lib		libexec		local		sbin		share		standalone
```

## /etc

Contiene ficheros de configuración.

```sh
bash-3.2$ cd /etc
bash-3.2$ ls
afpovertcp.cfg				gettytab~orig				ntp_opendirectory.conf			rmtab
afpovertcp.cfg~orig			group					openldap				rpc
aliases					group~previous				openssl					rpc~previous
aliases.db				hosts					pam.d					rtadvd.conf
apache2					hosts.equiv				passwd					rtadvd.conf~previous
asl					hosts~orig				passwd~orig				security
asl.conf				irbrc					paths					services
auto_home				kern_loader.conf			paths.d					services~previous
auto_master				kern_loader.conf~previous		paths~orig				shells
auto_master~orig			krb5.keytab				periodic				shells~orig
autofs.conf				localtime				pf.anchors				snmp
bashrc					locate.rc				pf.conf					ssh
bashrc_Apple_Terminal			mail.rc					pf.os					ssh_config~orig
bashrc~previous				mail.rc~orig				php-NOTICE-PLANNED-REMOVAL.txt		sshd_config~previous
com.apple.screensharing.agent.launchd	man.conf				php-fpm.conf.default			ssl
csh.cshrc				manpaths				php-fpm.d				sudo_lecture
csh.cshrc~orig				manpaths.d				php.ini.default				sudoers
csh.login				master.passwd				php.ini.default-5.2-previous		sudoers.d
csh.login~orig				master.passwd~orig			php.ini.default-5.2-previous~orig	sudoers~orig
csh.logout				moduli~previous				php.ini.default-previous		syslog.conf
csh.logout~orig				motd					postfix					syslog.conf~previous
cups					mullvad-vpn				ppp					ttys
defaults				nanorc					profile					ttys~previous
efax.rc~previous			networks				profile~orig				uucp
emond.d					networks~orig				protocols				wfs
find.codes				newsyslog.conf				protocols~previous			xtab
find.codes~orig				newsyslog.d				racoon					zprofile
fstab.hd~previous			nfs.conf				rc.common				zshrc
ftpusers				nfs.conf~orig				rc.common~previous			zshrc_Apple_Terminal
ftpusers~orig				notify.conf				rc.netboot
gettytab				ntp.conf				resolv.conf
```

## /sbin

Contiene programas necesarios de inicio de sistema

```sh
bash-3.2$ cd /sbin
bash-3.2$ ls
apfs_hfs_convert	fsck_cs			fstyp_udf		mount_9p		mount_ftp		mpioutil		pfctl
apfs_unlockfv		fsck_exfat		halt			mount_acfs		mount_hfs		newfs_apfs		ping
disklabel		fsck_hfs		ifconfig		mount_afp		mount_msdos		newfs_exfat		ping6
dmesg			fsck_msdos		kextload		mount_apfs		mount_nfs		newfs_hfs		quotacheck
dynamic_pager		fsck_udf		kextunload		mount_cd9660		mount_ntfs		newfs_msdos		reboot
emond			fstyp			launchd			mount_cddafs		mount_smbfs		newfs_udf		route
fibreconfig		fstyp_hfs		md5			mount_devfs		mount_tmpfs		nfsd			rtsol
fsck			fstyp_msdos		mknod			mount_exfat		mount_udf		nfsiod			shutdown
fsck_apfs		fstyp_ntfs		mount			mount_fdesc		mount_webdav		nologin			umount
```

## /tmp

Contiene ficheros temporales

```sh
bash-3.2$ cd /tmp
bash-3.2$ ls
com.apple.launchd.EL6EmJ1P94	com.apple.launchd.V35areNMAj	com.google.Keystone
com.apple.launchd.RfLq2XEAyl	com.apple.launchd.sri8ZywjRR	powerlog
```

## /var

Contiene ficheros de spool de datos, logs...

```sh
bash-3.2$ cd /var
bash-3.2$ ls
MobileSoftwareUpdate	chef			install			ma			protected		select
agentx			containers		jabberd			mail			root			spool
at			db			lib			msgs			rpc			tmp
audit			empty			log			netboot			run			vm
backups			folders			logs			networkd		rwho			yp
```

## pwd

Nos dice en cada momento la ruta completa de donde nos encontramos

```sh
bash-3.2$ cd /Users/katherine/
bash-3.2$ pwd
/Users/katherine
```

## ls

Nos muestra los archivos del directorio actual

```sh
bash-3.2$ ls
Applications	Code		Desktop		Documents	Downloads	Library		Movies		Music		Pictures	Public
```

**ls file_name**

```sh
bash-3.2$ ls -lah fig_s3d_position_602_codon_GCA.png
-rw-r--r--@ 1 katherine  staff   101B Jun  4 12:20 fig_s3d_position_602_codon_GCA.png
```

**ls \*.html**

```sh
bash-3.2$ ls *.html
home.html
```

**ls -l**

```sh
total 72
-rw-r--r--@ 1 katherine  staff  27226 Jun  2 10:40 cats.jpg
-rw-r--r--  1 katherine  staff    751 Jun  2 12:00 home.css
-rw-r--r--  1 katherine  staff   1463 Jun  2 11:48 home.html
```

**ls -a**  
Muestra todos los ficheros (y también los ocultos que empiezan por .)

```sh
bash-3.2$ ls -a
.		..		cats.jpg	home.css	home.html
```

**ls -la**  
Muestra todos los archivos junto con su tamaño, usuario y grupo, fecha de modificación.

```sh
bash-3.2$ ls -la
total 72
drwxr-xr-x   5 katherine  staff    160 Jun  2 19:16 .
drwxr-xr-x  11 katherine  staff    352 Jun  4 11:55 ..
-rw-r--r--@  1 katherine  staff  27226 Jun  2 10:40 cats.jpg
-rw-r--r--   1 katherine  staff    751 Jun  2 12:00 home.css
-rw-r--r--   1 katherine  staff   1463 Jun  2 11:48 home.html
```

## mkdir

Crea directorios

```sh
bash-3.2$ mkdir myweb
bash-3.2$ ls
cats.jpg	home.css	home.html	myweb
```

## rmdir

Elimina directorios vacios

```sh
bash-3.2$ ls
cats.jpg	home.css	home.html	myweb
bash-3.2$ rmdir myweb/
bash-3.2$ ls
cats.jpg	home.css	home.html
```

## cat

Muestra el contenido de un archivo

```sh
bash-3.2$ cat home.html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>The Cat House</title>
    <link rel="stylesheet" href="home.css">
</head>
<body>
    <div class="cat-house-text">
        <h3>
            <b>Why you should adopt a cat with us</b>
        </h3>
        <p class="description">According to Research Gate, owning a cat, or any pet you adopt from a shelter, has been shown<br>
            to have positive effects on human's ability to cope with stress, anxiety, depression and<br>
            loneliness. Taking a cat home from a shelter can inprove your sense of happines and general<br>
            well-being.
        </p>
    </div>
    <img src="cats.jpg"/>
</body>
<footer>
    <span class="copyright">
        All rights reserved
        <a class="cat-house-link" href="home.html">The Cat House</a> 2022
    </span>
</footer>

```

## head

Muestra las primeras 10 lineas de un archivo.

```sh
bash-3.2$ head home.html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>The Cat House</title>
    <link rel="stylesheet" href="home.css">
</head>
<body>
```

## tail

Muestra las ultimas 10 lineas de un archivo

```sh
bash-3.2$ tail home.html
    </div>
    <img src="cats.jpg"/>
</body>
<footer>
    <span class="copyright">
        All rights reserved
        <a class="cat-house-link" href="home.html">The Cat House</a> 2022
    </span>
</footer>
</html>bash-3.2$
```

```sh
tail -10 filename
```

## cp

Copiara los archivos y directorios.

```sh
bash-3.2$ cp home.html home.css ./proyect-about-cats/
bash-3.2$ cd proyect-about-cats; ls
home.css	home.html
```

## mv

Movera archivos, carpetas o directorios al destino deseado. También cambia el nombre.

```sh
bash-3.2$ mv cat-house.png ./proyect-about-cats/
bash-3.2$ cd proyect-about-cats; ls
cat-house.png
```

## rm -r

Elimina archivos, documentos y directorios.

```sh
bash-3.2$ ls
home.css		home.html		proyect-about-cats
bash-3.2$ rm -r proyect-about-cats/
bash-3.2$ ls
home.css	home.html
```

## dot .

Directorio actual.

```sh
bash-3.2$ pwd
/Users/katherine
bash-3.2$ cd .
bash-3.2$ pwd
/Users/katherine
```

## dot dot ..

Directorio padre.

```sh
bash-3.2$ pwd
/Users/katherine
bash-3.2$ cd ../
bash-3.2$ pwd
/Users
```

## top

## nohup

## Simbolos especiales.

Actuan como comodines para uno o multiples caracteres.

### Asterisk: \*

```sh
bash-3.2$ ls *.html
home.html

contact.html
```

### Question Mark: ?

### Pipe: |

Pipe redirecciona la salida estándar,envia los datos de un comando a otro.

```sh
bash-3.2$ ls | sort
exercises
github.com
scratch
```

### Redirección: < >

Trabajan con archivos intermedios.

`>` Se usa para enviar la respuesta de un comando a un archivo.
`<` Se usa para remplazar un parametro de algunos comandos de Linux (no todos los comandos) con un archivo.

```sh
bash-3.2$ date
Wed Jun  8 12:28:57 EST 2022
bash-3.2$ pbcopy < calender
bash-3.2$ ls
calender
```

### Semi-Colon ;

### Ampersand &

## Variables del Shell

### HOME

Indica el directorio Home del usuario.

```sh
bash-3.2$ echo $HOME
/Users/katherine
```

### PATH

Directorios donde el sistema busca un comando.

```sh
bash-3.2$ echo $PATH
/usr/local/bin:/usr/bin:/bin:/usr/sbin:/sbin:/Library/TeX/texbin:/opt/X11/bin
```

### TERM

Indica que tipo de terminal.

```sh
bash-3.2$ echo $TERM
xterm-256color
```

### USER

Nombre del usuario

```sh
bash-3.2$ echo $USER
katherine
```

### UID

Numero de identificación del usuario.

```sh
bash-3.2$ echo $UID
502
```

### PS1

Prompt del sistema

```sh
bash-3.2$ echo $PS1
\s-\v\$
```
