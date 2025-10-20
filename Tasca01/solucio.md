# Solució
## Anàlisi i Justificació (Document d'Informe)  
Les contrasenyes febles o reutilitzades representen un risc crític per a l’empresa ja que faciliten atacs informàtics com els atacs de diccionari i el credential stuffing. Aquests atacs exploten la reutilització massiva de contrasenyes filtrades en bases de dades públiques, permetent accedir a múltiples comptes amb la mateixa credencial robada. Això pot comportar pèrdues econòmiques, d’informació sensible i d’imatge corporativa. Per evitar-ho, és essencial que el personal utilitzi contrasenyes robustes i úniques per a cada servei. Un gestor de contrasenyes juga un paper crucial perquè permet generar, emmagatzemar i gestionar de forma segura contrasenyes complexes i diferents per a cada compte, eliminant la necessitat de recordar-les i reduint la probabilitat d’ús de contrasenyes.

| Característica             | Bitwarden (Online/Núvol)                                             | KeePassX/KeePassXC (Offline/Escriptori)                        |
|---------------------------|--------------------------------------------------------------------|----------------------------------------------------------------|
| Emmagatzematge            | Núvol amb sincronització automàtica multidispositiu                | Local en fitxer xifrat KDBX                                      |
| Model de seguretat        | Xifratge end-to-end: dades xifrades abans del núvol                | Codi obert, emmagatzematge local, xifrat amb algoritmes robustos|
| Accés des de múltiples dispositius | Sí, des de qualsevol dispositiu amb accés a internet         | Sí, amb còpia manual o sincronització externa de fitxer         |
| Cost/Model freemium       | Versió gratuïta amb funcions bàsiques, subscripció premium opcional| Totalment gratuït, codi obert                                    |
| Control de dades          | Dades gestionades pel proveïdor, però xifrades i només accessibles per usuari | Control total per l’usuari, sense dependència de serveis cloud   |
| Integracions corporatives | Sí, suporta autenticació SSO, MFA, informes d’auditoria            | Limitat a funcionalitats d’escriptori, sense integracions cloud |
| Actualitzacions i manteniment | Automàtic i reposat en equip de desenvolupament                   | Comunitat open source, actualitzacions depenen de voluntaris   |


**Avantatges i Inconvenients**

- Bitwarden

   - Avantatges: Màxima comoditat i accessibilitat, sincronització instantània, alta seguretat criptogràfica, suport corporatiu i escalabilitat.
   - Inconvenients: Dependència de tercer per emmagatzematge, possible risc de vulnerabilitats del proveïdor cloud, requisit de connexió a Internet.

- KeePassX/KeePassXC

   - Avantatges: Control total de les dades, independència del núvol, codi obert que garanteix transparència i auditable, sense costos ni subscripcions.
   - Inconvenients: Menys còmode per sincronitzar entre dispositius, major responsabilitat en la gestió manual, risc de pèrdua o dany del fitxer local si no es fa còpia de seguretat.

**Recomanació**  
Per al personal tècnic de l’empresa, es recomana l’ús de Bitwarden per la seva combinació equilibrada entre seguretat avançada i facilitat d’ús. La seva arquitectura basat en xifratge end-to-end i la possibilitat de sincronitzar contrasenyes de forma segura en múltiples dispositius faciliten una gestió més eficaç i segura de les credencials. Alhora, ofereix eines d’administració corporativa i compliment normatiu que reforcen la seguretat globals de l’empresa. Això ajuda a mitigar riscos crítics derivats de contrasenyes febles o reutilitzades. No obstant això, cal implementar bones pràctiques en formació de l’usuari i control d’accés per maximitzar la protecció.

## Fase 2: Guia d'Ús Tècnica de Bitwarden per a l'Equip Tècnic

**Introducció**
Aquesta guia està dissenyada per a que l'equip tècnic pugui gestionar les contrasenyes de manera segura utilitzant la versió web de Bitwarden. També s'indica com ampliar la funcionalitat mitjançant la instal·lació de l'aplicació d'escriptori o l'extensió del navegador per facilitar-ne l'ús diari.

---

**Accés i inici de sessió a la web**

1. **Accés a l’eina:**
   - Obriu el navegador i aneu a [Bitwarden Web](https://vault.bitwarden.com).
   
2. **Iniciar sessió:**
   - Introduïu el vostre correu electrònic i la contrasenya mestre.
   - Feu clic a "Iniciar sessió".
   - ![Inici de sessió a la web](img/web-login.png)

---

## Instal·lació de l’Aplicació d’Escritori o Extensió de Navegador

Per facilitar l’emplenament automàtic i la gestió de contrasenyes, podeu instal·lar:

- L’**aplicació d’escriptori** (disponible per Windows, Mac i Linux).
- L’**extensió de navegador** (per Chrome, Firefox, Edge, etc.).

**Per fer-ho:**

1. Des de la pàgina oficial de [Bitwarden](https://bitwarden.com/downloads/), descarregueu l’aplicació d’escriptori segons el vostre sistema operatiu.
2. Des de la botiga d’extensions del vostre navegador, busqueu i instal·leu l’extensió de Bitwarden.
3. Autentiqueu-vos amb el vostre compte existent.

### Imatges suggerides:
- Captura de la pàgina de descàrrega de l'aplicació
- Imatge de l'extensió instal·lada en el navegador

---

## Funcionament amb la web i opcions addicionals

### Usar la web per gestionar contrasenyes

- Des de la interface web, podeu:

  - **Afegir noves credencials:** cliqueu a "Afegeix un element" i trieu "Inici de sessió". Ompliu els camps amb la URL, usuari i contrasenya, que podeu generar a la mateixa eina.
  - **Editar o eliminar credencials:** simplement seleccionant l’entrada i fent clic a editar o eliminar.

### Generació de contrasenyes segures

- Des del web, cliqueu a "Generador de contrasenyes".
- Configureu la longitud i els paràmetres (majúscules, minúscules, números i caràcters especials).
- Copieu la contrasenya i deseu-la dins la vostra credencial.

### Afegir credencials i emplenar automàticament

- A l’extensió del navegador, quan visitis una pàgina de login, Bitwarden proposarà emplenar automàticament la informació.
- També podeu crear, veure i copiar credencials des de la interfície web si cal.

---

## Emplenament automàtic des de la extensió del navegador

1. **Accediu a la pàgina de login del servei web.**
2. **Cliqueu en la icona de Bitwarden del navegador.**
3. **Seleccioneu la credencial corresponent o utilitzeu “Emplenar” per omplir automàticament.**
4. **Per a crear noves credencials, cliqueu a "Afegeix un element" i ompliu les dades.**

### Imatge suggerida:
- Captura del menú d’emplenament automàtic en navegador

---

## Gestió de Còpies de Seguretat (Backup)

1. **Exportació de dades:**
   - A la web, entreu a "Configuració" > "Exportar bóveda".
   - Seleccioneu el format (preferentment xifrat) i feu l’exportació.
   - Guardeu la còpia en un dispositiu segur.

2. **Emmagatzematge segur:**
   - Conserveu la còpia en una clau USB xifrada o en un servei de núvol amb xifratge i control d’accés.
   - No deixeu còpies sense protecció ni en llocs accessibles públicament.

### Imatge suggerida:
- Pantalla d'exportació de la bóveda

---

## Resum
Pots gestionar de manera segura i còmoda les contrasenyes amb la web de Bitwarden, i ampliar les funcionalitats amb la instal·lació de la aplicació d’escriptori o la extensió del navegador per a un millor emmagatzematge, emplenament automàtic i generació de contrasenyes robustes.

---

**Nota:** Assegureu-vos que cada captura de pantalla sigui clara i visible, i que s’incorpori a la carpeta `img/`. Sigui com sigui, aquestes imatges es poden obtenir fent captures de pantalla del vostre entorn amb els passos indicats.
