# Sprint 3S


## Instalacio LDAP
###Preparatius
Ubuntu 24 (sebidor)  
Tot servidor té per a tindre la IP fitxa aniria bé configura netplan però para passa del pas u farem en interfície
![Error](./red.png)  

/etc/hostname: Defineix el nom del sistema com "alexcaballe".
![Error](./hostname.png)  

/etc/hosts: Assigna noms de domini a IPs locals(Aquesta configuració permet resoldre el nom de l'equip sense necessitat de DNS extern.)
![Error](./hosts.png)

Per a fer la base del nostre domini tenim dos opcion o feru pels arxius base o a través de una comanda natros u farem per comanda  

Aquí veurem la configuració que he aplicat al servidor LDAP.
![Error](./recon.png)

![Error](./recon1.png)

![Error](./recon2.png)

![Error](./recon3.png)

![Error](./recon4.png)

![Error](./recon5.png)

![Error](./recon6.png)  

En aquesta comanda veurem el contingut actual
![Error](./slapcat.png)  


![Error](./lsdesc.png)

![Error](./grupld.png)

![Error](./usuld.png)

![pendent](./pendentld.png)  

- `-c`: Continua el procés encara que hi hagi errors.  
- `-x`: Utilitza autenticació simple (no SASL).  
- `-D`: Especifica el DN de l'usuari administrador.  
- `-W`: Demana la contrasenya de manera interactiva.  
- `-f`: Indica el fitxer LDIF amb les dades a afegir.  

![Error](./ldapadd99.png)

![Error](./slapcat2.png)


Client+------------------------------------------


![Error](./installnscd.png)

![Error](./ldapconf1.png)

![Error](./ldapconf2.png)

![Error](./ldapconf3.png)

![Error](./ldapconf4.png)

![Error](./ldapconf5.png)

![Error](./ldapconf5.png)

Si lo client no se valida sa de fe un reconfigure del paquet anterior

![Error](./nsswitch.png)

![Error](./commonpas.png)

![Error](./commonses.png)


![Error](./prova789.png)

## Gestió d’usuaris 


## Unir equips al domini


## Servidor SAMBA


##Servidor NFS



