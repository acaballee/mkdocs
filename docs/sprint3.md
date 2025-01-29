# Sprint 3


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

Usarem els fitxes prefets pera a crear els grups i usuaris
![Error](./lsdesc.png)

En les següents dues captures adapto els fitxes al meu domini
![Error](./grupld.png)

![Error](./usuld.png)

![pendent](./pendentld.png)  

- `-c`: Continua el procés encara que hi hagi errors.  
- `-x`: Utilitza autenticació simple (no SASL).  
- `-D`: Especifica el DN de l'usuari administrador.  
- `-W`: Demana la contrasenya de manera interactiva.  
- `-f`: Indica el fitxer LDIF amb les dades a afegir.  

![Error](./ldapadd99.png)

I aquí un apartat posterior a la configuració
![Error](./slapcat2.png)


Client+------------------------------------------

Instal·lació de nscd
![Error](./installnscd.png)

###Configuració de ldap-auth-config  

Posarem la IP del servidor LDAP.
![Error](./ldapconf1.png)

Proporcionarem el nom del domini
![Error](./ldapconf2.png)

I la quenta que usarem
![Error](./ldapconf3.png)

Instal·larem aquest paquet para que el sistema Linux s'autentifique mediant-te un servidor LDAP
![Error](./ldapconf4.png)

![Error](./ldapconf5.png)

![Error](./ldapconf5.png)

Si lo client no se valida sa de fe un reconfigure del paquet anterior

![Error](./nsswitch.png)

![Error](./commonpas.png)

![Error](./commonses.png)

Com podem veure al final hem aconseguit connecta el client al servidor LDAP amb l'usuari creat anteriorment
![Error](./prova789.png)

## Gestió d’usuaris 


## Unir equips al domini


## Servidor SAMBA


##Servidor NFS



