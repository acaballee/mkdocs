# Sprint6
##Usuaris

Crearem 2 usuaris per interfície usant administracion de equipos
![Error](./adminieqi.png)

Farem un Usuario nuevo
![Error](./alumnelimi1.png)

Li posarem nom i contrasenya
![Error](./alumnelimi2.png)

Resultat
![Error](./alumnelimi3.png)

Ara crearem el grup Limitats
![Error](./gruplimi2.png)  

Li posarem els 2 usuaris creats anteriorment
![Error](./gruplimi.png)

##Script de còpia i automatització

Particio i creacio de volumen NTFS
![Error](./particio0.png)

![Error](./particio.png)

Li posarem el nom de Backups
![Error](./particio2.png)

![Error](./particio3.png)

Script en bat que copia el contingut de users i el pega al disc E\CopiesUusaris
![Error](./Script1.png)

Resultat
![Error](./resultat.png)
##Gestió de processos i serveis
La comanda tasklist mostra la llista de processos actius al sistema
![Error](./taskalist.png)

![Error](./procesosfixe.png)

###Processos no essencials del sistema

Llista de processos que poden ser considerats **no essencials** 

| Nom del procés                    | Memòria usada     | Justificació per eliminar-lo                                       |
|----------------------------------|-------------------|---------------------------------------------------------------------|
| `dwm.exe`                        | 71.572 KB         | Efectes visuals, prescindible en equips amb pocs recursos           |
| `fontdrvhost.exe`      | 3.412 KB          | Gestió de fonts, no essencial si no s’usen fonts especials          |
| `fontdrvhost.exe`      | 4.632 KB          | Idem anterior, duplicat per altra sessió                            |
| `MsMpEng.exe`                    | 280.964 KB        | Escàner en temps real de Windows Defender                           |
| `dllhost.exe`                    | 11.352 KB         | Host de COM, es pot desactivar si no es requereix                   |
| `svchost.exe`         | 62.216 KB         | Pot contenir serveis secundaris                                     |
| `MicrosoftEdgeUpdate.exe`        | 2.528 KB          | Actualitzador de Microsoft Edge, no essencial                       |
| `SgrmBroker.exe`                 | 7.252 KB          | Gestor de seguretat, no essencial en usuaris domèstics              |
| `MoUsoCoreWorker.exe`            | 44.324 KB         | Actualitzacions automàtiques, es pot desactivar temporalment        |
| `SearchIndexer.exe`              | 31.152 KB         | Indexador de fitxers, pot alentir l'equip                           |
| `ctfmon.exe`                     | 20.504 KB         | Entrada de llenguatge, prescindible si no s’usen idiomes alternatius|
| `smartscreen.exe`                | 25.768 KB         | Filtres de seguretat de Windows, es pot desactivar                  |
| `TextInputHost.exe`              | 39.068 KB         | Entrada tàctil o per veu, innecessari en dispositius sense això     |
| `StartMenuExperienceHost.exe`    | 78.388 KB         | Interfície del menú inici, no crític                                |
| `RuntimeBroker.exe`   | 26.296 KB         | Gestor d'autoritzacions, sovint no necessari                        |
| `SearchApp.exe`                  | 88.952 KB         | Cerca de Windows, es pot desactivar                                 |
| `RuntimeBroker.exe`   | 25.452 KB         | Idem anterior, duplicat                                             |
| `ShellExperienceHost.exe`        | 45.344 KB         | Interfície de Windows, no crític                                    |
| `RuntimeBroker.exe`   | 17.132 KB         | Idem anterior, duplicat                                             |
| `msedge.exe`                     | 162.652 KB        | Navegador Edge, es pot tancar si no s’està usant actualment         |

##Gestió de permisos

![Error](./carpetacontrol0.png)

![Error](./carpetacontrol3.png)

![Error](./carpetacontrol1.png)

![Error](./carpetacontrol2.png)













