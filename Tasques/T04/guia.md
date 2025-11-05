# Guia T04: Serveis de directori. LDAP

## 1. Preparació de la màquina Ubuntu Server
- Configura amb hostname:
  ```
  sudo hostnamectl set-hostname server.innovatechXX.test
  ```
- Comprova el nom i el domini:
  ```
  hostname
  hostname -f
  ```
- Revisa la xarxa:
  ```
  ip a
  ```
- Actualitza `/etc/hosts` amb l'IP i el domini corresponent.

## 2. Instal·lació del servei LDAP
- Instal·la:
  ```
  sudo apt update
  sudo apt install slapd ldap-utils -y
  ```
- Reconfigura:
  ```
  sudo dpkg-reconfigure slapd
  ```
- Durant la configuració, defineix:
  - Domini: `innovatechXX.test`
  - Contrasenya: `p@ssw0rd`
- Verifica la instal·lació:
  ```
  sudo slapcat
  ```

## 3. Creació de les Unitats Organitzatives (OUs)
- Crea el fitxer `OU_users.ldif` amb:
  ```
  dn: ou=users,dc=innovatechXX,dc=test
  ou: users
  objectClass: top
  objectClass: organizationalUnit

  dn: ou=groups,dc=innovatechXX,dc=test
  ou: groups
  objectClass: top
  objectClass: organizationalUnit
  ```
- Afegeix-les amb:
  ```
  ldapadd -D "cn=admin,dc=innovatechXX,dc=test" -W -f OU_users.ldif
  ```
- Comprova amb:
  ```
  ldapsearch -x -LLL -b "dc=innovatechXX,dc=test" ou
  ```

## 4. Instal·lació i configuració de LDAP Account Manager (LAM)
- Actualitza el sistema:
  ```
  sudo apt update && sudo apt upgrade -y
  ```
- Instal·la LAM:
  ```
  sudo apt install ldap-account-manager -y
  ```
- Accedeix a:
  `http://[IP_host-only]/lam`
- Configura:
  - Usuari: `lam`
  - Contrassenya: `lam`
  - Llista d’usuaris vàlids: `cn=admin,dc=innovatech24,dc=test`
  - Definiu les OU per usuaris i grups.
- Crea els grups (`tech` i `manager`) i usuaris (`tech01`, `manager01`) des de LAM.

## 5. Creació i assignació d'usuaris
- Crea usuaris:
  - `tech01` assignat al grup `tech`
  - `manager01` assignat al grup `manager`

## 6. Configuració del Client Ubuntu Desktop
- Instal·la:
  ```
  sudo apt install libnss-ldapd libpam-ldapd nslcd -y
  ```
- Edita `/etc/hosts` per incloure la IP i domini del servidor.
- Configura `/etc/nsswitch.conf` amb `ldap` en passwd, group.
- Modifica `/etc/ldap.conf` amb la IP i nom del servidor LDAP.
- Edita `/etc/pam.d/common-auth` per activar l’autenticació LDAP.
- Reinicia:
  ```
  sudo systemctl restart nslcd
  ```
- Verifica usuaris:
  ```
  getent passwd
  ```
- Reinicia el client i inicia sessió amb l’usuari `tech01`, pren capturas de pantalla.

🔙 [Tornar a la tasca](README.md)  
📍 [Tornar a la pàgina del projecte](../../README.md)
