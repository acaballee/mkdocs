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

## Gestió d’usuaris i grups

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


## Unir equips al domini

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

##Entorns grafics
En el meu cas he triat  LDAP Account Manager (LAM) que és una eina web per gestionar usuaris, grups i permisos en servidors LDAP de manera fàcil i visual.  


![Error](./installphp5.png)


![Error](./ldap121.png)


![Error](./ldap122.png)


![Error](./ldap123.png)


## Recursos en xarxa

Els servidors **Samba** i **NFS** serveixen per a compartir recursos en xarxa.

- El servidor **NFS** autentica a nivell de **màquina (host)** i no d'usuari.
- Permetre autenticació a nivell d'usuari amb **NFS** és complex i requereix **Kerberos**.
- Per aquest motiu, és més fàcil utilitzar **Samba** si es vol control d’accés per usuari.



### Servidor SAMBA
####Teoria:
El servidor Samba, a diferència del servidor NFS, permet l'autenticació a nivell d'usuari.
Permet la compartició de recursos que no són només carpetes, sinó també impressores.
Samba pot treballar conjuntament amb LDAP per utilitzar autenticació a nivell d'usuaris.
Samba permet la connexió de clients tant de Linux com de Windows.


![Error](./installsmb.png)

![Error](./grepperfils.png)

![Error](./configperfis.png)

![Error](./creauser.png)

![Error](./comptail.png)

![Error](./addgrupdam.png)

![Error](./smbcontra.png)

Client:

![Error](./installsmbclient.png)

![Error](./consmb.png)

Raul crea

![Error](./compraul.png)

Enric no crea

![pendent](./enricno.png)

###Servidor NFS


![Error](./instanfs.png)

![Error](./nanoexports.png)

![Error](./restartnfs.png)

Client Windous

![Error](./clientwind.png)

![Error](./clientwind2.png)

Client Ubuntu  
![Error](./clientubu1.png)

![Error](./clientubu2.png)

####Perfils mòbils

![Error](./instalnfsserver.png)

![Error](./etcnanoexport.png)

![Error](./grupldif.png)





![Error](./usuldif.png)

![Error](./aplicaldif.png)

Client:

![Error](./instalclinfs.png)

![Error](./etcfstabnano.png)

![Error](./comprovacioalu54.png)



