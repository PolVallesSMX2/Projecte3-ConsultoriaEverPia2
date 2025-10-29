# FASE 2: Part Pràctica

## A. Consulta bàsica de registre A

**Comanda:**
`dig xtec.cat`

**Resultat:**
- IP: `83.247.151.214`  
- TTL (Time To Live): `3044`  
- Classe de xarxa: `IN` (Internet)  
- Tipus de registre DNS: `A` → Associa el nom de domini amb una adreça IPv4  

---

## B. Consulta de servidors de noms (NS)

**Comanda:**
`dig tecnocampus.cat NS`

**Resultat:**
- TTL (Time To Live): `1686`  
- Classe de xarxa: `IN` (Internet)  
- Servidors de noms autoritatius per al domini:
  - `ns-1689.awsdns-19.co.uk`

**Explicació:**
Aquests són els servidors de noms autoritatius per al domini *tecnocampus.cat*.  
Són els que contenen la informació oficial del domini i gestionen les seves consultes DNS.

---

## C. Consulta SOA (Start of Authority)

**Comanda:**
`dig escolapia.cat SOA`

text

**Resultat:**
- TTL (Time To Live): `300`  
- Classe de xarxa: `IN` (Internet)  
- Tipus de registre: `SOA`  
- Nom del servidor principal: `dns1.nominalia.com`  
- Correu de l’administrador del domini: `root.dns1.nominalia.com`  
- Número de sèrie de la zona DNS: `1761028965`

---

## D. Consulta de la resolució inversa (IP a nom de domini)

**Comanda:**
`dig -x 147.83.2.135`

**Resultat:**

**Question Section:**  
Indica que s’ha consultat quin nom de domini (registre PTR) correspon a la IP `147.83.2.135`.

**Authority Section:**  
Apareixen els resultats PTR, que vinculen aquesta IP amb diversos noms de domini:

- `saladepremsa.upc.edu`  
- `upc.edu`  
- `masters.upc.edu`  
- `upc.cat`  
- `barcelonatech-upc.eu`  
- `edicioweb.produccio.upc.edu`  
- `barcelonatech.upc.edu`  
- `www.upc.es`

**Explicació:**
Aquesta adreça IP està associada a diversos noms de domini.  
Això sol passar en servidors que donen servei a múltiples dominis o subdominis dins d’una mateixa organització, com en aquest cas la *UPC* (Universitat Politècnica de Catalunya).

---

<div>
  <span>📝 </span><a href="README.md">Tornar a la tasca</a><br>
  <span>📍 </span><a href="../../../README.md">Tornar a la pàgina del projecte</a>
</div>
