# Readme

**GitLab**: [https://gitlab.com/marc.culle/proyecto.salle](https://gitlab.com/marc.culle/proyecto.salle)  
**OVAs per al Projecte Interdisciplinar del lasallefponline - ASIR**

---

## 📘 Títol

**Disseny i Implementació d’una Infraestructura Informàtica Empresarial amb Serveis Integrats sobre Maquinària Virtual**  
**Autor**: Marc Cullell Porter  
**Data d’última modificació**: 13/06/2025

---

## 📝 Descripció

Aquest projecte té com a finalitat la creació i implementació d’una infraestructura informàtica completa i funcional per a una empresa mitjana, utilitzant màquines virtuals allotjades en un entorn controlat.

La infraestructura dissenyada cobreix les necessitats bàsiques i avançades de qualsevol organització que requereixi un sistema centralitzat de gestió de xarxa, usuaris, serveis de monitorització, compartició d’arxius i serveis web.

La idea central és desenvolupar un entorn tecnològic basat principalment en **programari lliure** (excepte el servidor AD de Windows), amb un enfocament **modular i escalable**, que simuli una situació real i aplicable en el món laboral de l’administració de sistemes i xarxes.

---

## 💾 OVAs

Els serveis principals es desplegaran mitjançant les següents màquines virtuals:

- `ubuntu-server - DNS - PROYECTO SALLE.ova` *(També DHCP)*
- `windows-server - AD - PROYECTO SALLE.ova`
- `ubuntu-server - Zabbix - PROYECTO SALLE.ova`
- `ubuntu-server - FTP - PROYECTO SALLE.ova` *(conté FileZilla client)*
- `ubuntu-server - WEB - PROYECTO SALLE.ova`

També s'inclouen màquines client de prova:

- `Maquina recién formateada - PROYECTO SALLE.ova` *(Fora de domini)*
- `Maquina 1 - PROYECTO SALLE.ova` *(En domini, usuari: ton.ceo, amb FileZilla client instal·lat)*

---

## 🔐 Credencials d'accés

### Ubuntu Server (totes les màquines)
- **Usuari**: `marccp`  
- **Contrasenya**: `admin`

### Windows Server - AD
- **Usuari**: `MARCCP\Administrator`  
- **Contrasenya**: `Admin123`

### Clients
- **Usuari local**: `Administrador`  
- **Contrasenya**: `Admin123`  
- **Usuari de domini**: `marccp\ton.ceo`  
- **Contrasenya**: `Admin123`

### Zabbix
- **Usuari**: `Admin`  
- **Contrasenya**: `zabbix`

### FTP
- **Usuari**: `usuari1`  
- **Contrasenya**: `admin`

---

## 📂 Arxius d’interès

- **Configuració xarxa DNS-DHCP**: `/etc/netplan/50-cloud-init.yaml`
- **Configuració DNS**: `/etc/bind/db.marccp.edu`
- **Configuració DHCP**: `/etc/kea/kea-dhcp4.conf`
- **Zabbix**:
  - `/etc/zabbix/zabbix_server.conf`
  - `/etc/zabbix/zabbix_agentd.conf`
- **FTP**: `/etc/vsftpd.conf`
- **Web**:
  - `/var/www/html/index.html`
  - `/etc/apache2/sites-enabled/000-default.conf`

---

## 🛠️ Nota AD

S'han creat **6 usuaris** repartits entre **4 unitats organitzatives**:
- RRHH
- Finances
- CEO
- SysAdmin

També s'han configurat **GPOs globals** per al domini en relació amb:
- Gestió de contrasenyes
- Compartició d’arxius
- Personalització de l’escriptori

---
