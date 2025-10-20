# Anàlisi i Justificació (Document d'Informe)  
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

🔙 [Tornar a la tasca](README.md)  
📍 [Tornar a la pàgina del projecte](../../README.md)