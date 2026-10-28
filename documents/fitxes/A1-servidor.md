# A1 · Instal·lació d'Ubuntu Server i del servei DNS de l'aula

**Incidència associada:** #9 · Instal·lació de Ubuntu Server i serveis centrals

## Nom de la tasca (Què?)
Instal·lar Ubuntu Server al servidor de l'aula amb adreça IP fixa i configurar-hi el servei DNS de la zona `auladigital.local`, perquè els 20 equips, la pissarra digital i la impressora es puguen localitzar pel nom.

## Mòdul i RA (Per a què?)
- Mòdul: MP05 – Serveis en xarxa
- RA associat: MP05-RA2: Configura serveis de xarxa local (DHCP, DNS i impressió en xarxa).

## Modalitat (Com?)
Individual — AlumneA (Rol A, coordinador/a tècnic/a)

## Producte entregable (Suport)
- `configuracio/servidor/ubuntu-dns-install.md` publicat al repositori, amb els passos i els fitxers de configuració.
- Captura de la configuració de xarxa del servidor i de la resolució DNS correcta (ordre `nslookup`).

## Instruccions pas a pas
1. Instal·lar Ubuntu Server 26.04 i assignar-li l'adreça IP fixa 192.168.1.254/24 amb porta d'enllaç 192.168.1.1 (Netplan).
2. Activar l'accés SSH: `sudo apt install openssh-server -y`.
3. Instal·lar el servei DNS: `sudo apt install bind9 bind9-utils -y`.
4. Crear la zona directa `auladigital.local` i afegir-hi els registres del servidor, la impressora i la pissarra digital.
5. Configurar els reenviadors (forwarders) cap al DNS del proveïdor per a la resolució d'internet.
6. Comprovar amb el Rol A que el DHCP del router (#8) entrega 192.168.1.254 com a servidor DNS.
7. Verificar la resolució des d'un equip client amb `nslookup impressora.auladigital.local` i documentar els passos i les incidències al repositori.

## Recursos necessaris
- Servidor de l'aula i imatge d'instal·lació d'Ubuntu Server 26.04.
- Paquets `openssh-server`, `bind9` i `bind9-utils`.
- Un equip client de l'aula per a les proves.
- Apunts del mòdul de Serveis en xarxa.

## Durada i setmana (Quan?)
3 hores · Setmana 4 (fita M2)

## Lloc de realització (On?)
Aula objecte del projecte (IES Simarro)

## Responsable (Qui?)
- AlumneA (Rol A): execució i documentació.
- AlumneC (Rol C): revisa la resolució de noms des d'un equip client.

## Instrument d'avaluació
Rúbrica MP05 (professorat)
- [ ] Servidor instal·lat amb IP fixa i accés SSH (25%)
- [ ] Zona DNS creada i resolent noms correctament (25%)
- [ ] Documentació completa dels passos i les incidències (25%)
- [ ] Prova de resolució verificada des d'un equip client (25%)
