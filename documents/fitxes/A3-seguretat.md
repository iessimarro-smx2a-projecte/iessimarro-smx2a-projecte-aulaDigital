# A3 · Polítiques de seguretat i còpies de seguretat

**Incidència associada:** #12 · Polítiques de seguretat i còpies de seguretat

## Nom de la tasca (Què?)
Aplicar les mesures bàsiques de seguretat als equips de l'aula i al servidor, i programar una còpia de seguretat automàtica de la configuració del servidor.

## Mòdul i RA (Per a què?)
- Mòdul: MP06 – Seguretat informàtica
- RA associat: MP06-RA1: Aplica mesures bàsiques de seguretat i còpies de seguretat.

## Modalitat (Com?)
Individual — AlumneC (Rol C, tècnic/a de configuració)

## Producte entregable (Suport)
- `documents/seguretat/politiques.md` amb les mesures aplicades i el pla de còpies.
- Captures de l'antivirus actiu, dels comptes d'usuari limitats i de la primera còpia correcta.

## Instruccions pas a pas
1. Crear als equips Windows un compte d'alumne sense privilegis d'administració i protegir el compte d'administrador amb una contrasenya robusta.
2. Comprovar que l'antivirus i les actualitzacions automàtiques estan actius en tots els equips.
3. Activar el tallafoc del servidor (`ufw`) i permetre només SSH, DHCP i DNS.
4. Programar amb `cron` una còpia diària de `/etc` del servidor a un disc extern.
5. Restaurar un fitxer de prova des de la còpia per a verificar-la.
6. Documentar les mesures i les incidències al repositori.

## Recursos necessaris
- Equips de l'aula amb Windows 11 Education i servidor Ubuntu Server.
- Disc extern USB per a les còpies.
- Apunts del mòdul de Seguretat informàtica.

## Durada i setmana (Quan?)
3 hores · Setmana 5 (fita M2)

## Lloc de realització (On?)
Aula objecte del projecte (IES Simarro)

## Responsable (Qui?)
- AlumneC (Rol C): execució i documentació.
- AlumneA (Rol A): revisa la configuració del tallafoc del servidor.

## Instrument d'avaluació
Rúbrica MP06 (professorat)
- [ ] Comptes d'usuari i contrasenyes configurats correctament (25%)
- [ ] Antivirus, actualitzacions i tallafoc actius (25%)
- [ ] Còpia programada i restauració verificada (25%)
- [ ] Documentació completa de les mesures aplicades (25%)
