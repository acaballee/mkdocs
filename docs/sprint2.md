# Sprint2
## Usuaris:
A Ubuntu, els usuaris i grups són essencials per gestionar els permisos i l'accés als recursos del sistema. Els usuaris compten  cadascun amb el seu espai i configuració, mentre que els grups agrupen usuaris amb permisos similars per facilitar la gestió. Això permet controlar qui pot accedir o modificar certs fitxers o directoris.


###Directoris

1--/etc/shadow
    
Guarda informacio de les contrasenyes dels usuaris en format xifrat i altres paràmetres de seguretat(expiració de la contrasenya...)
El segon camp pot conteni * que significa que el compte esta totalment desavilitat o ! indica que està deshabilitat per accedir-hi amb contrasenya.
Tambe es important saber que el camp "epoch"  representa la data de l'últim canvi de contrasenya de l'usuari.

![1era](/img/cap7.png)

2--/etc/passwd

Conté la llista d’usuaris del sistema, el nom d’usuari, l’ID d’usuari (UID), l’ID de grup (GID), la carpeta personal i el shell per defecte...

3--/etc/gshadow

Emmagatzema informació xifrada sobre els grups i les seves contrasenyes, així com els administradors de cada grup i els usuaris amb accés al grup.

4--/etc/grup

Inclou la llista de grups del sistema amb el nom de cada grup, l'ID de grup (GID) i els usuaris que en formen part.

##Comandes bàsiques

###Creació d'usuaris
Les maneres més comunes de crear usuaris en Ubuntu són: (adduser, adduser)
adduser te fa una sèrie de preguntes inicials i user add no .
![Error](/img/cap78.png)

Per a elimina un usuari usem deluser podem usa sudo deluser --remove-home (usuari) para elimina tame el directori personal 
![8era](/img/cap8.png)
###Creació de grups

Per a crear un grup he usat addgroup
![78era](/img/cap99.png)

I per a eliminarlo delgroup
![65era](/img/cap65.png)
###Modificasio

Crearem un altre grup
![fuc](/img/cap111.png)

I li cambiarem lo nom a test2 en la comanda:
![fail](/img/cap112.png)

Una altra modificació seria canvia la contrasenya amb passwd
![fail](/img/cap113.png)

Ara assigno l'usuari pere com a administrador del grup jocs amb gpasswd. Després, afegeixo sprinttt al grup jocs amb usermod. Finalment, verifico que sprinttt és al grup /etc/group amb grep
![Error](/img/007.png)
#Verificacio
Comprovarem el canvi de nom:
![Error](/img/cap100.png)

###Paraules de pas als grup
![Error](/img/cap899.png)

![Error](/img/cap999.png)


##USUARIS
![Error](/img/141.png)

![Error](/img/231.png)

###hola

gentecon
