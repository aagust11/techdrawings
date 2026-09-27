# TechDrawings

Editor de dibuixos tecnològics en català, pensat per a esquemes de classe. Funciona directament al navegador amb HTML, CSS, SVG i JavaScript, sense instal·lació ni servidor.

## Temàtiques

- Forces i vectors: blocs, vectors, eixos, molles i suports.
- Esforços: tracció, compressió, flexió, torsió i cisallament.
- Elements estructurals: bigues, pilars, tirants, unions i arcs.
- Màquines simples: palanques, politges, engranatges, rodes i plans inclinats.
- Màquines tèrmiques: focus calent, motor, focus fred i fluxos d’energia.
- Circuits elèctrics: pila, interruptor, bombeta, resistència i conductors.

Cada tema té peces i exemples que es poden editar. Es poden moure elements, canviar etiquetes, posicions, mides i color, afegir text, línies o fletxes i desfer o refer canvis. El projecte es desa al navegador, i es pot importar/exportar com a JSON. També s’exporta com a SVG i PNG.

## Ús

Obre `index.html` en un navegador modern. El flux de `.github/workflows/pages.yml` publica la pàgina quan es puja codi a `main`. A **Settings → Pages → Build and deployment**, selecciona **GitHub Actions** com a origen de la publicació. L'adreça resultant és `https://aagust11.github.io/techdrawings/`.

## Afegir una temàtica

`modules.js` defineix l’ordre de les temàtiques, el seu nom, les peces i els exemples. Cada peça té un `id` que correspon a un símbol de `symbol()` a `app.js`. Els exemples són llistes d’objectes posicionats en un full SVG de 1200 × 720. Afegeix-hi un símbol nou a `symbol()` per ampliar el catàleg de formes.

## Privadesa i límits

Els dibuixos es desen a `localStorage` d’aquest navegador. No se sincronitzen entre dispositius; exporta el JSON per fer una còpia. Els exemples són esquemes didàctics, no plànols tècnics a escala.
